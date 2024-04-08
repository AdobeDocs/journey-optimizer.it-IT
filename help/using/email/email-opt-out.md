---
solution: Journey Optimizer
product: journey optimizer
title: Gestione della rinuncia e-mail
description: Scopri come gestire la rinuncia tramite e-mail
feature: Email Design, Privacy
topic: Content Management
role: User
level: Intermediate
keywords: rinuncia, e-mail, collegamento, annullamento dell’iscrizione
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: c082d9329949fd8dc68929e3934daf2d9dfdbd46
workflow-type: tm+mt
source-wordcount: '1029'
ht-degree: 76%

---

# Gestione della rinuncia e-mail {#email-opt-out}

Per consentire ai destinatari di annullare l’abbonamento alla ricezione di comunicazioni e-mail, devi sempre includere un’ **collegamento per annullare l’abbonamento** in ogni e-mail inviata ai destinatari. [Ulteriori informazioni sulla gestione della privacy e della rinuncia](../privacy/opt-out.md)

A questo scopo, puoi:

* Inserisci un **collegamento a una pagina di destinazione** in un messaggio e-mail per consentire agli utenti di annullare l’abbonamento alla ricezione di comunicazioni dal tuo marchio. Può essere:

   * A **[!DNL Journey Optimizer]pagina di destinazione**. [Scopri come aggiungere una pagina di destinazione di rinuncia](../landing-pages/lp-use-cases.md#opt-out)

   * A **una pagina di destinazione esterna**. [Scopri come aggiungere un collegamento di rinuncia esterno](#opt-out-external-lp)

* Aggiungi un **collegamento di rinuncia con un clic** nel contenuto dell’e-mail. Questo collegamento consentirà ai destinatari di annullare rapidamente l’iscrizione alle comunicazioni senza essere reindirizzati a una pagina di destinazione in cui confermare la rinuncia, per una procedura più snella. [Scopri come aggiungere un collegamento di rinuncia con un solo clic](#one-click-opt-out)

* Aggiungi un collegamento per annullare l’iscrizione nell’intestazione dell’e-mail. Se il **[!UICONTROL Annullamento iscrizione mailing list]** è abilitata a livello della superficie di canale, le e-mail corrispondenti inviate con Journey Optimizer includeranno un collegamento di annullamento all’abbonamento nell’intestazione dell’e-mail. [Ulteriori informazioni sulla rinuncia nell’intestazione dell’e-mail](#unsubscribe-header)

>[!NOTE]
>
>I messaggi e-mail di tipo marketing devono includere un collegamento di rinuncia, che non è necessario per i messaggi transazionali. La categoria del messaggio (**[!UICONTROL Marketing]** o **[!UICONTROL Transazionale]**) è definito nella sezione [superficie di canale](../configuration/channel-surfaces.md#email-type) e durante la creazione del messaggio).

## Rinuncia esterna {#opt-out-external-lp}

### Aggiungere un collegamento per annullare l’iscrizione {#add-unsubscribe-link}

Devi innanzitutto aggiungere a un messaggio un collegamento che consenta di annullare l’iscrizione. Per farlo, segui la procedura indicata di seguito:

1. Crea la pagina di destinazione per l’annullamento dell’abbonamento.

1. Inseriscila sul sistema di terze parti a tua scelta.

1. Crea un messaggio in un percorso.

1. Seleziona il testo nel contenuto e [inserisci un collegamento](../email/message-tracking.md#insert-links) utilizzando la barra degli strumenti contestuale.

   ![](assets/opt-out-insert-link.png)

1. Seleziona **[!UICONTROL Rinuncia/Annullamento iscrizione esterno]** dall’elenco a discesa **[!UICONTROL Tipo di collegamento]**.

   ![](assets/opt-out-link-type.png)

1. Nel campo **[!UICONTROL Collegamento]**, incolla il collegamento alla pagina di destinazione delle terze parti.

   ![](assets/opt-out-link-url.png)

1. Fai clic su **[!UICONTROL Salva]**.

### Implementare una chiamata API per la rinuncia {#opt-out-api}

Per consentire ai destinatari di rinunciare selezionando la preferenza dalla pagina di destinazione, devi implementare una **Chiamata API per abbonamento** da a [Adobe Developer](https://developer.adobe.com){target="_blank"} per aggiornare le preferenze dei profili corrispondenti.

La chiamata POST è la seguente:

Endpoint: https://platform.adobe.io/journey/imp/consent/preferences

Parametri query:

* **parametri**: contiene il payload crittografato
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

[!DNL Journey Optimizer] utilizzerà questi parametri per aggiornare la scelta del profilo corrispondente tramite [Adobe Developer](https://developer.adobe.com){target="_blank"} Chiamata API.

### Inviare il messaggio con il collegamento per annullare l’iscrizione {#send-message-unsubscribe-link}

Una volta configurato il collegamento che apre la pagina di destinazione in cui sarà possibile per annullare l’iscrizione, e implementata la chiamata API, il messaggio è pronto per essere inviato.

1. Invia il messaggio contenente il collegamento tramite un [percorso](../building-journeys/journey.md).

1. Una volta ricevuto il messaggio, se il destinatario fa clic sul collegamento per annullare l’iscrizione, viene visualizzata la pagina di destinazione.

   ![](assets/opt-out-lp-example.png)

1. Se il destinatario invia il modulo (in questo esempio, premendo il pulsante **Unsubscribe** nella pagina di destinazione), i dati del profilo vengono aggiornati tramite la [chiamata API](#opt-out-api).

1. Il destinatario che ha scelto l’opt-out viene quindi reindirizzato a una schermata con un messaggio di conferma che indica che la rinuncia è avvenuta con successo.

   ![](assets/opt-out-confirmation-example.png)

   L’utente non riceverà più comunicazioni dal tuo marchio, a meno che non acconsenta nuovamente.

1. Per verificare che la scelta del profilo corrispondente sia stata aggiornata, passa ad Experience Platform e accedi al profilo selezionando uno spazio dei nomi delle identità e un valore di identità corrispondente. Per ulteriori informazioni, consulta [Documentazione di Experienci Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=it#getting-started){target="_blank"}.

   ![](assets/opt-out-profile-choice.png)

   Nella scheda **[!UICONTROL Attributi]**, puoi vedere che il valore di **[!UICONTROL scelta]** è diventato **[!UICONTROL no]**.

## Rinuncia con un clic {#one-click-opt-out}

Per aggiungere un collegamento di rinuncia all’e-mail, segui la procedura seguente.

1. [Inserisci un collegamento](../email/message-tracking.md#insert-links) e seleziona il tipo di collegamento **[!UICONTROL Rinuncia con un clic]**.

   ![](assets/message-tracking-opt-out.png)

1. Immetti l’URL della pagina di destinazione a cui l’utente verrà reindirizzato una volta annullata l’iscrizione. Questa pagina è disponibile solo per confermare che la rinuncia è stata eseguita correttamente.

   >[!NOTE]
   >
   >Se hai attivato l’opzione **Annullamento iscrizione a mailing list** a livello della superficie di canale, questo URL verrà utilizzato anche quando gli utenti fanno clic sul collegamento di annullamento dell’iscrizione nell’intestazione dell’e-mail. [Ulteriori informazioni](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   Puoi personalizzare i tuoi collegamenti. Ulteriori informazioni sugli URL personalizzati sono disponibili in [questa sezione](../personalization/personalization-syntax.md).

1. Seleziona la modalità di applicazione della rinuncia: a livello di canale, identità o iscrizione.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Canale]**: la rinuncia si applica ai messaggi futuri inviati alla destinazione del profilo (ad esempio l’indirizzo e-mail) per il canale corrente. Se a un profilo sono associate più destinazioni, la rinuncia viene applicata a tutte le destinazioni (ad esempio gli indirizzi e-mail) nel profilo di quel canale.
   * **[!UICONTROL Identità]**: la rinuncia viene applicata ai messaggi futuri inviati alla destinazione specifica (ad esempio l’indirizzo e-mail) utilizzata per il messaggio corrente.
   * **[!UICONTROL Iscrizione]**: la rinuncia viene applicata ai messaggi futuri associati a un elenco iscrizioni specifico. Questa opzione può essere selezionata solo se il messaggio corrente è associato a un elenco di abbonamenti.

1. Salva le modifiche.

Quando il messaggio viene inviato tramite un [percorso](../building-journeys/journey.md), se un destinatario fa clic sul collegamento di rinuncia, il suo profilo viene immediatamente escluso.

## Collegamento per annullare l’iscrizione nell’intestazione dell’e-mail {#unsubscribe-header}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="Aggiungi un collegamento per annullare l’iscrizione nell’intestazione dell’e-mail"
>abstract="Abilita Annulla iscrizione mailing list per aggiungere un collegamento di annullamento iscrizione nell’intestazione dell’e-mail. Per impostare un URL per l’annullamento dell’iscrizione, inserisci un collegamento di rinuncia con un solo clic nel contenuto dell’e-mail."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=it#one-click-opt-out" text="Rinuncia con un clic"

Se l’opzione [Annullamento iscrizione a mailing list](email-settings.md#list-unsubscribe) è attiva a livello di superficie di canale, le e-mail corrispondenti inviate con [!DNL Journey Optimizer] includeranno un collegamento di annullamento dell’iscrizione nell’intestazione dell’e-mail.

Ad esempio, il collegamento per annullare l’iscrizione verrà visualizzato in Gmail in questo modo:

![](assets/unsubscribe-header.png)

>[!NOTE]
>
>Per visualizzare il collegamento di annullamento dell’iscrizione nell’intestazione dell’e-mail, il client e-mail dei destinatari deve supportare questa funzione.

L’indirizzo predefinito per l’annullamento dell’iscrizione è l’indirizzo **[!UICONTROL Invia a (annulla iscrizione)]** visualizzato nella superficie di canale corrispondente. [Ulteriori informazioni](email-settings.md#list-unsubscribe)

Per impostare un URL personalizzato per l’annullamento dell’iscrizione, inserisci un collegamento per la rinuncia con un solo clic nel contenuto del messaggio e-mail e immetti l’URL desiderato. [Ulteriori informazioni](#one-click-opt-out)

A seconda del client e-mail, clicca sul collegamento per annullare l’iscrizione dall’intestazione può avere uno degli effetti seguenti:

* La richiesta di annullamento dell’iscrizione viene inviata all’indirizzo predefinito di annullamento dell’iscrizione.

* Il destinatario viene indirizzato all’URL della pagina di destinazione specificato al momento dell’aggiunta del collegamento di rinuncia al messaggio.

  >[!NOTE]
  >
  >Se non aggiungi un collegamento di rinuncia con un solo clic nel contenuto del messaggio, non verrà visualizzata alcuna pagina di destinazione.

* Il profilo corrispondente viene immediatamente escluso e questa scelta viene aggiornata in Experience Platform. Per ulteriori informazioni, consulta [Documentazione di Experienci Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=it#getting-started){target="_blank"}.
