---
title: Gestire l’opt-out
description: Scopri come gestire l’opt-out e la privacy
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 1d0e28583c500d5eddf9f88250f279d188c4784a
workflow-type: tm+mt
source-wordcount: '1259'
ht-degree: 74%

---

# Gestire il consenso {#consent}

Utilizza [!DNL Journey Optimizer] per tenere traccia del consenso dei destinatari alle comunicazioni e capire in che modo desiderano interagire con il tuo marchio gestendo le preferenze e gli abbonamenti.

Regolamenti come il GDPR stabiliscono che si devono soddisfare requisiti specifici prima di poter utilizzare le informazioni degli interessati. Inoltre, gli interessati dovrebbero poter modificare il loro consenso in qualsiasi momento.

**Perché è importante?**

* Il mancato rispetto di queste normative introduce rischi legali normativi per il tuo marchio.
* Ti aiuta a evitare l’invio di comunicazioni non richieste ai destinatari, in modo che queste non vengano contrassegnate come spam danneggiando la tua reputazione.

Per ulteriori informazioni sulla gestione della privacy e sulle normative applicabili, consulta la [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=it){target=&quot;_blank&quot;}.

>[!NOTE]
>
>In [!DNL Journey Optimizer], il consenso è gestito dallo [Schema di consenso](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=it){target=&quot;_blank&quot;} di Experience Platform. Per impostazione predefinita, il valore del campo di consenso è vuoto e viene trattato come consenso alla ricezione delle comunicazioni. Puoi modificare questo valore predefinito durante l’onboarding in uno dei possibili valori elencati [qui](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=it#choice-values){target=&quot;_blank&quot;}.

## Gestione della rinuncia e-mail {#opt-out-management}

Come requisito legale, è necessario dare ai destinatari la possibilità di annullare l’iscrizione alla ricezione di comunicazioni da parte di un marchio. Ulteriori informazioni sulle normative applicabili sono disponibili nella [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=it#regulations){target=&quot;_blank&quot;}.

Pertanto, devi sempre includere un **collegamento che consenta di annullare l’abbonamento** in ogni e-mail inviata ai destinatari:

* Facendo clic su questo collegamento, i destinatari verranno indirizzati a una pagina di destinazione contenente un pulsante per confermare la rinuncia.
* Dopo aver confermato la scelta, i dati dei profili verranno aggiornati con queste informazioni.

>[!NOTE]
>
>I messaggi e-mail di tipo marketing devono includere un collegamento di rinuncia, che non è necessario per i messaggi transazionali. La categoria del messaggio (**[!UICONTROL Marketing]** o **[!UICONTROL Transactional]**) è definita nella [livello predefinito del messaggio](../configuration/message-presets.md#email-type) e quando [creazione del messaggio](get-started-content.md#create-new-message).

### Rinuncia esterna {#opt-out-external-lp}

In questo caso, puoi inserire in un’e-mail un collegamento a una pagina di destinazione esterna per consentire agli utenti di annullare l’abbonamento alla ricezione di comunicazioni dal tuo marchio.

#### Aggiungere un collegamento per annullare l’abbonamento {#add-unsubscribe-link}

Devi innanzitutto aggiungere a un messaggio un collegamento che consenta di annullare l’abbonamento. Per farlo, segui la procedura indicata di seguito:

1. Crea la pagina di destinazione per l’annullamento dell’abbonamento.

1. Inseriscilo sul sistema di terze parti a tua scelta.

1. [Crea un messaggio](get-started-content.md) in [!DNL Journey Optimizer].

1. Seleziona il testo nel contenuto e [inserisci un collegamento](../design/message-tracking.md#insert-links) utilizzando la barra degli strumenti contestuale.

   ![](assets/opt-out-insert-link.png)

1. Seleziona **[!UICONTROL External Opt-out/Unsubscription]** dall’elenco a discesa **[!UICONTROL Link type]**.

   ![](assets/opt-out-link-type.png)

1. Nel campo **[!UICONTROL Link]**, incolla il collegamento alla pagina di destinazione della terza parte.

   ![](assets/opt-out-link-url.png)

1. Fai clic su **[!UICONTROL Save]**.

1. Salva il contenuto e [pubblica il messaggio](publish-manage-message.md).

#### Implementare una chiamata API per la rinuncia {#opt-out-api}

Per fare in modo che i destinatari rinunciino quando inviano la loro scelta dalla pagina di destinazione, devi implementare un **Chiamata API per abbonamento** attraverso [Sviluppatore Adobe](https://developer.adobe.com/){target=&quot;_blank&quot;} per aggiornare le preferenze dei profili corrispondenti.

Questa chiamata POST è la seguente:

Endpoint: platform.adobe.io/journey/imp/consent/preferences

Parametri query:

* **parametri**: contiene il payload crittografato
* **sig**: signature
* **pid**: ID profilo crittografato

Questi tre parametri verranno inclusi nell’URL della pagina di destinazione di terze parti inviato al destinatario:

![](assets/opt-out-parameters.png)

Requisiti dell’intestazione:

* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* autorizzazione (token utente dal tuo account tecnico)

Corpo della richiesta:

```
{
   "marketing": [
       {
            "type": "email",           
            "choice": "no",          
            "scope": "channel"       
        }
    ],
 
}
```

[!DNL Journey Optimizer] utilizzerà questi parametri per aggiornare la scelta del profilo corrispondente tramite [Sviluppatore Adobe](https://developer.adobe.com)Chiamata API {target=&quot;_blank&quot;}.

#### Inviare il messaggio con il collegamento per annullare l’abbonamento {#send-message-unsubscribe-link}

Una volta configurato il collegamento che apre la pagina di destinazione in cui sarà possibile per annullare l’abbonamento, e implementata la chiamata API, il messaggio è pronto per essere inviato.

1. Invia il messaggio contenente il collegamento tramite un [percorso](../building-journeys/journey.md).

1. Una volta ricevuto il messaggio, se il destinatario fa clic sul collegamento per annullare l’abbonamento, viene visualizzata la pagina di destinazione.

   ![](assets/opt-out-lp-example.png)

1. Se il destinatario invia il modulo (qui, premendo il pulsante **Annulla sottoscrizione** nella pagina di destinazione), i dati del profilo vengono aggiornati tramite [Chiamata API](#opt-out-api).

1. Il destinatario che ha scelto l’opt-out viene quindi reindirizzato a una schermata con un messaggio di conferma che indica che la rinuncia è avvenuta con successo.

   ![](assets/opt-out-confirmation-example.png)

   L’utente non riceverà più comunicazioni dal tuo marchio, a meno che non acconsenta nuovamente.

1. Per verificare che la scelta del profilo corrispondente sia stata aggiornata, passa ad Experience Platform e accedi al profilo selezionando uno spazio dei nomi di identità e un valore di identità corrispondente. Per ulteriori informazioni, consulta la [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=it#getting-started){target=&quot;_blank&quot;}.

   ![](assets/opt-out-profile-choice.png)

   Nella scheda **[!UICONTROL Attributes]**, puoi vedere che il valore di **[!UICONTROL choice]** è stato modificato in **[!UICONTROL no]**.

### Rinuncia con un clic {#one-click-opt-out}

Poiché molti clienti cercano un processo più semplice per annullare l’abbonamento, puoi anche aggiungere al contenuto dell’e-mail un collegamento di rinuncia con un solo clic. Questo collegamento consentirà ai destinatari di annullare rapidamente l’abbonamento alle comunicazioni senza essere reindirizzati a una pagina di destinazione in cui confermare la rinuncia, per una procedura più snella.

Per aggiungere un collegamento di rinuncia all’e-mail, segui la procedura seguente.

1. [Inserisci un collegamento](../design/message-tracking.md#insert-links) e seleziona **[!UICONTROL One click Opt-out]** come tipo di collegamento.

   ![](assets/message-tracking-opt-out.png)

1. Seleziona la modalità di applicazione della rinuncia: a livello di canale, identità o abbonamento.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Channel]**: la rinuncia si applica ai messaggi futuri inviati alla destinazione del profilo (ad esempio l’indirizzo e-mail) per il canale corrente. Se a un profilo sono associate più destinazioni, la rinuncia si applica a tutte le destinazioni (ad esempio gli indirizzi e-mail) nel profilo di quel canale.
   * **[!UICONTROL Identity]**: la rinuncia si applica ai messaggi futuri inviati alla destinazione specifica (ad esempio l’indirizzo e-mail) utilizzata per il messaggio corrente.
   * **[!UICONTROL Subscription]**: la rinuncia si applica ai messaggi futuri associati a un elenco di abbonamento specifico. Questa opzione può essere selezionata solo se il messaggio corrente è associato a un elenco di abbonamenti.

1. Immetti l’URL della pagina di destinazione a cui l’utente verrà reindirizzato una volta annullato l’abbonamento. Questa pagina è disponibile solo per confermare che la rinuncia è stata eseguita correttamente.

   >[!NOTE]
   >
   >Se hai attivato la **Annulla sottoscrizione elenco** a livello del predefinito del messaggio, questo URL verrà utilizzato anche quando gli utenti fanno clic sul collegamento di annullamento dell’abbonamento nell’intestazione dell’e-mail. [Ulteriori informazioni](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   Puoi personalizzare i tuoi collegamenti. Ulteriori informazioni sugli URL personalizzati sono disponibili in [questa sezione](../personalization/personalization-syntax.md).

1. Salva le modifiche.

Quando il messaggio viene inviato tramite un [percorso](../building-journeys/journey.md), se un destinatario fa clic sul collegamento di rinuncia, il suo profilo viene immediatamente escluso.

### Collegamento per annullare l’abbonamento nell’intestazione del messaggio {#unsubscribe-header}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="Aggiungi un collegamento per annullare l’abbonamento all’intestazione dell’e-mail"
>abstract="Abilita Annulla sottoscrizione a elenco per aggiungere un collegamento di annullamento all’abbonamento all’intestazione dell’e-mail. Per impostare un URL per l’annullamento della sottoscrizione, inserisci un collegamento per la rinuncia con un solo clic nel contenuto del messaggio e-mail."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/messages/consent.html?lang=en#one-click-opt-out" text="Rinuncia con un clic"

Se la [Opzione Annulla sottoscrizione elenco](../configuration/message-presets.md#list-unsubscribe) è attivato a livello di predefinito del messaggio, le e-mail corrispondenti inviate con [!DNL Journey Optimizer] includerà un collegamento di annullamento all’abbonamento nell’intestazione dell’e-mail.

Ad esempio, il collegamento per annullare l’abbonamento verrà visualizzato in Gmail in questo modo:

![](assets/unsubscribe-header.png)

>[!NOTE]
>
>Per visualizzare il collegamento di annullamento all’abbonamento nell’intestazione dell’e-mail, il client e-mail dei destinatari deve supportare questa funzione.

L’indirizzo predefinito per l’annullamento della sottoscrizione è **[!UICONTROL Mailto (unsubscribe)]** indirizzo visualizzato nel predefinito messaggio corrispondente. [Ulteriori informazioni](../configuration/message-presets.md#list-unsubscribe).

Per impostare un URL personalizzato per l’annullamento della sottoscrizione, inserisci un collegamento per la rinuncia con un solo clic nel contenuto del messaggio e-mail e immetti l’URL desiderato. [Ulteriori informazioni](#one-click-opt-out)

A seconda del client e-mail, facendo clic sul collegamento per annullare l’abbonamento dall’intestazione possono avere i seguenti impatti:

* La richiesta di annullamento dell’abbonamento viene inviata all’indirizzo predefinito di annullamento dell’abbonamento.

* Il destinatario viene indirizzato all’URL della pagina di destinazione specificato al momento dell’aggiunta del collegamento di rinuncia al messaggio.

   >[!NOTE]
   >
   >Se non aggiungi un collegamento di rinuncia con un solo clic al contenuto del messaggio, non verrà visualizzata alcuna pagina di destinazione.

* Il profilo corrispondente viene immediatamente escluso e questa scelta viene aggiornata in Experience Platform. Per ulteriori informazioni, consulta la [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.

## Gestione degli opt-out per notifiche push {#push-opt-out-management}

I destinatari delle notifiche push possono annullare l’iscrizione dai propri dispositivi.

Ad esempio, al momento del download o dell’utilizzo dell’app, possono scegliere di interrompere le notifiche. Analogamente, possono modificare le impostazioni di notifica tramite il sistema operativo mobile.
