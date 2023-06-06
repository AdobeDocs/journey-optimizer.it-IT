---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione ai dati in Journey Optimizer
description: Scopri come utilizzare i dati in Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: dati, gestione, piattaforma
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: ef34cb0207d3011eca6d76ad6568f3edc00e13a3
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 1%

---

# Introduzione alla gestione dei dati in [!DNL Journey Optimizer] {#about-data}

La ricchezza e la copertura dei dati dei clienti finali sono ciò che definisce la forza e il successo di qualsiasi soluzione di customer experience; e questi dati sono sacri e di massimo valore per qualsiasi cliente. La selezione della tecnologia è ora integrata con una valutazione rigorosa delle funzionalità di gestione dei dati.

Con [!DNL Adobe Journey Optimizer], è possibile gestire, conservare ed esportare facilmente questi dati in piattaforme o sistemi che fanno parte dello stack tecnologico.

**I miei dati, le mie regole** - [!DNL Adobe Journey Optimizer] crea in modo continuo (e in tempo reale) un set completo di dati del profilo cliente, oltre a tutti i dati del percorso e dell’offerta inerenti alle sue operazioni. Le versioni Strawman dei dati utente acquisiti dai database vengono arricchite e trasformate in dati di alto valore con copertura e profondità. Volete dati sicuri, e allo stesso tempo onnipresenti, in modo da poterne sfruttare il valore nel vostro ecosistema IT complessivo.

In generale, la flessibilità che desideri dai dati è:


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="destinazioni" src="assets/do-not-localize/dest.png" /> 
    <br>Disponibile in altre destinazioni - Mentre [!DNL Adobe Journey Optimizer] sinergizza e integra i dati per un’esperienza del cliente iper-personalizzata. Questi dati devono essere presenti in altri sistemi nel tuo panorama tecnologico complessivo e puoi cercare altri modi per sfruttarli.
    <div>
     <a href="../start/ajo-integrations.md">Ulteriori informazioni</a></div>
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
    <br>Eliminato in base a una tempistica concordata o alla tua policy: l’eliminazione dei dati è un aspetto critico della protezione dei dati ed è un passaggio chiave in tutti i processi di governance dei dati. [!DNL Adobe Journey Optimizer] può produrre più dati del necessario. Inoltre, desideri prestare la massima attenzione a ciò che accade dopo la durata richiesta per un set di dati, a causa di utilità o regolamentazione. Il controllo necessario, consiste nell’eliminare i dati in un determinato momento. 
    </div>
      <div>
     <a href="../privacy/data-hygiene.md">Ulteriori informazioni</a></div>
    </div>
  </td>
</tr>
</table>

[!DNL Adobe Experience Platform], su cui [!DNL Adobe Journey Optimizer] è stato progettato per fornire i massimi livelli di controllo dei dati, sia durante il progetto che alla fine dello stesso. Entro [!DNL Journey Optimizer], hai il pieno controllo sui dati (che vengono inseriti o generati da, [!DNL Journey Optimizer]), la governance applicata a tali dati e le destinazioni a cui tali dati vengono inviati.

Tutti i dati sono considerati di proprietà dei clienti e possono essere mantenuti, crittografati, distribuiti o distrutti solo su richiesta dell’utente. Adobe agisce come tuo fiduciario, senza alcun diritto sui tuoi dati.

È possibile utilizzare [!DNL Journey Optimizer]la flessibilità dei dati di per soddisfare i requisiti specifici relativi alla conservazione, all&#39;archiviazione o all&#39;eliminazione dei dati:

* **Estrazione/Esportazione dati**: puoi avviare l’estrazione dei dati sorgente in qualsiasi momento tramite l’API di accesso ai dati senza penali o ritardi. Il [API di accesso ai dati](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html){target="_blank"} fornisce agli utenti un’interfaccia RESTful incentrata sulla reperibilità e l’accessibilità dei set di dati acquisiti in [!DNL Adobe Experience Platform]. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   Nota che il contenuto utilizzato nei percorsi o nelle campagne non può essere estratto tramite i metodi API o di destinazione menzionati in precedenza.

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer’s default setting of retaining this data for up to 30 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization’s data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **Rimozione e meccanismi di archiviazione**: la rimozione dei dati e l&#39;archiviazione possono essere definite e automatizzate in modo libero [!DNL Adobe Journey Optimizer] per automatizzare le regole di conservazione dei dati. È possibile definire diverse strategie di aging per le diverse entità di dati. È inoltre possibile definire meccanismi di esportazione per esportare automaticamente i dati obsoleti prima che vengano eliminati o archiviati.

   L’area di lavoro Igiene dei dati consente di creare e monitorare varie attività di igiene dei dati, tra cui l’eliminazione delle identità dei consumatori e la pianificazione delle scadenze dei set di dati. Questa area di lavoro è disponibile con lo scudo per la sicurezza e la privacy e con lo scudo sanitario. Per ulteriori informazioni, consulta [questa pagina](../privacy/data-hygiene.md).

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **Estrazione dati alla chiusura/uscita del coinvolgimento**: quando il contratto viene terminato, i dati vengono completamente rimossi dallo spazio di archiviazione di Adobe. Inoltre, è possibile estrarre estratti di profilo completi prima di rescindere un accordo. Questa funzione non comporta costi aggiuntivi. Questa operazione può essere eseguita in qualsiasi momento e non solo al momento della cessazione.

I metodi di cui sopra sono definiti contrattualmente e descritti in dettaglio nell’accordo sull’elaborazione dei dati (DPA) che Adobe concorda con te all’inizio di un impegno. applicazioni Adobi, tra cui [!DNL Journey Optimizer], sono progettati in base al principio che i dati di ciascun cliente devono essere trattati come risorsa di dati proprietaria di quel cliente.
