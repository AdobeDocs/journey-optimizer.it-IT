---
solution: Journey Optimizer
product: journey optimizer
title: Creare condizioni
description: Scopri come creare le condizioni
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: espressione, editor, condizionale, regole
exl-id: 246a4a55-059e-462c-ac1e-43b90f4abda4
source-git-commit: 59499dec7d15dd4565c7910d7b454d82243ff011
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 8%

---

# Utilizzare le regole condizionali {#conditions}

Le regole condizionali sono insiemi di regole che definiscono quale contenuto deve essere visualizzato nei messaggi, a seconda di vari criteri come gli attributi dei profili, l’appartenenza a un segmento o gli eventi contestuali.

Le regole condizionali vengono create utilizzando l’editor di espressioni e possono essere memorizzate se desideri riutilizzarle all’interno del contenuto. [Scopri come salvare una regola condizionale nella libreria](#save)

>[!NOTE]
>
>I singoli utenti avranno bisogno di [Gestisci elementi libreria](../administration/ootb-product-profiles.md) autorizzazione a salvare o eliminare le regole condizionali. Le condizioni salvate sono disponibili per l’utilizzo da parte di tutti gli utenti di un’organizzazione.

## Accedere al generatore di regole condizionali {#access}

Le regole condizionali vengono create dal **[!UICONTROL Condizioni]** nell’editor di espressioni, accessibile:

* Da E-mail Designer, quando si abilita il contenuto dinamico per un componente nel corpo dell’e-mail. [Scopri come aggiungere contenuto dinamico alle e-mail](dynamic-content.md#emails)

   ![](assets/conditions-access-email.png)

* In qualsiasi campo in cui puoi aggiungere la personalizzazione utilizzando [Editor espressioni](personalization-build-expressions.md).

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

1. Accedere a **[!UICONTROL Condizioni]** nell’editor di espressioni o in E-mail Designer, quindi fai clic su **[!UICONTROL Crea nuovo]**.

1. Crea la regola condizionale in base alle tue esigenze. A questo scopo, trascina e rilascia nell’area di lavoro gli attributi desiderati dal menu a sinistra.

   I passaggi per combinare gli attributi nell’area di lavoro sono simili all’esperienza di creazione dei segmenti. Per ulteriori informazioni su come utilizzare l’area di lavoro del generatore di regole, consulta [questa documentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#rule-builder-canvas).

   ![](assets/conditions-create.png)

   Gli attributi sono organizzati in tre schede:

   * **[!UICONTROL Profilo]**:
      * **[!UICONTROL Iscrizione al segmento]** elenca tutti gli attributi del segmento (ad esempio stato, versione, ecc.) per [Servizio di segmentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html),
      * **[!UICONTROL Profili individuali XDM]** elenca tutti gli attributi di profilo associati al profilo [Schema Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it) definiti in Adobe Experience Platform.
   * **[!UICONTROL Contestuale]**: quando il messaggio viene utilizzato in un percorso, i campi del percorso contestuale sono disponibili tramite questa scheda.
   * **[!UICONTROL Tipi di pubblico]**: elenca tutti i tipi di pubblico generati dai segmenti creati in [Servizio di segmentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

1. Una volta che la regola condizionale è pronta, puoi aggiungerla al messaggio per creare contenuto dinamico. [Scopri come aggiungere contenuti dinamici](dynamic-content.md)

   Puoi anche salvare la regola per consentire un ulteriore riutilizzo. [Scopri come salvare una condizione](#save)

## Salvare una regola condizionale {#save}

Se esistono regole di condizione che riutilizzerai frequentemente, puoi salvarle nella libreria delle condizioni. Tutte le regole salvate sono condivise e possono essere accessibili e utilizzate da singoli utenti all’interno dell’organizzazione.

>[!NOTE]
>
>Le regole condizionali che sfruttano gli attributi contestuali dei percorsi non possono essere salvate nella libreria.

1. Nella schermata di modifica delle condizioni, fai clic su **[!UICONTROL Salva condizione]** pulsante.

1. Assegna un nome e una descrizione (facoltativa) alla regola, quindi fai clic su **[!UICONTROL Aggiungi]**.

   ![](assets/conditions-name-description.png)

1. La regola condizionale viene salvata nella libreria. Ora puoi utilizzarlo per creare contenuto dinamico nei messaggi. [Scopri come aggiungere contenuti dinamici](dynamic-content.md)

## Modificare ed eliminare le regole condizionali salvate {#edit-delete}

Puoi eliminare una regola condizionale in qualsiasi momento utilizzando il pulsante con i puntini di sospensione.

![](assets/conditions-open.png)

Le regole condizionali salvate nella libreria non possono essere modificate. Tuttavia, puoi comunque utilizzarli per creare nuove regole. A questo scopo, apri la regola condizionale, apporta le modifiche desiderate, quindi salvala nella libreria. [Scopri come salvare una condizione nella libreria](#save)
