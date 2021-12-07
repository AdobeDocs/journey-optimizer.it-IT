---
title: Casi di utilizzo della pagina di destinazione
description: Scopri i casi d’uso più comuni con le pagine di destinazione in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
hidefromtoc: true
hide: true
exl-id: 8c00d783-54a3-45d9-bd8f-4dc58804d922
source-git-commit: 88b037e079a46e10f7ee4715e78e5edc5a34a6ce
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 19%

---

# Casi di utilizzo della pagina di destinazione

Di seguito sono riportati alcuni esempi di come è possibile utilizzare [!DNL Journey Optimizer] pagine di destinazione per consentire ai clienti di scegliere se accettare o meno alcune o tutte le tue comunicazioni.

<!--The main use cases are:
* Subscription to a service
* Opt-in
* Opt-out-->

## Iscrizione a un servizio {#subscription-to-a-service}

Uno dei casi d’uso più comuni consiste nell’invitare i clienti a [abbonamento a un servizio](subscription-list.md) (ad esempio una newsletter o un evento) tramite una pagina di destinazione. Le fasi principali sono presentate sul grafico seguente:

![](../assets/lp_subscription-uc.png)

Ad esempio, supponiamo che il mese prossimo organizzi un evento e desideri avviare una campagna di registrazione degli eventi<!--to keep your customers that are interested updated on that event-->. A questo scopo, invierai un’e-mail con un collegamento a una pagina di destinazione che consentirà ai destinatari di registrarsi a questo evento. Gli utenti che si registrano verranno aggiunti all’elenco di sottoscrizioni creato a questo scopo.

### Configurare la pagina di destinazione

1. Crea l&#39;elenco di iscrizione dell&#39;evento, che memorizzerà gli utenti registrati. Scopri come creare un elenco di abbonamenti [qui](subscription-list.md#define-subscription-list).

   ![](../assets/lp_subscription-uc-list.png)

1. [Creare una pagina di destinazione](create-lp.md) per consentire ai destinatari di registrarsi all’evento.

1. Configurare la registrazione [pagina di destinazione principale](create-lp.md#configure-primary-page).

1. Durante la progettazione della [contenuto della pagina di destinazione](design-lp.md), seleziona l’elenco di sottoscrizioni creato per aggiornarlo con i profili che selezionano la casella di controllo della registrazione.

   ![](../assets/lp_subscription-uc-lp-list.png)

1. Crea una pagina di ringraziamento che verrà visualizzata ai destinatari dopo l’invio del modulo di registrazione. Scopri come configurare le pagine secondarie di destinazione [qui](create-lp.md#configure-subpages).

   ![](../assets/lp_subscription-uc-thanks.png)

1. [Pubblica](create-lp.md#publish) la pagina di destinazione.

1. [Creare un messaggio e-mail](../create-message.md) per annunciare che la registrazione è ora aperta per il tuo evento.

1. [Inserire un collegamento](../message-tracking.md#insert-links) nel contenuto del messaggio. Seleziona **[!UICONTROL Landing page]** come **[!UICONTROL Link type]** e scegli la [pagina di destinazione](create-lp.md#configure-primary-page) creato per la registrazione.

   ![](../assets/lp_subscription-uc-link.png)

1. Salva il contenuto e [pubblica il messaggio](../publish-manage-message.md).

1. Invia il messaggio tramite un [percorso](../building-journeys/journey.md) per indirizzare il traffico verso la pagina di destinazione della registrazione.

   ![](../assets/lp_subscription-uc-journey.png)

   Una volta ricevuta l’e-mail, se i destinatari fanno clic sul collegamento alla pagina di destinazione, verranno indirizzati alla pagina di ringraziamento e verranno aggiunti all’elenco di iscrizione.

### Invia un messaggio e-mail di conferma {#send-confirmation-email}

Inoltre, puoi inviare un’e-mail di conferma ai destinatari che si sono registrati per l’evento. A questo scopo, segui i passaggi riportati qui sotto.

1. Crea un altro [percorso](../building-journeys/journey.md). Puoi eseguire questa operazione direttamente dalla pagina di destinazione facendo clic sul pulsante **[!UICONTROL Create journey]** pulsante . Puoi trovare ulteriori informazioni [qui](create-lp.md#configure-primary-page)

   ![](../assets/lp_subscription-uc-create-journey.png)

1. Apri **[!UICONTROL Events]** categoria e rilascia a **[!UICONTROL Segment Qualification]** nell’area di lavoro. Puoi trovare ulteriori informazioni [qui](../building-journeys/segment-qualification-events.md)

1. Fai clic in **[!UICONTROL Segment]** e selezionare l&#39;elenco di sottoscrizioni creato.

   ![](../assets/lp_subscription-uc-confirm-journey.png)

1. Seleziona l’e-mail di conferma desiderata e inviala attraverso il percorso.

   ![](../assets/lp_subscription-uc-confirm-email.png)

Tutti gli utenti che si sono registrati al tuo evento riceveranno l’e-mail di conferma.

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
