---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il provider Sinch
description: Scopri come configurare l’ambiente per l’invio di messaggi di testo con Journey Optimizer con Sinch
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: 528e1a54dd64503e5de716e63013c4fc41fd98db
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 3%

---

# Configurare il provider Sinch {#sms-configuration-sinch}

Quando utilizzi il provider Sinch con Journey Optimizer, puoi trovare due opzioni distinte:

* **Configurazione SMS**: configura le credenziali API Sinch per inviare messaggi SMS senza problemi.

* **Configurazione MMS**: per i messaggi multimediali (MMS), configura le credenziali API Sinch MMS. Tieni presente che il tracciamento e la risposta ai messaggi in entrata sono gestiti dalla configurazione SMS. La configurazione MMS è valida solo per il recapito in uscita del messaggio MMS.

## Credenziali API Sinch{#create-api}

>[!BEGINSHADEBOX]

Se non vengono fornite parole chiave di consenso o rinuncia, vengono utilizzati messaggi di consenso standard per rispettare la privacy dell’utente. L&#39;aggiunta di parole chiave personalizzate sostituisce automaticamente le impostazioni predefinite.

**Parole chiave predefinite:**

* **Consenso**: SOTTOSCRIVI, SÌ, RIPRENDI, AVVIA, CONTINUA, RIPRENDI, INIZIA
* **Rinuncia**: INTERROMPI, ESCI, ANNULLA, TERMINA, ANNULLA ISCRIZIONE, NO
* **Guida**: GUIDA

>[!ENDSHADEBOX]

Per configurare il provider Sinch per l’invio di messaggi SMS e MMS con Journey Optimizer, effettua le seguenti operazioni:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** `>` **[!UICONTROL Impostazioni SMS]** e seleziona il menu **[!UICONTROL Credenziali API]**. Fare clic sul pulsante **[!UICONTROL Crea nuove credenziali API]**.

1. Configura le credenziali API SMS, come descritto di seguito:

+++ Elenco delle credenziali SMS per la configurazione

   | Campi di configurazione | Descrizione |
   |---|---|    
   | Fornitore SMS | Sinch |
   | Nome | Scegli un nome per le credenziali API. |
   | ID servizio e token API | Accedi alla pagina API e individua le tue credenziali nella scheda SMS. Ulteriori informazioni sono disponibili nella [documentazione di Sinch](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}. |
   | Parole chiave di Opt-in | Immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il messaggio di consenso. Per più parole chiave, utilizza valori separati da virgola. |
   | Messaggio di Opt-in | Immetti la risposta personalizzata inviata automaticamente come messaggio di consenso. |
   | Parole chiave di rinuncia | Immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il messaggio di rinuncia. Per più parole chiave, utilizza valori separati da virgola. |
   | Messaggio di rinuncia | Immetti la risposta personalizzata inviata automaticamente come messaggio di rinuncia. |
   | Parole chiave della Guida | Immetti le parole chiave predefinite o personalizzate che attiveranno automaticamente il **Messaggio di aiuto**. Per più parole chiave, utilizza valori separati da virgola. |
   | Messaggio di aiuto | Immetti la risposta personalizzata inviata automaticamente come **Messaggio di aiuto**. |
   | Parole chiave per doppio consenso | Immetti le parole chiave che attivano il doppio processo di consenso. Se un profilo utente non esiste, viene creato a conferma avvenuta correttamente. Per più parole chiave, utilizza valori separati da virgola. [Ulteriori informazioni sul doppio consenso SMS](https://video.tv.adobe.com/v/3440287/?learn=on&captions=ita). |
   | Doppio messaggio di consenso | Immetti la risposta personalizzata inviata automaticamente in risposta alla conferma del doppio consenso. |
   | Numero in entrata | Aggiungi un numero in entrata univoco o un codice breve. Questo consente di utilizzare le stesse credenziali API in sandbox diverse, ciascuna con il proprio numero in entrata o codice breve. |
   | Parole chiave in entrata personalizzate | Definisci parole chiave univoche per azioni specifiche, ad esempio SCONTO, OFFERTE, ISCRIZIONE. Queste parole chiave vengono acquisite e memorizzate come attributi nel profilo, consentendoti di attivare una qualificazione del segmento di streaming all’interno del percorso e di fornire una risposta o un’azione personalizzata. |
   | Messaggio di risposta in entrata predefinito | Immetti la risposta predefinita inviata quando un utente finale invia un SMS in entrata che non corrisponde a nessuna delle parole chiave definite. |
   | Sovrascrivi URL | Immetti l’URL personalizzato per sostituire gli endpoint predefiniti per rapporti di consegna SMS, dati di feedback, messaggi in entrata o notifiche di eventi. Sinch invierà tutti gli aggiornamenti rilevanti a questo URL invece di quelli predefiniti. |

+++

1. Fai clic su **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

1. Nel menu **[!UICONTROL Credenziali API]**, fai clic sull&#39;icona bin per eliminare le credenziali API.

1. Per modificare le credenziali esistenti, individuare le credenziali API desiderate e fare clic sull&#39;opzione **[!UICONTROL Modifica]** per apportare le modifiche necessarie.

Dopo aver creato e configurato le credenziali API, ora è necessario creare una configurazione del canale per i messaggi SMS. [Ulteriori informazioni](sms-configuration-surface.md)

## Credenziali API Sinch MMS {#sinch-mms}

>[!IMPORTANT]
>
> Oltre alla configurazione di MMS, devi anche creare credenziali API Sinch specifiche per il tracciamento dei messaggi in entrata e la gestione delle richieste di consenso.

Per configurare Sinch MMS per l’invio di MMS con Journey Optimizer, effettua le seguenti operazioni:

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** `>` **[!UICONTROL Impostazioni SMS]** e seleziona il menu **[!UICONTROL Credenziali API]**. Fare clic sul pulsante **[!UICONTROL Crea nuove credenziali API]**.

1. Configura le credenziali API MMS, come descritto di seguito:

   * **[!UICONTROL Fornitore SMS]**: Sinch MMS.

   * **[!UICONTROL Nome]**: scegli un nome per le credenziali API.

   * **[!UICONTROL ID progetto]**, **[!UICONTROL ID app]** e **[!UICONTROL Token API]**: segui i passaggi seguenti per raccogliere le credenziali API MMS.

      * Per **[!UICONTROL ID progetto]** e **[!UICONTROL ID app]**: accedi alla pagina [Panoramica API di conversazione](https://dashboard.sinch.com/convapi/overview) del progetto Sinch nel tuo dashboard di Sinch.
      * Per **[!UICONTROL token API]**: ottieni le [chiavi di accesso](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638) per il tuo progetto Sinch e genera un **token API Base64** dal tuo progetto Sinch **chiavi di accesso**.

1. Fai clic su **[!UICONTROL Invia]** al termine della configurazione delle credenziali API.

1. Nel menu **[!UICONTROL Credenziali API]**, fai clic sull&#39;icona bin per eliminare le credenziali API.

1. Per modificare le credenziali esistenti, individuare le credenziali API desiderate e fare clic sull&#39;opzione **[!UICONTROL Modifica]** per apportare le modifiche necessarie.

Dopo aver creato e configurato le credenziali API, ora è necessario creare una configurazione del canale per i messaggi MMS. [Ulteriori informazioni](sms-configuration-surface.md)
