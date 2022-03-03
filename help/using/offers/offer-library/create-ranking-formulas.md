---
title: Creare formule di classificazione
description: Learn how to create formulas to rank offers
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8bc808da-4796-4767-9433-71f1f2f0a432
source-git-commit: 14ab70aa32f4f7978b8c72b3981d3b55f56fd08b
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 1%

---

# Creare formule di classificazione {#create-ranking-formulas}

## About ranking formulas {#about-ranking-formulas}

****

**** [](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html)

Once a ranking formula has been created, you can assign it to a placement in a decision. [](../offer-activities/configure-offer-selection.md)

## Create a ranking formula {#create-ranking-formula}

To create a ranking formula, follow the steps below:

1. **[!UICONTROL Components]****[!UICONTROL Rankings]** The list of rankings previously created is displayed.

   ![](../assets/rankings-list.png)

1. **[!UICONTROL Create ranking]**

   ![](../assets/ranking-create-formula.png)

1. Specify the ranking formula name, description, and formula.

   In this example, we want to boost the priority of all offers with the &quot;hot&quot; attribute if the actual weather is hot. ****

   ![](../assets/ranking-syntax.png)

1. Fai clic su **[!UICONTROL Save]**. Your ranking formula is created, you can select it from the list to get details and edit or delete it.

   [](../offer-activities/configure-offer-selection.md)

   ![](../assets/ranking-formula-created.png)

## Ranking formula examples {#ranking-formula-examples}

You can create many different ranking formulas according to your needs. Below are some examples.

<!--
Boost by offer ID

Boost the priority of an offer with the offer ID *xcore:personalized-offer:13d213cd4cb328ec* by 5.

**Ranking formula:**

```
if( offer._id = "xcore:personalized-offer:13d213cd4cb328ec", offer.rank.priority + 5, offer.rank.priority)
```

Change the offer priority based on a certain profile attribute

Set the offer priority to 30 for offer *xcore:personalized-offer:13d213cd4cb328ec* if the user lives in the city of Bondi.

**Ranking formula:**

```
if( offer._id = "xcore:personalized-offer:13d213cd4cb328ec" and homeAddress.city.equals("Bondi", false), 30, offer.rank.priority)
```

Boost multiple offers by offer ID based on the presence of a profile's segment membership

Boost the priority of offers based on whether the user is a member of a priority segment, which is configured as an attribute in the offer.

**Ranking formula:**

```
if( segmentMembership.get("ups").get(offer.characteristics.prioritySegmentId).status in (["realized","existing"]), offer.rank.priority + 10, offer.rank.priority)
```
-->

### Boost offers with certain offer attribute based on profile attribute

If the profile lives in the city corresponding to the offer, then double the priority for all offers in that city.

****

```
if( offer.characteristics.city = homeAddress.city, offer.rank.priority * 2, offer.rank.priority)
```

### Boost offers where the end date is less than 24 hours from now

****

```
if( offer.selectionConstraint.endDate occurs <= 24 hours after now, offer.rank.priority * 3, offer.rank.priority)
```

### Boost offers with certain offer attribute based on context data

Boost certain offers based on the context data being passed in the decisioning call. `contextData.weather=hot``attribute=hot`

****

```
if (@{_xdm.context.additionalParameters;version=1}.weather.isNotNull()
and offer.characteristics.weather=@{_xdm.context.additionalParameters;version=1}.weather, offer.rank.priority + 5, offer.rank.priority)
```

Note that when using the decisioning API, the context data is added to the profile element in the request body, such as in the example below.

****

```
"xdm:profiles": [
{
    "xdm:identityMap": {
        "crmid": [
            {
            "xdm:id": "CRMID1"
            }
        ]
    },
    "xdm:contextData": [
        {
            "@type":"_xdm.context.additionalParameters;version=1",
            "xdm:data":{
                "xdm:weather":"hot"
            }
        }
    ]
 }],
```

### Boost offers based on the customers propensity to purchase the product being offered

******

** `if`

****

```
if ( offer.characteristics.propensityType = "extraBaggagePropensity" and _salesvelocity.CustomerAI.extraBaggagePropensity.score > 90, offer.rank.priority + 50,
    (
        if ( offer.characteristics.propensityType = "travelInsurancePropensity" and _salesvelocity.CustomerAI.insurancePropensity.score > 90, offer.rank.priority + 50, offer.rank.priority )
    )
)
```

A better solution is to store the scores in an array of the profile. The following example will work across a variety of different propensity scores using just a simple ranking formula. The expectation is that you have a profile schema with an array of scores. **

![](../assets/ranking-example-schema.png)

Given this, for a profile such as:

```
{"_salesvelocity": {"individualScoring": [
                    {"core": {
                            "category":"insurance",
                            "propensityScore": 96.9
                        }},
                    {"core": {
                            "category":"personalLoan",
                            "propensityScore": 45.3
                        }},
                    {"core": {
                            "category":"creditCard",
                            "propensityScore": 78.1
                        }}
                    ]}
}
```

**

![](../assets/ranking-example-propensityType.png)

**** If no score is found, use the static priority set on the offer:

```
let score = (select _Individual_Scoring1 from _salesvelocity.individualScoring
             where _Individual_Scoring1.core.category.equals(offer.characteristics.propensityType, false)).head().core.propensityScore
in if(score.isNotNull(), score, offer.rank.priority)
```
