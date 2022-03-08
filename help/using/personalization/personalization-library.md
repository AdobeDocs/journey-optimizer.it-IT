---
title: Utilizzare espressioni salvate
description: Scopri come utilizzare le espressioni salvate dal [!DNL Journey Optimizer] libreria.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Utilizzare espressioni salvate {#expression-library}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="Informazioni sulla libreria di espressioni"
>abstract="[!DNL Journey Optimizer] fornisce una libreria in cui puoi accedere alle espressioni di personalizzazione salvate configurate dagli utenti Admin. "

[!DNL Journey Optimizer] fornisce una libreria in cui puoi accedere alle espressioni di personalizzazione salvate in precedenza che sono state aggiunte dagli utenti Admin.

1. Per accedere alle espressioni salvate, fai clic sul pulsante **[!UICONTROL Library]** nel riquadro a sinistra. Nell’elenco sono visualizzate tutte le espressioni salvate dagli utenti Admin (vedi [Salvare le espressioni nella libreria](#save-expressions)).

   >[!NOTE]
   >
   >Puoi utilizzare il pulsante info per ottenere ulteriori informazioni sul contenuto di un’espressione salvata. Se disponi delle autorizzazioni appropriate per gestire gli elementi della libreria, il pulsante informazioni verrà visualizzato nel menu ellisse.

   ![](assets/library-list.png)

1. Fai clic sul segno + per inserire l’espressione nell’editor. Puoi quindi personalizzare e convalidare il contenuto di personalizzazione come di consueto. [Ulteriori informazioni](../personalization/personalization-build-expressions.md)

   ![](assets/library-add.png)

## Salvare un’espressione nella libreria {#save-expressions}

[!DNL Journey Optimizer] consente agli utenti amministratori di salvare le espressioni di personalizzazione nella libreria. Queste espressioni saranno quindi disponibili per tutti gli utenti per creare contenuti di personalizzazione.

Per salvare un&#39;espressione nella libreria, effettua le seguenti operazioni:

1. Nell’interfaccia dell’editor, genera l’espressione e fai clic su **[!UICONTROL Add to library]**.

   >[!NOTE]
   >
   >Se il pulsante non è visibile, verifica nell’Admin Console di disporre delle autorizzazioni necessarie (consulta [Livelli di autorizzazione](../administration/high-low-permissions.md)).

   ![](assets/library-save.png)

1. Nel riquadro a destra, immetti un titolo e una descrizione per l’espressione per facilitarne la ricerca da parte degli utenti, quindi fai clic su **[!UICONTROL Add]**.

   ![](assets/add-expression.png)

1. L&#39;espressione viene aggiunta alla libreria. Gli utenti potranno ora utilizzarlo per creare i propri contenuti di personalizzazione.


>[!NOTE]
>
>* Puoi salvare fino a 40 espressioni nella libreria.
>
>* Le espressioni non possono superare i 200 KB.
>
>* Le espressioni salvate vengono ordinate per data di creazione: l’espressione aggiunta di recente verrà visualizzata per prima nell’elenco.



Per modificare un’espressione esistente, aggiungilo all’editor, quindi modificala in base alle tue esigenze. Fai clic su **[!UICONTROL Add to library]** per convalidare la sintassi e salvare l’espressione.

Per eliminare un’espressione, fai clic sul pulsante ellisse , quindi fai clic su **[!UICONTROL Delete]**.
