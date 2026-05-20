---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il provider Infobip
description: Scopri come configurare il tuo ambiente per l’invio di messaggi mobili e MMS con Journey Optimizer con Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
TQID: https://experienceleague.adobe.com/hkloRlDuOO-lNSezWvOcD3dtsHrhDqCJGo3cHq5pWog
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126
subfeature_v2: id: d2e8a157-b3b0-4143-9ff3-809bf400be56
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0201927f8d9260e8ba1d0db7014d6a7b30d09062
workflow-type: tm+mt
source-wordcount: 769
ht-degree: 1%

---

# Configurare il provider Infobip {#sms-configuration-infobip}

Integrando Infobip con Adobe Journey Optimizer, puoi distribuire messaggi mobili ai profili come parte dei tuoi percorsi e delle tue campagne.

Per configurare Infobip come provider SMS, segui i passaggi seguenti:

1. [Crea credenziali API](#api-credential)
1. [Creare webhook](mobile-webhook.md)
1. [Crea configurazione canale](mobile-configuration-surface.md)
1. [Creare un Percorso o una campagna con un’azione del canale SMS](create-mobile-message.md)

## Configurare le credenziali API per SMS {#api-credential}

Per configurare Infobip con Journey Optimizer, eseguire la procedura seguente:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** `>` **[!UICONTROL Canali]** e seleziona il menu **[!UICONTROL Credenziali API]**. Fare clic sul pulsante **[!UICONTROL Crea nuove credenziali API]**.

1. Configura le credenziali API SMS, come descritto di seguito:

   +++ Elenco delle credenziali SMS per la configurazione

   | Campi di configurazione | Descrizione |
   |---|---|
   | Fornitore SMS | Infobip |
   | Nome | Scegli un nome per le credenziali API. |
   | URL di base API e chiave API | Per trovare le credenziali, accedi alla home page dell’interfaccia web o alla pagina di gestione delle chiavi API. Per gli endpoint di dominio regionali o alternativi, ad esempio `api-ny2.infobip.com`, specificare l&#39;URL di base completo e verificare il token di autorizzazione con il supporto di Infobip. </br>Ulteriori informazioni nella [documentazione Infobip](https://www.infobip.com/docs/api){target="_blank"} |
   | ID entità principale | Immettere l&#39;ID entità entità principale DLT assegnato. |
   | ID modello contenuto | Immetti l&#39;ID del modello di contenuto DLT registrato. |
   | Periodo di validità | Immetti il periodo di validità del messaggio in ore. Nel caso in cui i messaggi non possano essere consegnati entro questo intervallo di tempo, il sistema effettuerà ulteriori tentativi per inviarli nuovamente. Il periodo di validità predefinito è impostato su 48 ore. |
   | Dati callback | Immetti i dati client aggiuntivi che verranno inviati sull’URL di notifica. |
   | Numero in entrata | Aggiungi il tuo numero univoco in entrata. Questo consente di utilizzare le stesse credenziali API in sandbox diverse, ciascuna con il proprio numero in entrata. |

   +++

1. Abilita l&#39;opzione **[!UICONTROL Rinuncia fuzzy]** per rilevare messaggi simili alle parole chiave di rinuncia (ad esempio, &#39;CANCIL&#39;) e personalizzare la risposta di conferma nel campo **[!UICONTROL Risposta automatica fuzzy]**.

   **[!UICONTROL La rinuncia fuzzy]** identifica i messaggi SMS che indicano che un utente desidera annullare l&#39;abbonamento, anche se il messaggio non corrisponde esattamente a una parola chiave di rinuncia definita. È in grado di rilevare frasi di rinuncia comuni e alcuni termini offensivi, garantendo il rispetto delle preferenze utente e la conformità delle campagne.

1. Seleziona **[!UICONTROL Usa set di dati personalizzato per in entrata]** per instradare gli SMS in entrata di questa credenziale a un set di dati precreato scelto dal menu a discesa. [Ulteriori informazioni sull&#39;utilizzo di un set di dati personalizzato per le parole chiave in entrata](custom-dataset-inbound-keywords.md)

   >[!NOTE]
   >
   >Lo schema del set di dati deve essere **[!UICONTROL XDM ExperienceEvent]** e includere almeno questi gruppi di campi:
   >* Adobe CJM ExperienceEvent - Dettagli sull’interazione del messaggio
   >* Adobe CJM ExperienceEvent - Dettagli sull’esecuzione dei messaggi
   >* Adobe CJM ExperienceEvent - Dettagli profilo messaggio
   >
   >Lo schema e il set di dati devono essere abilitati per il profilo.

1. Fai clic su **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

1. Nel menu **[!UICONTROL Credenziali API]**, fai clic sull&#39;icona bin per eliminare le credenziali API.

1. Per modificare le credenziali esistenti, individuare le credenziali API desiderate e fare clic sull&#39;opzione **[!UICONTROL Modifica]** per apportare le modifiche necessarie.

1. Fai clic su **[!UICONTROL Verifica connessione SMS]**, dalle credenziali API esistenti, per verificare le credenziali API SMS inviando un messaggio di esempio a un dispositivo designato.

1. Compila i campi **Numero** e **Messaggio** e fai clic su **[!UICONTROL Verifica connessione]**.

   >[!IMPORTANT]
   >
   >Il messaggio deve essere strutturato in modo da essere allineato al formato di payload del provider.

   ![](assets/verify-connection.png)

Dopo aver creato e configurato le credenziali API, ora è necessario creare una configurazione del canale per i messaggi SMS e MMS. [Ulteriori informazioni](mobile-configuration-surface.md)

## Configurare le credenziali API per RCS

La messaggistica RCS è supportata in Adobe Journey Optimizer tramite Infobip utilizzando la funzionalità [Provider SMS personalizzato](mobile-configuration-custom.md). Ciò consente la distribuzione di messaggi avanzati e interattivi tramite profili aziendali verificati, incorporando elementi quali caroselli, pulsanti e contenuti multimediali.

➡️ [Scopri come Infobip supporta RCS nella documentazione di Infobip](https://www.infobip.com/docs/api/channels/rcs)

Per abilitare la messaggistica RCS con Infobip, è necessario configurare le nuove credenziali API tramite un provider SMS personalizzato. Le credenziali SMS di Infobip esistenti non sono compatibili, in quanto RCS richiede un formato di payload distinto.

Per configurare RCS con Infobip:

1. **Registra la tua attività per RCS tramite Infobip**

   Inizia completando il processo di onboarding e registrazione RCS all’interno della piattaforma Infobip. Ciò comporta la configurazione del profilo del mittente RCS e la verifica che l’account sia abilitato per RCS. Ulteriori informazioni sono disponibili nella [documentazione di Infobip](https://www.infobip.com/docs/rcs/get-started)

1. **Creare un webhook SMS**

   [Configura un webhook SMS personalizzato](mobile-configuration-custom.md#webhook) in Journey Optimizer. Questo webhook sarà responsabile della gestione delle conferme di recapito, dei messaggi RCS in entrata e degli aggiornamenti dello stato dalla piattaforma Infobip.

1. **Crea credenziali API utilizzando Personalizzato come fornitore SMS**

   [Creare una nuova credenziale API](mobile-configuration-custom.md#api-credential) in Journey Optimizer, selezionando &quot;Personalizzato&quot; come provider SMS. Utilizza il metodo di autenticazione dell’endpoint RCS appropriato, l’URL di base e le intestazioni.

Dopo aver creato e configurato le credenziali API, devi creare [il tuo webhook](mobile-webhook.md) e una configurazione del canale per i messaggi RCS. [Ulteriori informazioni](mobile-configuration-surface.md)
