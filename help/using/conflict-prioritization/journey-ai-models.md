---
title: Modelli di IA per arbitraggio di percorso
description: Scopri come creare e utilizzare i modelli di intelligenza artificiale per classificare i percorsi a scopo di arbitrato, in modo da selezionare il percorso migliore per profilo in base ai punteggi basati sull’intelligenza artificiale.
feature: Journeys, Decisioning
role: User
level: Intermediate
version: Journey Orchestration
badge: label="Disponibilità limitata" type="Informative"
hide: true
hidefromtoc: true
source-git-commit: fe6e8221201ee813251a46c6603d85f0803873c0
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 4%

---

# Utilizzare i modelli AI per classificare i percorsi {#journey-ai-models}

>[!AVAILABILITY]
>
>Questa funzione è attualmente disponibile in modo limitato. Per ottenere l’accesso, contatta il rappresentante Adobe.

[!DNL Adobe Journey Optimizer] consente di controllare i percorsi che un profilo può inserire quando sono idonei per un numero maggiore di quello consentito dal sistema. A tale scopo, è possibile utilizzare [set di regole](rule-sets.md) per definire i limiti per l&#39;immissione o la concorrenza nel percorso. Quando un profilo è idoneo per un numero di percorsi superiore a quello consentito dal limite, la priorità assegnata a ciascun percorso determina quali percorsi sono selezionati.

Anziché utilizzare le formule di priorità o classificazione, è possibile utilizzare **modelli AI** per classificare dinamicamente i percorsi in base ai punteggi dei modelli addestrati. Puoi creare modelli AI dalla sezione **[!UICONTROL Classificazione orchestrazione]** nell&#39;interfaccia utente e utilizzarli nei set di regole per applicarli ai percorsi.

Per una panoramica dei tipi di modelli di IA disponibili in [!DNL Journey Optimizer], vedere [Introduzione ai modelli di IA](../experience-decisioning/ranking/ai-models.md#ai-model-types) nella sezione Decisioning.

## Creare un modello IA {#create-ai-model}

>[!CAUTION]
>
>Per creare, modificare o eliminare modelli AI, è necessario disporre dell&#39;autorizzazione **Gestisci strategie di classificazione**. [Ulteriori informazioni](../administration/high-low-permissions.md#manage-ranking-strategies)

Per creare un modello di intelligenza artificiale per la classificazione del percorso, segui i passaggi indicati di seguito.

1. Crea un set di dati in cui verranno raccolti gli eventi di conversione. [Scopri come](../experience-decisioning/data-collection/create-dataset.md)

1. Accedi alla sezione **[!UICONTROL Classificazione orchestrazione]**, quindi seleziona la scheda **[!UICONTROL Modelli AI]**. Viene visualizzato l’elenco dei modelli AI creati in precedenza.

1. Fare clic su **[!UICONTROL Crea modello di IA]**.

1. Specifica un nome univoco e, se necessario, una descrizione per il modello di IA.

   ![Riquadro dettagli modello IA con campi nome e descrizione](assets/journey-model-details.png){width="80%"}

   >[!NOTE]
   >
   >L’oggetto di classificazione è l’entità a cui verrà applicata la formula di classificazione. Per impostazione predefinita, l&#39;oggetto di classificazione è impostato su **[!UICONTROL Percorso]**.

<!--
1. Select the type of AI model you want to create:

    * **[!UICONTROL Auto-optimization]** optimizes based on past performance. [Learn more](../experience-decisioning/ranking/auto-optimization-model.md)
    * **[!UICONTROL Personalized optimization]** optimizes and personalizes based on audiences and performance. [Learn more](../experience-decisioning/ranking/personalized-optimization-model.md)-->

1. La sezione **[!UICONTROL Metrica di ottimizzazione]** fornisce informazioni sull&#39;evento di conversione utilizzato dal modello di IA. [!DNL Journey Optimizer] classifica in base al **tasso di conversione** (tasso di conversione = numero totale di eventi di conversione / numero totale di eventi di impression). Il tasso di conversione è calcolato utilizzando:

   * **Eventi di impression** (elementi visualizzati)
   * **Eventi di conversione** (elementi che determinano clic o conversioni)

   Questi eventi vengono acquisiti automaticamente tramite Web SDK o Mobile SDK. Ulteriori informazioni sono disponibili nella panoramica di [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it).

1. Seleziona i set di dati in cui vengono raccolti gli eventi di conversione e di impression. Scopri come creare tali set di dati in [questa sezione](../experience-decisioning/data-collection/create-dataset.md).

   ![Selezione di set di dati per eventi di conversione e impression](../experience-decisioning/assets/ai-model-datasets.png){width="85%"}

   >[!CAUTION]
   >
   >Nell&#39;elenco a discesa vengono visualizzati solo i set di dati creati da schemi associati al gruppo di campi **[!UICONTROL Evento esperienza - Interazioni proposta]** (precedentemente noto come mixin).

1. &#x200B;<!--If you are creating a **[!UICONTROL Personalized optimization]** AI model, -->Seleziona i segmenti da utilizzare per addestrare il modello di intelligenza artificiale.

   >[!NOTE]
   >
   >Puoi selezionare fino a 5 tipi di pubblico.

1. Salva e attiva il modello di intelligenza artificiale.

Il modello di IA è ora disponibile quando configuri un set di regole.

## Assegnare il modello di IA a un set di regole {#assign-ai-model-to-ruleset}

Per utilizzare un modello di IA per classificare i percorsi, è necessario utilizzarlo in una formula e assegnare la formula a un set di regole.

1. Crea una formula di classificazione utilizzando il modello di IA creato. [Scopri come](journey-ranking-formulas.md#create-journey-ranking-formula)

1. Creare un set di regole da utilizzare per l&#39;arbitraggio di percorso dal menu **[!UICONTROL Regole aziendali]**. [Scopri come](rule-sets.md#Create)

1. Assicurarsi di selezionare il dominio **[!UICONTROL Percorso]**.

1. Nelle proprietà del set di regole, impostare il metodo di classificazione **&#x200B;**&#x200B;su **[!UICONTROL Formula]** (anziché **[!UICONTROL Priorità]**).

1. Seleziona la formula che utilizza il modello di IA creato dall’elenco a discesa.

1. Creare le regole di limite di percorso da aggiungere al set di regole. [Scopri come](journey-capping.md#create-rule)

1. Salva il set di regole.

Ora la formula che utilizza il modello di IA viene assegnata al set di regole. Puoi quindi applicare il set di regole ai tuoi percorsi.

## Applicare il set di regole a un percorso {#assign-rule-set-to-journey}

Per assegnare il set di regole a un percorso, effettua le seguenti operazioni.

1. Creare o aprire il percorso a cui si desidera assegnare il set di regole. [Scopri come creare un percorso](../building-journeys/journey-gs.md)

1. Nelle proprietà del percorso, seleziona il set di regole dall’elenco a discesa. [Scopri come](journey-capping.md#apply-capping).

   >[!NOTE]
   >
   >È possibile applicare un solo set di regole a un percorso alla volta.

1. Salvare il percorso.

Tutti i percorsi che utilizzano questo set di regole vengono classificati con la formula selezionata utilizzando il modello di IA quando viene applicato il limite.
