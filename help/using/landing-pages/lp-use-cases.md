---
title: Casi di utilizzo della pagina di destinazione
description: Scopri i casi d’uso più comuni con le pagine di destinazione in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 21%

---

# Casi di utilizzo della pagina di destinazione

Di seguito sono riportati alcuni esempi di utilizzo [!DNL Journey Optimizer] pagine di destinazione per consentire ai clienti di scegliere se accettare o meno alcune o tutte le tue comunicazioni.

<!--The main use cases are:
* Subscription to a service
* Opt-in
* Opt-out-->

## Iscrizione a un servizio {#subscription-to-a-service}

I passaggi principali per l’abbonamento dei destinatari a un servizio sono descritti di seguito.

![](../assets/lp_subscription-uc.png)

Ad esempio, supponiamo che il mese prossimo organizzi un evento e desideri lanciare una campagna di registrazione dell’evento per aggiornare i clienti interessati a tale evento.

1. Crea l&#39;elenco di iscrizione dell&#39;evento. Ulteriori informazioni su [elenchi di abbonamenti](subscription-list.md)

1. [Creare una pagina di destinazione](create-lp.md), che consentirà ai destinatari di registrarsi all’evento.

1. Configura e progetta la pagina di destinazione della registrazione, compreso il collegamento all’elenco di sottoscrizione. Ulteriori informazioni sulla creazione di [pagina di destinazione principale](create-lp.md#configure-primary-page)

1. Crea una pagina di ringraziamento che verrà visualizzata ai destinatari dopo l’invio del modulo di registrazione. Ulteriori informazioni su [pagine secondarie di destinazione](create-lp.md#configure-subpages)

1. Crea un messaggio e-mail. Ulteriori informazioni su [creazione di messaggi](../create-message.md)

1. [Inserire un collegamento](../message-tracking.md#insert-links) nel messaggio. Seleziona **[!UICONTROL Landing page]** come **[!UICONTROL Link type]** e scegli la [pagina di destinazione](create-lp.md#configure-primary-page) creato per la registrazione.

   ![](../assets/lp_subscription-uc-link.png)

1. Salva il contenuto e [pubblica il messaggio](../publish-manage-message.md).

1. Invia il messaggio tramite un [percorso](../building-journeys/journey.md) per annunciare che la registrazione è ora aperta per il tuo evento e per indirizzare il traffico verso la pagina di destinazione della registrazione.

   Una volta ricevuta l’e-mail, se i destinatari fanno clic sul collegamento alla pagina di destinazione, verranno indirizzati alla pagina di ringraziamento e verranno aggiunti all’elenco degli abbonamenti.

1. Puoi inviare un’e-mail di conferma ai destinatari che si sono registrati per l’evento. Per farlo, invialo tramite un altro percorso utilizzando la **[!UICONTROL Segment qualification]** e seleziona l’elenco di sottoscrizioni creato come segmento.

<!--The event registration's subscription list tracks the profiles who registered and you can send them targeted event updates.-->

## Rinuncia {#opt-out}

Per consentire ai destinatari di annullare l’iscrizione alle comunicazioni, puoi includere un collegamento a una pagina di destinazione di rinuncia nelle e-mail.

Ulteriori informazioni sulla gestione del consenso dei destinatari e sull’importanza di questo in [questa sezione](../consent.md).

### Gestione degli opt-out {#opt-out-management}

Come requisito legale, è necessario dare ai destinatari la possibilità di annullare l’iscrizione alla ricezione di comunicazioni da un marchio. Ulteriori informazioni sulla legislazione applicabile nel [Documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target=&quot;_blank&quot;}.

Pertanto, devi sempre includere un **collegamento per l’annullamento dell’iscrizione** in ogni e-mail inviata ai destinatari:

* Facendo clic su questo collegamento, i destinatari verranno indirizzati a una pagina di destinazione contenente un pulsante per confermare l’opt-out.
* Facendo clic sul pulsante di rinuncia, i dati del profilo vengono aggiornati con queste informazioni.

### Configurare la rinuncia {#configure-opt-out}

Per consentire ai destinatari di un messaggio di annullare l’iscrizione alle comunicazioni tramite una pagina di destinazione, effettua le seguenti operazioni.

1. Crea [pagina di destinazione](create-lp.md). Utilizza le specifiche della pagina di destinazione **[!UICONTROL Form]** componente, definire un **[!UICONTROL Opt-out]** seleziona e scegli di aggiornare **[!UICONTROL Channel (email)]**: il profilo che controlla la casella di rinuncia nella pagina di destinazione verrà escluso da tutte le comunicazioni. [Ulteriori informazioni](design-lp.md)

   <!--You can also build your own landing page and host it on the third-party system of your choice. To keep?-->

1. [Crea un messaggio ](../create-message.md) in [!DNL Journey Optimizer].

1. Selezionare il testo nel contenuto e [inserire un collegamento](../message-tracking.md#insert-links) mediante la barra degli strumenti contestuale. Puoi anche utilizzare un collegamento su un pulsante.

   ![](../assets/lp_opt-out-insert-link.png)

1. Seleziona **[!UICONTROL Landing page]** dall’elenco a discesa **[!UICONTROL Link type]**.

1. Seleziona la [pagina di destinazione](create-lp.md#configure-primary-page) creato per la rinuncia.

   ![](../assets/lp_opt-out-landing-page.png)

1. Fai clic su **[!UICONTROL Save]**.

1. Salva il contenuto e [pubblica il messaggio](../publish-manage-message.md).

1. Invia il messaggio tramite un [percorso](../building-journeys/journey.md).

1. Una volta ricevuto il messaggio, se il destinatario fa clic sul collegamento di annullamento dell’iscrizione, viene visualizzata la pagina di destinazione.

   <!--![](../assets/lp_opt-out-lp-example.png)-->

1. Se il destinatario fa clic sul collegamento di rinuncia nella pagina di destinazione, i dati del profilo vengono aggiornati e non riceveranno comunicazioni dal brand se non si è effettuato nuovamente l’abbonamento.

   <!--The opted-out recipient is then redirected to a confirmation message screen indicating that opting out was successful.-->

   <!--![](../assets/lp_opt-out-confirmation-example.png)-->

Per verificare che la scelta del profilo corrispondente sia stata aggiornata, passa ad Experience Platform e accedi al profilo selezionando uno spazio dei nomi di identità e un valore di identità corrispondente. Ulteriori informazioni nel [Documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.

![](../assets/lp_opt-out-profile-choice.png)

Nella scheda **[!UICONTROL Attributes]**, puoi vedere che il valore di **[!UICONTROL choice]** è stato modificato in **[!UICONTROL no]**.

<!--

### Other ways to opt out

You can also enable your recipients to unsubscribe whithout using landing pages.

* **One-click opt-out**

    You can add a one-click opt-out link into your email content. This will enable your recipients to quickly unsubscribe from your communications, without being redirected to a landing page where they need to confirm opting out. [Learn more](../message-tracking.md#one-click-opt-out-link)

* **Unsubscribe link in header**

    If the recipients' email client supports displaying an unsubscribe link in the email header, emails sent with [!DNL Journey Optimizer] automatically include this link. [Learn more](../consent.md#unsubscribe-email)
-->