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
source-git-commit: 3cbda018a1380e13ba3670563240238367517353
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 8%

---

# Controllo dell’accesso a livello di oggetto {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Etichette per la gestione degli accessi"
>abstract="È possibile limitare l&#39;accesso a un oggetto in base alle etichette di accesso. Il suo scopo è proteggere le risorse digitali sensibili da utenti non autorizzati, consentendo un&#39;ulteriore protezione dei dati personali. **Assicurarsi di selezionare solo le etichette per le quali si dispone dell&#39;autorizzazione.**"

È possibile limitare l&#39;accesso a un oggetto in base alle etichette di accesso. Il suo scopo è proteggere le risorse digitali sensibili da utenti non autorizzati, consentendo un&#39;ulteriore protezione dei dati personali.

La funzionalità OLAC (Object Level Access Control) consente di definire le autorizzazioni per gestire l&#39;accesso ai dati a una selezione di oggetti:

* Percorso
* Campaign
* Modello
* Frammento
* Landing page
* Nome
* Raccolta di offerte statiche
* Decisione sull’offerta
* Configurazione dei canali
* Piano di riscaldamento IP


## Prerequisiti {#prereq-labels}

Per poter [creare etichette](#create-labels), devi far parte di un ruolo con l&#39;autorizzazione **[!UICONTROL Gestisci etichette di utilizzo]**.

Per poter [assegnare etichette](#assign-labels), devi far parte di un ruolo con autorizzazione **Gestisci**, ovvero [!DNL Manage journeys], [!DNL Manage Campaigns] o [!DNL Manage decisions]. Senza questa autorizzazione, il pulsante **[!UICONTROL Gestisci accesso]** è disattivato.

Ulteriori informazioni sulle autorizzazioni sono disponibili in [questa sezione](../administration/permissions.md).

## Create labels (Creare etichette) {#create-labels}

**[!UICONTROL Etichette]** ti consentono di categorizzare set di dati e campi in base ai criteri di utilizzo applicabili a tali dati. **[!UICONTROL Le etichette]** possono essere applicate in qualsiasi momento, offrendo flessibilità nella scelta di gestire i dati.

Utilizza le etichette per fornire accesso agli utenti e applicare la governance dei dati e i criteri di consenso. Queste etichette di governance possono influire sul consumo a valle.

È possibile creare etichette nel prodotto [!DNL Permissions]. Per ulteriori informazioni, consulta [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html?lang=it){target="_blank"}.

Puoi anche creare **[!UICONTROL etichette]** direttamente in Journey Optimizer. Per creare un’etichetta, effettua le seguenti operazioni:

1. Da un oggetto Adobe Journey Optimizer, qui una **[!UICONTROL Campaign]** appena creata, fai clic sul pulsante **[!UICONTROL Gestisci accesso]**.

   ![](assets/olac_1.png)

1. Dalla finestra **[!UICONTROL Gestisci accesso]**, fai clic su **[!UICONTROL Crea etichetta]**.

   ![](assets/olac_2.png)

1. Configurare l’etichetta, è necessario specificare:
   * **[!UICONTROL Nome]**
   * **[!UICONTROL Nome descrittivo]**
   * **[!UICONTROL Descrizione]**

   ![](assets/olac_3.png)

1. Fai clic su **[!UICONTROL Crea]** per salvare la **[!UICONTROL Etichetta]**.

La **[!UICONTROL etichetta]** appena creata è ora disponibile nell&#39;elenco. Se necessario, è possibile modificarlo nel prodotto [!DNL Permissions].

## Assegna etichette {#assign-labels}

Per assegnare etichette di utilizzo dei dati personalizzate o di base agli oggetti Journey Optimizer:

1. Da un oggetto Adobe Journey Optimizer, qui una **[!UICONTROL Campaign]** appena creata, fai clic sul pulsante **[!UICONTROL Gestisci accesso]**.

   ![](assets/olac_1.png)

1. Dalla finestra **[!UICONTROL Gestisci accesso]**, seleziona le etichette di utilizzo dei dati personalizzate o di base per gestire l&#39;accesso a questo oggetto.

   Per ulteriori informazioni sulle etichette di utilizzo dei dati di base, consulta [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=it){target="_blank"}.

   ![](assets/olac_4.png)

1. Fai clic su **[!UICONTROL Salva]** per applicare questa restrizione dell&#39;etichetta.

Per poter accedere a questo oggetto, gli utenti dovranno includere l&#39;**[!UICONTROL Etichetta]** specifica nei loro **[!UICONTROL Ruoli]**.
Ad esempio, un utente con l’etichetta C1 avrà accesso solo a oggetti con etichetta C1 o senza etichetta.

Per ulteriori informazioni su come assegnare **[!UICONTROL Label]** a un **[!UICONTROL Role]**, fare riferimento a [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=it#manage-labels-for-a-role){target="_blank"}.