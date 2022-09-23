---
title: Controllo dell'accesso a livello di oggetto
description: Informazioni sul controllo degli accessi a livello di oggetto
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 40061255a2fcec3de1b39a168cadbdedd2e12d87
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 4%

---

# Controllo dell&#39;accesso a livello di oggetto {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Controllo dell&#39;accesso a livello di oggetto"
>abstract="Se si applicano etichette a cui non si dispone dell&#39;accesso, l&#39;accesso a questo oggetto verrà revocato."

Il controllo dell’accesso a livello di oggetto (OLAC) consente di definire le autorizzazioni per gestire l’accesso ai dati per una selezione di oggetti:

* Percorso
* Campaign
* Landing page
* Offerte
* Raccolta di offerte
* Offer decisioning

Il suo scopo è proteggere i beni digitali sensibili da utenti non autorizzati che consentono un&#39;ulteriore protezione dei dati personali.

In Adobe Journey Optimizer, OLAC consente di proteggere i dati e concedere un accesso specifico a oggetti specifici.

## Create labels (Creare etichette) {#create-assign-labels}

>[!IMPORTANT]
>
>Per poter creare etichette, devi far parte di un ruolo con il **[!UICONTROL Gestire le etichette di utilizzo]** autorizzazione.

**[!UICONTROL Etichette]** consente di classificare set di dati e campi in base ai criteri di utilizzo applicati a tali dati. **[!UICONTROL Etichette]** può essere applicato in qualsiasi momento, offrendo flessibilità nella scelta di come gestire i dati.

Puoi creare etichette nella [!DNL Permissions] prodotto. Per ulteriori informazioni, consulta [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html).

**[!UICONTROL Etichette]** può anche essere creato direttamente in Journey Optimizer:

1. Da un oggetto Adobe Journey Optimizer, qui è stata creata una nuova **[!UICONTROL Campaign]**, fai clic su **[!UICONTROL Gestisci accesso]** pulsante .

   ![](assets/olac_1.png)

1. Da **[!UICONTROL Gestisci accesso]** finestra, fai clic su **[!UICONTROL Crea etichetta]**.

   ![](assets/olac_2.png)

1. Configura l’etichetta, devi specificare:
   * **[!UICONTROL Nome]**
   * **[!UICONTROL Nome descrittivo]**
   * **[!UICONTROL Descrizione]**

   ![](assets/olac_3.png)

1. Fai clic su **[!UICONTROL Crea]** per salvare il **[!UICONTROL Etichetta]**.

La nuova creazione **[!UICONTROL Etichetta]** è ora disponibile nell’elenco. Se necessario, puoi modificarlo nella sezione [!DNL Permissions] prodotto.

## Assegnare le etichette {#assign-labels}

>[!IMPORTANT]
>
>Per poter assegnare le etichette, devi far parte di un ruolo con un’autorizzazione Gestisci , ovvero [!DNL Manage journeys], [!DNL Manage Campaigns] o [!DNL Manage decisions]. Senza questa autorizzazione, il **[!UICONTROL Gestisci accesso]** il pulsante sarà disabilitato.

Per assegnare etichette di utilizzo dati personalizzate o principali agli oggetti Journey Optimizer:

1. Da un oggetto Adobe Journey Optimizer, qui è stata creata una nuova **[!UICONTROL Campaign]**, fai clic su **[!UICONTROL Gestisci accesso]** pulsante .

   ![](assets/olac_1.png)

1. Da **[!UICONTROL Gestisci accesso]** seleziona le etichette di utilizzo dati personalizzate o principali per gestire l’accesso a questo oggetto.

   Per ulteriori informazioni sulle etichette di utilizzo dei dati di base, consulta [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html).

   ![](assets/olac_4.png)

1. Fai clic su **[!UICONTROL Salva]** per applicare questa restrizione dell’etichetta.

Per poter accedere a questo oggetto, gli utenti dovranno disporre delle **[!UICONTROL Etichetta]** inclusi nella **[!UICONTROL Ruoli]**.

Per ulteriori informazioni su come assegnare **[!UICONTROL Etichetta]** a **[!UICONTROL Ruolo]**, fare riferimento a [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=en#manage-labels-for-a-role).



