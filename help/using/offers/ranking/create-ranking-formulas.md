---
title: Formule di classificazione
description: Scopri come creare formule per classificare le offerte
feature: Ranking, Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 8bc808da-4796-4767-9433-71f1f2f0a432
source-git-commit: baf76d3c571c62105c1f0a59e07ca70e61a83cc6
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 3%

---

# Formule di classificazione {#create-ranking-formulas}

## Informazioni sulla classificazione delle formule {#about-ranking-formulas}

**Classificazione delle formule** ti consente di definire regole che determineranno quale offerta deve essere presentata per prima per un determinato posizionamento, anziché tenere conto dei punteggi di priorità delle offerte.

Le formule di classificazione sono espresse in **Sintassi PQL** e possono sfruttare gli attributi del profilo, i dati contestuali e gli attributi dell’offerta. Per ulteriori informazioni su come utilizzare la sintassi PQL, consulta [documentazione dedicata](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=it).

Una volta creata una formula di classificazione, puoi assegnarla a un posizionamento in una decisione. Per ulteriori informazioni, consulta [Configurare la selezione delle offerte nelle decisioni](../offer-activities/configure-offer-selection.md).

## Creare una formula di classificazione {#create-ranking-formula}

Per creare una formula di classificazione, effettua le seguenti operazioni:

1. Accedere a **[!UICONTROL Componenti]** , quindi selezionare **[!UICONTROL Classificazione]** scheda. Il **[!UICONTROL Formule]** è selezionata per impostazione predefinita. Viene visualizzato l&#39;elenco delle formule create in precedenza.

   ![](../assets/rankings-list.png)

1. Clic **[!UICONTROL Crea classificazione]** per creare una nuova formula di classificazione.

   ![](../assets/ranking-create-formula.png)

1. Specificare il nome, la descrizione e la formula della formula.

   In questo esempio, vogliamo aumentare la priorità di tutte le offerte con l’attributo &quot;hot&quot; (caldo) se il tempo effettivo è caldo. Per eseguire questa operazione, il **contextData.weather=hot** è stato passato nella chiamata di decisione.

   ![](../assets/ranking-syntax.png)

   >[!IMPORTANT]
   >
   >Durante la creazione di una formula di classificazione, non è supportato guardare indietro a un periodo di tempo precedente. Ad esempio, se specifichi un evento esperienza che si è verificato nell’ultimo mese come componente della formula. Qualsiasi tentativo di includere un periodo di lookback durante la creazione della formula attiverà un errore durante il salvataggio.

1. Fai clic su **[!UICONTROL Salva]**. La formula di classificazione viene creata, puoi selezionarla dall’elenco per ottenere i dettagli e modificarla o eliminarla.

   È ora pronto per essere utilizzato in una decisione di classificare le offerte idonee per un posizionamento (vedi [Configurare la selezione di offerte nelle decisioni](../offer-activities/configure-offer-selection.md)).

   ![](../assets/ranking-formula-created.png)

## Esempi di formule di classificazione {#ranking-formula-examples}

Puoi creare diverse formule di classificazione in base alle tue esigenze. Di seguito sono riportati alcuni esempi.

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

Boost multiple offers by offer ID based on the presence of a profile's audience membership

Boost the priority of offers based on whether the user is a member of a priority audience, which is configured as an attribute in the offer.

**Ranking formula:**

```
if( segmentMembership.get("ups").get(offer.characteristics.get("prioritySegmentId")).status in (["realized","existing"]), offer.rank.priority + 10, offer.rank.priority)
```
-->

### Incrementa le offerte con un determinato attributo di offerta basato sull’attributo del profilo

Se il profilo risiede nella città corrispondente all’offerta, allora raddoppia la priorità per tutte le offerte in quella città.

**Formula di classificazione:**

```
if( offer.characteristics.get("city") = homeAddress.city, offer.rank.priority * 2, offer.rank.priority)
```

### Incrementa le offerte la cui data di fine è inferiore a 24 ore

**Formula di classificazione:**

```
if( offer.selectionConstraint.endDate occurs <= 24 hours after now, offer.rank.priority * 3, offer.rank.priority)
```

### Incrementa le offerte con un determinato attributo di offerta basato sui dati contestuali

Incrementa alcune offerte in base ai dati contestuali trasmessi nella chiamata decisionale. Ad esempio, se `contextData.weather=hot` viene passato nella chiamata di decisione, la priorità di tutte le offerte con `attribute=hot` deve essere potenziato.

**Formula di classificazione:**

```
if (@{_xdm.context.additionalParameters;version=1}.weather.isNotNull()
and offer.characteristics.get("weather")=@{_xdm.context.additionalParameters;version=1}.weather, offer.rank.priority + 5, offer.rank.priority)
```

Tieni presente che quando utilizzi l’API di decisioning, i dati contestuali vengono aggiunti all’elemento profilo nel corpo della richiesta, come nell’esempio seguente.

**Frammento dal corpo della richiesta:**

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

### Incrementa le offerte in base alla propensione dei clienti ad acquistare il prodotto che viene offerto

Puoi aumentare il punteggio di un’offerta in base al punteggio di tendenza del cliente.

In questo esempio, il tenant dell’istanza è *_salesvelocity* e lo schema del profilo contiene un intervallo di punteggi memorizzati in un array:

![](../assets/ranking-example-schema.png)

Considerato questo, per un profilo come:

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

Le offerte contengono un attributo per *propensityType* che corrisponde alla categoria dai punteggi:

![](../assets/ranking-example-propensityType.png)

La formula di classificazione può quindi impostare la priorità di ogni offerta in modo che sia uguale ai clienti *propensityScore* per quello *propensityType*. Se non viene trovato alcun punteggio, utilizza la priorità statica impostata sull’offerta:

```
let score = (select _Individual_Scoring1 from _salesvelocity.individualScoring
             where _Individual_Scoring1.core.category.equals(offer.characteristics.get("propensityType"), false)).head().core.propensityScore
in if(score.isNotNull(), score, offer.rank.priority)
```
