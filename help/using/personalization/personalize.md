---
title: Personalizzare i contenuti in Journey Optimizer
description: Introduzione alla personalizzazione
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 7be83409f7a594747963c5b125f3bf96c0b4f8b6
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 14%

---

# Guida introduttiva alla personalizzazione{#add-personalization}

Scopri [!DNL Adobe Journey Optimizer] funzionalità di personalizzazione per adattare i messaggi a ogni destinatario specifico sfruttando i dati e le informazioni disponibili su di essi. Può essere il loro nome, i loro interessi, dove vivono, quello che hanno comprato, e altro ancora.

➡️ [Scopri come personalizzare un messaggio in questi video](#video-perso)

[!DNL Journey Optimizer] utilizza un **inline** semplice sintassi di personalizzazione basata su Handlebars che consente di creare espressioni con contenuti racchiusi tra parentesi graffe e doppie **{{}}**. È possibile aggiungere più espressioni nello stesso contenuto o campo senza limitazioni. Ulteriori informazioni in [Sintassi di personalizzazione](personalization-syntax.md).

La personalizzazione si basa sui dati del profilo gestiti dallo schema **Profilo individuale XDM** definito in Adobe Experience Platform. Ulteriori informazioni in [Documentazione di Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target=&quot;_blank&quot;}.

>[!CAUTION]
>La **Profilo individuale XDM** schema è l’unico schema utilizzabile per personalizzare il contenuto in [!DNL Journey Optimizer].

**Esempi:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Durante l’elaborazione del messaggio (e-mail e push), Journey Optimizer sostituisce l’espressione con i dati contenuti nel database di Experience Cloud Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` diventa &quot;Ciao John Doe&quot;.


## Contesti di personalizzazione{#personalization-areas}

Contenuto e visualizzazione dei messaggi inviati da [!DNL Journey Optimizer] può essere personalizzato in diversi modi.

In tutti i campi con l’icona dell’editor, puoi aprire l’editor di personalizzazione (noto anche come editor espressioni) e definire la personalizzazione.

![](assets/perso_icon.png)

### Personalizzare le e-mail

Quando crei un messaggio e-mail, puoi aggiungere la personalizzazione nel **[!UICONTROL Subject line]** campo del messaggio.

![](assets/perso_subject.png)

Nella finestra di progettazione e-mail puoi personalizzare il contenuto:

* In **message**: fai clic all’interno di un blocco di testo, fai clic sul pulsante **Personalizza** dalla barra degli strumenti contestuale e seleziona **Inserisci personalizzazione** campo . Per ulteriori informazioni sull’interfaccia di E-mail Designer, consulta la sezione [sezione](../design-emails.md).

   ![](assets/perso_insert.png)

* Per **collegamento**: seleziona un testo o un&#39;immagine all&#39;interno di un blocco di testo, fai clic sul pulsante **Inserisci collegamento** dalla barra degli strumenti contestuale. Nella finestra puoi aggiungere un blocco di personalizzazione facendo clic sul pulsante **Aggiungi personalizzazione** icona.

   ![](assets/perso_link.png)

In entrambi i casi, accedi all’editor di personalizzazione.

![](assets/perso_ee.png)

### Personalizzare le notifiche push

Puoi anche personalizzare il tuo **Notifiche push** nei campi seguenti:

* **Titolo**
* **Corpo**
* **Audio personalizzato**
* **Badge**
* **Dati personalizzati**

![](assets/perso_push.png)

Ulteriori informazioni sulla configurazione delle notifiche push in [questa sezione](../push-gs.md).

### Personalizzare le offerte {#personalize-offers}

Puoi anche accedere all’editor di personalizzazione quando aggiungi contenuto di tipo testo alle rappresentazioni delle offerte.

Ulteriori informazioni sulla gestione dei contenuti con la gestione delle decisioni in [questa sezione](../offers/offer-library/creating-personalized-offers.md#custom-text).

## Utilizzare l’editor espressioni {#use-expression-editor}

L’editor di espressioni è il fulcro della personalizzazione in [!DNL Journey Optimizer].

È disponibile in ogni contesto in cui devi definire la personalizzazione come e-mail, push e offerte.

Nell’interfaccia dell’editor di espressioni, seleziona, organizza, personalizza e convalida tutti i dati per creare una personalizzazione personalizzata per il contenuto.

![](assets/perso_ee1.png)

Nella parte sinistra della schermata viene visualizzato un selettore di dominio che consente di selezionare l’origine da personalizzare.

![](assets/perso_ee3.png)

Le origini disponibili sono:

* **[!UICONTROL Profile attributes]** : elenca tutti i riferimenti associati allo schema di profilo descritto in [Documentazione di Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.
* **[!UICONTROL Segment memberships]** : elenca tutti i segmenti creati nel servizio Segmentazione di Adobe Experience Platform. Ulteriori informazioni sulla segmentazione disponibili [qui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}.
* **[!UICONTROL Offer decisions]** : elenca tutte le offerte associate a un posizionamento specifico. Seleziona il posizionamento e inserisci le offerte nel contenuto. Per una documentazione completa sulla gestione delle offerte, consulta [questa sezione](../deliver-personalized-offers.md).
* **[!UICONTROL Contextual attributes]** : quando **Messaggio** in un percorso, i campi percorso contestuale sono disponibili tramite questo menu. [Ulteriori informazioni](personalization-use-case.md).
* **[!UICONTROL Helper functions]** : elenca tutte le funzioni di supporto disponibili per eseguire operazioni sui dati, ad esempio calcoli, formattazione dei dati o conversioni, condizioni e manipolarle nel contesto della personalizzazione. [Ulteriori informazioni](functions/functions.md).

Una volta selezionato, il riferimento viene aggiunto nell’editor.

>[!NOTE]
>
>L’icona Info accanto all’icona &quot;+&quot; apre una descrizione comandi che fornisce ulteriori dettagli per ogni variabile.

Nell’esempio seguente, l’editor di espressioni ti consente di selezionare i profili che compiono il loro compleanno oggi e quindi di completare la personalizzazione inserendo un’offerta specifica corrispondente a questo giorno.

![](assets/perso_ee2.png)

## Video sulle procedure{#video-perso}

Scopri come utilizzare le informazioni sugli eventi contestuali provenienti da un percorso per personalizzare un messaggio.

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

Scopri come utilizzare le informazioni sugli eventi contestuali provenienti da un percorso per personalizzare un messaggio.

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
