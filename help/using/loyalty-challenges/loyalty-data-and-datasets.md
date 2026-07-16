---
solution: Journey Optimizer
product: journey optimizer
title: Dati e set di dati sulla fedeltà
description: Scopri quali dati di profilo e set di dati di Adobe Experience Platform richiedono problematiche di fidelizzazione e come il time-to-live dei set di dati (TTL) influisce sulla conservazione.
feature: Journeys
topic: Content Management
role: Admin, Developer
level: Intermediate
hide: true
badge: label="Beta privata" type="Informative"
mini-toc-levels: 1
exl-id: a7c4e1b2-8f3d-4a6c-9e0b-1d2e3f4a5b6c
feature_v2: []
subfeature_v2: []
source-git-commit: 56b57f083d747726847c0a3e658cd4ff4921fc81
workflow-type: tm+mt
source-wordcount: 613
ht-degree: 8%

---

# Dati e set di dati sulla fedeltà {#loyalty-data-and-datasets}

>[!BEGINSHADEBOX]

**Sommario**

[Introduzione alle sfide di fedeltà](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**Crea e gestisci le sfide**

* [Accesso e gestione di sfide e attività](access-loyalty-challenges.md)
* [Creare le sfide](create-challenges.md)
* [Creare le attività](create-tasks.md)
* [Monitorare le prestazioni della sfida fedeltà](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**Configura e integra**

* [Configurare le sfide relative alla fedeltà](loyalty-admin.md)
* **Dati e set di dati fedeltà** ◀︎ **Sei qui**
* [Riferimento API per le sfide di fedeltà](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata**. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta [Ciclo di rilascio di Journey Optimizer](../rn/releases.md).

## Panoramica {#overview}

Le sfide relative alla fedeltà si basano su Adobe Experience Platform per identità, attributi di profilo, eventi di esperienza e tipi di pubblico. Utilizzare questa pagina per scoprire quali dati preparare, quali set di dati sono coinvolti e come **il time-to-live (TTL)** influisce sulla conservazione prima di creare le sfide o utilizzare le API delle sfide di fidelizzazione.

Contatta l&#39;amministratore di Adobe per la configurazione del programma Journey Optimizer oppure configura la mappatura di eventi e gratifiche nel menu **[!UICONTROL Amministratore fedeltà]**. [Scopri come configurare le sfide relative alla fedeltà](loyalty-admin.md). Per gli endpoint REST e l&#39;autenticazione, consulta il riferimento API [Sfide fedeltà](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}.

## Connettori fedeltà tramite origini {#loyalty-connectors-sources}

Se i tuoi dati fedeltà vengono gestiti in una piattaforma di premi esterna, puoi acquisire tali dati in Adobe Experience Platform utilizzando i connettori **Sorgenti**, quindi utilizzarli in Sfide di fedeltà.

I connettori per fidelizzazione e premi elencati nella documentazione di Journey Optimizer includono:

* **Talon.One**
* **Capillare**
* **Kobie**

Per l&#39;onboarding del connettore e la configurazione end-to-end, consulta [Introduzione ai connettori di origine](../start/get-started-sources.md) e il [catalogo origini di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=it#sources-catalog){target="_blank"}.

## Dati Adobe Experience Platform {#aep-data}

### Attributi del profilo {#profile-attributes}

I tipi di pubblico, la personalizzazione e il reporting della sfida utilizzano i profili nella classe **[!DNL XDM Individual Profile]**. Allinea l&#39;identità [spazio dei nomi](https://experienceleague.adobe.com/it/docs/experience-platform/identity/features/namespaces){target="_blank"} utilizzata per le sfide di fedeltà con il modo in cui i membri vengono identificati nei dati del profilo e con lo spazio dei nomi selezionato nelle **[!UICONTROL Impostazioni globali]** nel menu **[!UICONTROL Amministratore fedeltà]**.

Per gli attributi di fedeltà standard nel profilo (punti, livello, programma, stato e campi correlati), utilizza il gruppo di campi dello schema **[Dettagli fedeltà](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/profile/loyalty-details){target="_blank"}** di Experience Platform. Questo gruppo di campi definisce l&#39;oggetto `loyalty` e le relative proprietà (ad esempio `points`, `tier`, `program` e `status`).

➡️ [Gruppo di campi schema Dettagli fedeltà](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/profile/loyalty-details){target="_blank"}

### Eventi esperienza {#experience-events}

Le attività **[!UICONTROL Purchase]**, **[!UICONTROL Spend]** e **[!UICONTROL Custom event]** dipendono dagli eventi esperienza acquisiti in Adobe Experience Platform. Per le attività **[!UICONTROL Custom event]**, le definizioni degli eventi corrispondenti (percorso identificatore, ID schema XDM facoltativo, schema e trasformatore) devono essere configurate nel menu **[!UICONTROL Loyalty admin]** prima che gli addetti al marketing possano immettere valori degli eventi personalizzati nel generatore di attività. [Scopri come configurare le definizioni degli eventi](loyalty-admin.md#event-definitions)

Assicurati che i payload dell’evento utilizzino lo stesso spazio dei nomi di identità della configurazione Sfide di fedeltà in modo che l’avanzamento possa essere attribuito al profilo corretto.

### Tipi di pubblico e reporting {#audiences-reporting}

Gli addetti al marketing selezionano i tipi di pubblico della piattaforma [1} durante la configurazione dell&#39;idoneità per la verifica. ](../audience/about-audiences.md)Le dashboard di reporting sulla fedeltà utilizzano Adobe Customer Journey Analytics. [Scopri come monitorare le prestazioni della sfida fedeltà](loyalty-reporting.md)

## Durata del set di dati (TTL) {#dataset-ttl}

Sfide di fedeltà memorizza i dati operativi e di reporting nei set di dati di Adobe Experience Platform (inclusi i set di dati relativi a eventi e personalizzazione creati per il programma). Il set di dati **TTL (time-to-live)** controlla per quanto tempo i dati vengono conservati nel data lake e, se applicabile, nell&#39;archivio profili.

Journey Optimizer applica i guardrail TTL a molti set di dati generati dal sistema. I set di dati relativi alla fedeltà seguono lo stesso modello di conservazione di Platform per la sandbox.

➡️ [Guardrail TTL (Time-to-live) dei set di dati in Journey Optimizer](../data/datasets-ttl.md)

>[!NOTE]
>
>La configurazione della fedeltà a livello di organizzazione può includere impostazioni di archiviazione e conservazione (ad esempio, durata dell’archivio) gestite tramite il servizio di metadati Fedeltà. Se hai la necessità di regolare la conservazione per l’ambiente beta privato, rivolgiti al tuo amministratore Adobe.
