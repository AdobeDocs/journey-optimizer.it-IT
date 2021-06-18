---
title: Personalizzare i contenuti in Journey Optimizer
description: Introduzione alla personalizzazione
feature: Personalizzazione
topic: Personalizzazione
role: Data Engineer
level: Beginner
source-git-commit: 9656fc4b9f0935949abfd83db194c00da0f35cf4
workflow-type: tm+mt
source-wordcount: '624'
ht-degree: 13%

---

# Guida introduttiva alla personalizzazione{#add-personalization}

Scopri le funzionalità di personalizzazione [!DNL Adobe Journey Optimizer] per adattare i tuoi messaggi a ogni destinatario specifico sfruttando i dati e le informazioni che hai su di lui/lei. Può essere il suo nome, i suoi interessi, dove vive, quello che ha comprato, e altro ancora.

[!DNL Journey Optimizer] utilizza una sintassi di personalizzazione  **** semplice basata su Handlebars che ti consente di creare espressioni con contenuti racchiusi tra parentesi graffe doppie **{{}}**. È possibile aggiungere più espressioni nello stesso contenuto o campo senza limitazioni. Ulteriori informazioni sono disponibili in [Sintassi di personalizzazione](personalization-syntax.md).

La personalizzazione si basa sui dati del profilo gestiti dallo schema **Profilo individuale XDM** definito in Adobe Experience Platform. Per ulteriori informazioni, consulta la documentazione di [Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it).

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

## Utilizzare l’editor espressioni

L’editor di espressioni è il fulcro della personalizzazione in [!DNL Journey Optimizer].

È disponibile in ogni contesto in cui devi definire la personalizzazione come e-mail, push e offerte.

Nell’interfaccia dell’editor di espressioni, seleziona, organizza, personalizza e convalida tutti i dati per creare una personalizzazione personalizzata per il contenuto.

![](assets/perso_ee1.png)

Nella parte sinistra della schermata viene visualizzato un selettore di dominio che consente di selezionare l’origine da personalizzare. Le origini disponibili sono:

* **Profilo** : elenca tutti i riferimenti associati allo schema di profilo descritto nella documentazione di  [Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html).
* **Iscrizione**  al segmento: elenca tutti i segmenti creati nel servizio Segmentazione di Adobe Experience Platform. Ulteriori informazioni sulla segmentazione sono disponibili [qui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=en)
* **Offerte** : elenca tutte le offerte associate a un posizionamento specifico. Seleziona il posizionamento e inserisci le offerte nel contenuto. Per una documentazione completa su come gestire le offerte, consulta [questa sezione](../deliver-personalized-offers.md)
* **Contesto** : quando  **** Messageactivity viene utilizzato in un percorso, i campi percorso contestuale sono disponibili in questo menu. [Ulteriori informazioni](personalization-use-case.md)
* **Funzioni**  di supporto: elenca tutte le funzioni di supporto disponibili per eseguire operazioni sui dati, ad esempio calcoli, formattazione dei dati o conversioni, condizioni e manipolarle nel contesto della personalizzazione. [Ulteriori informazioni](functions/functions.md)

Una volta selezionato, il riferimento viene aggiunto nell’editor.

>[!NOTE]
>
>L’icona Info accanto all’icona &quot;+&quot; apre una descrizione comandi che fornisce ulteriori dettagli per ogni variabile.

Nell’esempio seguente, l’editor di espressioni ti consente di selezionare i profili che compiono il loro compleanno oggi e quindi di completare la personalizzazione inserendo un’offerta specifica corrispondente a questo giorno.

![](assets/perso_ee2.png)

