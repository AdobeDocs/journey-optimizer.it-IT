---
title: Estensione Helper per editing video
description: Scopri l’estensione di Chrome Visual Editing Helper che consente di creare e visualizzare in anteprima pagine web in Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: f4a0ec45-d624-4f80-b888-42e5987cdc4f
badge: label="Beta" type="Informativo"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 18%

---

# Estensione Helper per editing video {#visual-editing-helper}

>[!BEGINSHADEBOX]

Informazioni disponibili in questa documentazione:

* [Introduzione al canale Web](get-started-web.md)
* [Creare esperienze web](create-web.md)
* [Creare pagine web](author-web.md)
* **[Estensione Helper per editing video](visual-editing-helper.md)**
* [Generazione rapporti Web](web-report.md)

>[!ENDSHADEBOX]

Per creare e visualizzare in anteprima rapidamente le esperienze web, l’estensione del browser Adobe Experience Cloud Visual Editing Helper per Google Chrome consente di caricare i siti web in modo affidabile all’interno dell’Adobe [!DNL Journey Optimizer] web designer.

## Installare l’estensione Helper per editing video {#install-visual-editing-helper}

Per ottenere e installare l’estensione del browser Helper per editing video, effettua le seguenti operazioni.

1. Dal Google Chrome Web Store, passa a [Helper per editing video Adobe Experience Cloud](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} estensione del browser.

1. Fai clic su **[!UICONTROL Aggiungi a Chrome]** > **[!UICONTROL Aggiungi estensione]**.

1. Creare una campagna per canale web in [!DNL Journey Optimizer]. [Scopri come](author-web.md#create-web-campaign)

1. Apri [!DNL Journey Optimizer] web designer per iniziare a creare la tua esperienza web. [Ulteriori informazioni](author-web.md)

1. Accertati che l’estensione del browser Helper per editing video sia abilitata nella barra degli strumenti del browser Chrome, facendo clic sull’icona corrispondente.

   ![](assets/web-visual-editing-extension.png)

Adobe Experience Cloud Visual Editing Helper viene ora attivato automaticamente quando un sito web viene aperto in [!DNL Journey Optimizer] web designer per potenziare l’authoring.

L’estensione non dispone di impostazioni condizionali e gestisce automaticamente tutte le impostazioni, incluse le impostazioni dei cookie SameSite.

>[!NOTE]
>
>Alcuni siti web potrebbero non aprirsi in modo affidabile nel [!DNL Journey Optimizer] web designer per uno dei motivi seguenti:
>
> * Il sito web dispone di criteri di sicurezza rigidi.
> * Il sito web si trova in un iframe.
> * Il sito per il controllo qualità o il sito di staging del cliente non è disponibile nel mondo esterno (è un sito interno).


## Risoluzione dei problemi

Quando si utilizza l’Adobe [!DNL Journey Optimizer] web designer, se si tenta di caricare un sito web che non riesce, viene visualizzato un messaggio per suggerirti di installare [Estensione del browser Helper per editing video](#install-visual-editing-helper).

Se Adobe Experience Platform Web SDK non è ancora implementato sul sito Web, nella finestra di progettazione Web viene visualizzato un messaggio per suggerirti di installare l’estensione del browser Helper per editing video e implementare [SDK per web](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target="_blank"}.

Se il sito non viene caricato o si comporta in modo imprevisto, è possibile che vengano accettati dei cookie sul sito web nel browser prima di tentare di caricarlo in Adobe [!DNL Journey Optimizer].

Per le pagine in autenticazione, se la pagina di accesso non viene caricata o se dopo aver tentato di accedere non hai ancora effettuato l’accesso, prova ad accedere prima da una scheda diversa del browser e quindi carica il sito web nell’Adobe [!DNL Journey Optimizer] web designer.
