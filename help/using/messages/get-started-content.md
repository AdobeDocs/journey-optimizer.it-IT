---
title: Introduzione ai messaggi
description: Scopri come creare e distribuire messaggi personalizzati in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 712dc172-6c0d-4ce8-ba16-de99d65fc641
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 6%

---

# Introduzione ai messaggi {#get-started-messages}

>[!CONTEXTUALHELP]
>id="ajo_journey_message"
>title="Azioni sul canale"
>abstract="Utilizza le azioni del canale per inviare un messaggio push, SMS o e-mail."

Utilizzo [!DNL Journey Optimizer] creare e inviare notifiche push, SMS e messaggi e-mail personalizzati. Tutti i messaggi sono modificabili in linea come parte di un’azione sull’area di lavoro del Percorso.  Utilizza la funzionalità Salva come modello per riutilizzare facilmente il contenuto. È possibile:

* Utilizzo [!DNL Journey Optimizer] **funzionalità di progettazione e-mail** per creare o importare e-mail reattive.

* Sfruttamento **Adobe Experience Manager Assets Essentials** per arricchire le e-mail, crea e gestisci il database delle risorse.

* Trova **Foto di Adobe Stock** per creare i contenuti e migliorare la progettazione delle e-mail.

* Migliora l&#39;esperienza dei clienti creando **notifiche push, SMS ed e-mail** in base agli attributi del profilo.

* **Inviare consegne** in base a questi contenuti e tenere traccia del comportamento del cliente.

>[!NOTE]
>
>Gli utenti possono accedere, creare, modificare e/o pubblicare percorsi a seconda del loro profilo di prodotto. Ulteriori informazioni sulle autorizzazioni per gli utenti [in questa sezione](../administration/permissions.md).


## Aggiungi messaggi nei tuoi percorsi{#messages-in-journeys}

>[!CONTEXTUALHELP]
>id="ajo_message_category"
>title="Categoria messaggio"
>abstract="Scegliere Marketing per i messaggi commerciali o Transazionale per i messaggi non commerciali, come la conferma dell&#39;ordine, le notifiche di reimpostazione della password o le informazioni di consegna"

>[!CONTEXTUALHELP]
>id="ajo_message_surface"
>title="Superficie del canale"
>abstract="Una superficie del canale è un&#39;istanza di quel canale che dispone di tutte le impostazioni per eseguire correttamente un&#39;azione tramite una campagna o un percorso. Viene definito da un amministratore di sistema."

Per aggiungere messaggi nei percorsi, è sufficiente aggiungere un’attività push, SMS o e-mail nell’area di lavoro del percorso.

1. Inizia il tuo percorso con un [Evento](../building-journeys/general-events.md) o [Leggi segmento](../building-journeys/read-segment.md) attività.

1. Da **Azioni** sezione della palette, trascinare e rilasciare un **email**, un **SMS** o **Push** nell’area di lavoro.

   ![](assets/add-a-message.png)

1. Immetti un’etichetta e una descrizione.

1. Seleziona il messaggio **[!UICONTROL Category]**: scegli **Marketing** per i messaggi commerciali, o **Transazionale** per messaggi non commerciali quali conferma dell’ordine, notifiche di reimpostazione della password o informazioni di consegna.

   >[!CAUTION]
   >
   >Se hai definito [regole di frequenza](../configuration/frequency-rules.md) per un canale e una categoria specifici, vengono applicati automaticamente al messaggio selezionando tale canale e categoria. Attualmente solo il **[!UICONTROL Marketing]** categoria disponibile per le regole di frequenza.

   ![](assets/inline-message-category.png)

   >[!CAUTION]
   >
   >I messaggi di tipo marketing devono includere un [collegamento di rinuncia](../messages/consent.md#opt-out-management). Questo non è necessario per i messaggi transazionali in quanto questi possono essere inviati a profili che hanno annullato l’abbonamento a comunicazioni di marketing.

1. Seleziona il canale **[!UICONTROL Surface]** (ad es. predefinito messaggio) da utilizzare per inviare il messaggio.

   Una superficie è una configurazione definita da un [Amministratore di sistema](../start/path/administrator.md). Contiene tutti i parametri tecnici per l’invio del messaggio, ad esempio parametri di intestazione, sottodominio, app mobili e così via. [Ulteriori informazioni](../configuration/channel-surfaces.md).

   >[!CAUTION]
   >
   >È necessario scegliere una superficie di canale valida per la categoria di messaggi e il canale selezionati.

   Puoi accedere e modificare l’etichetta, la descrizione e la superficie del messaggio in qualsiasi momento utilizzando la **[!UICONTROL Properties]** nell’interfaccia dei messaggi.

1. Crea il contenuto del messaggio.

   Scopri i passaggi dettagliati per creare il contenuto del messaggio nella pagina seguente:

   * [Creare un messaggio e-mail](create-email.md)
   * [Creare una notifica push](create-push.md)
   * [Creare un messaggio SMS](create-sms.md)

## Abilita ottimizzazione del tempo di invio{#sto-in-journeys}

Per le notifiche e-mail e push, puoi abilitare **[!UICONTROL Send-time optimization]**.

Utilizzo **[!UICONTROL Send-time optimization]** per pianificare l’invio di messaggi personalizzati in modo che ogni utente possa aumentare le percentuali di apertura e clic dei messaggi. [Ulteriori informazioni](../messages/send-time-optimization.md).


## Parametri avanzati{#adv-settings}

I parametri avanzati sono di sola lettura e nascosti per impostazione predefinita.

Per accedere ai parametri avanzati, fai clic sul pulsante **[!UICONTROL Show read-only fields]** nella parte superiore del riquadro dei messaggi.

![](assets/show-read-only.png)

I parametri avanzati vengono visualizzati nella parte inferiore del riquadro dei messaggi. Questi parametri sono definiti dalla [amministratore di sistema](../start/path/administrator.md) in [superficie del canale](../configuration/channel-surfaces.md) (ad es. predefinito messaggio) associato al messaggio.

Per le notifiche push, puoi visualizzare i seguenti parametri: Token, AppID, AppPlatform.

![](assets/push-adv-parameters.png)

Per l’e-mail, puoi visualizzare l’indirizzo e-mail principale.

Per un uso specifico, è possibile ignorare questi valori in contesti specifici. Per forzare un valore, fai clic sul pulsante **Abilita sostituzione parametro** a destra del campo. Questa opzione può essere utile ad esempio per:

* Testa un&#39;e-mail, puoi aggiungere il tuo indirizzo e-mail. Dopo aver pubblicato il percorso, l’e-mail ti viene inviata.
* Fai riferimento all’indirizzo e-mail degli abbonati a un elenco. Ulteriori informazioni in [questo caso d&#39;uso](../building-journeys/message-to-subscribers-uc.md).

Fai clic sulla stessa icona per ripristinare il parametro predefinito.


## Sfoglia messaggi{#browse-message}

Quando in un percorso vengono utilizzati più messaggi, è possibile passare da un messaggio all’altro dal **Modifica contenuto** schermo.

![](assets/inline-messages-multi-content.png)

È quindi possibile [controllare gli avvisi](alerts.md) e [simulare](../design/preview.md) ogni contenuto da una singola visualizzazione.

## Duplica un messaggio {#duplicate-message}

Puoi copiare un messaggio esistente dall’area di lavoro del percorso.

Per eseguire questa operazione, effettua le seguenti operazioni:

1. Seleziona il messaggio da copiare.

1. Utilizza la **[!UICONTROL Copy]** dal pulsante **[!UICONTROL Action]** riquadro.

   ![](assets/message-duplicate.png)

1. Invio **crtl+V** per incollare il messaggio.

   Il messaggio viene aggiunto all’area di lavoro del percorso. Tutte le impostazioni e la configurazione verranno copiate nel nuovo messaggio.

   ![](assets/message-duplicated.png)

1. Rinomina il messaggio per essere in grado di distinguere il messaggio iniziale dalla copia, ad esempio durante la modifica dei messaggi, come segue:

   ![](assets/multi-message.png)


>[!NOTE]
>
>Per le e-mail, puoi anche trasformare un messaggio esistente in un modello. [Ulteriori informazioni](../design/email-templates.md).

## Eliminare un messaggio{#delete-message}

Per eliminare un messaggio, utilizza l’icona del cestino nella parte superiore del riquadro attività del canale.

![](assets/delete-message.png)

Utilizza la **[!UICONTROL Confirm]** da convalidare.
