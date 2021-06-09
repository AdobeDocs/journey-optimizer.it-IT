---
title: Creare formule di classificazione
description: Scopri come creare formule di classificazione in Adobe Experience Platform.
source-git-commit: ea8a3644ecef911a14ea087b03d367976f0c898d
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 2%

---

# Creare formule di classificazione {#create-ranking-formulas}

## Informazioni sulla classificazione delle formule {#about-ranking-formulas}

**Le** formule di classificazione consentono di definire regole che determinano quale offerta deve essere presentata prima per un determinato posizionamento, anziché tenere conto dei punteggi di priorità delle offerte.

Le formule di classificazione sono espresse in **sintassi PQL** e possono sfruttare gli attributi di profilo, i dati contestuali e gli attributi di offerta. Per ulteriori informazioni su come utilizzare la sintassi PQL, consulta la [documentazione dedicata](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html).

Una volta creata una formula di classificazione, puoi assegnarla a un posizionamento in una decisione (precedentemente nota come attività di offerta). Per ulteriori informazioni, consulta [Configurare la selezione delle offerte nelle decisioni](../offer-activities/configure-offer-selection.md).

## Creare una formula di classificazione {#create-ranking-formula}

Per creare una formula di classificazione, segui i passaggi seguenti:

1. Accedi al menu **[!UICONTROL Components]**, quindi seleziona la scheda **[!UICONTROL Rankings]** . Viene visualizzato l’elenco delle classificazioni create in precedenza.

   ![](../../assets/rankings-list.png)

1. Fare clic su **[!UICONTROL Create ranking]** per creare una nuova formula di classificazione.

   ![](../../assets/ranking-create-formula.png)

1. Specificare il nome, la descrizione e la formula della formula di classificazione.

   In questo esempio, vogliamo aumentare la priorità di tutte le offerte con l’attributo &quot;caldo&quot; se il tempo effettivo è caldo. A questo scopo, il **contextData.weather=hot** è stato passato nella chiamata decisionale.

   ![](../../assets/ranking-syntax.png)

1. Fai clic su **[!UICONTROL Save]**. La formula di classificazione viene creata, è possibile selezionarla dall&#39;elenco per ottenere i dettagli e modificarla o eliminarla.

   È ora pronto per essere utilizzato in una decisione per classificare le offerte idonee per un posizionamento (consulta [Configurare la selezione di offerte nelle decisioni](../offer-activities/configure-offer-selection.md)).

   ![](../../assets/ranking-formula-created.png)
