---
title: Anteprima e test del contenuto
description: Scopri come visualizzare in anteprima e testare il contenuto.
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 736fc861-17f2-47b7-8635-9afd261ea3a8
source-git-commit: aa28d13b2ad874e4dc61510bfdc250415e8e8be1
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 57%

---

# Anteprima e test del contenuto {#preview-test}

>[!CONTEXTUALHELP]
>id="ac_preview_testprofiles"
>title="Controllare come viene eseguito il rendering del contenuto"
>abstract="Una volta definito il contenuto, puoi utilizzare i profili di test per visualizzarne l’anteprima e verificare se il rendering è corretto in base al canale in uso."

>[!CONTEXTUALHELP]
>id="ajo_preview_simulate"
>title="Controllare come viene eseguito il rendering del contenuto"
>abstract="Una volta definito il contenuto, puoi visualizzarne l’anteprima e verificare se il rendering è corretto in base al canale in uso."

Una volta definito il contenuto, puoi visualizzarne l’anteprima prima di inviare il messaggio. Questo è un passaggio fondamentale per garantire che sia accurato ma anche privo di errori, sia nelle impostazioni del contenuto che della personalizzazione.

Puoi anche inviare le consegne di test dei messaggi e-mail a destinatari o abbonati specifici per il test e la convalida e verificarne il rendering nei client desktop, mobili e basati su web più diffusi.

Tutte queste azioni possono essere eseguite utilizzando il pulsante **[!UICONTROL Simula contenuto]**, accessibile dalla schermata di modifica del contenuto del messaggio oppure dai designer e-mail e web per i rispettivi canali.

![](../email/assets/email-preview-button.png)

## Verifica tramite i dati dei profili di test o i dati di input di esempio {#methods}

Journey Optimizer offre due esperienze per testare il contenuto:

* **Verifica del contenuto tramite i dati dei profili di test**

  Puoi utilizzare i profili di test per visualizzare in anteprima il contenuto, inviare bozze e-mail e controllare il rendering delle e-mail. Se hai aggiunto campi personalizzati, puoi controllarne la visualizzazione utilizzando i dati del profilo di test. Per ulteriori informazioni, consulta queste sezioni:

  ➡️ [Seleziona profili di test](test-profiles.md)
➡️ [Anteprima tramite profili di test](preview.md)
➡️ [Invia bozze e-mail](proofs.md)
➡️ [Verifica rendering e-mail](rendering.md)
➡️ [Anteprima e verifica dell&#39;e-mail (video)](#video-preview)

* **Verifica delle varianti di contenuto tramite dati di input di esempio**

  [!DNL Journey optimizer] consente di visualizzare in anteprima e inviare bozze per diverse varianti di contenuto utilizzando dati di input di esempio caricati da un file CSV / JSON o aggiunti manualmente.

  Tutti gli attributi dei profili utilizzati nel contenuto per la personalizzazione vengono rilevati automaticamente dal sistema e possono essere utilizzati per i test per creare più varianti.

  ➡️ [Simula varianti di contenuto](../test-approve/simulate-sample-input.md)

## Da leggere

* **Autorizzazioni richieste** - È necessario includere l&#39;autorizzazione **[!DNL Manage Simulate Content]** nel profilo di prodotto **[!DNL Content Library Manager]**. [Ulteriori informazioni](../administration/ootb-product-profiles.md#content-library-manager).

  Per inviare le bozze, devi disporre delle autorizzazioni **Approva e pubblica** per la risorsa specifica (campagna o percorso) associata all&#39;e-mail. Inoltre, per inviare bozze in un percorso, è necessaria anche l&#39;autorizzazione **Pubblica percorso**. [Ulteriori informazioni sulle autorizzazioni](../administration/ootb-permissions.md).

* **Personalization con dati contestuali** - Quando si visualizza l&#39;anteprima di un messaggio o si inviano bozze, vengono visualizzati solo i dati di personalizzazione del profilo. La personalizzazione basata su dati contestuali, come le informazioni sull’evento, può essere testata solo nel contesto di un percorso. Scopri come in [questo caso d&#39;uso](../personalization/personalization-use-case.md).

* **Anteprima del contenuto con più varianti condizionali** - Durante la simulazione o il rendering di bozze per e-mail contenenti più varianti condizionali, Journey Optimizer potrebbe richiedere più tempo di elaborazione. In caso di timeout o messaggi di errore, considera di ridurre il numero totale di varianti o di semplificare le regole condizionali. Per ulteriori informazioni sui contenuti condizionali, consulta [questa pagina](../personalization/dynamic-content.md).

## Video introduttivo {#video-preview}

Scopri come utilizzare i profili di test per testare il rendering delle e-mail nelle caselle in entrata, visualizzare in anteprima le e-mail personalizzate rispetto ai profili di test e inviare bozze.

>[!VIDEO](https://video.tv.adobe.com/v/3430338?quality=12&captions=ita)
