---
solution: Journey Optimizer
product: journey optimizer
title: Creare condizioni
description: Scopri come creare le condizioni
feature: Personalization, Rules
topic: Personalization
role: Developer
level: Intermediate
keywords: espressione, editor, condizionale, regole
exl-id: 246a4a55-059e-462c-ac1e-43b90f4abda4
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 8%

---

# Utilizzare le regole condizionali {#conditions}

Le regole condizionali sono insiemi di regole che definiscono quale contenuto deve essere visualizzato nei messaggi, a seconda di vari criteri come gli attributi dei profili, l’appartenenza a un pubblico o gli eventi contestuali.

Le regole condizionali vengono create utilizzando l’editor di personalizzazione e possono essere memorizzate se desideri riutilizzarle nei contenuti. [Scopri come salvare una regola condizionale nella libreria](#save)

>[!NOTE]
>
>Gli utenti dovranno disporre dell&#39;autorizzazione [Gestisci elementi libreria](../administration/ootb-product-profiles.md) per salvare o eliminare le regole condizionali. Le condizioni salvate sono disponibili per l’utilizzo da parte di tutti gli utenti di un’organizzazione.

## Accedere al generatore di regole condizionali {#access}

Le regole condizionali vengono create dal menu **[!UICONTROL Condizioni]** all&#39;interno dell&#39;editor di personalizzazione, accessibile:

* Da E-mail Designer, quando si abilita il contenuto dinamico per un componente nel corpo dell’e-mail. [Scopri come aggiungere contenuto dinamico alle e-mail](dynamic-content.md#emails)

  ![](assets/conditions-access-email.png)

* In qualsiasi campo in cui puoi aggiungere la personalizzazione utilizzando l&#39;[editor di personalizzazione](personalization-build-expressions.md).

  ![](assets/conditions-access-editor.png)

## Creare una regola condizionale {#create-condition}

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions_create"
>title="Creare una condizione"
>abstract="Combina gli attributi di profilo, gli eventi contestuali o i segmenti di pubblico per creare regole che definiscano quali contenuti visualizzare nei messaggi."

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions"
>title="Creare una condizione"
>abstract="Combina gli attributi di profilo, gli eventi contestuali o i segmenti di pubblico per creare regole che definiscano quali contenuti visualizzare nei messaggi."

I passaggi per creare una regola condizionale sono i seguenti:

1. Accedi al menu **[!UICONTROL Condizioni]** dall&#39;editor di personalizzazione o da E-mail Designer, quindi fai clic su **[!UICONTROL Crea nuovo]**.

1. Crea la regola condizionale in base alle tue esigenze. A questo scopo, trascina e rilascia nell’area di lavoro gli attributi desiderati dal menu a sinistra.

   I passaggi per combinare gli attributi nell’area di lavoro sono simili all’esperienza di creazione dei segmenti. Per ulteriori informazioni su come utilizzare l&#39;area di lavoro del generatore di regole, consultare [questa documentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=it#rule-builder-canvas).

   ![](assets/conditions-create.png)

   Gli attributi sono organizzati in tre schede:

   * **[!UICONTROL Profilo]**:
      * **[!UICONTROL Tipi di pubblico]** elenca tutti gli attributi del pubblico (ad esempio stato, versione ecc.) per [Servizio di segmentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=it){target="_blank"},
      * **[!UICONTROL Profili individuali XDM]** elenca tutti gli attributi di profilo associati allo schema [Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"} definito in Adobe Experience Platform.
   * **[!UICONTROL Contestuale]**: quando il messaggio viene utilizzato in un percorso, i campi del percorso contestuale sono disponibili tramite questa scheda.
   * **[!UICONTROL Tipi di pubblico]**: elenca tutti i tipi di pubblico generati dalle definizioni dei segmenti create nel [servizio di segmentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=it){target="_blank"}.

1. Una volta che la regola condizionale è pronta, puoi aggiungerla al messaggio per creare contenuto dinamico. [Scopri come aggiungere contenuti dinamici](dynamic-content.md)

   Puoi anche salvare la regola per consentire un ulteriore riutilizzo. [Scopri come salvare una condizione](#save)

## Salvare una regola condizionale {#save}

Se esistono regole di condizione che riutilizzerai frequentemente, puoi salvarle nella libreria delle condizioni. Tutte le regole salvate sono condivise e possono essere accessibili e utilizzate da singoli utenti all’interno dell’organizzazione.

>[!NOTE]
>
>Le regole condizionali che sfruttano gli attributi contestuali dei percorsi non possono essere salvate nella libreria.

1. Nella schermata di modifica della condizione, fare clic sul pulsante **[!UICONTROL Salva condizione]**.

1. Assegna un nome e una descrizione (facoltativa) alla regola, quindi fai clic su **[!UICONTROL Aggiungi]**.

   ![](assets/conditions-name-description.png)

1. La regola condizionale viene salvata nella libreria. Ora puoi utilizzarlo per creare contenuto dinamico nei messaggi. [Scopri come aggiungere contenuti dinamici](dynamic-content.md)


>[!CAUTION]
>
>Quando si denominano le varianti di contenuto condizionale, utilizza solo caratteri alfanumerici (A-Z, a-z, 0-9). L&#39;utilizzo di caratteri speciali (ad esempio `<`, `>`, `=`, `{`, `}` e così via) nei nomi delle varianti può causare l&#39;interruzione o la mancata visualizzazione dei componenti da parte dell&#39;editor modelli.

## Modificare ed eliminare le regole condizionali salvate {#edit-delete}

Puoi eliminare una regola condizionale in qualsiasi momento utilizzando il pulsante con i puntini di sospensione.

![](assets/conditions-open.png)

Le regole condizionali salvate nella libreria non possono essere modificate. Tuttavia, puoi comunque utilizzarli per creare nuove regole. A questo scopo, apri la regola condizionale, apporta le modifiche desiderate, quindi salvala nella libreria. [Scopri come salvare una condizione nella libreria](#save)
