---
title: Creare formule di classificazione
description: Scopri come creare formule di classificazione in Adobe Experience Platform.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 3%

---

# Creare formule di classificazione {#create-ranking-formulas}

## Informazioni sulla classificazione delle formule {#about-ranking-formulas}

**Le** formule di classificazione consentono di definire regole che determinano quale offerta deve essere presentata prima per un determinato posizionamento, anziché tenere conto dei punteggi di priorità delle offerte.

Le formule di classificazione sono espresse in **sintassi PQL** e possono sfruttare gli attributi di profilo, i dati contestuali e gli attributi di offerta. Per ulteriori informazioni su come utilizzare la sintassi PQL, consulta la [documentazione dedicata](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html).

Una volta creata una formula di classificazione, puoi assegnarla a un posizionamento in una decisione (precedentemente nota come attività di offerta). Per ulteriori informazioni, consulta [Configurare la selezione delle offerte nelle decisioni](../offer-activities/configure-offer-selection.md).

## Creare una formula di classificazione {#create-ranking-formula}

Per creare una formula di classificazione, segui i passaggi seguenti:

* Accedi al menu **[!UICONTROL Components]**, quindi seleziona la scheda **[!UICONTROL Rankings]** .

* Fare clic su **[!UICONTROL Create formula]** per creare una nuova formula di classificazione.

   ![](../../assets/ranking-create-formula.png)

* Specificare il nome, la descrizione e la formula della formula di classificazione.

   In questo esempio, vogliamo aumentare la priorità di tutte le offerte con l’attributo &quot;caldo&quot; se il tempo effettivo è caldo. A questo scopo, il **contextData.weather=hot** è stato passato nella chiamata decisionale.

   ![](../../assets/ranking-syntax.png)

* Fai clic su **[!UICONTROL Save]**. La formula di classificazione viene creata, è possibile selezionarla dall&#39;elenco per ottenere i dettagli e modificarla o eliminarla.

   È ora pronto per essere utilizzato in una decisione per classificare le offerte idonee per un posizionamento (consulta [Configurare la selezione di offerte nelle decisioni](../offer-activities/configure-offer-selection.md)).

   ![](../../assets/ranking-formula-created.png)
