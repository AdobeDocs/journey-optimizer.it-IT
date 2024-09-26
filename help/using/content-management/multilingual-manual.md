---
solution: Journey Optimizer
product: journey optimizer
title: Creare contenuto multilingue con traduzione manuale
description: Scopri come creare contenuti multilingue con traduzione manuale in Journey Optimizer
feature: Multilingual Content
topic: Content Management
role: User
level: Beginner
keywords: introduzione, inizio, contenuto, esperimento
exl-id: 6244d717-fbd6-468e-9164-60451d0d62f0
badge: label="Disponibilità limitata" type="Informative"
source-git-commit: dd4173698d7034173b7ae9f44afec397d62a6f78
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 6%

---

# Creare contenuto multilingue con traduzione manuale {#multilingual-manual}

>[!AVAILABILITY]
>
>Il contenuto multilingue è attualmente disponibile solo per alcune organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.

Utilizzando il flusso manuale, puoi tradurre facilmente il contenuto direttamente nella tua campagna e nel percorso E-mail, Notifica push o SMS, offrendoti opzioni precise di controllo e personalizzazione per i messaggi multilingue. Inoltre, puoi importare facilmente contenuti multilingue preesistenti con l’opzione Importa HTML.

Per creare contenuti multilingue mediante la traduzione manuale, segui la procedura riportata di seguito:

1. [Crea le tue impostazioni locali](#create-locale).

1. [Crea impostazioni lingua](#create-language-settings).

1. [Crea un contenuto multilingue](#create-a-multilingual-campaign).

## Creare lingua {#create-locale}

Durante la configurazione delle impostazioni della lingua, come descritto nella sezione [Creare le impostazioni della lingua](#language-settings), se non è disponibile una lingua specifica per il contenuto multilingue, è possibile creare il numero di nuove lingue necessario utilizzando il menu **[!UICONTROL Traduzione]**.

1. Dal menu **[!UICONTROL Gestione contenuto]**, accedi a **[!UICONTROL Traduzione]**.

1. Dalla scheda **[!UICONTROL Dizionario impostazioni internazionali]**, fare clic su **[!UICONTROL Aggiungi impostazioni locali]**.

   ![](assets/locale_1.png)

1. Seleziona il codice della lingua dall&#39;elenco **[!UICONTROL Lingua]** e dall&#39;area **[!UICONTROL Regione]** associata.

1. Fai clic su **[!UICONTROL Salva]** per creare le impostazioni internazionali.

   ![](assets/locale_2.png)

## Creare le impostazioni della lingua {#language-settings}

In questa sezione puoi impostare la lingua principale e le lingue associate per la gestione dei contenuti multilingue. Puoi anche scegliere l’attributo da utilizzare per cercare le informazioni relative alla lingua del profilo

1. Dal menu **[!UICONTROL Amministrazione]**, accedere a **[!UICONTROL Canale]** > **[!UICONTROL Impostazioni generali]**.

1. Nel menu **[!UICONTROL Impostazioni lingua]**, fare clic su **[!UICONTROL Crea impostazioni lingua]**.

   ![](assets/language_settings_1.png)

1. Digitare il nome delle **[!UICONTROL impostazioni lingua]**.

1. Seleziona le **[!UICONTROL impostazioni internazionali]** associate a queste impostazioni. Puoi aggiungere un massimo di 50 impostazioni internazionali.

   Se manca una **[!UICONTROL Lingua]**, puoi crearla manualmente in anticipo dal menu **[!UICONTROL Traduzione]** o tramite API. Consulta [Crea una nuova lingua](#create-locale).

   ![](assets/multilingual-settings-2.png)

1. Dal menu **[!UICONTROL Preferenza di invio]**, selezionare l&#39;attributo che si desidera cercare per trovare informazioni sulle lingue del profilo.

   ![](assets/multilingual-settings-3.png)

1. Fai clic su **[!UICONTROL Modifica]** accanto alla tua **[!UICONTROL Impostazioni locali]** per personalizzarla ulteriormente e aggiungere **[!UICONTROL Preferenze profilo]**.

   ![](assets/multilingual-settings-4.png)

1. Seleziona altre **[!UICONTROL Impostazioni internazionali]** dal menu a discesa Preferenze profilo e fai clic su **[!UICONTROL Aggiungi profili]**.

1. Accedi al menu avanzato di **[!UICONTROL Impostazioni locali]** per definire le **[!UICONTROL Impostazioni locali primarie]**, ovvero la lingua predefinita se l&#39;attributo del profilo non è specificato.

   È inoltre possibile eliminare le impostazioni locali da questo menu avanzato.

   ![](assets/multilingual-settings-5.png)

1. Fai clic su **[!UICONTROL Invia]** per creare le **[!UICONTROL impostazioni lingua]**.

<!--
1. Access the **[!UICONTROL channel configurations]** menu and create a new channel configuration or select an existing one.


1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.

1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## Creare un contenuto multilingue {#create-multilingual-campaign}

Dopo aver configurato il contenuto multilingue, puoi creare la campagna o il percorso e personalizzarne il contenuto per ciascuna delle lingue selezionate.

1. Inizia creando e configurando la tua notifica e-mail, SMS o push [campagna](../campaigns/create-campaign.md) o [percorso](../building-journeys/journeys-message.md) in base alle tue esigenze.

   >[!AVAILABILITY]
   >
   >Si consiglia di includere un solo progetto di traduzione al percorso.

1. Crea o importa il contenuto originale e personalizzalo in base alle esigenze.

1. Una volta creato il contenuto principale, fai clic su **[!UICONTROL Salva]** e torna alla schermata di configurazione della campagna.

   ![](assets/multilingual-campaign-2.png)

1. Fai clic su **[!UICONTROL Aggiungi lingue]** e seleziona le **[!UICONTROL Impostazioni lingua]** create in precedenza. [Ulteriori informazioni](#create-language-settings)

   ![](assets/multilingual-campaign-3.png)

1. Accedi alle impostazioni avanzate del menu **[!UICONTROL Impostazioni internazionali]** e seleziona **[!UICONTROL Copia primario in tutte le impostazioni internazionali]**.

   ![](assets/multilingual-campaign-4.png)

1. Ora che il contenuto principale è duplicato in tutte le **[!UICONTROL Impostazioni locali]** selezionate, accedi a ciascuna impostazione locale e fai clic su **[!UICONTROL Modifica corpo dell&#39;e-mail]** per tradurre il contenuto.

   ![](assets/multilingual-campaign-5.png)

1. Puoi scegliere di disabilitare o abilitare le impostazioni internazionali con il menu **[!UICONTROL Ulteriori azioni]** della lingua selezionata.

   ![](assets/multilingual-campaign-6.png)

1. Per disattivare la configurazione multilingue, fare clic su **[!UICONTROL Aggiungi lingue]** e selezionare la lingua da mantenere come lingua locale.

   ![](assets/multilingual-campaign-7.png)

1. Fai clic su **[!UICONTROL Rivedi per attivare]** per visualizzare un riepilogo della campagna.

   Il riepilogo ti consente di modificare la campagna, se necessario, e di verificare se un parametro è errato o mancante.

1. Sfoglia i contenuti multilingue per visualizzare il rendering in ogni lingua.

   ![](assets/multilingual-campaign-8.png)

Ora puoi attivare la campagna o il percorso. Una volta inviato, puoi misurare l’impatto del percorso multilingue o della campagna all’interno dei rapporti.

>[!IMPORTANT]
>
>A partire dalla versione di settembre, una nuova esperienza di attivazione di una campagna e di un percorso consente di gestire l’intero processo di approvazione, garantendo che le campagne e i percorsi vengano rivisti e approvati accuratamente dalle parti interessate prima della pubblicazione. Questa funzione è disponibile in Disponibilità limitata. [Ulteriori informazioni](../test-approve/gs-approval.md)

<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.

-->
