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
source-git-commit: 76bb202375cdfe1c8abacc1670ba6e794175215d
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 5%

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

Quando utilizzi l’editor HTML avanzato, sono attivate le seguenti protezioni per proteggere la compatibilità dei contenuti e impostare le aspettative.

* Attualmente, nell&#39;editor HTML avanzato non è presente **alcun processo di convalida**. Gli errori di sintassi e i layout interrotti non vengono controllati. Assicurati di rivedere attentamente il contenuto prima di salvarlo.

* I futuri aggiornamenti del sistema potrebbero ripristinare le modifiche apportate al markup predefinito. Tieni presente che **le modifiche potrebbero essere sovrascritte**.

* I problemi causati da codice personalizzato e modifiche manuali **non possono essere risolti** o dal team di supporto [!DNL Adobe]. Assicurati di disporre di un backup del contenuto nel caso sia necessario ripristinare una versione precedente.

* Per garantire la compatibilità del contenuto, **il salvataggio non è disponibile** nella visualizzazione avanzata di HTML. Quando si è pronti per salvare le modifiche, è necessario tornare alla vista Desktop.

>[!WARNING]
>
>L&#39;editor avanzato di HTML nel modello di contenuto non è lo stesso della modalità **[!UICONTROL Crea il codice]** nel Designer e-mail. In modalità [!UICONTROL Crea il codice per te], non puoi tornare all&#39;editor visivo; una volta scelto quel percorso, puoi continuare a modificare solo il codice. L’editor HTML avanzato, invece, consente di passare dalla visualizzazione HTML alla visualizzazione desktop (visiva) in qualsiasi momento. [Ulteriori informazioni sull’editor di codice](../email/code-content.md)

## Passa alla visualizzazione avanzata di HTML {#switch-to-desktop-view}

1. Apri o crea un [modello e-mail](../content-management/create-content-templates.md) e apri il [Designer e-mail](../email/get-started-email-design.md) per modificare il contenuto.

1. Fai clic sul pulsante **[!UICONTROL HTML]** nell&#39;angolo in alto a destra dello schermo.

   ![](assets/email-template-expert-mode-button.png)

1. La prima volta che apri l’editor di HTML avanzato, viene visualizzato un messaggio di avviso. Rivederlo attentamente e fare clic su **[!UICONTROL OK]** per continuare. [Ulteriori informazioni](#guardrails)

   >[!NOTE]
   >
   >Questo avviso viene visualizzato solo la prima volta che apri l’editor HTML avanzato e viene ripristinato ogni mese.

   ![](assets/email-template-expert-mode-warning.png){zoomable="yes"}

1. Viene visualizzato l’editor di HTML avanzato.

   ![](assets/email-template-expert-mode.png)

1. Aggiungi le modifiche desiderate al contenuto dell’e-mail.

   >[!WARNING]
   >
   >Assicurarsi di immettere il codice HTML e CSS corretto poiché non esiste alcun processo di convalida della sintassi e [!DNL Adobe] non fornisce alcun supporto. [Ulteriori informazioni](#guardrails)

1. Il salvataggio non è disponibile nella vista HTML avanzata. Torna alla vista Desktop per salvare le modifiche.

   ![](assets/email-template-expert-mode-save.png){zoomable="yes"}

   >[!NOTE]
   >
   >Il contenuto può essere salvato solo in visualizzazione Desktop per motivi di compatibilità con il contenuto. Le modifiche apportate vengono mantenute quando si passa da una visualizzazione all&#39;altra.

1. La simulazione dei contenuti non è disponibile nella vista HTML avanzata. Per simulare i contenuti, passa alla vista Desktop.

   ![](assets/email-template-expert-mode-simulate.png){zoomable="yes"}

