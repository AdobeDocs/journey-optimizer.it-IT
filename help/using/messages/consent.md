---
title: Gestire l’opt-out
description: Scopri come gestire l’opt-out e la privacy
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 06a7abc2ada930356cbaf45ce01eed5e3156f2e3
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 98%

---

# Gestire l’opt-out {#consent}

Utilizza [!DNL Journey Optimizer] per tenere traccia del consenso dei destinatari alla comunicazione e capire in che modo desiderano interagire con il tuo marchio gestendo le preferenze e gli abbonamenti.

Regolamenti come il GDPR stabiliscono che si devono soddisfare requisiti specifici prima di poter utilizzare le informazioni degli interessati. Inoltre, gli interessati dovrebbero poter modificare il loro consenso in qualsiasi momento.

**Perché è importante?**

* Il mancato rispetto di queste normative introduce rischi legali normativi per il tuo marchio.
* Ti aiuta a evitare l’invio di comunicazioni non richieste ai destinatari, in modo che queste non vengano contrassegnate come spam danneggiando la tua reputazione.

Per ulteriori informazioni sulla gestione della privacy e sulle normative applicabili, consulta la [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=it){target=&quot;_blank&quot;}.

## Gestione degli opt-out {#opt-out-management}

Come requisito legale, è necessario dare ai destinatari la possibilità di annullare l’iscrizione alla ricezione di comunicazioni da parte di un marchio. Ulteriori informazioni sulle normative applicabili sono disponibili nella [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=it#regulations){target=&quot;_blank&quot;}.

Pertanto, devi sempre includere un **collegamento per l’annullamento dell’iscrizione** in ogni e-mail inviata ai destinatari:

* Facendo clic su questo collegamento, i destinatari verranno indirizzati a una pagina di destinazione contenente un pulsante per confermare l’opt-out.
* Facendo clic sul pulsante di opt-out, viene effettuata una chiamata Adobe I/O per aggiornare i dati del profilo con queste informazioni. [Ulteriori informazioni](#consent-service-api).

### Aggiungi un collegamento per annullare l’abbonamento {#add-unsubscribe-link}

Per aggiungere un collegamento per l’annullamento dell’iscrizione, effettua le seguenti operazioni:

1. Crea la pagina di destinazione per l’annullamento dell’iscrizione.

1. Inseriscilo sul sistema di terze parti a tua scelta.

1. [Crea un messaggio ](create-message.md) in [!DNL Journey Optimizer].

1. Seleziona il testo nel contenuto e inserisci un collegamento utilizzando la barra degli strumenti contestuale.

   ![](assets/opt-out-insert-link.png)

1. Seleziona **[!UICONTROL Unsubscription link]** dall’elenco a discesa **[!UICONTROL Link type]**.

   ![](assets/opt-out-link-type.png)

1. Nel campo **[!UICONTROL Link]**, copia il collegamento alla pagina di destinazione.

   ![](assets/opt-out-link-url.png)

1. Fai clic su **[!UICONTROL Save]**.

1. Salva il contenuto e [pubblica il messaggio](publish-manage-message.md).

   >[!NOTE]
   >
   >L’URL della pagina di destinazione di terze parti includerà tre parametri che verranno utilizzati per aggiornare le preferenze dei profili tramite una chiamata di Adobe I/O. [Ulteriori informazioni](#consent-service-api).

1. Invia il messaggio con il collegamento alla pagina di destinazione tramite un [percorso](../building-journeys/journey.md).

1. Una volta ricevuto il messaggio, se il destinatario fa clic sul collegamento di annullamento dell’iscrizione, viene visualizzata la pagina di destinazione.

   ![](assets/opt-out-lp-example.png)

1. Se il destinatario fa clic sul pulsante di opt-out nella pagina di destinazione (qui, il pulsante **Annulla iscrizione**), i dati del profilo vengono aggiornati tramite una chiamata di [Adobe I/O](#opt-out-api).

   Il destinatario che ha scelto l’opt-out viene quindi reindirizzato a una schermata con un messaggio di conferma che indica che la rinuncia è avvenuta con successo.

   ![](assets/opt-out-confirmation-example.png)

   L’utente non riceverà più comunicazioni dal tuo marchio, a meno che non acconsenta nuovamente.

Per verificare che la scelta del profilo corrispondente sia stata aggiornata, passa ad Experience Platform e accedi al profilo selezionando uno spazio dei nomi di identità e un valore di identità corrispondente. Per ulteriori informazioni, consulta la [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=it#getting-started){target=&quot;_blank&quot;}.

![](assets/opt-out-profile-choice.png)

Nella scheda **[!UICONTROL Attributes]**, puoi vedere che il valore di **[!UICONTROL choice]** è stato modificato in **[!UICONTROL no]**.

### Chiamata API per opt-out {#opt-out-api}

Una volta che il destinatario ha rinunciato facendo clic sul collegamento di annullamento dell’iscrizione, viene effettuata una chiamata API di Adobe I/O  per aggiornare le preferenze del profilo corrispondente.

La chiamata Adobe I/O POST è la seguente:

Endpoint: platform.adobe.io/journey/imp/consent/preferences

Parametri query:

* **parametri**: contiene il payload crittografato
* **sig**: signature
* **pid**: ID profilo crittografato

Questi parametri sono disponibili dal collegamento di annullamento dell’iscrizione inviato al destinatario, ovvero l’URL che consnete di aprire la pagina di destinazione di terze parti per un determinato destinatario:

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

[!DNL Journey Optimizer] utilizzerà questi parametri per aggiornare la scelta del profilo corrispondente.

## Rinuncia con un clic {#one-click-opt-out}

Poiché molti clienti cercano un processo più semplice per annullare l’abbonamento, puoi anche aggiungere al contenuto dell’e-mail un collegamento di rinuncia con un solo clic. Questo collegamento consentirà ai destinatari di annullare rapidamente l’abbonamento alle comunicazioni senza essere reindirizzati a una pagina di destinazione in cui devono confermare la rinuncia.

Scopri come aggiungere al contenuto del messaggio un collegamento di rinuncia in [questa sezione](message-tracking.md#one-click-opt-out-link).

Una volta inviato il messaggio tramite un [percorso](../building-journeys/journey.md), se un destinatario fa clic sul collegamento di rinuncia, il suo profilo viene immediatamente escluso.

## Collegamento per annullare l’abbonamento nell’intestazione {#unsubscribe-email}

Se il client e-mail dei destinatari supporta la visualizzazione di un collegamento di annullamento all’abbonamento nell’intestazione e-mail, le e-mail inviate con [!DNL Journey Optimizer] includono automaticamente questo collegamento.

Ad esempio, il collegamento per annullare l’abbonamento verrà visualizzato in Gmail in questo modo:

![](assets/unsubscribe-email.png)

A seconda del client e-mail, facendo clic sul collegamento per annullare l’abbonamento dall’intestazione si verifica uno dei seguenti impatti:

* Il profilo corrispondente viene immediatamente escluso e questa scelta viene aggiornata in Experience Platform. Per ulteriori informazioni, consulta la [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}.

* Ha lo stesso effetto di fare clic sul collegamento per annullare l’abbonamento dal contenuto dell’e-mail: il destinatario viene reindirizzato a una pagina di destinazione con un pulsante per confermare la rinuncia. Ulteriori informazioni sulla gestione delle rinunce sono disponibili in [questa sezione](#opt-out-management).

## Gestione degli opt-out per notifiche push {#push-opt-out-management}

I destinatari delle notifiche push possono annullare l’iscrizione dai propri dispositivi.

Ad esempio, al momento del download o dell’utilizzo dell’app, possono scegliere di interrompere le notifiche. Analogamente, possono modificare le impostazioni di notifica tramite il sistema operativo mobile.
