---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione ai contenuti multilingue
description: Ulteriori informazioni sui contenuti multilingue in Journey Optimizer
feature: Multilingual
topic: Content Management
role: User
level: Beginner
keywords: introduzione, inizio, contenuto, esperimento
hide: true
hidefromtoc: true
source-git-commit: 3b1acd7ada0637ce22e360e6e1bb35921dde2315
workflow-type: tm+mt
source-wordcount: '869'
ht-degree: 7%

---

# Creare contenuti multilingue {#multilingual-automated}

La funzione multilingue consente di creare facilmente contenuti in più lingue all’interno di una singola campagna. Grazie a questa funzione, è possibile cambiare lingua durante la modifica della campagna, semplificando l’intero processo di modifica e migliorando la capacità di gestire in modo efficiente i contenuti multilingue.

## Crea lingua {#create-locale}

Durante la configurazione delle impostazioni della lingua, come descritto in [Creare le impostazioni della lingua](#language-settings) , se non è disponibile una lingua specifica per il contenuto multilingue, è possibile creare il numero di lingue desiderato utilizzando **[!UICONTROL Traduzione]** menu.

1. Dalla sezione **[!UICONTROL Amministrazione]** menu, accesso **[!UICONTROL Canale]**.

   Il menu delle traduzioni consente di accedere all’elenco delle lingue attivate.

1. Dalla sezione **[!UICONTROL Dizionario impostazioni internazionali]** , fare clic su **[!UICONTROL Aggiungi lingua]**.

   ![](assets/locale_1.png)

1. Selezionare il codice di impostazioni internazionali dall&#39; **[!UICONTROL Lingua]** e il relativo **[!UICONTROL Regione]**.

1. Clic **[!UICONTROL Salva]** per creare la lingua.

   ![](assets/locale_2.png)

## Crea progetto di traduzione {#translation-project}

1. Dalla sezione **[!UICONTROL Progetti di traduzione]** menu in **[!UICONTROL Gestione dei contenuti]**, fai clic su **[!UICONTROL Crea progetto]**.

1. Digitare a **[!UICONTROL Nome]** e **[!UICONTROL Descrizione]**.

1. Seleziona la **[!UICONTROL Lingua di origine]**.

1. Scegli se le traduzioni vengono pubblicate automaticamente dopo l’approvazione e se desideri abilitare il flusso di lavoro di revisione.

1. Clic **[!UICONTROL Aggiungi lingua]** per accedere al menu e definire le lingue per il progetto di traduzione.

   Se un **[!UICONTROL Lingua]** mancante, è possibile crearlo manualmente in anticipo dalla **[!UICONTROL Traduzione]** menu o tramite API. Fai riferimento a [Crea una nuova lingua](#create-locale).

1. Seleziona dall’elenco il tuo **[!UICONTROL Impostazioni locali di destinazione]** e scegliere quale **[!UICONTROL Provider traduzione]** si desidera utilizzare per ogni lingua.

1. Clic **[!UICONTROL Aggiungi una lingua]** una volta terminato il collegamento delle impostazioni internazionali di Target con il provider di traduzione corretto.

1. Clic **[!UICONTROL Salva]** quando il progetto di traduzione è configurato.

1. Dal menu Avanzate del progetto di traduzione, puoi scegliere di modificarlo, disattivarlo o eliminarlo.

## Creare le impostazioni della lingua {#language-settings}

In questa sezione puoi impostare la lingua principale e le lingue associate per la gestione dei contenuti multilingue. Puoi anche scegliere l’attributo da utilizzare per cercare le informazioni relative alla lingua del profilo

1. Dalla sezione **[!UICONTROL Amministrazione]** menu, accesso **[!UICONTROL Canale]**.

1. In **[!UICONTROL Impostazioni lingua]** menu, fai clic su **[!UICONTROL Creare le impostazioni della lingua]**.

1. Digita il nome della tua **[!UICONTROL Impostazioni lingua]**.

1. Scegli la **[!UICONTROL Progetto di traduzione]** opzione.

1. Dalla sezione **[!UICONTROL Progetto di traduzione]** , fare clic su **[!UICONTROL Modifica]** e scegli il creato in precedenza **[!UICONTROL Progetto di traduzione]**.

   Le impostazioni internazionali configurate in precedenza vengono importate automaticamente. Se aggiorni il tuo **[!UICONTROL Progetto di traduzione]**, fai clic su **[!UICONTROL Aggiorna]** per riflettere queste modifiche nel **[!UICONTROL Impostazioni lingua]**.

1. Dalla sezione **[!UICONTROL Preferenza di invio]** selezionare l&#39;attributo che si desidera cercare per trovare informazioni sulle lingue del profilo.

1. Clic **[!UICONTROL Modifica]** accanto al tuo **[!UICONTROL Lingua]** per personalizzarlo ulteriormente e aggiungere **[!UICONTROL Preferenze profilo]**.

1. Clic **[!UICONTROL Invia]** per creare **[!UICONTROL Impostazioni lingua]**.

<!--
1. Access the **[!UICONTROL Channel surfaces]** menu and create a new channel surface or select an existing one.

1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.

1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## Creare una campagna multilingue {#create-multilingual-campaign}

1. Inizia creando e configurando la campagna in base alle tue esigenze. [Ulteriori informazioni](../campaigns/create-campaign.md)

1. Accedi a **[!UICONTROL Azioni]** e selezionare **[!UICONTROL Modifica contenuto]**.

1. Crea o importa il contenuto originale e personalizzalo in base alle esigenze.

1. Una volta creato il contenuto principale, fai clic su **[!UICONTROL Salva]** e torna alla schermata di configurazione della campagna.

1. Clic **[!UICONTROL Aggiungi lingue]** e seleziona il creato in precedenza **[!UICONTROL Impostazioni lingua]**. [Ulteriori informazioni](#create-language-settings)

1. Accedi alle impostazioni avanzate di **[!UICONTROL Impostazioni internazionali]** menu e seleziona **[!UICONTROL Copia principale in tutte le lingue]**.

1. Ora che il contenuto principale viene duplicato in tutto il file selezionato  **[!UICONTROL Impostazioni internazionali]**, accedere alle impostazioni locali e fare clic su **[!UICONTROL Modifica corpo dell’e-mail]** per tradurre il contenuto.

1. È possibile scegliere di disabilitare o abilitare le impostazioni internazionali con **[!UICONTROL Altre azioni]** nel menu della lingua selezionata.

1. Per disattivare la configurazione multilingue, fai clic su **[!UICONTROL Aggiungi lingue]** e selezionare la lingua da mantenere come lingua locale.

1. Clic **[!UICONTROL Controlla per attivare]** per visualizzare un riepilogo della campagna.

   Il riepilogo ti consente di modificare la campagna, se necessario, e di verificare se un parametro è errato o mancante.

1. Sfoglia i contenuti multilingue per visualizzare il rendering in ogni lingua.

1. Verifica che la campagna sia configurata correttamente, quindi fai clic su **[!UICONTROL Attiva]**.

La campagna è ora attivata. Il messaggio configurato nella campagna viene inviato immediatamente o alla data specificata. Non è possibile modificare la campagna non appena è attiva. Per riutilizzare il contenuto, puoi duplicare la campagna.

Una volta inviato, puoi misurare l’impatto delle campagne all’interno dei rapporti sulle campagne.

## Rapporto campagna multilingue {#multilingual-campaign-report}

Rapporti globali, accessibili dalla **Sempre** , visualizza gli eventi che si sono verificati almeno due ore fa e copre gli eventi in un periodo di tempo selezionato. Il rapporto globale della campagna è accessibile direttamente dalla campagna con **[!UICONTROL Visualizza rapporto]** pulsante.

Per ulteriori informazioni sui dati disponibili nel rapporto della campagna, consulta [questa pagina](../reports/campaign-global-report.md).

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per i contenuti multilingue.

![](assets/report_multilingual.png)

Il **[!UICONTROL Statistiche sull’invio di e-mail per lingue]** Il widget descrive il successo della consegna in base alla **[!UICONTROL Impostazioni internazionali]**:

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante la consegna e l’elaborazione automatica dei messaggi restituiti rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante una consegna e che ne hanno impedito l’invio ai profili.

Il **[!UICONTROL Statistiche di tracciamento e-mail per lingue]** Il widget contiene i dati disponibili per l’attività del destinatario per la consegna in base al **[!UICONTROL Impostazioni internazionali]**:

* **[!UICONTROL Annulla iscrizione]**: numero di clic sul collegamento di annullamento dell’abbonamento.

* **[!UICONTROL Aperture]**: numero di volte in cui il messaggio è stato aperto.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto.
+++


<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.


-->
