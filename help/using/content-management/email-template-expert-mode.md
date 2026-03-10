---
solution: Journey Optimizer
product: journey optimizer
title: Modificare i modelli e-mail con l’editor HTML avanzato
description: Utilizza la modalità Expert per visualizzare e modificare la sorgente HTML del contenuto delle e-mail nell’editor di WYSIWYG, con controllo dei flag di funzione, protezioni e convalida del salvataggio.
feature: Templates
topic: Content Management
role: User
hidefromtoc: true
hide: true
level: Experienced
exl-id: 0c586565-0c65-435f-986d-cd08b59de159
source-git-commit: 2240a4bf85d3f5f41a12d128afdc15431dbab75b
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 7%

---

# Modificare i modelli e-mail con l’editor HTML avanzato {#email-template-expert-mode}

>[!AVAILABILITY]
>
>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.

L&#39;**editor avanzato di HTML** è una modalità esperta che consente di visualizzare e modificare il codice sorgente non elaborato dei modelli di contenuto e-mail direttamente dall&#39;interfaccia di Designer e-mail [!DNL Journey Optimizer].

Questa funzionalità consente di inserire espressioni avanzate, ad esempio condizioni, direttamente nell’origine. Quando si torna alla visualizzazione visiva (desktop), il contenuto viene nuovamente sottoposto a rendering in modo da poter verificare l&#39;aspetto e continuare a modificare in entrambe le visualizzazioni.

>[!NOTE]
>
>Questa funzione è disponibile solo nei modelli di contenuto e per il canale e-mail.

## Guardrail {#guardrails}

Quando utilizzi l’editor HTML avanzato, i seguenti guardrail proteggono la compatibilità dei contenuti e impostano le aspettative.

* L&#39;editor HTML avanzato **non convalida** il codice. Non controlla gli errori di sintassi o i layout interrotti. Rivedi attentamente i contenuti prima di salvarli.

* I futuri aggiornamenti del sistema potrebbero sovrascrivere le modifiche apportate al markup predefinito. **È possibile che le modifiche non persistano**.

* Il team di supporto [!DNL Adobe] **non è in grado di risolvere i problemi** causati da codice personalizzato e modifiche manuali. Conserva un backup del contenuto nel caso sia necessario ripristinarlo.

* Non è possibile simulare contenuti nella vista HTML avanzata. Passa alla vista Desktop per visualizzare in anteprima il contenuto.

* Per garantire la compatibilità del contenuto, **non è possibile salvare** nella visualizzazione avanzata di HTML. Tornare alla vista Desktop quando si è pronti a salvare le modifiche.

>[!WARNING]
>
>L&#39;editor avanzato di HTML nel modello di contenuto non è lo stesso della modalità **[!UICONTROL Crea il codice]** nel Designer e-mail. In modalità [!UICONTROL Crea il codice per te], non puoi tornare all&#39;editor visivo; una volta scelto quel percorso, puoi continuare a modificare solo il codice. L’editor HTML avanzato, invece, consente di passare dalla visualizzazione HTML alla visualizzazione desktop (visiva) in qualsiasi momento. [Ulteriori informazioni sull’editor di codice](../email/code-content.md)

## Passa alla visualizzazione avanzata di HTML {#switch-to-html-view}

Per aprire l’editor di HTML avanzato e modificare l’origine del modello, segui la procedura riportata di seguito.

1. Apri o crea un [modello e-mail](../content-management/create-content-templates.md) e apri il [Designer e-mail](../email/get-started-email-design.md) per modificare il contenuto.

1. Fai clic sul pulsante **[!UICONTROL HTML]** nell&#39;angolo in alto a destra dello schermo.

   ![Posizione del pulsante HTML nella barra degli strumenti di E-mail Designer](assets/email-template-expert-mode-button.png)

1. La prima volta che apri l’editor di HTML avanzato, viene visualizzato un messaggio di avviso. Rivederlo attentamente e fare clic su **[!UICONTROL OK]** per continuare. [Ulteriori informazioni](#guardrails)

   ![Finestra di dialogo di avviso alla prima apertura dell&#39;editor avanzato di HTML](assets/email-template-expert-mode-warning.png){zoomable="yes"}

   >[!NOTE]
   >
   >Questo avviso viene visualizzato solo la prima volta che apri l’editor HTML avanzato e viene ripristinato ogni mese.

1. Viene visualizzato l’editor HTML avanzato.

   ![L&#39;interfaccia dell&#39;editor HTML avanzato mostra il codice sorgente del modello e-mail](assets/email-template-expert-mode.png)

1. Aggiungi le modifiche desiderate al contenuto dell’e-mail.

   >[!WARNING]
   >
   >Assicurarsi di immettere il codice HTML e CSS corretto poiché non esiste alcun processo di convalida della sintassi e [!DNL Adobe] non fornisce alcun supporto. [Ulteriori informazioni](#guardrails)

1. La simulazione e il salvataggio dei contenuti non sono disponibili nella visualizzazione HTML avanzata per motivi di compatibilità. Torna alla vista Desktop per visualizzare in anteprima il contenuto e salvare le modifiche.

   ![Torna alla vista Desktop per salvare le modifiche](assets/email-template-expert-mode-save.png){zoomable="yes"}

   >[!NOTE]
   >
   >Le modifiche apportate vengono mantenute quando si passa da una visualizzazione all&#39;altra.

<!--
    ![](assets/email-template-expert-mode-simulate.png){zoomable="yes"}-->

## Argomenti correlati

* [Creare il codice del contenuto e-mail](../email/code-content.md)
* [Creare modelli di contenuto](create-content-templates.md)
* [Guida introduttiva a E-mail Designer](../email/get-started-email-design.md)

