---
solution: Journey Optimizer
product: journey optimizer
title: Aggiungere metadati al contenuto dell’e-mail
description: Scopri come migliorare la leggibilità e l’accessibilità dei contenuti delle e-mail con i metadati in Journey Optimizer
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: preintestazione, editor, riepilogo, e-mail
exl-id: 7ed52b2e-eabf-414f-b169-4b004733dea9
source-git-commit: 50491d039f2baf8c30a6af0c1b59fe9041244ac7
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 23%

---

# Aggiungere metadati al contenuto dell’e-mail {#email-metadata}

>[!CONTEXTUALHELP]
>id="ac_edition_preheader"
>title="Aggiungere una preintestazione"
>abstract="Una preintestazione è un breve testo di riepilogo che segue l’oggetto quando un’e-mail viene visualizzata dal client e-mail. In molti casi, fornisce un breve riepilogo dell’e-mail e in genere consiste in una sola frase."

Durante la progettazione delle e-mail, per una migliore leggibilità e una migliore accessibilità, puoi definire metadati aggiuntivi per il contenuto. Il [!DNL Journey Optimizer] [Messaggio di posta elettronica di Designer](get-started-email-design.md) consente di specificare i seguenti elementi:

![](assets/email_body_settings_ex.png)

* **[!UICONTROL Preheader]**: un preheader è un breve testo di riepilogo che segue la riga dell&#39;oggetto durante la visualizzazione di un&#39;e-mail dal client di posta elettronica. In molti casi, fornisce un breve riepilogo dell’e-mail e in genere consiste in una sola frase.

  >[!NOTE]
  >
  >Le preintestazioni non sono supportate da tutti i client e-mail. Se non è supportata, la preintestazione non viene visualizzata.

* **[!UICONTROL Titolo documento]**: questo campo, che corrisponde all&#39;elemento `<title>`, fornisce informazioni descrittive sul contenuto dell&#39;e-mail, in genere visualizzato come descrizione comando al passaggio del mouse. Può aiutare gli utenti con disabilità fornendo ulteriore contesto e può contribuire a una migliore comprensione dei contenuti da parte dei motori di ricerca.

* **[!UICONTROL Lingua del documento]**: per garantire l&#39;accessibilità, è possibile specificare la lingua che gli assistenti vocali utilizzeranno per convertire testo e immagini in linguaggio vocale o Braille, per gli utenti con disabilità visive o di apprendimento. Questa impostazione corrisponde all&#39;attributo `lang` nell&#39;elemento `<html>`.

Per configurare queste impostazioni, segui la procedura indicata di seguito.

1. Da [E-mail Designer](content-from-scratch.md), aggiungi almeno un **[!UICONTROL Componente struttura]** per iniziare a progettare l&#39;e-mail.

1. Fai clic su **[!UICONTROL Corpo]**, nella **[!UICONTROL struttura di navigazione]** a sinistra o nella parte superiore del riquadro di destra.

   ![](assets/email_body.png)

1. Nella scheda **[!UICONTROL Impostazioni]** digitare del testo nei campi **[!UICONTROL Preheader]**, **[!UICONTROL Titolo documento]** e/o **[!UICONTROL Lingua documento]**.

1. Puoi anche fare clic sull’icona di personalizzazione accanto a ciascun campo per personalizzare il contenuto da attributi di profilo, tipi di pubblico, attributi contestuali e altro ancora. [Ulteriori informazioni sulla personalizzazione](../personalization/personalization-build-expressions.md)

   ![](assets/email_body_settings.png)

1. Fai clic su **[!UICONTROL Salva]** per confermare le modifiche.