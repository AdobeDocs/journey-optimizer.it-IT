---
title: Personalizzare i contenuti in Journey Optimizer
description: Introduzione alla personalizzazione
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: a174944bb8efcb67d758d4fe215674c1b8bbee13
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 14%

---

# Guida introduttiva alla personalizzazione{#add-personalization}

Scopri le funzionalità di personalizzazione [!DNL Adobe Journey Optimizer] per adattare i messaggi a ogni destinatario specifico sfruttando i dati e le informazioni disponibili su di essi. Può essere il loro nome, i loro interessi, dove vivono, quello che hanno comprato, e altro ancora.

➡️ [Scopri come personalizzare un messaggio in questi video](#video-perso)

[!DNL Journey Optimizer] utilizza una sintassi di personalizzazione  **** semplice basata su Handlebars che ti consente di creare espressioni con contenuti racchiusi tra parentesi graffe doppie **{{}}**. È possibile aggiungere più espressioni nello stesso contenuto o campo senza limitazioni. Ulteriori informazioni sono disponibili in [Sintassi di personalizzazione](personalization-syntax.md).

La personalizzazione si basa sui dati del profilo gestiti dallo schema **Profilo individuale XDM** definito in Adobe Experience Platform. Ulteriori informazioni sono disponibili nella documentazione [Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target=&quot;_blank&quot;}.

>[!CAUTION]
>Lo schema **XDM Singolo profilo** è l’unico schema utilizzabile per personalizzare il contenuto in [!DNL Journey Optimizer].

**Esempi:**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

Durante l’elaborazione del messaggio (e-mail e push), Journey Optimizer sostituisce l’espressione con i dati contenuti nel database di Experience Cloud Platform:  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` diventa &quot;Hello John Doe&quot;.


## Contesti di personalizzazione{#personalization-areas}

Il contenuto e la visualizzazione dei messaggi inviati da [!DNL Journey Optimizer] possono essere personalizzati in diversi modi.

In tutti i campi con l’icona dell’editor, puoi aprire l’editor di personalizzazione (noto anche come editor espressioni) e definire la personalizzazione.

![](assets/perso_icon.png)

### Personalizzare le e-mail

Quando crei un’e-mail, puoi aggiungere la personalizzazione nel campo **Oggetto e-mail** del messaggio.

![](assets/perso_subject.png)

Nella finestra di progettazione e-mail puoi personalizzare il contenuto:

* Nel **messaggio**: fai clic all’interno di un blocco di testo, fai clic sull’icona **Personalizza** nella barra degli strumenti contestuale e seleziona il campo **Inserisci personalizzazione** . Per ulteriori informazioni sull’interfaccia di E-mail Designer, consulta questa sezione [a1/>.](../design-emails.md)

   ![](assets/perso_insert.png)

* Per un **collegamento**: seleziona un testo o un&#39;immagine all&#39;interno di un blocco di testo, fai clic sull&#39;icona **Inserisci collegamento** nella barra degli strumenti contestuale. Nella finestra puoi aggiungere un blocco di personalizzazione facendo clic sull&#39;icona **Aggiungi personalizzazione** .

   ![](assets/perso_link.png)

In entrambi i casi, accedi all’editor di personalizzazione.

![](assets/perso_ee.png)

### Personalizzare le notifiche push

Puoi anche personalizzare le **notifiche push** nei campi seguenti:

* **Titolo**
* **Corpo**
* **Audio personalizzato**
* **Badge**
* **Dati personalizzati**

![](assets/perso_push.png)

Ulteriori informazioni sulla configurazione delle notifiche push in [questa sezione](../push-gs.md).

### Personalizzare le offerte {#personalize-offers}

Puoi anche accedere all’editor di personalizzazione quando aggiungi contenuto di tipo testo alle rappresentazioni delle offerte.

Ulteriori informazioni sulla gestione dei contenuti con Gestione delle decisioni in [questa sezione](../offers/offer-library/creating-personalized-offers.md#custom-text).

## Utilizzare l’editor espressioni {#use-expression-editor}

L’editor di espressioni è il fulcro della personalizzazione in [!DNL Journey Optimizer].

È disponibile in ogni contesto in cui devi definire la personalizzazione come e-mail, push e offerte.

Nell’interfaccia dell’editor di espressioni, seleziona, organizza, personalizza e convalida tutti i dati per creare una personalizzazione personalizzata per il contenuto.

![](assets/perso_ee1.png)

Nella parte sinistra della schermata viene visualizzato un selettore di dominio che consente di selezionare l’origine da personalizzare. Le origini disponibili sono:

* **Profilo** : elenca tutti i riferimenti associati allo schema di profilo descritto nella documentazione di  [Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.
* **Iscrizione**  al segmento: elenca tutti i segmenti creati nel servizio Segmentazione di Adobe Experience Platform. Ulteriori informazioni sulla segmentazione sono disponibili [qui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}.
* **Offerte** : elenca tutte le offerte associate a un posizionamento specifico. Seleziona il posizionamento e inserisci le offerte nel contenuto. Per una documentazione completa su come gestire le offerte, consulta [questa sezione](../deliver-personalized-offers.md).
* **Contesto** : quando  **** Messageactivity viene utilizzato in un percorso, i campi percorso contestuale sono disponibili in questo menu. [Ulteriori informazioni](personalization-use-case.md).
* **Funzioni**  di supporto: elenca tutte le funzioni di supporto disponibili per eseguire operazioni sui dati, ad esempio calcoli, formattazione dei dati o conversioni, condizioni e manipolarle nel contesto della personalizzazione. [Ulteriori informazioni](functions/functions.md).

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
