---
solution: Journey Optimizer
product: journey optimizer
title: Copiare un percorso in un’altra sandbox
description: Scopri come copiare un percorso in un’altra sandbox
feature: Journeys, Sandboxes
topic: Content Management
role: User, Developer, Data Engineer
level: Experienced
keywords: sandbox, percorso, copia, ambiente
exl-id: 8c63f2f2-5cec-4cb2-b3bf-2387eefb5002
source-git-commit: b7c31db7a126eb134c353e26c9e263a9bd1674a6
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 9%

---

# Copiare un percorso in un’altra sandbox {#copy-to-sandbox}

<!--
>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="Copy a journey to another sandbox"
>abstract="Journey Optimizer allows you to copy an entire journey from one sandbox to another. For example, you can copy a journey from the Stage sandbox environment to your Production sandbox. In addition to the Journey itself, Journey Optimizer also copies most of the objects the journey depends on."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="Sandbox details"
>abstract="Select the destination sandbox you want to copy the journey to. Only sandboxes within your organization are available."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="Object details"
>abstract="This is the journey you are going to copy."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="Dependent objects"
>abstract="This is the list of associated objects used in the journey. This list displays the name, the object type, as well as the internal Journey Optimizer ID."
-->

Gli strumenti sandbox consentono di copiare oggetti in più sandbox sfruttando le funzioni di esportazione e importazione dei pacchetti. Un pacchetto può essere costituito da uno o più oggetti. Tutti gli oggetti inclusi in un pacchetto devono appartenere alla stessa sandbox.

Questa pagina descrive il caso di utilizzo degli strumenti Sandbox nel contesto di Journey Optimizer. Per ulteriori informazioni sulla funzione stessa, consulta la [documentazione dell&#39;Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html).

>[!NOTE]
>
>Questa funzione richiede le seguenti autorizzazioni dalla funzionalità **Amministrazione sandbox**: Gestisci sandbox (o Visualizza sandbox) e Gestisci pacchetti. [Ulteriori informazioni](../administration/ootb-permissions.md)

## Introduzione agli strumenti sandbox{#sandbox-gs}

Journey Optimizer consente di copiare un intero percorso da una sandbox all’altra. Ad esempio, puoi copiare un percorso dall’ambiente sandbox di Stage alla sandbox di produzione. Oltre al percorso stesso, Journey Optimizer copia anche la maggior parte degli oggetti da cui dipende il percorso: tipi di pubblico, schemi, eventi e azioni. Per ulteriori dettagli sugli oggetti copiati, consulta questa [sezione](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html#abobe-journey-optimizer-objects).

>[!CAUTION]
>
>Non è garantito che tutti gli elementi collegati vengano copiati nella sandbox di destinazione. È consigliabile eseguire un controllo approfondito prima di pubblicare il percorso. In questo modo è possibile identificare eventuali oggetti mancanti.

Gli oggetti copiati nella sandbox di destinazione sono univoci e non esiste alcun rischio di sovrascrittura degli elementi esistenti. Sia il percorso che i messaggi all&#39;interno del percorso vengono trasferiti in modalità bozza. Ciò ti consente di eseguire una convalida completa prima della pubblicazione sulla sandbox di destinazione. Il processo di copia viene copiato solo sui metadati relativi al percorso e agli oggetti di tale Percorso. Non vengono copiati dati di profilo o set di dati come parte di questo processo.

Il processo di copia viene eseguito tramite un’esportazione e un’importazione di pacchetti tra le sandbox di origine e di destinazione. Di seguito sono riportati i passaggi generali per copiare un percorso da una sandbox a un’altra:

1. Aggiungi il percorso come pacchetto nella sandbox di origine.
1. Esporta il pacchetto nella sandbox di destinazione.

Inoltre, puoi sfruttare l&#39;API REST del servizio Copia oggetti di Journey Optimizer **1} per gestire gli oggetti delle sandbox.** [Scopri come utilizzare il servizio Copia oggetti REST API](https://developer.adobe.com/journey-optimizer-apis/references/sandbox/)

## Aggiungere il percorso come pacchetto{#export}

Per copiare un percorso in un’altra sandbox, devi innanzitutto aggiungere il percorso come pacchetto nella sandbox sorgente. Segui questi passaggi:

1. Nella sezione del menu GESTIONE PERCORSO fare clic su **[!UICONTROL Percorsi]**. Viene visualizzato l’elenco dei percorsi.

1. Cerca il percorso da copiare, fai clic sull&#39;icona **Altre azioni** (i tre punti accanto al nome del percorso) e fai clic su **Aggiungi al pacchetto**.

   ![](assets/journey-sandbox1.png)

   Viene visualizzata la finestra **Aggiungi al pacchetto**.

   ![](assets/journey-sandbox2.png)

1. Scegliere se si desidera aggiungere il percorso a un pacchetto esistente o crearne uno nuovo:

   * **Pacchetto esistente**: selezionare il pacchetto dal menu a discesa.
   * **Creare un nuovo pacchetto**: digitare il nome del pacchetto. Puoi anche aggiungere una descrizione.

1. Nella sezione del menu AMMINISTRAZIONE fare clic su **[!UICONTROL Sandbox]**, selezionare la scheda **Pacchetti** e fare clic sul pacchetto che si desidera esportare.

   ![](assets/journey-sandbox3.png)

1. Selezionare gli oggetti da esportare e fare clic su **Publish**

   ![](assets/journey-sandbox4.png)

   Se la pubblicazione non è riuscita, puoi controllare i registri per identificare il motivo dell’errore. Apri il pacchetto, fai clic su **Visualizza processi non riusciti**, seleziona il processo di importazione e fai clic su **Visualizza dettagli importazione**.

   ![](assets/journey-sandbox9.png)

## Esportare il pacchetto nella sandbox di destinazione {#import}

Una volta pubblicato il pacchetto, devi esportarlo nella sandbox di destinazione.

1. Nella sandbox di origine, fai clic sul menu **[!UICONTROL Sandbox]**, seleziona la scheda **Pacchetti** e fai clic sull&#39;icona + accanto al pacchetto da esportare.

   ![](assets/journey-sandbox5.png)

1. Seleziona la **sandbox di destinazione** dal campo a discesa e fai clic su **Avanti**. Sono disponibili solo le sandbox all’interno dell’organizzazione.

   ![](assets/journey-sandbox6.png)

1. Esaminare gli oggetti pacchetto e le dipendenze. Questo è l’elenco degli oggetti associati utilizzati nel percorso. In questo elenco vengono visualizzati il nome e il tipo di oggetto. Per ogni oggetto, puoi scegliere di crearne uno nuovo o utilizzarne uno esistente nella sandbox di destinazione.

   ![](assets/journey-sandbox7.png)

1. Fai clic sul pulsante **Fine** nell&#39;angolo in alto a destra per iniziare a copiare il pacchetto nella sandbox di destinazione. Il processo di copia varia in base alla complessità del percorso e al numero di oggetti da copiare.

1. Fare clic sul processo di importazione per esaminare il risultato della copia:

   * Fare clic su **Visualizza oggetti importati** per visualizzare ogni singolo oggetto copiato.
   * Fare clic su **Visualizza dettagli importazione** per verificare i risultati dell&#39;importazione per ogni oggetto.

   ![](assets/journey-sandbox8.png)

1. Accedi alla sandbox di destinazione ed esegui un controllo completo di tutti gli oggetti copiati.
