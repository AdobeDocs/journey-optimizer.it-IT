---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione ai dati in [!DNL Journey Optimizer]
description: Scopri come utilizzare i dati in [!DNL Journey Optimizer]
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 25519acb-a017-446a-992b-653d3a8a3d96
source-git-commit: 504e93a5c21baadf6ac938a9298c1adeb2a2d878
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# Guida introduttiva alla gestione dei dati in [!DNL Journey Optimizer] {#about-data}

Ricchezza e copertura dei dati dei clienti finali è ciò che definisce la forza e il successo di qualsiasi soluzione di customer experience; e questi dati sono sacri e del valore più alto per qualsiasi cliente. La selezione della tecnologia è ora intrinsecamente integrata con una valutazione rigorosa delle funzionalità di gestione dei dati.

Con [!DNL Adobe Journey Optimizer], puoi gestire, conservare ed esportare facilmente questi dati in piattaforme o sistemi che fanno parte dello stack di tecnologia.

**Dati personali, regole personali** - [!DNL Adobe Journey Optimizer] crea continuamente (e in tempo reale) un set completo di dati di profilo del cliente, oltre a tutti i dati di percorso e di offerta inerenti alle sue operazioni. Le versioni semplici dei dati utente acquisiti dai database vengono arricchiti e trasformati in dati di alto valore con copertura e profondità. Si desidera che questi dati siano sicuri, e allo stesso tempo onnipresenti, in modo da sfruttare il loro valore nell&#39;intero ecosistema IT.

In generale, la flessibilità desiderata dai dati è:


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <div><img alt="destinazioni" src="assets/do-not-localize/dest.png" /> 
    <br>Disponibile in altre destinazioni - Mentre [!DNL Adobe Journey Optimizer] sinergizza e integra i dati per un’esperienza cliente iper-personalizzata; desideri che questi dati siano presenti in altri sistemi nel tuo panorama tecnologico complessivo, mentre ti avvicini ad altri modi per sfruttare questi dati.
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
    <br>Base eliminata e tempistica concordata per la tua politica: l’eliminazione dei dati è un aspetto critico della protezione dei dati ed è un passaggio fondamentale in tutti i processi di governance dei dati. [!DNL Adobe Journey Optimizer] può produrre più dati del necessario. Inoltre, si desidera prendersi la massima cura di ciò che accade dopo la durata richiesta per un set di dati - che sia a causa di utilità o regolamentazione. Il controllo necessario consiste nell’eliminare i dati in qualsiasi momento. <a href="https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html">Ulteriori informazioni sull’igiene dei dati nella documentazione di Adobe Experience Platform</a></div>
  </td>
</tr>
</table>

[!DNL Adobe Experience Platform], che [!DNL Adobe Journey Optimizer] è generato, fornisce i più alti livelli di controllo dei dati per te - durante il coinvolgimento e anche alla fine del coinvolgimento. Within [!DNL Journey Optimizer], hai il pieno controllo sui dati (che vengono inseriti o generati da, [!DNL Journey Optimizer]), la governance dei dati e le destinazioni a cui tali dati vengono inviati.

Tutti i dati sono considerati proprietà dei clienti e possono essere conservati, cifrati, distribuiti o distrutti solo su tua richiesta. L&#39;Adobe agisce come tuo fiduciario, senza alcun diritto ai tuoi dati.

È possibile utilizzare [!DNL Journey Optimizer]Flessibilità dei dati per soddisfare i requisiti specifici relativi a conservazione, archiviazione o eliminazione dei dati:

* **Estrazione/Esportazione dati**: Puoi avviare l’estrazione dei dati sorgente in qualsiasi momento tramite l’API di accesso ai dati senza penali o ritardi nel tempo. La [API di accesso ai dati](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html){target=&quot;_blank&quot;} fornisce agli utenti un&#39;interfaccia RESTful incentrata sulla rivelabilità e l&#39;accessibilità dei set di dati acquisiti all&#39;interno di [!DNL Adobe Experience Platform]. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   Tieni presente che il contenuto utilizzato in percorsi o campagne non può essere estratto tramite i metodi API o Destinazione di cui sopra.

<!--
* **Profile Service Data Retention**: For Behavioral and Time series data appended to any Profile, you may choose to use Journey Optimizer’s default setting of retaining this data for up to 30 days from the date of its addition to a Profile, or until an alternative time-period selected by the you. The time that Adobe keeps this data varies from contract to contract, and is outlined in an organization’s data retention policy.

  Learn more about Experience Event expirations in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/event-expirations.html){target="_blank"}.
-->

* **Purgoni e meccanismi di archiviazione**: La pulizia dei dati e dell&#39;archivio può essere liberamente definita e automatizzata in [!DNL Adobe Journey Optimizer] per automatizzare i criteri di conservazione dei dati. È possibile definire strategie di invecchiamento diverse per le diverse entità di dati. È inoltre possibile definire meccanismi di esportazione per esportare automaticamente i dati obsoleti prima che vengano eliminati o archiviati.

   L’area di lavoro Igiene dati nell’interfaccia utente di Adobe Experience Platform consente di creare e monitorare varie attività di igiene dei dati, tra cui l’eliminazione delle identità dei consumatori e la pianificazione delle scadenze dei set di dati. Questa area di lavoro è disponibile con lo scudo per la sicurezza e la privacy e con lo scudo sanitario. Ulteriori informazioni in [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/hygiene/ui/overview.html){target=&quot;_blank&quot;}.

<!--
* **Data Lake and Deletions**: Customer Data stored in the Data Lake can be retained by Journey Optimizer:
    
    * for 7 days to facilitate the onboarding of Customer Data into the Profile Services, after which it may be permanently deleted, or
    * until chosen to be deleted by you

-->

* **Estrazione dati alla cessazione/uscita del coinvolgimento**: Quando il contratto viene terminato, i dati vengono completamente rimossi dallo spazio di archiviazione di Adobe. Inoltre, puoi estrarre estratti completi del profilo prima di terminare un contratto. Questa funzione non comporta costi aggiuntivi. Questo può essere fatto in qualsiasi momento e non solo al termine.

I metodi di cui sopra sono definiti contrattualmente e descritti in dettaglio nell’accordo di elaborazione dei dati (DPA) che l’Adobe concorda con te all’inizio di un impegno. applicazioni di Adobe, tra cui [!DNL Journey Optimizer], sono basati sul principio che i dati di ciascun cliente devono essere trattati come risorsa di dati proprietaria del cliente.
