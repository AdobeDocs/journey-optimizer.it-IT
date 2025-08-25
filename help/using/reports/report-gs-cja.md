---
solution: Journey Optimizer
product: journey optimizer
title: Esperienza di reporting aggiornata
description: Introduzione al rapporto tutte le ore
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: bfd88d2a-e7b8-4e3b-85a1-4a14b0ba56dc
source-git-commit: 15a73ba3f2d91a38d61e6518d704fc218ad0eea3
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 25%

---

# Introduzione al rapporto tutte le ore {#channel-report-gs-cja}

>[!CONTEXTUALHELP]
>id="cja_connections_enable_cja"
>title="Abilitare Customer Journey Analytics"
>abstract="Per analizzare questo rapporto in Customer Journey Analytics, contatta l’amministratore per assicurarti che la tua organizzazione abbia acquistato Customer Journey Analytics e che l’integrazione sia configurata correttamente."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/channels/email/design-email/add-content/content-components#add-content-components" text="Customer Journey Analytics"

La funzione di reporting di Journey Optimizer include una migliorata interoperabilità con le funzionalità di Customer Journey Analytics, per standardizzare il reporting su entrambe le piattaforme e migliorare la coerenza e l’affidabilità dei dati. Questa integrazione ottimizzata tra Journey Optimizer e Customer Journey Analytics consente una visione più chiara delle metriche delle prestazioni, in modo che gli utenti possano prendere decisioni più informate.

L’accesso a queste funzionalità di reporting dipende dal contesto e dalle aree di prodotto:

* **Percorsi** - Se desideri eseguire il targeting di uno o più percorsi nel contesto di un percorso, dal menu **[!UICONTROL Percorsi]**, accedi al tuo percorso e fai clic sul pulsante **[!UICONTROL Visualizza report]**.

  Dall&#39;elenco del percorso esistente, puoi anche selezionare **[!UICONTROL Report]** dal menu avanzato del percorso selezionato. [Ulteriori informazioni sul report Percorso](journey-global-report-cja.md)

  ![](assets/gs-cja-report-3.png)

* **Campagne** - Se desideri eseguire il targeting di una campagna, dal menu **[!UICONTROL Campagne]**, accedi alla campagna e fai clic sul pulsante **[!UICONTROL Rapporti]**, quindi **[!UICONTROL Visualizza tutti i rapporti temporali]**.

  Dall&#39;elenco delle campagne esistenti, puoi anche selezionare **[!UICONTROL Report]** dal menu avanzato della campagna selezionata. [Ulteriori informazioni sul report della campagna](campaign-global-report-cja.md)

  ![](assets/gs-cja-report-2.png)

* **Globale** - Se desideri eseguire il targeting delle metriche per tutte le campagne e i percorsi all&#39;interno del tuo ambiente, accedi al report **Panoramica** accedendo al menu **[!UICONTROL Report]** nella sezione **[!UICONTROL Gestione Percorsi]**. [Ulteriori informazioni sul rapporto Panoramica](channel-report-cja.md)

  ![](assets/gs-cja-report-1.png)

>[!IMPORTANT]
>
>La generazione di rapporti in Adobe Journey Optimizer è attualmente standardizzata in UTC. La possibilità di personalizzare il fuso orario per la generazione di rapporti verrà introdotta in una versione futura.

## Prerequisiti {#prerequisites}

* Se **non** possiedi Customer Journey Analytics o se ne sei il proprietario ma **non** hai accesso ad alcun profilo di prodotto Customer Journey Analytics, le autorizzazioni vengono gestite in Journey Optimizer. In questo caso, è necessario disporre dell&#39;autorizzazione **[!UICONTROL Visualizza report canale]** o dei ruoli correlati. [Ulteriori informazioni](../administration/permissions.md)

* Se **possiedi** Customer Journey Analytics e hai accesso a un profilo di prodotto Customer Journey Analytics, devi:

   * **[!UICONTROL Autorizzazioni per la creazione di tipi di pubblico]** e **[!UICONTROL Autorizzazioni per la visualizzazione del pubblico]** per Customer Journey Analytics. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/analytics-platform/using/technotes/access-control){target="_blank"}

   * **[!UICONTROL Gestione dei profili]** - Autorizzazione per Adobe Journey Optimizer. [Ulteriori informazioni](../administration/permissions.md)

* Le visualizzazioni dati di Customer Journey Analytics devono essere configurate con l&#39;impostazione seguente: **Imposta come visualizzazione dati predefinita in Adobe Journey Optimizer**. [Ulteriori informazioni sulle visualizzazioni dati](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}


## Video dimostrativo{#video}

Il video seguente mostra come utilizzare la funzionalità avanzata di reporting di Journey Optimizer con Customer Journey Analytics.

>[!VIDEO](https://video.tv.adobe.com/v/3443159?captions=ita)