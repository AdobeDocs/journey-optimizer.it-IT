---
solution: Journey Optimizer
product: journey optimizer
title: Creare contenuto multilingue con traduzione automatica
description: Ulteriori informazioni sul contenuto multilingue in Journey Optimizer
feature: Multilingual Content
topic: Content Management
role: User
level: Beginner
keywords: introduzione, inizio, contenuto, esperimento
exl-id: 38e82eb2-67d9-4a7d-8c1f-77dab20bcec4
badge: label="Disponibilità limitata" type="Informative"
source-git-commit: 59dee15d2952438a074db57a94b3d896b38cd4f3
workflow-type: tm+mt
source-wordcount: '1331'
ht-degree: 4%

---

# Creare contenuto multilingue con traduzione automatica {#multilingual-automated}

>[!AVAILABILITY]
>
>Il contenuto multilingue è attualmente disponibile solo per alcune organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.

Utilizzando il flusso automatizzato, è sufficiente selezionare la lingua di destinazione e il provider della lingua. Il contenuto viene quindi inviato direttamente alla traduzione, pronto per una revisione finale al completamento.

Per creare contenuti multilingue mediante la traduzione automatica, segui la procedura riportata di seguito:

1. [Crea le tue impostazioni locali](#create-locale).

1. [Crea un progetto lingua](#create-translation-project).

1. [Crea impostazioni lingua](#create-language-settings).

1. [Crea un contenuto multilingue](#create-a-multilingual-campaign).

1. [Rivedi l&#39;attività di traduzione (facoltativo)](#review-translation-project).

## Crea lingua {#create-locale}

Durante la configurazione delle impostazioni della lingua, come descritto nella sezione [Creare le impostazioni della lingua](#language-settings), se non è disponibile una lingua specifica per il contenuto multilingue, è possibile creare il numero di nuove lingue necessario utilizzando il menu **[!UICONTROL Traduzione]**.

1. Dal menu **[!UICONTROL Gestione contenuto]**, accedi a **[!UICONTROL Traduzione]**.

1. Dalla scheda **[!UICONTROL Dizionario impostazioni internazionali]**, fare clic su **[!UICONTROL Aggiungi impostazioni locali]**.

   ![](assets/locale_1.png)

1. Seleziona il codice della lingua dall&#39;elenco **[!UICONTROL Lingua]** e dall&#39;area **[!UICONTROL Regione]** associata.

1. Fai clic su **[!UICONTROL Salva]** per creare le impostazioni internazionali.

   ![](assets/locale_2.png)

## Crea progetto di traduzione {#translation-project}

Avvia il progetto di traduzione specificando la lingua di Target, che indica la lingua o l’area geografica specifica per il contenuto. Puoi quindi scegliere il provider di traduzione.

1. Dal menu **[!UICONTROL Traduzione]** in **[!UICONTROL Gestione contenuto]**, fare clic su **[!UICONTROL Crea progetto]** nella scheda **[!UICONTROL Progetti]**.

   ![](assets/translation_project_1.png)

1. Digitare un **[!UICONTROL Nome]** e una **[!UICONTROL Descrizione]**.

1. Selezionare le **[!UICONTROL impostazioni locali di Source]**.

   ![](assets/translation_project_2.png)

1. Scegli se desideri abilitare le seguenti opzioni:

   * **[!UICONTROL Pubblica automaticamente le traduzioni approvate]**: una volta approvate, le traduzioni vengono automaticamente integrate nella campagna senza la necessità di un intervento manuale.
   * **[!UICONTROL Abilita flusso di lavoro di revisione]**: applicabile solo alle lingue tradotte dall&#39;utente. Questo consente a un revisore interno di valutare e approvare o rifiutare in modo efficiente i contenuti tradotti. [Ulteriori informazioni](#review-translation-project)

1. Fai clic su **[!UICONTROL Aggiungi impostazioni locali]** per accedere al menu e definire le lingue per il progetto di traduzione.

   Se manca una **[!UICONTROL Lingua]**, puoi crearla manualmente in anticipo dal menu **[!UICONTROL Traduzione]** o tramite API. Consulta [Crea una nuova lingua](#create-locale).

   ![](assets/translation_project_3.png)

1. Seleziona dall&#39;elenco le tue **[!UICONTROL impostazioni locali di destinazione]** e scegli quale **[!UICONTROL provider di traduzione]** desideri utilizzare per ciascuna impostazione locale.

   È possibile accedere alle impostazioni del **[!UICONTROL provider di traduzione]** dal menu **[!UICONTROL Traduzione]** nella sezione del menu **[!UICONTROL Amministrazione]**.

   >[!NOTE]
   >
   >La gestione dei contratti con il fornitore di traduzione esula dall’ambito di questa funzione. Assicurati di disporre di un contratto valido e attivo con il partner di traduzione designato.
   >
   ></br>Il fornitore di traduzione è responsabile della qualità del contenuto tradotto.

1. Fare clic su **[!UICONTROL Aggiungi una lingua]** al termine del collegamento delle impostazioni locali di destinazione con il provider di traduzione corretto. Quindi fare clic su **[!UICONTROL Salva]**.

   Si noti che se un provider è disattivato per una lingua di destinazione, indica che il provider non supporta tale lingua specifica.

   ![](assets/translation_project_4.png)

1. Fai clic su **[!UICONTROL Salva]** quando il progetto di traduzione è configurato.

Il progetto di traduzione viene ora creato e può essere utilizzato in una campagna multilingue.

## Creare le impostazioni della lingua {#language-settings}

In questa sezione puoi impostare la lingua principale e le lingue associate per la gestione dei contenuti multilingue. Puoi anche scegliere l’attributo da utilizzare per cercare le informazioni relative alla lingua del profilo.

1. Dal menu **[!UICONTROL Amministrazione]**, accedi a **[!UICONTROL Canale]**.

1. Nel menu **[!UICONTROL Impostazioni lingua]**, fare clic su **[!UICONTROL Crea impostazioni lingua]**.

   ![](assets/language_settings_1.png)

1. Digitare il nome delle **[!UICONTROL impostazioni lingua]**.

1. Scegli l&#39;opzione **[!UICONTROL Progetto di traduzione]**.

1. Dal campo **[!UICONTROL Progetto di traduzione]**, fai clic su **[!UICONTROL Modifica]** e scegli il **[!UICONTROL Progetto di traduzione]** creato in precedenza.

   Le impostazioni internazionali configurate in precedenza vengono importate automaticamente.

   ![](assets/language_settings_2.png)

1. Dal menu **[!UICONTROL Preferenza di invio]**, selezionare l&#39;attributo che si desidera cercare per trovare informazioni sulle lingue del profilo.

1. Fai clic su **[!UICONTROL Modifica]** accanto alla tua **[!UICONTROL Impostazioni locali]** per personalizzarla ulteriormente e aggiungere **[!UICONTROL Preferenze profilo]**.

   ![](assets/language_settings_3.png)

1. Se il **[!UICONTROL progetto di traduzione]** è aggiornato, fai clic su **[!UICONTROL Aggiorna]** per riflettere le modifiche nelle **[!UICONTROL impostazioni lingua]**.

   ![](assets/language_settings_4.png)

1. Fai clic su **[!UICONTROL Invia]** per creare le **[!UICONTROL impostazioni lingua]**.

<!--
1. Access the **[!UICONTROL Channel surfaces]** menu and create a new channel surface or select an existing one.

1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.


1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## Creare un contenuto multilingue {#create-multilingual-campaign}

Dopo aver configurato il progetto di traduzione e le impostazioni della lingua, puoi creare la campagna o il percorso e personalizzare il contenuto per le diverse lingue.

1. Inizia creando e configurando la tua notifica e-mail, SMS o push [campagna](../campaigns/create-campaign.md) o [percorso](../building-journeys/journeys-message.md) in base alle tue esigenze.

1. Una volta creato il contenuto principale, fai clic su **[!UICONTROL Salva]** e torna alla schermata di configurazione della campagna.

1. Fare clic su **[!UICONTROL Aggiungi lingue]**.  [Ulteriori informazioni](#create-language-settings)

   ![](assets/multilingual-campaign-automated-1.png)

1. Seleziona le **[!UICONTROL Impostazioni lingua]** create in precedenza.

   ![](assets/multilingual-campaign-automated-2.png)

1. Dopo aver importato le impostazioni internazionali, fai clic su **[!UICONTROL Invia per tradurre]** per inoltrare il contenuto al provider di traduzione selezionato in precedenza.

   ![](assets/multilingual-campaign-automated-3.png)

1. Una volta inviato per la traduzione, il contenuto non è più modificabile. Per apportare modifiche al contenuto originale, fai clic sull’icona del lucchetto.

   Tieni presente che se desideri apportare modifiche a questo contenuto, dovrai creare un nuovo progetto di traduzione e inviarlo di nuovo per la traduzione.

   ![](assets/multilingual-campaign-automated-4.png)

1. Fai clic su **[!UICONTROL Apri traduzione]** per accedere al progetto di traduzione e rivederlo.

   ![](assets/multilingual-campaign-automated-5.png)

1. In questa pagina, segui lo stato del progetto di traduzione:

   * **[!UICONTROL Traduzione in corso]**: il provider di servizi sta lavorando attivamente alla traduzione.

     Se hai selezionato **Traduzione interna** durante la configurazione delle **Impostazioni lingua**, puoi tradurre il contenuto direttamente nel progetto di traduzione. [Ulteriori informazioni](#manage-ht-project)

   * **[!UICONTROL Pronto per la revisione]**: il processo di revisione è pronto per iniziare, consentendo di accedere alla traduzione e di rifiutarla o approvarla.

     Se hai selezionato **[!UICONTROL Abilita flusso di lavoro di revisione]** nel **[!UICONTROL progetto di traduzione]**, puoi rivedere la traduzione direttamente in Journey Optimizer dopo il completamento da parte del provider di traduzione selezionato. [Ulteriori informazioni](#review-translation-project)

   * **[!UICONTROL Rivisto]**: la traduzione è stata approvata e pronta per essere pubblicata e inviata alla campagna.

   * **[!UICONTROL Pronto per la pubblicazione]**: la traduzione automatica è stata completata e ora può essere inviata alla tua campagna.

   * **[!UICONTROL Completato]**: la traduzione è ora disponibile nella tua campagna.

   ![](assets/multilingual-campaign-automated-6.png)

1. Una volta completata la traduzione, il contenuto multilingue è pronto per essere inviato.

   ![](assets/translation_review_9.png)

1. Fai clic su **[!UICONTROL Rivedi per attivare]** per visualizzare un riepilogo della campagna.

   Il riepilogo ti consente di modificare la campagna, se necessario, e di verificare se un parametro è errato o mancante.

1. Sfoglia i contenuti multilingue per visualizzare il rendering in ogni lingua.

   ![](assets/multilingual-campaign-automated-7.png)

1. Verifica che la tua campagna sia configurata correttamente, quindi fai clic su **[!UICONTROL Attiva]**.

Ora puoi attivare la campagna o il percorso. Una volta inviato, puoi misurare l’impatto del percorso multilingue o della campagna all’interno dei rapporti.

## Gestisci progetto di traduzione interna {#manage-ht-project}

Se hai selezionato la traduzione interna durante la configurazione delle impostazioni di lingua, puoi tradurre il contenuto direttamente nel progetto di traduzione.

1. Dal **[!UICONTROL progetto di traduzione]**, accedi al menu **[!UICONTROL Altre azioni]** e seleziona **[!UICONTROL Traduzione interna]**.

   ![](assets/inhouse-translation-1.png)

1. Puoi esportare il file CSV per la traduzione utilizzando un software di traduzione esterno. In alternativa, puoi importare nuovamente il file CSV nel progetto di traduzione facendo clic sul pulsante **[!UICONTROL Importa CSV]**.

   ![](assets/inhouse-translation-3.png)

1. Fai clic su **[!UICONTROL Modifica]** per aggiungere il contenuto della traduzione.

   ![](assets/inhouse-translation-2.png)

1. Se si è pronti a pubblicare il testo tradotto, fare clic su **[!UICONTROL Finalizza]**.

## Rivedi il progetto di traduzione {#review-translation-project}

Se hai selezionato **[!UICONTROL Abilita flusso di lavoro di revisione]** nel **[!UICONTROL progetto di traduzione]**, puoi rivedere la traduzione direttamente in Journey Optimizer dopo il completamento da parte del provider di traduzione selezionato.

Se questa opzione è disabilitata, al termine della traduzione da parte del provider, lo stato dell&#39;attività di traduzione viene impostato automaticamente su **[!UICONTROL Rivisto]**, consentendo di procedere rapidamente facendo clic su **[!UICONTROL Publish]**.

1. Una volta completata la traduzione dal provider di servizi, puoi accedere alla traduzione per la revisione dal **[!UICONTROL progetto di traduzione]** o direttamente dalla **[!UICONTROL Campaign]**.

   Dal menu **[!UICONTROL Altre azioni]**, fai clic su **[!UICONTROL Rivedi]**.

   ![](assets/translation_review_1.png)

1. Dalla finestra Revisione, sfoglia il contenuto tradotto e accetta o rifiuta ogni stringa di traduzione.

   ![](assets/translation_review_3.png)

1. Fai clic su **[!UICONTROL Modifica]** per modificare il contenuto della stringa di traduzione.

   ![](assets/translation_review_2.png)

1. Immetti la traduzione aggiornata e fai clic su **[!UICONTROL Conferma]** al termine.

   ![](assets/translation_review_4.png)

1. Puoi anche scegliere di **[!UICONTROL Rifiutare tutti]** o **[!UICONTROL Approvare tutti]** direttamente.

   Quando selezioni **[!UICONTROL Rifiuta tutto]**, aggiungi un commento e fai clic su **[!UICONTROL Rifiuta]**.

1. Fai clic su **[!UICONTROL Anteprima]** per verificare il rendering del contenuto tradotto in ogni lingua.

1. Se si è pronti a pubblicare il testo tradotto, fare clic su **[!UICONTROL Finalizza]**.

   ![](assets/translation_review_5.png)

1. Dal **[!UICONTROL progetto di traduzione]**, seleziona uno dei tuoi progetti per accedere a ulteriori dettagli. Se hai rifiutato la traduzione, puoi scegliere di inviarla nuovamente alla traduzione.

   ![](assets/translation_review_6.png)

1. Una volta impostato lo stato di **[!UICONTROL Progetto di traduzione]** su Rivisto, puoi inviarlo alla tua campagna.

   Dal menu **[!UICONTROL Altre azioni]**, fare clic su **[!UICONTROL Publish]**.

   ![](assets/translation_review_7.png)

1. Nella campagna, verifica che lo stato della traduzione sia cambiato in **[!UICONTROL Traduzione completata]**. Ora puoi inviare contenuti multilingue, fai riferimento al passaggio 10 in [questa sezione](#create-multilingual-campaign).

   ![](assets/translation_review_9.png)

<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.


-->
