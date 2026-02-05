---
solution: Journey Optimizer
product: journey optimizer
title: Dashboard utilizzo licenze
description: Scopri la dashboard Utilizzo licenze Journey Optimizer
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 7e91face-c8f4-4e70-9123-9e36bae7e67e
source-git-commit: db1e4ee5b2b4bb3a3d7d9e86aded14ad3c613765
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 1%

---

# Dashboard utilizzo licenze {#license-usage}

L&#39;[!DNL Adobe Journey Optimizer] [interfaccia utente](../start/user-interface.md) fornisce un dashboard che visualizza informazioni importanti sull&#39;utilizzo delle licenze dell&#39;organizzazione, acquisite durante uno snapshot giornaliero.

Per accedere a questo dashboard, vai a **[!UICONTROL Amministrazione]** > **[!UICONTROL Utilizzo licenze]**. Verrà aperta la scheda **[!UICONTROL Panoramica]** in cui viene visualizzato il dashboard.

![Panoramica dashboard utilizzo licenze](assets/license-usage-dashboard.png)

>[!NOTE]
>
>* Per visualizzare il dashboard, è necessario disporre dell&#39;autorizzazione [Visualizza dashboard utilizzo licenze](https://experienceleague.adobe.com/docs/experience-platform/dashboards/permissions.html#available-permissions){target="_blank"}.
>
>* Alcune metriche (ad esempio, ore di calcolo, e-mail) non vengono visualizzate per le sandbox di sviluppo, come indicato da `N/A` nella colonna delle quote. Nel dashboard vengono visualizzati solo i valori non nulli: quando le metriche sono pari a zero o vicine a zero, non vengono popolate.


Per [!DNL Adobe Journey Optimizer], il dashboard consente di controllare il numero di **profili coinvolgibili**.

## Che cos’è un profilo Engageable? {#what-is-engageable-profile}

Un **profilo coinvolgibile** è un record di informazioni che rappresenta un individuo memorizzato nel servizio profili e che è stato coinvolto da percorsi o campagne.

Caratteristiche principali dei profili coinvolgibili:

* **Intervallo continuo di 12 mesi**: i profili coinvolgibili vengono conteggiati in base al coinvolgimento negli ultimi 12 mesi. Questa metrica mostra il numero di profili univoci con cui hai tentato di interagire utilizzando le funzionalità di authoring, decisioning, consegna, sperimentazione o orchestrazione di Journey Optimizer.

* **Conteggio univoco per sandbox**: se un profilo accede a più percorsi o campagne all&#39;interno di una sandbox, viene conteggiato una sola volta come singolo profilo Engageable per tale sandbox.

* **In base al pubblico indirizzabile**: i profili indirizzabili sono calcolati in base al pubblico indirizzabile. Il conteggio rappresenta il pubblico coinvolto negli ultimi 12 mesi utilizzando una qualsiasi delle funzionalità di Journey Optimizer, rispetto al totale del pubblico indirizzabile.

* **Comportamento della metrica**: conteggio dei profili associabili:
   * Può aumentare quando vengono coinvolti nuovi profili tramite percorsi o campagne
   * Non può diminuire a meno che non ci sia nessun coinvolgimento con alcuni profili per oltre 12 mesi
   * Può diminuire quando i profili pseudonimi sono uniti a profili noti

>[!NOTE]
>
>Se osservi un picco improvviso nel conteggio dei profili coinvolgibili, consulta la [sezione Risoluzione dei problemi](#troubleshooting-engageable-profiles) di seguito per indicazioni dettagliate su come comprendere e risolvere il problema.

## Risoluzione dei problemi: aumento significativo del numero di profili coinvolgibili {#troubleshooting-engageable-profiles}

Se si osserva un picco improvviso nel conteggio dei profili coinvolgibili (ad esempio, profili che passano da centinaia di migliaia a milioni in un giorno), questa sezione fornisce indicazioni per comprendere e risolvere il problema.

### Comprendere l’aumento

La metrica Profili coinvolgibili riflette il numero di profili univoci coinvolti da percorsi o campagne negli ultimi 12 mesi. Un aumento improvviso può derivare da:

* Pubblico di grandi dimensioni interessato da nuovi percorsi o campagne
* Modifiche nei set di dati abilitati per il servizio Profilo
* Elaborazione in batch di tipi di pubblico non utilizzati di recente

### Passaggi di risoluzione

Per risolvere questo problema, effettua le seguenti operazioni:

1. **Comprendere la logica di conteggio dei profili:**

   * I profili coinvolgibili vengono calcolati in base a profili univoci coinvolti da percorsi o campagne negli ultimi 12 mesi.
   * Se un profilo entra in più percorsi, viene conteggiato come un unico profilo Engageable per quella sandbox.
   * La metrica non può diminuire a meno che non ci sia nessun coinvolgimento con alcuni profili per oltre 12 mesi o se i profili pseudonimi sono uniti a quelli noti.
   * I profili coinvolgibili vengono calcolati utilizzando il pubblico indirizzabile di un cliente.
   * Il pubblico coinvolto negli ultimi 12 mesi utilizzando una qualsiasi delle funzionalità di Journey Optimizer, rispetto al pubblico indirizzabile totale, determina il conteggio dei profili coinvolgibili.

2. **Esaminare percorsi, campagne e decisioni destinati a tipi di pubblico di grandi dimensioni:**

   * Rivedi i percorsi e le campagne recenti che eseguono il targeting di un numero elevato di profili utilizzando [query di profili coinvolgibili](../reports/query-examples.md#engageable-profiles-queries) o [Query Service](https://experienceleague.adobe.com/en/docs/experience-platform/query/home){target="_blank"}.
   * Identifica specifiche versioni del percorso che hanno contribuito al picco nei conteggi dei profili.
   * È probabile che percorsi, campagne e decisioni che coinvolgono nuovi profili portino a un aumento del conteggio degli eventi nei set di dati dei Percorsi, contribuendo all’aumento del conteggio dei profili coinvolgibili.

3. **Filtra i tipi di pubblico a livello di percorso e di campagne:**

   * Applica i filtri a livello di pubblico prima di avviare percorsi o campagne per evitare inutili aumenti nei profili coinvolgibili.
   * Assicurati che solo i tipi di pubblico rilevanti siano oggetto di targeting durante gli impegni.

4. **Riduci dimensioni pubblico indirizzabile:**

   * Se necessario, elimina i profili pseudonimi. Tieni presente che questa azione interessa sia Journey Optimizer che Real-Time Customer Data Platform.
   * Ulteriori informazioni sulla [scadenza dei dati del profilo pseudonimo](https://experienceleague.adobe.com/it/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"} nella Guida del profilo cliente in tempo reale.
   * **Nota:** la scadenza dei dati del profilo pseudonimo non può essere configurata tramite l&#39;interfaccia utente o le API di Platform. Contatta l’assistenza per abilitare questa funzione.

5. **Monitora modifiche set di dati:**

   * Verifica che i set di dati siano abilitati per la profilatura e assicurati che non contengano ECID (Experience Cloud ID) eccessivi.
   * Se necessario, elimina i set di dati con conteggi ECID elevati e ricreali con record ridotti.

6. **Sviluppare una strategia di riduzione a lungo termine:**

   * Il conteggio dei profili utilizzabili diminuirà naturalmente se alcuni profili rimangono disattivati per più di 12 mesi.

**Vedere anche:**

* [Esempi di query per profili associabili](../reports/query-examples.md#engageable-profiles-queries) - Query di esempio per monitorare e analizzare i profili associabili
* [Panoramica di Adobe Experience Platform Query Service](https://experienceleague.adobe.com/en/docs/experience-platform/query/home){target="_blank"}

## Documentazione correlata {#related-documentation}

Per ulteriori informazioni, consulta la documentazione di Adobe Experience Platform:

* [Panoramica dashboard utilizzo licenze](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/license-usage.html){target="_blank"}
* [Esplorazione del dashboard utilizzo licenze](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/license-usage.html#exploring-the-license-usage-dashboard){target="_blank"}
* [Metriche disponibili](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/license-usage.html?lang=it#available-metrics){target="_blank"}
* [Scadenza dati profilo pseudonimo](https://experienceleague.adobe.com/docs/experience-platform/profile/pseudonymous-profiles.html?lang=it){target="_blank"}
