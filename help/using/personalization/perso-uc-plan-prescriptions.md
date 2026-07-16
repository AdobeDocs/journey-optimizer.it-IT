---
title: Esempi di Template Personalization
description: Esempi di Journey Optimizer Personalization
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 832b0bfa-ec74-4b1d-ad85-d4e4ea2f8863
TQID: https://experienceleague.adobe.com/fZtkkz9pvdZ3G7ojmHlNhasxawVbXmBHX-uznq6hseY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
  - id: a757b957-83f3-4a4d-9775-a93854f84f77
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 522
ht-degree: 1%

---

# E-mail sulle prescrizioni dei piani sanitari {#plan-prescription}

>[!BEGINSHADEBOX]

**In questa pagina:** Segui un caso di utilizzo di personalizzazione che esegue iterazioni su array di profili nidificati con regole condizionali per creare un piano di integrità che elenca le prescrizioni pronte per il ritiro o richiamate.

>[!ENDSHADEBOX]

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

## Riferimento rapido {#quick-reference}

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

>[!BEGINTABS]

>[!TAB Panoramica]

**TL;DR**

Questa pagina illustra un caso di utilizzo di personalizzazione completo: l’iterazione su array di profili nidificati (piani di integrità contenenti prescrizioni) con filtro condizionale per visualizzare solo le prescrizioni in stato &quot;pronto&quot; o &quot;richiamo&quot; in un’e-mail.

**Intenti**

* Vedi un esempio di output renderizzato di un’e-mail personalizzata per il piano di integrità
* Comprendere il modello HTML utilizzando blocchi `{{#each}}` e `{%#if%}` nidificati per l&#39;iterazione dell&#39;array condizionale
* Comprendere la struttura dati di profilo richiesta: un array `plans` in cui ogni piano contiene un array `prescriptions` con campi `state`

>[!TAB Glossario]

* **Iterazione nidificata**: utilizzo di `{{#each}}` cicli all&#39;interno di altri `{{#each}}` cicli per attraversare strutture di array multilivello nei dati del profilo (ad esempio, piani → prescrizioni).
* **Stato della prescrizione**: un campo su ciascun oggetto della prescrizione che indica lo stato del ciclo di vita in questo caso d&#39;uso. I valori utilizzati sono &quot;ready&quot;, &quot;recall&quot; e &quot;pick up&quot;. *(specifico per il caso d&#39;uso)*
* **`{%#if%}`/`{%/if%}`**: sintassi di blocco condizionale utilizzata nei modelli di messaggio per filtrare gli elementi array durante l&#39;iterazione (distinta dalla sintassi Handlebars `{{#if}}` a doppia curvatura).

>[!TAB Terminologia]

* **Nome canonico:** iterazione matrice nidificata — varianti: cicli nidificati, ognuno nidificato, iterazione a più livelli
* **Non confondere:** `{{#each}}` / `{{/each}}` (sintassi di iterazione Handlebars, parentesi graffe doppie) ≠ `{%#if%}` / `{%/if%}` (sintassi condizionale, parentesi graffe percentuali) — entrambi vengono utilizzati insieme in questo modello
* **Non confondere:** &quot;pronto&quot; (prescrizione disponibile per il ritiro) ≠ &quot;richiamato&quot; (prescrizione richiamata) ≠ &quot;prelevato&quot; (prescrizione già raccolta, esclusa dall&#39;output dal filtro condizionale)

>[!TAB Domande frequenti]

**Q: quali stati di prescrizione sono inclusi nell&#39;output dell&#39;e-mail?**

Vengono visualizzate solo le prescrizioni con lo stato &quot;pronto&quot; o &quot;richiamo&quot;. Le prescrizioni con stato &quot;prelevato&quot; sono escluse dal filtro condizionale `{%#if prescription.state = "ready" or prescription.state = "recall"%}`.

**D: quale struttura dati di profilo è necessaria per questo caso d&#39;uso?**

Un profilo con un array `plans`, in cui ogni oggetto del piano contiene un array `prescriptions`. Ogni oggetto di prescrizione deve avere `prescription_id`, `name` e `state` campi.

**D: come vengono iterati i piani e le prescrizioni nel modello?**

Il ciclo `{{#each profile.plans as |plan|}}` esterno scorre su ogni piano di integrità. Al suo interno, `{{#each plan.prescriptions as |prescription|}}` esegue iterazioni sulle prescrizioni di ogni piano e un blocco condizionale filtra solo gli stati &quot;pronto&quot; o &quot;richiamato&quot;.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 4b68d597 -->
