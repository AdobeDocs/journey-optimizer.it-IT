---
title: Esempi di Template Personalization
description: Esempi di Journey Optimizer Personalization
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 832b0bfa-ec74-4b1d-ad85-d4e4ea2f8863
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# E-mail sulle prescrizioni dei piani sanitari {#plan-prescription}

Un profilo contiene piani sanitari e ogni piano include prescrizioni. Le prescrizioni hanno vari stati, come &quot;pronto&quot;, &quot;richiamo&quot; o &quot;raccolto&quot;.

In questo caso d’uso, vogliamo inviare un’unica e-mail a ciascun profilo, incluse tutte le prescrizioni pronte per essere prelevate o richiamate. Fai clic su ciascuna scheda di seguito per ulteriori informazioni sulla sintassi da utilizzare per implementare questo caso d’uso.

>[!BEGINTABS]

>[!TAB Messaggio con rendering]

<p>Ciao John Doe,</p>
<p>Di seguito sono riportate le prescrizioni che sono pronte per il ritiro o che sono state richiamate:</p>

**Piano di integrità A**

<ul>

<li>
      <strong>ID prescrizione:</strong> pres1<br>
      <strong>Nome:</strong> Medicinale A<br>
      <strong>Stato:</strong> pronto
   </li>

<li>
      <strong>ID prescrizione:</strong> pres2<br>
      <strong>Nome:</strong> Medicinale B<br>
      <strong>Stato:</strong> richiamo
   </li>

</ul>

**Piano di integrità B**

<ul>

<li>
      <strong>ID prescrizione:</strong> pres4<br>
      <strong>Nome:</strong> Medicinale D<br>
      <strong>Stato:</strong> pronto
   </li>

</ul>

>[!TAB Modello HTML]

```html
<p>Hi {{profile.person.firstName}} {{profile.person.lastName}},</p>
<p>Here are the prescriptions that are either ready for pick up or have been recalled:</p>
{{#each profile.plans as |plan|}}
<h3>{{plan.name}}</h3>
<ul>
   {{#each plan.prescriptions as |prescription|}}
   {%#if prescription.state = "ready" or prescription.state = "recall"%}
   <li>
      <strong>Prescription ID:</strong> {{prescription.prescription_id}}<br>
      <strong>Name:</strong> {{prescription.name}}<br>
      <strong>State:</strong> {{prescription.state}}
   </li>
   {%/if%}
   {{/each}}
</ul>
{{/each}}
```

>[!TAB Dati profilo]

```javascript
{
  "profile": {
    "person": {
      "firstName": "John",
      "lastName": "Doe"
    },
    "plans": [
      {
        "planId": "plan1",
        "name": "Health Plan A",
        "prescriptions": [
          {
            "prescription_id": "pres1",
            "name": "Medication A",
            "state": "ready"
          },
          {
            "prescription_id": "pres2",
            "name": "Medication B",
            "state": "recall"
          }
        ]
      },
      {
        "planId": "plan2",
        "name": "Health Plan B",
        "prescriptions": [
          {
            "prescription_id": "pres3",
            "name": "Medication C",
            "state": "picked up"
          },
          {
            "prescription_id": "pres4",
            "name": "Medication D",
            "state": "ready"
          }
        ]
      }
    ]
  }
}
```

>[!ENDTABS]
