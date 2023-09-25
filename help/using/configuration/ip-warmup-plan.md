---
solution: Journey Optimizer
product: journey optimizer
title: Creare un piano di riscaldamento IP
description: Scopri come creare un piano di riscaldamento IP
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pool, gruppo, sottodomini, recapito messaggi
hide: true
hidefromtoc: true
source-git-commit: 1ec2c406e777e08de97c3ad53cee5986afeb3c44
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 5%

---

# Creare un piano di riscaldamento IP {#ip-warmup}

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione di guida:

* [Introduzione al riscaldamento dell’IP](ip-warmup-gs.md)
* [Creare campagne di riscaldamento IP](ip-warmup-campaign.md)
* **[Creare un piano di riscaldamento IP](ip-warmup-plan.md)**
* [Eseguire il piano di riscaldamento IP](ip-warmup-running.md)

>[!ENDSHADEBOX]

Una volta creati uno o più [Campagne di riscaldamento IP](ip-warmup-campaign.md) con una superficie dedicata e l’opzione corrispondente abilitata, puoi iniziare a creare il piano di riscaldamento IP.

## Compila il modello di riscaldamento IP {#upload-plan}

Prima di poter creare un piano di riscaldamento IP nell’interfaccia di Journey Optimizer, è necessario compilare un modello in formato Excel con tutti i dati che alimenteranno il piano.

>[!CAUTION]
>
>Rivolgiti al tuo consulente di recapito messaggi per assicurarti che il file del piano di riscaldamento IP sia configurato correttamente.

Di seguito è riportato un esempio di file contenente un piano di riscaldamento IP.

![](assets/ip-warmup-sample-file.png)

### Scheda Piano di riscaldamento IP

Il riscaldamento dell’IP è un’attività che consiste nell’aumentare gradualmente il volume di e-mail che escono dagli IP e dal dominio verso i principali provider di servizi Internet (ISP) al fine di stabilire la tua reputazione di mittente legittimo.

Questa attività viene tipicamente eseguita con l’aiuto di un consulente o esperto di recapito messaggi che prepara un piano ben pensato in base al dominio del settore, al caso d’uso, all’area geografica, agli ISP e a vari altri fattori.

* In questo esempio, è stato preparato un piano che si estende su 17 giorni per raggiungere un volume target di xxx profili.

* Il piano prevede 6 fasi.

* Puoi avere tutte le colonne che desideri per i domini a cui desideri recapitare. In questo esempio, il piano è diviso in quattro colonne che corrispondono ai gruppi di dominio da utilizzare nel piano: Gmail, Adobe, Yahoo e Altri.

L’idea è quella di avere più esecuzioni nelle prime fasi e di aumentare progressivamente il numero di indirizzi mirati, riducendo nel contempo il numero di esecuzioni.

L’elenco dei domini predefiniti è il seguente:

* Gmail
* Adobe
* WP
* Comcast
* Yahoo
* Bigpond
* Arancione
* Softbank
* Docomo
* United Internet
* Microsoft
* KDDI
* Italia Online
* La Poste
* Apple

### Scheda Gruppo di dominio personalizzato

Puoi anche aggiungere altre colonne con i gruppi di dominio personalizzati.

Utilizza il **[!UICONTROL Gruppo di dominio personalizzato]** per definire un nuovo dominio e per ciascun dominio puoi aggiungere tutti i sottodomini coperti.<!--TBC-->

## Accesso e gestione dei piani di riscaldamento IP {#manage-ip-warmup-plans}

1. Accedere a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Piani di riscaldamento IP]** menu. Vengono visualizzati tutti i piani di riscaldamento IP creati finora.

   ![](assets/ip-warmup-filter-list.png)

1. Puoi filtrare in base allo stato. I diversi stati sono:

   * **Non avviato**: non è stata ancora attivata alcuna esecuzione. [Ulteriori informazioni](ip-warmup-running.md#define-runs)
   * **In corso / Live**: il piano assume questo stato non appena la prima esecuzione nella prima fase è stata attivata correttamente. [Ulteriori informazioni](ip-warmup-running.md#define-runs)
   * **Completato**: il piano è stato contrassegnato come completato. Questa opzione è disponibile solo se tutte le esecuzioni del piano sono in **[!UICONTROL Completato]** o **[!UICONTROL Bozza]** stato (nessuna esecuzione può essere **[!UICONTROL Live]**). [Ulteriori informazioni](ip-warmup-running.md#define-runs#mark-as-completed)
   * **In pausa**<!--: to check (user action)-->

1. Per eliminare un piano di riscaldamento IP, selezionare **[!UICONTROL Elimina]** accanto a una voce di elenco e confermare l&#39;eliminazione.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >Il piano di riscaldamento IP selezionato verrà eliminato definitivamente.

## Creare un piano di riscaldamento IP {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="Specificare il piano di riscaldamento IP"
>abstract="Scarica il modello CSV e compilalo con i dati per le fasi di riscaldamento IP e il numero di profili target."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="Seleziona una superficie di marketing"
>abstract="Devi selezionare la stessa superficie di quella selezionata nella campagna da associare al piano di riscaldamento IP."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=it" text="Impostare le superfici di canale"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=it" text="Creare campagne di riscaldamento IP"

Quando una o più campagne live con **[!UICONTROL Attivazione del piano di riscaldamento IP]** opzione attivata, è possibile associarle a un piano di riscaldamento IP.

>[!CAUTION]
>
>Per creare, modificare ed eliminare i piani di riscaldamento IP, è necessario disporre del **[!UICONTROL Consulente per il recapito messaggi]** autorizzazione. <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->
>
>Rivolgiti al tuo consulente di recapito messaggi per assicurarti che il modello di piano di riscaldamento IP sia configurato correttamente. <!--TBC-->

1. Accedere a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Piani di riscaldamento IP]** , quindi fai clic su **[!UICONTROL Crea piano di riscaldamento IP]**.

   ![](assets/ip-warmup-create-plan.png)

1. Compila i dettagli del piano di riscaldamento IP: fornisci un nome e una descrizione.

   ![](assets/ip-warmup-plan-details.png)

1. Seleziona un [superficie](channel-surfaces.md). Solo le superfici di marketing sono disponibili per la selezione. [Ulteriori informazioni sul tipo di e-mail](../email/email-settings.md#email-type)

   >[!CAUTION]
   >
   >Devi selezionare la stessa superficie di quella selezionata nella campagna da associare al piano di riscaldamento IP. [Scopri come creare una campagna di riscaldamento IP](#create-ip-warmup-campaign)

1. Carica il file Excel contenente il tuo piano di riscaldamento IP<!--which formats are allowed?-->. Puoi utilizzare il modello fornito dal team di recapito messaggi.<!--TBC?--> [Ulteriori informazioni](#upload-plan)
   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

1. Fai clic su **[!UICONTROL Crea]**. Il numero di fasi definite nel file caricato viene visualizzato automaticamente in tutte le esecuzioni di ogni fase. [Ulteriori informazioni](#upload-plan)

   ![](assets/ip-warmup-plan-phases.png)

## Ricarica un piano di riscaldamento IP {#re-upload-plan}

Puoi ricaricare un altro piano di riscaldamento IP utilizzando il pulsante corrispondente.

![](assets/ip-warmup-re-upload-plan.png)

>[!NOTE]
>
>I dettagli del piano di riscaldamento IP cambiano in base al file appena caricato. Non influisce sulle esecuzioni complete e attivate.