---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alla gestione dei dati in Journey Optimizer
description: Scopri come utilizzare i dati in Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: dati, gestione, piattaforma
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 96%

---

# Introduzione alla gestione dei dati {#about-data}

Dalla ricchezza e la copertura dei dati dei clienti finali dipende la potenza e il successo di qualsiasi soluzione di customer experience; e questi dati sono sacri e di grande valore per ogni cliente! La scelta della tecnologia è ora incorporata con una valutazione rigorosa delle funzionalità per la gestione dei dati.

Con [!DNL Adobe Journey Optimizer] puoi gestire, conservare ed esportare facilmente questi dati in piattaforme o sistemi che fanno parte del tuo stack tecnologico.

**I miei dati, le mie regole**: [!DNL Adobe Journey Optimizer] crea in modo continuo (e in tempo reale) un set completo di dati di profilo cliente, oltre a tutti i dati dei percorsi e delle offerte specifici per le tue attività. Le versioni preliminari dei dati utente acquisiti dai tuoi database vengono arricchite e trasformate in dati approfonditi e di alto valore. Questi dati dovranno essere al sicuro, ma allo stesso disponibili ovunque ti servano in modo da poterne sfruttare il valore nel tuo intero ecosistema IT.

In generale, questi dati dovranno essere abbastanza flessibili da rispondere a queste esigenze:


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="destinazioni" src="assets/do-not-localize/dest.png" /> 
   <br>Disponibilità in altre destinazioni: mentre [!DNL Adobe Journey Optimizer] assicura sinergia e integrazione dei dati per un’esperienza del cliente iper-personalizzata, i dati stessi dovranno essere disponibili anche in altri sistemi del tuo panorama tecnologico complessivo, per consentirti di sfruttarli anche altri modi.
    <div>
     <a href="../integrations/ajo-integrations.md">Ulteriori informazioni</a></div>
    </div>
    <br>
  </td>
</tr>
</table>

<!--td>
    <div><img alt="retention" src="assets/do-not-localize/retention.png" />  
    <br>Retained for a stipulated duration – Industry or regional regulations (such as GDPR or CCPA) or internal data governance policies stipulate how long or how short a duration, data needs to be maintained or archived in Adobe Experience Platform Data Lake. <a href="../privacy/get-started-privacy.md">Learn more</a></div>
  </td>
</tr>
<tr style="border: 0;"-->
<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="policy" src="assets/do-not-localize/policy.png" /> 
    <br>Eliminati in base a una timeline concordata o alla tua policy: l’eliminazione dei dati è un aspetto critico della protezione degli stessi ed è un passaggio chiave in tutti i processi di governance. [!DNL Adobe Journey Optimizer] potrebbe produrre più dati del necessario. Inoltre, vorrai poter controllare ciò che accade ai dati alla scadenza della durata richiesta per un set di dati, che sia per ragioni pratiche o per conformità a specifiche regolamentazioni. È importante essere in grado di eliminare i dati in un determinato momento. 
    </div>
      <div>
     <a href="../privacy/data-hygiene.md">Ulteriori informazioni</a></div>
    </div>
  </td>
</tr>
</table>

[!DNL Adobe Experience Platform], su cui [!DNL Adobe Journey Optimizer] è stato progettato, offre i massimi livelli di controllo dei dati, sia durante che dopo il coinvolgimento del cleinte. [!DNL Journey Optimizer] ti offre il pieno controllo sui dati (che vengono inseriti in o generati da [!DNL Journey Optimizer]), sulle funzionalità di governance da applicare a tali dati e sulle destinazioni a cui tali dati vengono inviati.

Tutti i dati sono considerati di proprietà dei clienti e possono essere mantenuti, crittografati, distribuiti o distrutti solo su richiesta dell’utente. Adobe agisce come tuo fiduciario, senza alcun diritto sui tuoi dati.

Puoi utilizzare la flessibilità dei dati offerta da [!DNL Journey Optimizer] per soddisfare i tuoi requisiti specifici relativi alla conservazione, all’archiviazione o all’eliminazione dei dati:

* **Estrazione/Esportazione dati**: puoi avviare l’estrazione dei dati di origine in qualsiasi momento tramite l’API di accesso ai dati senza penali né ritardi. L&#39;[API di accesso ai dati](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html?lang=it){target="_blank"} fornisce agli utenti un&#39;interfaccia RESTful incentrata sulla reperibilità e l&#39;accessibilità dei set di dati acquisiti all&#39;interno di [!DNL Adobe Experience Platform]. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

  I contenuti utilizzato nei percorsi o nelle campagne non possono essere estratti tramite i metodi API o di destinazione menzionati in precedenza.

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer's default setting of retaining this data for up to 91 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization's data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **Rimozione e meccanismi di archiviazione**: la rimozione dei dati e l’archiviazione possono essere definite e automatizzate liberamente in [!DNL Adobe Journey Optimizer] in modo da automatizzare i criteri di conservazione dei dati. È possibile definire diverse strategie di durata per le diverse entità di dati. È inoltre possibile definire meccanismi di esportazione per esportare automaticamente i dati obsoleti prima che vengano eliminati o archiviati.

  L’area di lavoro Ciclo di vita dei dati consente di creare e monitorare varie attività relative al ciclo di vita dei dati, tra cui l’eliminazione delle identità dei consumatori e la pianificazione delle scadenze dei set di dati. Questa area di lavoro è disponibile con Security &amp; Privacy Shield e Healthcare Shield. Ulteriori informazioni sono disponibili in [questa pagina](../privacy/data-hygiene.md).

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **Estrazione dati alla chiusura/uscita del coinvolgimento**: quando il contratto viene terminato, i dati vengono completamente rimossi dallo spazio di archiviazione di Adobe. Inoltre, è possibile richiamare estratti di profilo completi prima di rescindere un accordo. Questa funzione non è soggetta a costi aggiuntivi. Tale operazione può essere eseguita in qualsiasi momento, e non solo al momento della cessazione.

I metodi di cui sopra sono definiti contrattualmente e descritti in dettaglio nell’accordo sull’elaborazione dei dati (DPA, data processing agreement) che Adobe concorda con te all’inizio di un coinvolgimento. Le applicazioni Adobe, compreso [!DNL Journey Optimizer], sono progettate in base al principio che i dati di ciascun cliente devono essere trattati come risorsa di dati di proprietà di quel cliente.
