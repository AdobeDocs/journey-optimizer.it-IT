---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il provider Infobip
description: Scopri come configurare l’ambiente per l’invio di messaggi di testo e MMS con Journey Optimizer con Infobip
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 7b6dc89a-1a81-49c2-b2a7-bf24b9d215e3
source-git-commit: bd925e1fd053a19e2102536049278e48b0784960
workflow-type: tm+mt
source-wordcount: '902'
ht-degree: 2%

---

# Configurare il provider Infobip {#sms-configuration-infobip}

>[!BEGINSHADEBOX]

Se non vengono fornite parole chiave di consenso o rinuncia, vengono utilizzati messaggi di consenso standard per rispettare la privacy dell’utente. L&#39;aggiunta di parole chiave personalizzate sostituisce automaticamente le impostazioni predefinite.

**Parole chiave predefinite:**

* **Consenso**: SOTTOSCRIVI, SÌ, RIPRENDI, AVVIA, CONTINUA, RIPRENDI, INIZIA
* **Rinuncia**: INTERROMPI, ESCI, ANNULLA, TERMINA, ANNULLA ISCRIZIONE, NO
* **Guida**: GUIDA

>[!ENDSHADEBOX]

## Configurare le credenziali API per SMS

Per configurare Infobip con Journey Optimizer, eseguire la procedura seguente:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** `>` **[!UICONTROL Canali]** e seleziona il menu **[!UICONTROL Credenziali API]**. Fare clic sul pulsante **[!UICONTROL Crea nuove credenziali API]**.

1. Configura le credenziali API SMS, come descritto di seguito:

   +++ Elenco delle credenziali SMS per la configurazione

   | Campi di configurazione | Descrizione |
   |---|---|    
   | Fornitore SMS | Infobip |
   | Nome | Scegli un nome per le credenziali API. |
   | URL di base API e chiave API | Per trovare le credenziali, accedi alla home page dell’interfaccia web o alla pagina di gestione delle chiavi API. Per gli endpoint di dominio regionali o alternativi, ad esempio `api-ny2.infobip.com`, specificare l&#39;URL di base completo e verificare il token di autorizzazione con il supporto di Infobip. </br>Ulteriori informazioni nella [documentazione Infobip](https://www.infobip.com/docs/api){target="_blank"} |
   | Parole chiave di Opt-in | Immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il messaggio di consenso. Per più parole chiave, utilizza valori separati da virgola. |
   | Messaggio di Opt-in | Immetti la risposta personalizzata inviata automaticamente come messaggio di consenso. |
   | Parole chiave di rinuncia | Immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il messaggio di rinuncia. Per più parole chiave, utilizza valori separati da virgola. |
   | Messaggio di rinuncia | Immetti la risposta personalizzata inviata automaticamente come messaggio di rinuncia. |
   | Parole chiave della Guida | Immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il **Messaggio di aiuto**. Per più parole chiave, utilizza valori separati da virgola. |
   | Messaggio di aiuto | Immetti la risposta personalizzata inviata automaticamente come **Messaggio di aiuto**. |
   | Parole chiave per doppio consenso | Immetti le parole chiave che attivano il doppio processo di consenso. Se un profilo utente non esiste, viene creato a conferma avvenuta correttamente. Per più parole chiave, utilizza valori separati da virgola. [Ulteriori informazioni sul doppio consenso SMS](https://video.tv.adobe.com/v/3440287/?captions=ita&learn=on). |
   | Doppio messaggio di consenso | Immetti la risposta personalizzata inviata automaticamente in risposta alla conferma del doppio consenso. |
   | ID entità principale | Immettere l&#39;ID entità entità principale DLT assegnato. |
   | ID modello contenuto | Immetti l&#39;ID del modello di contenuto DLT registrato. |
   | Periodo di validità | Immetti il periodo di validità del messaggio in ore. Nel caso in cui i messaggi non possano essere consegnati entro questo intervallo di tempo, il sistema effettuerà ulteriori tentativi per inviarli nuovamente. Il periodo di validità predefinito è impostato su 48 ore. |
   | Dati callback | Immetti i dati client aggiuntivi che verranno inviati sull’URL di notifica. |
   | Numero in entrata | Aggiungi il tuo numero univoco in entrata. Questo consente di utilizzare le stesse credenziali API in sandbox diverse, ciascuna con il proprio numero in entrata. |
   | Parole chiave in entrata personalizzate | Definisci parole chiave univoche non correlate al consenso per azioni basate su batch, ad esempio SCONTO, OFFERTE, ISCRIZIONE. Queste parole chiave vengono acquisite e memorizzate come attributi nel profilo, consentendoti di attivare la qualifica di un segmento in batch all’interno del percorso e di fornire una risposta o un’azione personalizzata. |
   | Messaggio di risposta in entrata predefinito | Immetti la risposta predefinita inviata quando un utente finale invia un SMS in entrata che non corrisponde a nessuna delle parole chiave definite. |

   +++

1. Abilita l&#39;opzione **[!UICONTROL Rinuncia fuzzy]** per rilevare messaggi simili alle parole chiave di rinuncia (ad esempio, &#39;CANCIL&#39;) e personalizzare la risposta di conferma nel campo **[!UICONTROL Risposta automatica fuzzy]**.

   **[!UICONTROL La rinuncia fuzzy]** identifica i messaggi SMS che indicano che un utente desidera annullare l&#39;abbonamento, anche se il messaggio non corrisponde esattamente a una parola chiave di rinuncia definita. È in grado di rilevare frasi di rinuncia comuni e alcuni termini offensivi, garantendo il rispetto delle preferenze utente e la conformità delle campagne.

1. Fai clic su **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

1. Nel menu **[!UICONTROL Credenziali API]**, fai clic sull&#39;icona bin per eliminare le credenziali API.

1. Per modificare le credenziali esistenti, individuare le credenziali API desiderate e fare clic sull&#39;opzione **[!UICONTROL Modifica]** per apportare le modifiche necessarie.

1. Fai clic su **[!UICONTROL Verifica connessione SMS]**, dalle credenziali API esistenti, per verificare le credenziali API SMS inviando un messaggio di esempio a un dispositivo designato.

1. Compila i campi **Numero** e **Messaggio** e fai clic su **[!UICONTROL Verifica connessione]**.

   >[!IMPORTANT]
   >
   >Il messaggio deve essere strutturato in modo da essere allineato al formato di payload del provider.

   ![](assets/verify-connection.png)

Dopo aver creato e configurato le credenziali API, ora è necessario creare una configurazione del canale per i messaggi SMS e MMS. [Ulteriori informazioni](sms-configuration-surface.md)

## Configurare le credenziali API per RCS

La messaggistica RCS è supportata in Adobe Journey Optimizer tramite Infobip utilizzando la funzionalità [Provider SMS personalizzato](sms-configuration-custom.md). Ciò consente la distribuzione di messaggi avanzati e interattivi tramite profili aziendali verificati, incorporando elementi quali caroselli, pulsanti e contenuti multimediali.

➡️ [Scopri come Infobip supporta RCS nella documentazione di Infobip](https://www.infobip.com/docs/api/channels/rcs)

Per abilitare la messaggistica RCS con Infobip, è necessario configurare le nuove credenziali API tramite un provider SMS personalizzato. Le credenziali SMS di Infobip esistenti non sono compatibili, in quanto RCS richiede un formato di payload distinto.

Per configurare RCS con Infobip:

1. **Registra la tua attività per RCS tramite Infobip**

   Inizia completando il processo di onboarding e registrazione RCS all’interno della piattaforma Infobip. Ciò comporta la configurazione del profilo del mittente RCS e la verifica che l’account sia abilitato per RCS. Ulteriori informazioni sono disponibili nella [documentazione di Infobip](https://www.infobip.com/docs/rcs/get-started)

1. **Creare un webhook SMS**

   [Configura un webhook SMS personalizzato](sms-configuration-custom.md#webhook) in Journey Optimizer. Questo webhook sarà responsabile della gestione delle conferme di recapito, dei messaggi RCS in entrata e degli aggiornamenti dello stato dalla piattaforma Infobip.

1. **Crea credenziali API utilizzando Personalizzato come fornitore SMS**

   [Creare una nuova credenziale API](sms-configuration-custom.md#api-credential) in Journey Optimizer, selezionando &quot;Personalizzato&quot; come provider SMS. Utilizza il metodo di autenticazione dell’endpoint RCS appropriato, l’URL di base e le intestazioni.

Dopo aver creato e configurato le credenziali API, ora è necessario creare una configurazione del canale per i messaggi RCS. [Ulteriori informazioni](sms-configuration-surface.md)
