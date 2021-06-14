---
title: Contesti di personalizzazione in Journey Optimizer
description: Scopri in quali contesti puoi aggiungere la personalizzazione
feature: Personalizzazione
topic: Personalizzazione
role: Data Engineer
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 3%

---

# Contesto e strumento di personalizzazione {#personalization-areas}

![](../assets/do-not-localize/badge.png)

Il contenuto e la visualizzazione dei messaggi inviati da Journey Optimizer possono essere personalizzati in diversi modi.

Tutti i campi associati all’icona dell’editor possono aprire l’editor di personalizzazione e ricevere contenuti di personalizzazione.

![](assets/perso_icon.png)

## Personalizzare le e-mail

Quando crei un’e-mail, puoi aggiungere la personalizzazione nel campo **Oggetto e-mail** del messaggio.

![](assets/perso_subject.png)

Nella finestra di progettazione e-mail puoi personalizzare il contenuto:

* Nel **messaggio**: fai clic all’interno di un blocco di testo, fai clic sull’icona **Personalizza** nella barra degli strumenti contestuale e seleziona il campo **Inserisci personalizzazione** . Per ulteriori informazioni sull’interfaccia di E-mail Designer, consulta questa sezione [a1/>.](../design-emails.md)

   ![](assets/perso_insert.png)

* Per un **collegamento**: seleziona un testo o un&#39;immagine all&#39;interno di un blocco di testo, fai clic sull&#39;icona **Inserisci collegamento** nella barra degli strumenti contestuale. Nella finestra puoi aggiungere un blocco di personalizzazione facendo clic sull&#39;icona **Aggiungi personalizzazione** .

   ![](assets/perso_link.png)

## Personalizzare le notifiche push

Puoi anche personalizzare le **notifiche push** nei campi seguenti:

* **Titolo**
* **Corpo**
* **Audio personalizzato**
* **Badge**
* **Dati personalizzati**

![](assets/perso_push.png)

Ulteriori informazioni sulla configurazione delle notifiche push in [questa sezione](../create-push.md).

## Utilizzare l’editor di espressioni

L’editor di espressioni è il fulcro della personalizzazione in Journey Optimizer.

È disponibile in ogni contesto in cui devi definire la personalizzazione come e-mail, push e offerte.

Nell’interfaccia dell’editor di espressioni, seleziona, organizza, personalizza e convalida tutti i dati per creare una personalizzazione personalizzata per il contenuto.

![](assets/perso_ee1.png)

Nella parte sinistra della schermata viene visualizzato un selettore di dominio che consente di selezionare l’origine da personalizzare.

* **Profilo** : elenca tutti i riferimenti associati allo schema di profilo descritto nella documentazione di  [Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it).
* **Iscrizione**  al segmento: elenca tutti i segmenti creati nel servizio Segmentazione di Adobe Experience Platform. Ulteriori informazioni sulla segmentazione sono disponibili [qui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=en)
* **Offerte** : elenca tutte le offerte associate a un posizionamento specifico. Seleziona il posizionamento e inserisci le offerte nel contenuto. Per una documentazione completa su come gestire le offerte, consulta [questa sezione](../deliver-personalized-offers.md)
* **Contesto** : quando  **** Messageactivity viene utilizzato in un percorso, i campi percorso contestuale sono disponibili in questo menu. Fai riferimento a [questa sezione](personalization-use-case.md)
* **Funzioni**  di supporto: elenca tutte le funzioni di supporto disponibili per eseguire operazioni sui dati, ad esempio calcoli, formattazione dei dati o conversioni, condizioni e manipolarle nel contesto della personalizzazione. [Ulteriori informazioni](functions/functions.md)



Una volta selezionato, il riferimento viene aggiunto nell’editor.

>[!NOTE]
>
>L’icona Info accanto all’icona &quot;+&quot; apre una descrizione comandi che fornisce ulteriori dettagli per ogni variabile.

Nell’esempio seguente, l’editor di espressioni ti consente di selezionare i profili che compiono il loro compleanno oggi e quindi di completare la personalizzazione inserendo un’offerta specifica corrispondente a questo giorno.

![](assets/perso_ee2.png)




