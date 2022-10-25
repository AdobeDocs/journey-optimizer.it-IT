---
title: Estensione Helper per editing video
description: Scopri l’estensione Visual Editing Helper Chrome che consente di creare e visualizzare in anteprima pagine web in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 50bafd20671912ecbcb595a59fed0e7bad95a200
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 13%

---

# Estensione Helper per editing video {#visual-editing-helper}

Per creare e visualizzare in anteprima rapidamente le esperienze web, l’estensione Adobe Experience Cloud Visual Editing Helper per il browser Google Chrome consente di caricare i siti web in modo affidabile all’interno dell’Adobe [!DNL Journey Optimizer] web designer.

>[!NOTE]
>
>La funzione canale web è attualmente disponibile come versione beta solo per gli utenti selezionati.

## Installare l’estensione Visual Editing Helper {#install-visual-editing-helper}

Per ottenere e installare l’estensione del browser Visual Editing Helper, segui i passaggi riportati di seguito.

1. Dal Web Store Google Chrome, passa al [Helper per l&#39;editing video di Adobe Experience Cloud ]((https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"}) estensione del browser.

1. Fai clic su **[!UICONTROL Aggiungi a Chrome]** > **[!UICONTROL Aggiungi estensione]**.

1. Creare una campagna di canale web in [!DNL Journey Optimizer]. [Scopri come](author-web.md#create-web-campaign)

1. Apri [!DNL Journey Optimizer] web designer per iniziare a creare la tua esperienza web. [Ulteriori informazioni](author-web.md)

1. Accertati che l’estensione del browser Visual Editing Helper sia abilitata nella barra degli strumenti del browser Chrome facendo clic sull’icona corrispondente.

   ![](assets/web-visual-editing-extension.png)

L’Helper per per l’editing visivo di Adobe Experience Cloud viene ora abilitato automaticamente quando un sito web viene aperto in [!DNL Journey Optimizer] web designer per potenziare l&#39;authoring.

L’estensione non dispone di impostazioni condizionali e gestisce automaticamente tutte le impostazioni, incluse le impostazioni dei cookie SameSite.

>[!NOTE]
>
>Alcuni siti web potrebbero non essere aperti in modo affidabile nel [!DNL Journey Optimizer] web designer per uno dei motivi seguenti:
>
> * Il sito web dispone di criteri di sicurezza rigidi.
> * Il sito web si trova in un iframe.
> * Il sito per il controllo qualità o il sito di staging del cliente non è disponibile nel mondo esterno (è un sito interno).


## Risoluzione dei problemi

Quando si utilizza l’Adobe [!DNL Journey Optimizer] web designer, se si tenta di caricare un sito web che non riesce a caricarsi, viene visualizzato un messaggio per suggerirti di installare [Estensione di Visual Editing Helper per il browser](#install-visual-editing-helper).

Se l&#39;SDK per web di Adobe Experience Platform non è ancora implementato sul sito web, nella finestra di progettazione web viene visualizzato un messaggio per suggerirti di installare l&#39;estensione per browser di Visual Editing Helper e di implementare l&#39; [SDK per web](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=it){target=&quot;_blank&quot;}.

Se il sito non viene caricato o si comporta in modo imprevisto, è possibile accettare i cookie sul sito web nel browser prima di provare a caricarlo in Adobe [!DNL Journey Optimizer].

Per le pagine sotto autenticazione, se la pagina di accesso non viene caricata o se dopo aver provato a effettuare l&#39;accesso non si è ancora connessi, cerca prima di accedere in una scheda diversa del browser e quindi carica il sito web nell&#39;Adobe [!DNL Journey Optimizer] web designer.
