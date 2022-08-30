---
title: Aggiungere messaggi nelle campagne
description: Scopri come aggiungere messaggi in una campagna
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 87f9a4661b64cf24a8cd62bb9c70d5f1c9fcaddf
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 80%

---


# Aggiungere messaggi nelle campagne{#messages-in- campaigns}

Nelle campagne, seleziona il canale per progettare e personalizzare il messaggio da inviare al pubblico. Quando aggiungi un’e-mail, un SMS o un push alla campagna, puoi inviarlo immediatamente o pianificare il messaggio.

>[!NOTE]
>Puoi anche creare percorsi per l’invio dei messaggi attivati. [Ulteriori informazioni](messages-in-journeys.md).

Scopri come aggiungere e configurare messaggi in una campagna [in questa sezione](../campaigns/create-campaign.md)

Scopri i passaggi dettagliati per creare il contenuto del messaggio nella pagina seguente:

* [Creare un messaggio e-mail](create-email.md)
* [Creare una notifica push](create-push.md)
* [Creare un messaggio SMS](create-sms.md)

## Abilitare l’ottimizzazione dell’ora di invio{#sto-in-journeys}

Per le notifiche e-mail e push, puoi abilitare **[!UICONTROL Send-time optimization]**.

Utilizza **[!UICONTROL Send-time optimization]** per pianificare un’ora di invio personalizzata in modo da aumentare le percentuali di apertura e clic sui messaggi da parte di ogni utente. [Ulteriori informazioni](../messages/send-time-optimization.md).

## Parametri avanzati{#adv-settings}

I parametri avanzati sono di sola lettura e nascosti per impostazione predefinita.

Per accedere ai parametri avanzati, fai clic sull’icona **[!UICONTROL Show read-only fields]** nella parte superiore del riquadro dei messaggi.

![](assets/show-read-only.png)

I parametri avanzati vengono visualizzati nella parte inferiore del riquadro dei messaggi. Questi parametri sono definiti dall’[amministratore di sistema](../start/path/administrator.md) nella [superficie di canale](../configuration/channel-surfaces.md) (ossia il predefinito per messaggi) associata al messaggio.

Per le notifiche push, puoi visualizzare i seguenti parametri: Token, AppID, AppPlatform.

![](assets/push-adv-parameters.png)

Per l’e-mail, puoi visualizzare l’indirizzo e-mail principale.

Per un uso particolare, è possibile ignorare questi valori in contesti specifici. Per forzare un valore, fai clic sul pulsante **Abilita sovrascrittura del parametro** a destra del campo. Questa opzione può essere utile ad esempio nelle seguenti situazioni:

* Per il test di un’e-mail, puoi utilizzare il tuo indirizzo e-mail. Dopo aver pubblicato il percorso, l’e-mail viene inviata al tuo indirizzo.
* Fai riferimento all’indirizzo e-mail degli iscritti a un elenco. Per ulteriori informazioni, consulta [questo caso d’uso](../building-journeys/message-to-subscribers-uc.md).

Fai clic sulla stessa icona per nascondere le impostazioni avanzate.

## Sfogliare i messaggi{#browse-message}

Quando in un percorso vengono utilizzati più messaggi, è possibile passare da un messaggio all’altro dalla schermata **Modifica contenuto**.

![](assets/inline-messages-multi-content.png)

È quindi possibile [controllare gli avvisi](alerts.md) e [simulare](../design/preview.md) ogni contenuto da una singola visualizzazione.

## Duplicare un messaggio {#duplicate-message}

Puoi copiare un messaggio esistente dall’area di lavoro del percorso.

Per farlo, segui la procedura indicata di seguito:

1. Seleziona il messaggio da copiare.

1. Utilizza il pulsante **[!UICONTROL Copy]** dal riquadro **[!UICONTROL Action]**.

   ![](assets/message-duplicate.png)

1. Usa **Crtl+V** per incollare il messaggio.

   Il messaggio viene aggiunto all’area di lavoro del percorso. Tutte le impostazioni e la configurazione verranno copiate nel nuovo messaggio.

   ![](assets/message-duplicated.png)

1. Rinomina il messaggio per essere in grado di distinguere quello iniziale dalla copia, ad esempio durante la modifica dei messaggi, come segue:

   ![](assets/multi-message.png)


>[!NOTE]
>
>Per le e-mail, puoi anche convertire un messaggio esistente in un modello. [Ulteriori informazioni](../design/email-templates.md).

## Eliminare un messaggio{#delete-message}

Per eliminare un messaggio, utilizza l’icona del cestino nella parte superiore del riquadro Attività dell’azione del canale.

![](assets/delete-message.png)

Utilizza il pulsante **[!UICONTROL Confirm]** per confermare.
