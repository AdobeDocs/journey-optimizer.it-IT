---
solution: Journey Optimizer
product: journey optimizer
title: Controllo dell’accesso a livello di oggetto
description: Scopri il controllo dell’accesso a livello di oggetto, che consente di definire le autorizzazioni per gestire l’accesso ai dati per una selezione di oggetti
feature: Access Management
topic: Administration
role: Admin, Developer, Architect
level: Experienced
keywords: oggetto, livello, accesso, controllo, etichette, olac, autorizzazione
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: 342b9210f79266cb11628dcdc411f90844a84e37
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 7%

---

# Controllo dell’accesso a livello di oggetto {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Controllo dell’accesso a livello di oggetto"
>abstract="Per mantenere l’accesso a questo oggetto, applica solo le etichette per le quali disponi dell’autorizzazione."

Il controllo dell&#39;accesso a livello di oggetto (OLAC) consente di definire le autorizzazioni per gestire l&#39;accesso ai dati a una selezione di oggetti:

* Percorso
* Campaign
* Modello
* Frammento
* Landing page
* Nome
* Raccolta di offerte statiche
* Decisione sull’offerta
* Superficie di canale
* Piano di riscaldamento IP

Il suo scopo è proteggere le risorse digitali sensibili da utenti non autorizzati, consentendo un&#39;ulteriore protezione dei dati personali.

In Adobe Journey Optimizer, OLAC consente di proteggere i dati e concedere un accesso specifico a oggetti specifici.

## Create labels (Creare etichette) {#create-assign-labels}

>[!IMPORTANT]
>
>Per poter creare le etichette, devi far parte di un ruolo con **[!UICONTROL Gestisci etichette di utilizzo]** autorizzazione.

**[!UICONTROL Etichette]** consente di categorizzare set di dati e campi in base ai criteri di utilizzo applicabili a tali dati. **[!UICONTROL Etichette]** può essere applicata in qualsiasi momento, fornendo flessibilità nella scelta di come gestire i dati.

È possibile creare etichette in [!DNL Permissions] prodotto. Per ulteriori informazioni, consulta [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html).

**[!UICONTROL Etichette]** può essere creato direttamente in Journey Optimizer:

1. Da un oggetto Adobe Journey Optimizer, qui è stato creato un nuovo oggetto **[!UICONTROL Campagna]**, fare clic su **[!UICONTROL Gestisci accesso]** pulsante.

   ![](assets/olac_1.png)

1. Dalla sezione **[!UICONTROL Gestisci accesso]** finestra, fai clic su **[!UICONTROL Crea etichetta]**.

   ![](assets/olac_2.png)

1. Configurare l’etichetta, è necessario specificare:
   * **[!UICONTROL Nome]**
   * **[!UICONTROL Nome intuitivo]**
   * **[!UICONTROL Descrizione]**

   ![](assets/olac_3.png)

1. Clic **[!UICONTROL Crea]** per salvare **[!UICONTROL Etichetta]**.

Il nuovo **[!UICONTROL Etichetta]** è ora disponibile nell’elenco. Se necessario, puoi modificarlo in [!DNL Permissions] prodotto.

## Assegna etichette {#assign-labels}

>[!IMPORTANT]
>
>Per poter assegnare le etichette, devi far parte di un ruolo con un’autorizzazione Gestione, ad esempio [!DNL Manage journeys], [!DNL Manage Campaigns] o [!DNL Manage decisions]. Senza questa autorizzazione, il **[!UICONTROL Gestisci accesso]** il pulsante sarà disattivato.

Per assegnare etichette di utilizzo dei dati personalizzate o di base agli oggetti Journey Optimizer:

1. Da un oggetto Adobe Journey Optimizer, qui è stato creato un nuovo oggetto **[!UICONTROL Campagna]**, fare clic su **[!UICONTROL Gestisci accesso]** pulsante.

   ![](assets/olac_1.png)

1. Dalla sezione **[!UICONTROL Gestisci accesso]** per gestire l&#39;accesso a questo oggetto, seleziona le etichette di utilizzo dei dati personalizzate o di base.

   Per ulteriori informazioni sulle etichette di utilizzo dei dati di base, consulta [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html).

   ![](assets/olac_4.png)

1. Clic **[!UICONTROL Salva]** per applicare questa restrizione dell’etichetta.

Per avere accesso a questo oggetto, gli utenti dovranno disporre del **[!UICONTROL Etichetta]** incluso nel loro **[!UICONTROL Ruoli]**.
Ad esempio, un utente con l’etichetta C1 avrà accesso solo a oggetti con etichetta C1 o senza etichetta.

Per ulteriori informazioni su come assegnare **[!UICONTROL Etichetta]** a un **[!UICONTROL Ruolo]**, fare riferimento a [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html#manage-labels-for-a-role).