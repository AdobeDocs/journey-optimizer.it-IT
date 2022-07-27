---
title: Gestione del fuso orario
description: Informazioni sulla gestione del fuso orario
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 2%

---

# Gestione del fuso orario {#timezone_management}

È possibile definire un fuso orario nel [proprietà](../building-journeys/journey-gs.md#change-properties) del tuo percorso.

Per accedere a Proprietà Percorso, fai clic sull’icona a forma di matita in alto a destra nella schermata.

Questo fuso orario verrà utilizzato per ogni attività del percorso contenente un elemento temporale come:

* [Condizione di tempo](../building-journeys/condition-activity.md#time_condition)
* [Condizione data](../building-journeys/condition-activity.md#date_condition)
* [Attesa personalizzata](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

Puoi selezionare un fuso orario o scegliere di utilizzarlo nel profilo utente.

>[!NOTE]
>
>Il fuso orario del profilo funziona con **timeZone** campo esistente nel **Dettagli sulle preferenze** gruppo di campi.

## Definire un fuso orario fisso {#fixed-timezone}

È inoltre possibile correggere il fuso orario. Deseleziona il fuso orario predefinito e selezionane uno dall’elenco a discesa. Se utilizzi un fuso orario fisso, sarà lo stesso per tutti gli utenti che accedono al percorso.

Per farlo, nella **[!UICONTROL Journey Properties]** selezionare un fuso orario.

![](assets/journey72.png)

## Utilizzare i profili per definire il fuso orario percorso {#timezone-from-profiles}

Se l’evento di ingresso del percorso dispone di uno spazio dei nomi, ovvero se il percorso può raggiungere il servizio Profilo cliente in tempo reale di Adobe Experience Platform, puoi utilizzare il fuso orario definito a livello di profilo. Per farlo, in **Proprietà**, controlla **Usa fuso orario del profilo in attese e condizioni**. Questa opzione non è selezionata per impostazione predefinita.

Se è stato definito un fuso orario per un profilo, questo verrà recuperato e utilizzato dal percorso. In caso contrario, il fuso orario utilizzato sarà quello definito nel campo relativo al fuso orario.

![](assets/journey73.png)

## Usa fusi orari nelle espressioni {#timezone-in-expressions}

Le date di inizio e di fine di un percorso non possono essere collegate a un fuso orario specifico. Vengono automaticamente associati al fuso orario dell’istanza.
