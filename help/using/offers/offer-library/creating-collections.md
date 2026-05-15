---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Creare raccolte
description: Scopri come organizzare le offerte utilizzando le raccolte
badge: label="Legacy" type="Informative"
feature: Decision Management, Collections
topic: Integrations
role: User
level: Intermediate
exl-id: 0c8808e3-9148-4a33-9fd5-9218e02c2dfd
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/7IXZss-Qpg5D67uPfkFbo3Gmp1n2gdSD24Y4rbL3-Fk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 34%

---

# Creare raccolte {#create-collections}

>[!TIP]
>
>La funzione Decisioni, la nuova funzionalità decisionale di [!DNL Adobe Journey Optimizer], è ora disponibile tramite i canali e-mail e di esperienza basati su codice. [Ulteriori informazioni](../../experience-decisioning/gs-experience-decisioning.md)

>[!CONTEXTUALHELP]
>id="ajo_decisioning_decision_collection"
>title="Informazioni sulle raccolte di offerte"
>abstract="Le raccolte consentono di organizzare le offerte raggruppandole in categorie a tua scelta."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_dynamic"
>title="Raccolta dinamica"
>abstract="Utilizza i qualificatori di raccolta per qualificare dinamicamente le offerte per una raccolta."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_static"
>title="Raccolta statica"
>abstract="Seleziona e raggruppa manualmente le offerte utilizzando criteri quali lo stato, i qualificatori di raccolta, la data e il canale."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_static_select"
>title="Anteprima raccolta statica"
>abstract="Le raccolte statiche vengono create selezionando manualmente le singole offerte da includere nella raccolta. La raccolta può essere aggiornata solo aggiungendo manualmente altre offerte."

>[!CONTEXTUALHELP]
>id="ajo_decisioning_collection_dynamic_select"
>title="Anteprima raccolta dinamica"
>abstract="Le raccolte dinamiche raccolgono le offerte in base ai qualificatori di raccolta. Queste raccolte vengono aggiornate automaticamente. Ad esempio, se viene creata una nuova offerta con il qualificatore di raccolta “sport”, questa verrà aggiunta automaticamente alla raccolta corrispondente."

Le raccolte ti consentono di organizzare le offerte raggruppandole in categorie a tua scelta. Ad esempio, puoi creare una raccolta &quot;sport&quot; che conterrà solo offerte relative allo sport.

➡️ [Scopri questa funzione nel video](#video)

L&#39;elenco delle raccolte di offerte è accessibile nel menu **[!UICONTROL Offerte]**.

![](../assets/collections_list.png)

Puoi creare due tipi di raccolte:

* **Le raccolte dinamiche** sono raccolte di offerte basate su qualificatori di raccolta (noti in precedenza come &quot;tag&quot;). Queste raccolte vengono aggiornate automaticamente. Ad esempio, se viene creata una nuova offerta con il qualificatore di raccolta selezionato, questa verrà aggiunta automaticamente alla raccolta.

* **Le raccolte statiche** sono raccolte create selezionando manualmente le singole offerte da includere nella raccolta. La raccolta può essere aggiornata solo aggiungendo manualmente altre offerte.

Per creare una raccolta, effettua le seguenti operazioni:

1. Vai alla scheda **[!UICONTROL Raccolte]**, quindi fai clic su **[!UICONTROL Crea raccolta]**.

1. Specifica il nome e il tipo di raccolta da creare.

   ![](../assets/collection_create.png)

1. Per creare una raccolta dinamica, utilizzare il riquadro a sinistra per selezionare il qualificatore di raccolta delle offerte da aggiungere alla raccolta, quindi fare clic su **[!UICONTROL Salva]**. Tutte le offerte con il qualificatore di raccolta selezionato verranno salvate nella raccolta.

   Per ulteriori informazioni sulla creazione di qualificatori di raccolta, vedere [Creare qualificatori di raccolta](../offer-library/creating-tags.md).

   ![](../assets/dynamic_collection.png)

1. Per creare una raccolta statica, utilizza il riquadro a sinistra per filtrare l’elenco delle offerte (stato, qualificatore della raccolta, data, canale, tipo di contenuto), quindi seleziona le offerte da aggiungere alla raccolta.

   ![](../assets/static_collection.png)

   >[!NOTE]
   >
   >Le raccolte statiche non vengono aggiornate automaticamente. Per aggiungere offerte a una raccolta statica, devi modificarla e aggiungerle manualmente.

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base a una raccolta statica, selezionare **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni sul controllo degli accessi a livello di oggetto (OLAC)](../../administration/object-based-access.md)

   >[!NOTE]
   >
   >L&#39;utilizzo di OLAC non è disponibile per le raccolte dinamiche. Deve essere gestito a livello di offerta. Di conseguenza, se non hai accesso a nessuna di queste offerte, è possibile che non venga visualizzata alcuna offerta all’interno di una raccolta dinamica.

1. Una volta creata la raccolta, questa viene visualizzata nell’elenco. Puoi selezionarla per modificarla o eliminarla.

   ![](../assets/collection_created.png)

## Video introduttivo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/346688?captions=ita&quality=12)


