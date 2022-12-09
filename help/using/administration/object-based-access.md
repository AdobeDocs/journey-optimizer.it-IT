---
solution: Journey Optimizer
product: journey optimizer
title: Controllo dell'accesso a livello di oggetto
description: Informazioni sul controllo degli accessi a livello di oggetto
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Controllo dell&#39;accesso a livello di oggetto {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Controllo dell&#39;accesso a livello di oggetto"
>abstract="Se si applicano etichette a cui non si dispone dell&#39;accesso, l&#39;accesso a questo oggetto verrà revocato."

>[!IMPORTANT]
>
>L’utilizzo del controllo di accesso a livello di oggetto è attualmente limitato a clienti selezionati e verrà distribuito a tutti gli ambienti in una versione futura.

Il controllo dell’accesso a livello di oggetto (OLAC) consente di definire le autorizzazioni per gestire l’accesso ai dati per una selezione di oggetti:

* Percorso
* Campaign
* Pagina di destinazione
* Offerte
* Raccolta di offerte
* Decisioni sulle offerte

Il suo scopo è proteggere i beni digitali sensibili da utenti non autorizzati che consentono un&#39;ulteriore protezione dei dati personali.

In Adobe Journey Optimizer, OLAC consente di proteggere i dati e concedere un accesso specifico a oggetti specifici.

## Creare etichette {#create-assign-labels}

>[!IMPORTANT]
>
>Per poter creare etichette, devi far parte di un ruolo con il **[!UICONTROL Manage usage labels]** autorizzazione.

**[!UICONTROL Labels]** consente di classificare set di dati e campi in base ai criteri di utilizzo applicati a tali dati. **[!UICONTROL Labels]** può essere applicato in qualsiasi momento, offrendo flessibilità nella scelta di come gestire i dati.

Puoi creare etichette nella [!DNL Permissions] prodotto. Per ulteriori informazioni, consulta [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html).

**[!UICONTROL Labels]** può anche essere creato direttamente in Journey Optimizer:

1. Da un oggetto Adobe Journey Optimizer, ecco una nuova creazione **[!UICONTROL Campaign]**, fai clic su **[!UICONTROL Manage access]** pulsante .

   ![](assets/olac_1.png)

1. Da **[!UICONTROL Manage access]** finestra, fai clic su **[!UICONTROL Create label]**.

   ![](assets/olac_2.png)

1. Configura l’etichetta, devi specificare:
   * **[!UICONTROL Name]**
   * **[!UICONTROL Friendly name]**
   * **[!UICONTROL Description]**

   ![](assets/olac_3.png)

1. Fai clic su **[!UICONTROL Create]** per salvare il **[!UICONTROL Label]**.

La nuova creazione **[!UICONTROL Label]** è ora disponibile nell’elenco. Se necessario, puoi modificarlo nella sezione [!DNL Permissions] prodotto.

## Assegnare le etichette {#assign-labels}

>[!IMPORTANT]
>
>Per poter assegnare le etichette, devi far parte di un ruolo con un’autorizzazione Gestisci , ovvero [!DNL Manage journeys], [!DNL Manage Campaigns] o [!DNL Manage decisions]. Senza questa autorizzazione, il **[!UICONTROL Manage access]** il pulsante sarà disabilitato.

Per assegnare etichette di utilizzo dati personalizzate o di base agli oggetti di Journey Optimizer:

1. Da un oggetto Adobe Journey Optimizer, ecco una nuova creazione **[!UICONTROL Campaign]**, fai clic su **[!UICONTROL Manage access]** pulsante .

   ![](assets/olac_1.png)

1. Da **[!UICONTROL Manage access]** seleziona le etichette di utilizzo dati personalizzate o principali per gestire l’accesso a questo oggetto.

   Per ulteriori informazioni sulle etichette di utilizzo dei dati di base, consulta [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html).

   ![](assets/olac_4.png)

1. Fai clic su **[!UICONTROL Save]** per applicare questa restrizione dell’etichetta.

Per poter accedere a questo oggetto, gli utenti dovranno disporre delle **[!UICONTROL Label]** inclusi nella **[!UICONTROL Roles]**.
Ad esempio, un utente con l’etichetta C1 avrà accesso solo agli oggetti con etichetta C1 o senza etichetta.

Per ulteriori informazioni su come assegnare **[!UICONTROL Label]** a **[!UICONTROL Role]**, fare riferimento a [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=en#manage-labels-for-a-role).
