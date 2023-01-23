---
solution: Journey Optimizer
product: journey optimizer
title: Creare condizioni
description: Scopri come creare condizioni
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: espressione, editor, condizionale, regole
exl-id: 246a4a55-059e-462c-ac1e-43b90f4abda4
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 1%

---

# Utilizzare le regole condizionali {#conditions}

Le regole condizionali sono insiemi di regole che definiscono quale contenuto visualizzare nei messaggi, a seconda di vari criteri come gli attributi dei profili, l’appartenenza al segmento o gli eventi contestuali.

Le regole condizionali vengono create utilizzando l’editor di espressioni e possono essere memorizzate se desideri riutilizzarle all’interno del contenuto. [Scopri come salvare una regola condizionale nella libreria](#save)

>[!NOTE]
>
>Gli individui avranno bisogno del [Gestisci elementi libreria](../administration/ootb-product-profiles.md) autorizzazione per salvare o eliminare regole condizionali. Le condizioni salvate sono disponibili per l’utilizzo da parte di tutti gli utenti di un’organizzazione.

## Accedere al generatore di regole condizionali {#access}

Le regole condizionali vengono create dal **[!UICONTROL Condizioni]** all’interno dell’editor di espressioni, accessibile:

* Da E-mail Designer, quando si abilita il contenuto dinamico per un componente nel corpo dell’e-mail. [Scopri come aggiungere contenuto dinamico alle e-mail](dynamic-content.md#emails)

   ![](assets/conditions-access-email.png)

* In qualsiasi campo in cui puoi aggiungere la personalizzazione utilizzando la [Editor espressioni](personalization-build-expressions.md).

   ![](assets/conditions-access-editor.png)

## Creare una regola condizionale {#create-condition}

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions_create"
>title="Crea condizione"
>abstract="Combina gli attributi di profilo, gli eventi contestuali o i tipi di pubblico per creare regole che definiscano quale contenuto visualizzare nei messaggi."

>[!CONTEXTUALHELP]
>id="ajo_expression_editor_conditions"
>title="Crea condizione"
>abstract="Combina gli attributi di profilo, gli eventi contestuali o i tipi di pubblico per creare regole che definiscano quale contenuto visualizzare nei messaggi."

I passaggi per creare una regola condizionale sono i seguenti:

1. Accedere al **[!UICONTROL Condizioni]** dall’Editor espressioni o da E-mail Designer, quindi fai clic su **[!UICONTROL Crea nuovo]**.

1. Crea la regola condizionale in base alle tue esigenze. A questo scopo, trascina e rilascia e disponi gli attributi desiderati dal menu a sinistra nell’area di lavoro.

   I passaggi per combinare gli attributi nell’area di lavoro sono simili all’esperienza di creazione dei segmenti. Per ulteriori informazioni su come utilizzare l&#39;area di lavoro del generatore di regole, consulta [questa documentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#rule-builder-canvas).

   ![](assets/conditions-create.png)

   Gli attributi sono organizzati in tre schede:

   * **[!UICONTROL Profilo]**:
      * **[!UICONTROL Appartenenza al segmento]** elenca tutti gli attributi del segmento (ad es. stato, versione, ecc.) per [Servizio di segmentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html),
      * **[!UICONTROL Profili individuali XDM]** elenca tutti gli attributi del profilo associati alla [Schema Experience Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it) definito in Adobe Experience Platform.
   * **[!UICONTROL Contestuale]**: quando il messaggio viene utilizzato in un percorso, i campi del percorso contestuale sono disponibili in questa scheda.
   * **[!UICONTROL Tipi di pubblico]**: elenca tutti i tipi di pubblico generati dai segmenti creati in [Servizio di segmentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

1. Quando la regola condizionale è pronta, puoi aggiungerla al messaggio per creare contenuto dinamico. [Scopri come aggiungere contenuto dinamico](dynamic-content.md)

   Puoi anche salvare la regola per consentirne un ulteriore riutilizzo. [Scopri come salvare una condizione](#save)

## Salvare una regola condizionale {#save}

Se sono presenti regole di condizione che verranno riutilizzate di frequente, è possibile salvarle nella libreria delle condizioni. Tutte le regole salvate sono condivise e possono essere utilizzate da singoli utenti all’interno della tua organizzazione.

>[!NOTE]
>
>Non è possibile salvare nella libreria le regole condizionali che sfruttano gli attributi contestuali dei percorsi.

1. Nella schermata di modifica della condizione, fai clic sul pulsante **[!UICONTROL Salva condizione]** pulsante .

1. Assegna un nome e una descrizione (facoltativi) alla regola, quindi fai clic su **[!UICONTROL Aggiungi]**.

   ![](assets/conditions-name-description.png)

1. La regola condizionale viene salvata nella libreria. Ora puoi utilizzarlo per creare contenuti dinamici nei messaggi. [Scopri come aggiungere contenuto dinamico](dynamic-content.md)

## Modificare ed eliminare le regole condizionali salvate {#edit-delete}

Puoi eliminare una regola condizionale in qualsiasi momento utilizzando il pulsante di ellisse .

![](assets/conditions-open.png)

Impossibile modificare le regole condizionali salvate nella libreria. Tuttavia, puoi comunque utilizzarli per creare nuove regole. A questo scopo, apri la regola condizionale, apporta le modifiche desiderate e salvala nella libreria. [Scopri come salvare una condizione nella libreria](#save)
