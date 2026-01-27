---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare filtri preimpostati
description: Scopri come salvare, applicare e gestire filtri predefiniti nelle campagne orchestrate
version: Campaign Orchestration
source-git-commit: e486aae3a6635d8eec0c398bfe03b6a63a007ef1
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 11%

---


# Utilizzare filtri preimpostati {#predefined-filters}

I filtri predefiniti sono regole salvate che puoi riutilizzare nel generatore di regole. Utilizzale per evitare di ricostruire le query comuni e per standardizzare la logica di targeting tra campagne orchestrate.

Puoi contrassegnare i filtri predefiniti come preferiti, condividerli con altri utenti e aggiungere parametri in modo che i campi selezionati possano essere modificati quando viene applicato il filtro.

## Creare un filtro preimpostato {#create}

Salva un filtro personalizzato dal generatore di regole per renderlo disponibile per un utilizzo futuro. Segui questi passaggi:

1. Apri il generatore di regole e definisci le condizioni del filtro. [Scopri come creare una regola](../orchestrated/build-query.md)

1. Facoltativo: per rendere modificabili alcuni campi quando si utilizza il filtro, selezionare il campo e attivare **[!UICONTROL Imposta come parametro]**. Quando applichi il filtro, è possibile modificare solo questi campi.

   ![](assets/predefined-filter-parameter-enable.png)

1. Per salvare il filtro, fare clic su **[!UICONTROL Seleziona o salva il filtro]** e selezionare **[!UICONTROL Salva come filtro]**.

   ![](assets/predefined-filter-save.png)

1. Immetti un&#39;etichetta e una descrizione per il filtro, quindi fai clic su **[!UICONTROL Salva]**.

   * Per salvare il filtro come preferito, attiva l’opzione **[!UICONTROL Filtro preferito]**. Ulteriori informazioni in [questa sezione](#fav-filter).
   * Per rendere il filtro accessibile ad altri utenti, abilitare l&#39;opzione **[!UICONTROL Filtro condiviso]**. Ulteriori informazioni in [questa sezione](#share-filter).

   ![](assets/predefined-filter-save-name.png)

Il filtro personalizzato è ora disponibile nell&#39;elenco **Filtri predefiniti**.

## Utilizzare un filtro predefinito in una regola {#apply}

I filtri predefiniti sono disponibili quando si definiscono le query nel generatore di regole.

1. Nel riquadro **[!UICONTROL Proprietà regola]** fare clic su **[!UICONTROL Seleziona o salva filtro]**.

1. Scegliere **[!UICONTROL Seleziona filtro predefinito]** e selezionare un filtro. Puoi anche selezionare direttamente un filtro predefinito dall’elenco, se è stato aggiunto ai preferiti.

   ![](assets/predefined-filter-apply.png)

   >[!IMPORTANT]
   >
   >Quando si seleziona un filtro predefinito, la regola creata nell’area di lavoro viene sostituita con il filtro selezionato.

1. Il filtro si apre nell’area di lavoro. Continua a modificare la condizione in base alle esigenze.

   ![](assets/predefined-filter-added.png)

   Se il filtro selezionato include parametri, è possibile modificare solo i campi contrassegnati come parametri. Vengono visualizzati nel riquadro accanto al riquadro **[!UICONTROL Proprietà regola]**.

   ![](assets/predefined-filter-parameter-apply.png)

   Per modificare il filtro predefinito stesso, fare clic sul pulsante ![puntini di sospensione](assets/do-not-localize/rule-builder-icon-more.svg) e selezionare **[!UICONTROL Passa all&#39;edizione delle regole]**. Tutte le modifiche vengono applicate solo alla regola corrente che si sta creando. Il filtro predefinito non viene modificato.

   ![](assets/predefined-filter-parameter-edit.png)

## Salvare un filtro come preferito {#fav-filter}

Quando crei un filtro predefinito, abilita l&#39;opzione **[!UICONTROL Filtro preferito]** per visualizzare questo filtro predefinito nei preferiti.

Quando un filtro viene salvato come preferito, viene visualizzato nella sezione **[!UICONTROL Filtri preferiti]** dell&#39;elenco dei filtri, come illustrato di seguito:

![Sezione Filtri preferiti](assets/predefined-filter-favorites.png)

## Condividere un filtro predefinito {#share-filter}

Per impostazione predefinita, i filtri predefiniti creati sono privati e visibili solo a te. Per rendere un filtro accessibile ad altri operatori dell&#39;organizzazione, abilitare l&#39;opzione **[!UICONTROL Filtro condiviso]**.

![Opzione filtro condiviso](assets/predefined-filter-shared.png)

I filtri condivisi vengono visualizzati nell’elenco dei filtri predefinito per tutti gli utenti, consentendo loro di utilizzarli nelle proprie regole.

## Gestire i filtri predefiniti {#manage-predefined-filter}

Per modificare o eliminare i filtri predefiniti, effettuare le seguenti operazioni:

1. Aprire l&#39;elenco di filtri predefiniti utilizzando il pulsante **[!UICONTROL Seleziona o salva filtro]** nella build della regola.

1. Seleziona il pulsante ![puntini di sospensione](assets/do-not-localize/rule-builder-icon-more.svg) accanto a un filtro e scegli l&#39;azione desiderata.

![](assets/predefined-filters-edit.png)
