---
title: Contesti di personalizzazione in Journey Optimizer
description: Scopri in quali contesti puoi aggiungere la personalizzazione
translation-type: tm+mt
source-git-commit: 568b37f0bbcb663cf7062f26b90d57d89452e862
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 2%

---

# Aree di personalizzazione {#personalization-areas}

![](../assets/do-not-localize/badge.png)

Il contenuto e la visualizzazione dei messaggi inviati da Journey Optimizer possono essere personalizzati in diversi modi.

Tutti i campi associati all’icona dell’editor possono aprire l’editor di personalizzazione e ricevere contenuti di personalizzazione.

![](assets/perso_icon.png)

## Personalizzare le e-mail

Durante la creazione dei messaggi del canale e-mail, il campo **Oggetto e-mail** è personalizzabile.

![](assets/perso_subject.png)

Nella finestra di progettazione e-mail puoi personalizzare il contenuto:

* Nel **messaggio**: fai clic all’interno di un blocco di testo, fai clic sull’icona **Personalizza** nella barra degli strumenti contestuale e seleziona il campo **Inserisci personalizzazione** . Per ulteriori informazioni sull’interfaccia di E-mail Designer, consulta questa sezione [a1/>.](../design-emails.md)

   ![](assets/perso_insert.png)

* Per un **collegamento**: seleziona un testo o un&#39;immagine all&#39;interno di un blocco di testo, fai clic sull&#39;icona **Inserisci collegamento** nella barra degli strumenti contestuale. Nella finestra puoi aggiungere un blocco di personalizzazione facendo clic sull&#39;icona **Aggiungi personalizzazione** .

   ![](assets/perso_link.png)

## Personalizzare le notifiche push

Nel **canale push**, la personalizzazione ti consente di ottimizzare la notifica push.

Puoi aggiungere la personalizzazione nei campi seguenti:

* **Titolo**
* **Corpo**
* **Audio personalizzato**
* **Badge**
* **Dati personalizzati**

![](assets/perso_push.png)

Per una documentazione completa sulla configurazione delle notifiche push, consulta [questa sezione](../configure-push.md).


## Utilizzare l’editor di espressioni

L’editor di espressioni è il fulcro della personalizzazione in Journey Optimizer.

È disponibile in ogni contesto in cui devi definire la personalizzazione come e-mail, push e offerte.

Nell’interfaccia dell’editor di espressioni, seleziona, organizza, personalizza e convalida tutti i dati per creare una personalizzazione personalizzata per il contenuto.

![](assets/perso_ee1.png)

Nella parte sinistra della schermata viene visualizzato un selettore di dominio che consente di selezionare l’origine da personalizzare.

* **Profilo** : elenca tutti i riferimenti associati allo schema di profilo descritto nella documentazione di  [Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it).
* **Iscrizione**  al segmento: elenca tutti i segmenti creati nel servizio Segmentazione di Adobe Experience Platform. Ulteriori informazioni sulla segmentazione sono disponibili [qui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=en)
* **Offerte** : elenca tutte le offerte associate a un posizionamento specifico. Seleziona il posizionamento e inserisci le offerte nel contenuto. Per una documentazione completa su come gestire le offerte, consulta [questa sezione](https://experienceleague.adobe.com/docs/customer-journey-management/using/create-messages/deliver-personalized-offers.html?lang=en#about-offer-decisioning)

Una volta selezionato, il riferimento viene aggiunto nell’editor.

>[!NOTE]
>
>L’icona Info accanto all’icona &quot;+&quot; apre una descrizione comandi che fornisce ulteriori dettagli per ogni variabile.

Nell’esempio seguente, l’editor di espressioni ti consente di selezionare i profili che compiono il loro compleanno oggi e quindi di completare la personalizzazione inserendo un’offerta specifica corrispondente a questo giorno.

![](assets/perso_ee2.png)




