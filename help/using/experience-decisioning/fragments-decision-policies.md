---
title: Sfruttare i frammenti nei criteri di decisione
description: Scopri come sfruttare i frammenti nei criteri decisionali
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 70f64348-092b-4350-91dc-72c3c07300f9
TQID: https://experienceleague.adobe.com/5Vpngi03UnC9YPlB5tdTRcd0NoT7iglH2pRDkmeZKOg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 5ff88c5deec3f9fa326fe6fd2d71133ba4135fc4
workflow-type: tm+mt
source-wordcount: 1744
ht-degree: 0%

---

# Sfruttare i frammenti nei criteri di decisione {#fragments}

>[!BEGINSHADEBOX]

**In questa pagina:** sfrutta i frammenti di contenuto di Journey Optimizer e i frammenti di contenuto di AEM nei criteri decisionali, in modo da poter personalizzare e ottimizzare le decisioni sui contenuti per i diversi canali.

>[!ENDSHADEBOX]

Gli elementi decisionali supportano due tipi di contenuto di frammenti che possono essere utilizzati durante l’authoring dei messaggi all’interno di un criterio decisionale:

* **Frammenti di contenuto di Journey Optimizer**: frammenti di espressione riutilizzabili creati in Journey Optimizer e aggiunti alla sezione **[!UICONTROL Frammenti]** dell&#39;elemento di decisione. [Ulteriori informazioni sui frammenti di contenuto di AJO](../content-management/fragments.md)
* **Frammenti di contenuto di AEM**: contenuto creato in Adobe Experience Manager, mappato agli attributi dell&#39;elemento decisionale e selezionato nell&#39;editor di personalizzazione per nome chiave. [Scopri come collegare un frammento di contenuto AEM a un elemento di decisione](items.md#aem-fragments)

## Frammenti di contenuto Journey Optimizer {#ajo-fragments}

Se i criteri di decisione contengono elementi di decisione, compresi frammenti di contenuto di AJO, puoi sfruttarli durante l’authoring di un messaggio all’interno dei criteri di decisione in tutti i canali in cui è disponibile Decisioning (esperienza basata su codice, e-mail, push, SMS e percorsi).

Ad esempio, supponiamo che tu voglia visualizzare contenuti diversi per diversi modelli di dispositivi mobili. Aggiungi i frammenti specificati, ciascuno relativo a un modello di telefono diverso, all’elemento decisionale utilizzato nel criterio decisionale. [Scopri come aggiungere frammenti a un elemento decisionale](items.md#attributes).

![Sezione Frammenti di un elemento di decisione che mostra i riferimenti ai frammenti e le chiavi di posizionamento.](assets/item-fragments.png){width=70%}

Al termine, puoi utilizzare uno dei seguenti metodi:

>[!BEGINTABS]

>[!TAB Inserisci direttamente il codice]

È sufficiente copiare e incollare il blocco di codice riportato di seguito nel codice del criterio di decisione. Sostituisci `variable` con l&#39;ID frammento e `placement` con la chiave di riferimento frammento:

```handlebars
{% let variable =  get(item._experience.decisioning.offeritem.contentReferencesMap, "placement").id %}
{{fragment id = variable required=false}}
```

>[!TAB Segui i passaggi dettagliati]

1. Passare alle **[!UICONTROL Funzioni helper]** e aggiungere la funzione **Let** `{% let variable = expression %} {{variable}}` al riquadro del codice, in cui è possibile dichiarare la variabile per il frammento.

   ![Editor di codice dei criteri di decisione che mostra la funzione di supporto Let aggiunta al riquadro del codice.](assets/decision-let-function.png)

1. Utilizza la **Mappa** > **Ottieni** funzione `{%= get(map, string) %}` per generare la tua espressione. La mappa è il frammento a cui si fa riferimento nell’elemento decisionale. La stringa può essere il modello di dispositivo immesso nell&#39;elemento di decisione come **[!UICONTROL chiave di riferimento frammento]**.

   ![Funzioni Map e Get utilizzate per fare riferimento alla mappa frammento e alla chiave di riferimento frammento.](assets/decision-map-function.png)

1. Puoi anche utilizzare un attributo contestuale che contenga questo ID modello dispositivo.

   ![Attributo contestuale selezionato per l&#39;identificatore del modello di dispositivo.](assets/decision-contextual-attribute.png)

1. Aggiungi la variabile scelta per il frammento come ID frammento.

   ![Variabile ID frammento impostata dall&#39;elemento decisione nel codice dei criteri di decisione.](assets/decision-fragment-id.png)

>[!ENDTABS]

L&#39;ID frammento e la chiave di riferimento verranno selezionati dalla sezione **[!UICONTROL Frammenti]** dell&#39;elemento di decisione.

>[!WARNING]
>
>Se la chiave del frammento non è corretta o se il contenuto del frammento non è valido, il rendering potrebbe non riuscire e causare un errore nella chiamata di Edge.
>
>Per evitare errori quando un frammento non è temporaneamente disponibile, viene utilizzato il flag `required=false` in modo che il frammento venga ignorato. [Ulteriori informazioni sui frammenti temporaneamente non disponibili](#temporary-unavailable-fragments)

### Utilizzo e guardrail {#fragments-guardrails}

I seguenti guardrail si applicano in modo specifico a **Frammenti di contenuto di AJO** utilizzati negli elementi decisionali.

+++Simulare frammenti di contenuto ed espressione nelle e-mail

Per il canale **E-mail**, i frammenti di espressione associati a un elemento di decisione vengono visualizzati correttamente quando **[!UICONTROL Invia bozza]** o quando la campagna viene attivata. Tuttavia, **[!UICONTROL Simula contenuto]** non visualizza il frammento di espressione dall&#39;elemento di decisione.

+++

+++Frammenti visivi ed elementi decisionali nelle e-mail

Impossibile assegnare un **[!UICONTROL frammento visivo]** a un elemento decisione. In questo contesto sono supportati solo **frammenti espressione**.

+++

+++Elemento decisionale e attributi di contesto

Gli attributi degli elementi decisionali e gli attributi contestuali non sono supportati per impostazione predefinita nei frammenti [!DNL Journey Optimizer]. Tuttavia, puoi utilizzare in alternativa le variabili globali, come descritto di seguito.

Supponiamo che desideri utilizzare la variabile *sport* nel frammento.

1. Fai riferimento a questa variabile nel frammento, ad esempio:

   ```text
   Elevate your practice with new {{sport}} gear!
   ```

1. Definisci la variabile con la funzione **Let** all&#39;interno del blocco dei criteri di decisione. Nell&#39;esempio seguente, *sport* è definito con l&#39;attributo elemento decisione:

   ```handlebars
   {#each decisionPolicy.13e1d23d-b8a7-4f71-a32e-d833c51361e0.items as |item|}}
   {% let sport = item._cjmstage.value %}
   {{fragment id = get(item._experience.decisioning.offeritem.contentReferencesMap, "placement1").id }}
   {{/each}}
   ```

+++

+++Convalida del contenuto del frammento di elemento decisione

* A causa della natura dinamica di questi frammenti, quando vengono utilizzati in una campagna, la convalida dei messaggi durante la creazione del contenuto della campagna viene ignorata per i frammenti a cui si fa riferimento negli elementi decisionali.

* La convalida del contenuto del frammento viene eseguita solo durante la creazione e la pubblicazione del frammento.

* Per i frammenti di espressione di tipo JSON, il contenuto viene convalidato sintatticamente al momento del salvataggio del frammento. Gli errori di convalida vengono visualizzati come avvisi.

In fase di esecuzione, viene convalidato il contenuto della campagna (incluso il contenuto del frammento dagli elementi decisionali). In caso di errore di convalida, la campagna non verrà rappresentata.

+++

+++I frammenti temporaneamente non disponibili sono stati ignorati {#temporary-unavailable-fragments}

Quando percorsi o campagne fanno riferimento a frammenti allegati a elementi decisionali, possono verificarsi brevi ritardi di sincronizzazione prima che i frammenti aggiornati siano disponibili su Edge.

Per evitare errori quando un frammento non è temporaneamente disponibile, per impostazione predefinita i frammenti hanno ora il flag `required` impostato su `false` e vengono quindi saltati invece di causare un errore nel percorso o nella campagna.

Ciò significa che se il frammento non è temporaneamente disponibile in Edge, viene semplicemente ignorato. Se il frammento è disponibile, viene riprodotto normalmente.

**Esempio**

Se il criterio decisionale è valido per due offerte e ciascuna di esse contiene un frammento, ad esempio &quot;20% di sconto&quot; e &quot;30% di sconto&quot;, e il secondo frammento non è temporaneamente disponibile, con `required=false` il percorso esegue il rendering dell&#39;offerta disponibile (20% di sconto) e ignora l&#39;altro frammento (30% di sconto) invece di generare un errore nel sistema o nella campagna. Ciò migliora l’affidabilità quando il contenuto è ancora sincronizzato.

+++

>[!NOTE]
>
>È comunque possibile contrassegnare un frammento come obbligatorio impostando il flag `required` su `true`. Tuttavia, se manca temporaneamente un frammento, potrebbe verificarsi un errore nel rendering del percorso o della campagna.

## Frammenti di contenuto di AEM {#aem-fragments-decisioning}

>[!AVAILABILITY]
>
>Questa funzione è disponibile per i canali in uscita con supporto Decisioning.

Prima di sfruttare i frammenti di contenuto di AEM in un criterio decisionale, assicurati di disporre di:

* Il frammento di contenuto è stato creato in Adobe Experience Manager e contrassegnato con `ajo-enabled:{OrgId}/{SandboxName}` affinché possa essere individuato da Journey Optimizer. [Scopri come creare e assegnare un tag](../integrations/aem-fragments.md#create-tag)
* Ha collegato il frammento alla sezione **[!UICONTROL Frammenti AEM]** dell&#39;elemento dell&#39;offerta assegnandogli un nome di riferimento univoco. [Scopri come collegare un frammento di contenuto AEM a un elemento di decisione](items.md#attributes)

Nell’editor di personalizzazione sono disponibili tutti i Frammenti di contenuto di AEM associati agli elementi decisionali selezionati dal criterio. Viene visualizzata una cartella per nome chiave di frammento.

➡️ [Scopri come utilizzare AEM Content Fragments con Journey Optimizer Decisioning nel video](#video)

In questo esempio, il criterio di decisione include due elementi di decisione a cui sono associati frammenti di AEM tramite il nome di riferimento.

![Editor Personalization che mostra i frammenti di contenuto di AEM disponibili per nome chiave di frammento in un criterio di decisione.](assets/aem-fragment-select.png)

1. Fai clic sul pulsante + per aggiungere il frammento desiderato all’espressione.

   Poiché un singolo nome di riferimento può avere più frammenti associati a esso tra diversi articoli di offerta, Decisioning determina quello migliore da consegnare a ciascun cliente in base ai criteri di classificazione dei criteri di decisione.

1. Una volta selezionato il frammento, puoi sfruttarne gli attributi, ad esempio URL di immagini, campi di testo o altro contenuto, e utilizzare Decisioning per presentare al cliente giusto il contenuto al momento giusto.

   ![Attributi selezionati dei frammenti di contenuto di AEM disponibili per la personalizzazione nell&#39;espressione dei criteri di decisione.](assets/aem-fragment-attribute.png)

1. Prima di attivare la campagna o il percorso, utilizza uno di questi metodi di simulazione per visualizzare in anteprima come verranno visualizzati i valori dei campi Frammento di contenuto di AEM. [Ulteriori informazioni sulla simulazione del contenuto](../content-management/preview-test.md)

### Utilizzare i frammenti di contenuto di AEM nei diversi canali {#aem-fragments-channels}

La modalità di inserimento degli attributi dei frammenti di contenuto di AEM da un criterio decisionale dipende dal canale in cui stai lavorando.

>[!BEGINTABS]

>[!TAB E-mail]

Per inserire gli attributi dei frammenti di contenuto di AEM nell’e-mail utilizzando un criterio di decisione:

1. Apri la bozza dell&#39;e-mail in E-mail Designer e fai clic sull&#39;icona **[!UICONTROL Decisioning]** nella barra a destra per aprire il pannello dei criteri di decisione.
1. Seleziona la strategia di selezione assemblata e specifica un **posizionamento** per definire l&#39;area dell&#39;e-mail in cui verrà popolata l&#39;offerta.
1. Fai clic sull&#39;icona **+** e seleziona il campo specifico dal frammento di contenuto di AEM che deve essere riprodotto in quell&#39;area, ad esempio il campo URL dell&#39;immagine principale.

   ![Invia un messaggio e-mail al pannello dei criteri di decisione di Designer con un campo Frammento di contenuto di AEM selezionato per un posizionamento.](assets/aem-fragment-email.png)

1. Prima di pubblicare, fai clic su **[!UICONTROL Simula contenuto]** per visualizzare in anteprima il risultato e verificare che l&#39;offerta con priorità più alta e il relativo frammento di contenuto eseguano il rendering come previsto per un profilo di test.

>[!TAB Esperienza basata su codice (JSON)]

Quando crei un’esperienza basata su codice JSON, utilizza la seguente struttura per eseguire il rendering degli attributi dei frammenti di contenuto di AEM da un criterio decisionale.

```handlebars
[
{{#each decisionPolicy.YOUR_POLICY_ID.items as |item|}}
{% let frag = get(item._experience.decisioning.offeritem.aemContentReferencesMap, "YOUR_REFERENCE_KEY").id %}
{{fragment id = frag result='YOUR_REFERENCE_KEY' required=false}}
{
  "fieldName": "{{{YOUR_REFERENCE_KEY.fieldName}}}"
},
{{/each}}
]
```

>[!NOTE]
>
>I frammenti di contenuto di AEM utilizzano `aemContentReferencesMap` per cercare i frammenti in base alla chiave di riferimento. È diverso da `contentReferencesMap`, utilizzato per i frammenti di contenuto di Journey Optimizer.

Quando crei il payload JSON, tieni presente quanto segue:

* Posizionare le parentesi dell&#39;array JSON `[` e `]` **all&#39;esterno** del ciclo `#each`.
* Utilizza **parentesi graffe** `{{{ }}}` per i valori dei campi all&#39;interno delle stringhe JSON per evitare che HTML sfugga ai caratteri speciali e garantire un output JSON valido.
* Il parametro `result='YOUR_REFERENCE_KEY'` acquisisce il contenuto del frammento risolto con quel nome in modo da poter fare riferimento ai relativi campi con `YOUR_REFERENCE_KEY.fieldName`.

![Editor esperienza basato su codice che mostra gli attributi dei frammenti di contenuto di AEM sottoposti a rendering da un criterio di decisione in JSON.](assets/aem-fragments-cbe.png)

>[!TAB Esperienza basata su codice (HTML)]

Per esperienze basate su codice basate su HTML, utilizza le doppie parentesi graffe standard per il rendering dei campi:

```handlebars
{{#each decisionPolicy.YOUR_POLICY_ID.items as |item|}}
{% let frag = get(item._experience.decisioning.offeritem.aemContentReferencesMap, "YOUR_REFERENCE_KEY").id %}
{{fragment id = frag result='YOUR_REFERENCE_KEY' required=false}}
<div>{{YOUR_REFERENCE_KEY.fieldName}}</div>
{{/each}}
```

>[!ENDTABS]

### Utilizzare le risorse dai frammenti di contenuto di AEM {#aem-cf-assets}

I frammenti di contenuto di AEM possono includere campi immagine che fanno riferimento a risorse memorizzate in AEM. Poiché Journey Optimizer riceve solo il **percorso relativo** di tali risorse, è possibile che le immagini non vengano caricate a meno che l&#39;URL di pubblicazione completo non sia preceduto.

>[!NOTE]
>
>La risoluzione nativa dei riferimenti alle risorse AEM all’interno dei frammenti di contenuto non è ancora supportata. Gli approcci riportati di seguito sono soluzioni alternative disponibili fino all’aggiunta di tale supporto.

>[!BEGINTABS]

>[!TAB Anteponi il dominio di pubblicazione AEM]

1. Dall&#39;URL dell&#39;istanza di AEM, identificare il dominio di authoring, ad esempio `author-p12345-e67890.adobeaemcloud.com`.

   ![URL dell&#39;istanza di AEM che mostra il dominio di authoring utilizzato per derivare il dominio di pubblicazione.](assets/aem-fragment-author-domain.png)

1. Sostituire `author` con `publish` per ottenere il dominio di pubblicazione: `publish-p12345-e67890.adobeaemcloud.com`.

1. Nell’editor di personalizzazione di Journey Optimizer, aggiungi il dominio di pubblicazione al campo di riferimento della risorsa dal frammento di contenuto.

   ![L&#39;editor di Personalization con il dominio di pubblicazione di AEM è stato aggiunto a un campo di riferimento per le risorse di un frammento di contenuto.](assets/aem-fragment-publish-domain.png)

Al momento della consegna, l’immagine verrà risolta nel relativo URL di pubblicazione completo.

>[!TAB Archivia l&#39;URL di pubblicazione in un campo di testo]

1. Apri il frammento di contenuto in AEM.
1. Vai all&#39;anteprima JSON e controlla la sezione **Riferimenti** per individuare l&#39;URL della risorsa pubblicata.

   ![Sezione dei riferimenti di anteprima JSON per frammenti di contenuto di AEM che mostra l&#39;URL della risorsa pubblicata.](assets/aem-fragment-published-url.png)

1. Copia l’URL di pubblicazione e incollalo in un campo di testo dedicato all’interno del Frammento di contenuto.

   ![Campo di testo Frammento di contenuto AEM contenente l&#39;URL di pubblicazione copiato per la risorsa di riferimento.](assets/aem-fragment-copy-url.png)

1. In Journey Optimizer, fai riferimento a tale campo di testo direttamente come origine dell’immagine nell’espressione di personalizzazione.

   ![Espressione di personalizzazione Journey Optimizer che fa riferimento al campo di testo Frammento di contenuto come origine dell&#39;immagine.](assets/aem-fragment-use-url.png)

Questo approccio evita la costruzione manuale degli URL e mantiene l’URL di pubblicazione all’interno del frammento di contenuto stesso.

>[!ENDTABS]

## Video introduttivo {#video}

Scopri come utilizzare Frammenti di contenuto di Adobe Experience Manager con Journey Optimizer Decisioning per personalizzare e ottimizzare i contenuti.

>[!VIDEO](https://video.tv.adobe.com/v/3492215/?learn=on&enablevpops)
