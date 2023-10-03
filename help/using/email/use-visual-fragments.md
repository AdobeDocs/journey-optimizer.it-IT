---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare frammenti visivi
description: Scopri come utilizzare i frammenti visivi durante la creazione di e-mail nelle campagne e nei percorsi Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: dd463d36550b53faaffca90691550278498c862a
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 2%

---

# Aggiungi frammenti visivi alle e-mail {#use-visual-fragments}

È possibile utilizzare un frammento visivo in una [email](get-started-email-design.md) in un percorso, in una campagna o in un [modello di contenuto](../content-management/content-templates.md).

>[!NOTE]
>
>Scopri come creare e gestire i frammenti in [questa sezione](../content-management/fragments.md).

➡️ [Scopri come gestire, creare e utilizzare i frammenti in questo video](../content-management/fragments.md#video-fragments)

## Utilizzare un frammento {#use-fragment}

1. Apri qualsiasi contenuto e-mail o modello utilizzando [E-mail Designer](get-started-email-design.md).

1. Seleziona la **[!UICONTROL Frammenti]** dalla barra a sinistra.

   ![](assets/fragments-in-designer.png)

1. Viene visualizzato l’elenco di tutti i frammenti visivi creati nella sandbox corrente. Puoi eseguire le seguenti operazioni:

   * Cerca un frammento specifico iniziando a digitarne l’etichetta.
   * Ordina i frammenti in ordine crescente o decrescente.
   * Modifica la modalità di visualizzazione dei frammenti (scheda o elenco).

   >[!NOTE]
   >
   >I frammenti sono ordinati per data di creazione: i frammenti visivi aggiunti di recente vengono visualizzati per primi nell’elenco.

1. Puoi cercare e aggiornare l’elenco.

   >[!NOTE]
   >
   >Se alcuni frammenti sono stati modificati o aggiunti durante la modifica del contenuto, l’elenco verrà aggiornato con le modifiche più recenti.

1. Trascina un frammento dall’elenco nell’area in cui desideri inserirlo.

   ![](assets/fragment-insert.png)

1. Come qualsiasi altro componente, puoi spostare il frammento all’interno del contenuto.

1. Seleziona il frammento per visualizzare il riquadro corrispondente a destra. Da lì puoi eliminare il frammento dal contenuto o duplicarlo. Puoi anche eseguire queste azioni direttamente dal menu contestuale visualizzato sopra il frammento.

   ![](assets/fragment-right-pane.png)

1. Dalla sezione **[!UICONTROL Impostazioni]** , è possibile:

   * Scegli i dispositivi su cui vuoi visualizzare il frammento.
   * Apri il frammento in una nuova scheda per modificarlo, se necessario. [Ulteriori informazioni](../content-management/fragments.md#edit-fragments)
   * Esplora i riferimenti. [Ulteriori informazioni](../content-management/fragments.md#explore-references)

1. Puoi personalizzare ulteriormente il frammento utilizzando **[!UICONTROL Stili]** scheda.

1. Se necessario, puoi interrompere l’ereditarietà con il frammento originale. [Ulteriori informazioni](#break-inheritance)

1. Aggiungi tutti i frammenti desiderati e **[!UICONTROL Salva]** le tue modifiche.

## Interrompi ereditarietà {#break-inheritance}

Quando modifichi un frammento visivo, le modifiche vengono sincronizzate. Vengono propagati automaticamente a tutti **[!UICONTROL Bozza]** percorsi/campagne e modelli di contenuto contenenti tale frammento.

>[!NOTE]
>
>Le modifiche non vengono propagate alle e-mail utilizzate in **[!UICONTROL Live]** percorsi o campagne.

I frammenti aggiunti a un messaggio e-mail o a un modello di contenuto vengono sincronizzati per impostazione predefinita.

Tuttavia, puoi interrompere l’ereditarietà dal frammento originale. In tal caso, il contenuto del frammento viene copiato nella progettazione corrente e le modifiche non vengono più sincronizzate.

Per interrompere l’ereditarietà, effettua le seguenti operazioni:

1. Seleziona il frammento.

1. Fai clic sull’icona Sblocca nella barra degli strumenti contestuale.

   ![](assets/fragment-break-inheritance.png)

1. Il frammento diventa un elemento autonomo non più collegato al frammento originale. Modificalo come qualsiasi altro componente del contenuto. [Ulteriori informazioni](content-components.md)

