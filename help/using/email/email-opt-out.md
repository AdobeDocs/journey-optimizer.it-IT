---
solution: Journey Optimizer
product: journey optimizer
title: Gestione della rinuncia e-mail
description: Scopri come gestire la rinuncia tramite e-mail
feature: Email Design, Consent Management
topic: Content Management
role: User
level: Intermediate
keywords: rinuncia, e-mail, collegamento, annullamento dell’iscrizione
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: b1d262723b68083d1a32d259f3974a287f898579
workflow-type: tm+mt
source-wordcount: '1031'
ht-degree: 26%

---

# Gestione della rinuncia e-mail {#email-opt-out}

Quando invii messaggi da percorsi o campagne, devi sempre assicurarti che i clienti abbiano la possibilità di annullare l’iscrizione in modo da non ricevere più comunicazioni. Una volta annullata l’iscrizione, i profili vengono rimossi automaticamente dal pubblico dei messaggi di marketing futuri.  [Ulteriori informazioni sulla gestione della privacy e della rinuncia](../privacy/opt-out.md)

>[!NOTE]
>
>Tutti i messaggi di marketing devono includere un collegamento di rinuncia. Questo non è necessario per i messaggi transazionali. La categoria del messaggio - **[!UICONTROL Marketing]** o **[!UICONTROL Transazionale]** - è definita al livello [configurazione canale](email-settings.md#email-type) e durante la creazione del messaggio.

Per inserire un collegamento di annullamento all’abbonamento nel contenuto dell’e-mail, puoi:

* Aggiungi un URL con un solo clic per annullare l’iscrizione nell’intestazione dell’e-mail. L&#39;opzione **[!UICONTROL Abilita annullamento sottoscrizione a elenco]** a livello di configurazione del canale aggiunge un collegamento di rinuncia all&#39;intestazione dell&#39;e-mail. [Ulteriori informazioni sulla rinuncia nell&#39;intestazione dell&#39;e-mail](#unsubscribe-header)

* Abilita **collegamento rinuncia con un solo clic** per l&#39;e-mail.  [Scopri come aggiungere un collegamento di rinuncia con un solo clic](#one-click-opt-out)

* Inserisci un **collegamento a una pagina di destinazione**. [Scopri come aggiungere una pagina di destinazione di rinuncia](#opt-out-external-lp)

Quando un destinatario fa clic sul collegamento di rinuncia, la sua richiesta di annullamento dell’iscrizione viene elaborata di conseguenza.

Per verificare che la scelta del profilo corrispondente sia stata aggiornata, passa ad Experience Platform e [individua il profilo](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide?lang=en#browse-tab){target="_blank"}. Nella [scheda Attributi](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide#attributes){target="_blank"}, puoi vedere che il valore di **[!UICONTROL choice]** è stato modificato in **[!UICONTROL no]**. Scopri di più sull’elaborazione del consenso nella [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/consent/adobe/overview.html?lang=it){target="_blank"}.

![](assets/opt-out-profile-choice.png)

>[!NOTE]
>
>Talvolta, gli eventi per l’annullamento dell’iscrizione potrebbero richiedere più tempo per essere riflessi a livello di profilo, a causa dell’elaborazione dei dati a valle. È necessario attendere affinché il sistema si aggiorni.

## Rinuncia in un unico passaggio {#opt-out-one-step}

Con [!DNL Adobe Journey Optimizer], puoi configurare le [impostazioni di configurazione e-mail](email-settings.md#list-unsubscribe) con un URL di annullamento dell&#39;iscrizione con un solo clic e un indirizzo e-mail generato automaticamente nell&#39;intestazione e-mail, oppure puoi includere un URL di rinuncia con un solo clic nel corpo dell&#39;e-mail.

### URL per annullamento iscrizione con un clic nell’intestazione dell’e-mail {#unsubscribe-header}

L’URL per l’annullamento dell’iscrizione all’elenco con un solo clic è un collegamento o un pulsante per l’annullamento dell’iscrizione visualizzato accanto alle informazioni sul mittente dell’e-mail e che consente ai destinatari di annullare immediatamente l’iscrizione alle mailing list con un solo clic. Scopri come gestire l’opzione **[!UICONTROL Annulla sottoscrizione elenco]** in [questa sezione](list-unsubscribe.md).

### Rinuncia con un clic dal contenuto dell’e-mail {#one-click-opt-out}

Per impostare un URL personalizzato per l’annullamento dell’iscrizione, inserisci un collegamento di rinuncia con un solo clic nel contenuto del messaggio e-mail e immetti l’URL desiderato, come descritto di seguito:

1. Accedi al contenuto dell&#39;e-mail e [inserisci un collegamento](../email/message-tracking.md#insert-links).
1. Seleziona **[!UICONTROL Rinuncia con un clic]** come tipo di collegamento.

   ![](assets/message-tracking-opt-out.png)

1. Immetti l’URL della pagina di destinazione a cui l’utente viene reindirizzato una volta annullata l’iscrizione. Questa pagina contiene una conferma del successo della rinuncia.

   >[!NOTE]
   >
   >Se hai attivato l&#39;opzione **[!UICONTROL Annulla sottoscrizione elenco]** al [livello di configurazione del canale](email-settings.md#list-unsubscribe) e l&#39;opzione predefinita **[!UICONTROL URL annullamento iscrizione]** con un solo clic è deselezionata, l&#39;URL della pagina di destinazione viene utilizzato anche quando gli utenti fanno clic sul collegamento di annullamento dell&#39;iscrizione nell&#39;intestazione dell&#39;e-mail. [Ulteriori informazioni](list-unsubscribe.md)

   ![](assets/message-tracking-opt-out-confirmation.png)

   Puoi personalizzare i tuoi collegamenti. Ulteriori informazioni sugli URL personalizzati in [questa sezione](../personalization/personalization-syntax.md).

1. Seleziona la modalità di applicazione della rinuncia: a livello di canale o di identità.

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Canale]**: la rinuncia si applica ai messaggi futuri inviati alla destinazione del profilo (ad esempio l’indirizzo e-mail) per il canale corrente. Se a un profilo sono associate più destinazioni, la rinuncia si applica a tutte le destinazioni (ad esempio gli indirizzi e-mail) nel profilo di quel canale.
   * **[!UICONTROL Identità]**: la rinuncia viene applicata ai messaggi futuri inviati alla destinazione specifica (ad esempio l’indirizzo e-mail) utilizzata per il messaggio corrente.
     <!--* **[!UICONTROL Subscription]**: The opt-out applies to future messages associated with a specific subscription list. This option can only be selected if the current message is associated with a subscription list.-->

1. Salva le modifiche.


## Rinuncia in due fasi {#opt-out-external-lp}

Il meccanismo di rinuncia standard si basa su due passaggi: l’abbonato fa clic sul collegamento di rinuncia in un’e-mail, quindi viene reindirizzato a una pagina di destinazione di rinuncia per confermare l’annullamento dell’abbonamento.

Per implementare questa modalità di annullamento dell’abbonamento, devi creare e pubblicare una pagina di destinazione di rinuncia e aggiungere un collegamento di annullamento dell’abbonamento nei messaggi e-mail, con un collegamento alla pagina di destinazione. Questi passaggi sono descritti di seguito.


### Prerequisiti {#prereq-lp}

Per impostare un meccanismo di rinuncia in due fasi, devi creare pagine di destinazione di annullamento dell’abbonamento personalizzate. La prima pagina di destinazione sarà collegata al messaggio e deve contenere un pulsante call-to-action. Quando l’utente fa clic sul pulsante, dovrebbe essere visualizzato un messaggio di conferma.

Scopri come creare una pagina di destinazione in Adobe Journey Optimizer per gestire gli annullamenti di abbonamenti in [questa pagina](../landing-pages/lp-use-cases.md#opt-out).

Puoi anche utilizzare una pagina di destinazione esterna. In tal caso, configura l’API per inviare le informazioni a Adobe Journey Optimizer quando un destinatario ha annullato l’abbonamento.

+++ Scopri come implementare una chiamata API di rinuncia

Per consentire ai destinatari di rinunciare selezionando la preferenza dalla pagina di destinazione, devi implementare una **chiamata API per abbonamento** tramite [Adobe Developer](https://developer.adobe.com){target="_blank"} per aggiornare le preferenze dei profili corrispondenti.

La chiamata POST è la seguente:

Endpoint: https://platform.adobe.io/journey/imp/consent/preferences

Parametri query:

* **parametri**: contiene il payload crittografato
* **pid**: ID profilo crittografato

Questi due parametri verranno inclusi nell’URL della pagina di destinazione di terze parti inviato al destinatario:

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

[!DNL Journey Optimizer] utilizza questi parametri per aggiornare la scelta del profilo corrispondente tramite la chiamata API [Adobe Developer](https://developer.adobe.com){target="_blank"}.

+++


### Aggiungere un collegamento per annullare l’iscrizione {#add-unsubscribe-link}

Devi innanzitutto aggiungere a un messaggio un collegamento che consenta di annullare l’iscrizione. Per farlo, segui la procedura indicata di seguito:

1. Crea un messaggio e [inserisci un collegamento](../email/message-tracking.md#insert-links) utilizzando la barra degli strumenti contestuale.

   ![](assets/opt-out-insert-link.png)

1. Seleziona la **[!UICONTROL pagina di destinazione]** dall&#39;elenco a discesa **[!UICONTROL Tipo]** e la pagina di destinazione di rinuncia nel campo **[!UICONTROL Pagina di destinazione]**.

   Se utilizzi una pagina di destinazione esterna, seleziona **[!UICONTROL Rinuncia/Annullamento iscrizione esterno]** dall&#39;elenco a discesa **[!UICONTROL Tipo]**.

   ![](assets/opt-out-link-type.png)

   Nel campo **[!UICONTROL Collegamento]**, incolla il collegamento alla pagina di destinazione delle terze parti.

   ![](assets/opt-out-link-url.png)

1. Fai clic su **[!UICONTROL Salva]**.


### Inviare il messaggio con il collegamento per annullare l’iscrizione {#send-message-unsubscribe-link}

Una volta configurato il collegamento che apre la pagina di destinazione in cui sarà possibile per annullare l’iscrizione, puoi creare e inviare il messaggio.

1. Configura il messaggio con un collegamento di annullamento dell’abbonamento e invialo ai tuoi abbonati.

1. Una volta ricevuto il messaggio, se il destinatario fa clic sul collegamento per annullare l’iscrizione, viene visualizzata la pagina di destinazione.

   ![](assets/opt-out-lp-example.png)

   >[!WARNING]
   >
   >Fai clic sul collegamento per annullare l’iscrizione nell’e-mail per aprire solo la pagina di destinazione. Il destinatario deve **inviare il modulo facendo clic sul pulsante di rinuncia nella pagina di destinazione** per completare l&#39;annullamento dell&#39;abbonamento e aggiornare il consenso al profilo.

1. Se il destinatario invia il modulo (in questo esempio, premendo il pulsante **[!UICONTROL Annulla iscrizione]** nella pagina di destinazione), i dati del profilo vengono aggiornati tramite la chiamata API.

1. Il destinatario che ha scelto l’opt-out viene quindi reindirizzato a una schermata con un messaggio di conferma che indica che la rinuncia è avvenuta con successo.

   ![](assets/opt-out-confirmation-example.png)

   L’utente non riceverà più comunicazioni dal tuo marchio, a meno che non acconsenta nuovamente.

