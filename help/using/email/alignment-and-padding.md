---
solution: Journey Optimizer
product: journey optimizer
title: Regolare l’allineamento verticale e la spaziatura in Journey Optimizer
description: Scopri come regolare l’allineamento verticale e la spaziatura
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: allineamento verticale, editor e-mail, spaziatura
exl-id: 1e1d90ff-df5d-4432-a63a-a32d0d281d48
TQID: https://experienceleague.adobe.com/vJhROWi5ZiOLJrESMe-oUkmve1vSXrE5sNewDLpv-eE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: bc98cb2b61c7c5c8dac78b494fe293a4106a88c4
workflow-type: tm+mt
source-wordcount: 412
ht-degree: 6%

---

# Regolare l’allineamento verticale e la spaziatura {#alignment-and-padding}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come regolare l&#39;allineamento verticale e la spaziatura interna di colonne e strutture in E-mail Designer, incluso come correggere la spaziatura interna dei frammenti residui per un rendering mobile corretto.

>[!ENDSHADEBOX]

In questo esempio regoleremo la spaziatura e l’allineamento verticale all’interno di un componente struttura composto da tre colonne.

1. Seleziona il componente struttura direttamente nel messaggio e-mail o utilizzando la **[!UICONTROL Struttura di navigazione]** disponibile nel menu a sinistra.

1. Dalla barra degli strumenti, fare clic su **[!UICONTROL Selezionare una colonna]** e scegliere quella che si desidera modificare. Puoi anche selezionarla dall’albero della struttura.

   I parametri modificabili per tale colonna vengono visualizzati nella scheda **[!UICONTROL Stili]**.

   ![](assets/alignment_2.png)

1. In **[!UICONTROL Allineamento]**, selezionare **[!UICONTROL Superiore]**, **[!UICONTROL Centro]** o **[!UICONTROL Inferiore]**.

   ![](assets/alignment_3.png)

1. In **[!UICONTROL Spaziatura interna]**, definire la spaziatura per tutti i lati.

   Selezionare **[!UICONTROL Spaziatura interna diversa per ogni lato]** per ottimizzare la spaziatura. Fai clic sull’icona del lucchetto per interrompere la sincronizzazione.

   ![](assets/alignment_4.png)

1. Procedi in modo simile per regolare l’allineamento e la spaziatura delle altre colonne.

1. Salva le modifiche.

>[!TIP]
>
>Durante la progettazione di contenuti e-mail per Gmail su dispositivi Android, accertati che le immagini e i divisori utilizzino la spaziatura interna delle colonne anziché margini fissi di grandi dimensioni. In Android, spesso Gmail esegue il rendering di immagini e margini di dimensioni eccessive in modo errato, causando un overflow del layout o una riduzione delle linee di divisione. Utilizza una larghezza immagine inferiore o utilizza la spaziatura interna basata su colonne per una visualizzazione coerente.

## Gestire la spaziatura interna dei frammenti con la navigazione delle breadcrumb {#fragment-padding-breadcrumb}

Quando si lavora con [frammenti](../content-management/fragments.md) nel Designer e-mail, è possibile che la spaziatura nascosta o residua influisca sul rendering mobile in modo diverso rispetto al desktop. Ciò è particolarmente comune quando i frammenti sono stati sbloccati o quando l&#39;ereditarietà [è stata interrotta](use-visual-fragments.md#break-inheritance), in quanto lo stile rimanente può rimanere nella colonna o nei componenti di testo sottostanti.

Per identificare e modificare la spaziatura rimanente nei frammenti:

1. Utilizza la **[!UICONTROL struttura di navigazione]** o fai clic direttamente sugli elementi nell&#39;editor per selezionare ogni struttura o colonna padre all&#39;interno del frammento. Questo consente di individuare una spaziatura nascosta o un margine specifico per i dispositivi mobili.

1. Dopo aver selezionato l&#39;elemento nella breadcrumb, passa alla scheda **[!UICONTROL Stili]** a destra.

1. Rivedi le impostazioni di **[!UICONTROL Spaziatura interna]** e rimuovi o regola la spaziatura interna in base alle esigenze per ottenere il corretto allineamento per dispositivi mobili.

1. Se i problemi di allineamento persistono durante il riutilizzo dei frammenti, ripeti questo processo per altre colonne o componenti di testo all’interno del frammento.

>[!NOTE]
>
>Questo comportamento è previsto quando i frammenti vengono inseriti e rimossi ripetutamente, in quanto le regole di stile possono accumularsi. Verifica sempre i valori di spaziatura tramite la navigazione tra breadcrumb, in particolare quando esegui il targeting di dispositivi mobili.