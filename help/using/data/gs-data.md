---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione ai dati in [!DNL Journey Optimizer]
description: Scopri come utilizzare i dati in [!DNL Journey Optimizer]
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 34f6f25560cbe7873f8aea9edda3d63dab63935a
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Guida introduttiva alla gestione dei dati in [!DNL Journey Optimizer] {#about-data}

Ricchezza e copertura dei dati dei clienti finali è ciò che definisce la forza e il successo di qualsiasi soluzione di customer experience; e questi dati sono sacri e del valore più alto per qualsiasi cliente dato. La selezione della tecnologia è ora intrinsecamente integrata con una valutazione rigorosa delle funzionalità di gestione dei dati.

Con Adobe Journey Optimizer puoi gestire, conservare ed esportare facilmente questi dati in piattaforme o sistemi che fanno parte dello stack di tecnologia.

**Dati personali, regole personali** - Journey Optimizer crea continuamente (e in tempo reale) un set completo di dati di profilo del cliente, oltre a tutti i dati di percorso e di offerta inerenti alle sue operazioni. Le versioni semplici dei dati utente acquisiti dai database vengono arricchiti e trasformati in dati di alto valore con copertura e profondità. Si desidera che questi dati siano sicuri, e allo stesso tempo onnipresenti, in modo da sfruttare il loro valore nell&#39;intero ecosistema IT.

In generale, la flessibilità desiderata dai dati è triplicata:


<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <img alt="destinazioni" src="assets/do-not-localize/dest.png" />
    <br>
  </td>
  <td>
    <div>Disponibile in altre destinazioni - Journey Optimizer sinergizza e integra i dati per un’esperienza cliente iper-personalizzata, ma desideri che questi dati siano disponibili in altri sistemi nel tuo panorama tecnologico complessivo, cercando altri modi per sfruttare questi dati.
    <div>
     <a href="../start/ajo-integrations.md">Ulteriori informazioni</a></div>
    </div>
    <br>
  </td>
</tr>
<tr style="border: 0;">
  <td>
    <img alt="conservazione" src="assets/do-not-localize/retention.png" />
  </td>
  <td>
    <div>Mantenuti per una durata prestabilita: le normative di settore o regionali (come RGPD o CCPA) o le politiche interne di governance dei dati stabiliscono per quanto tempo o per quanto tempo i dati devono essere conservati o archiviati in Adobe Experience Platform Data Lake. <a href="../privacy/get-started-privacy.md">Ulteriori informazioni</a></div>
  </td>
</tr>
<tr style="border: 0;">
  <td>
    <img alt="policy" src="assets/do-not-localize/policy.png" />
    <br>
  </td>
  <td>
    <div>Base eliminata e tempistica concordata per la tua politica: l’eliminazione dei dati è un aspetto critico della protezione dei dati ed è un passaggio fondamentale in tutti i processi di governance dei dati. Journey Optimizer può produrre più dati del necessario. Inoltre, si desidera prendersi la massima cura di ciò che accade dopo la durata richiesta per un set di dati - che sia a causa di utilità o regolamentazione. Il controllo necessario consiste nell’eliminare i dati in qualsiasi momento.</div>
  </td>
</tr>
</table>

Adobe Experience Platform, su cui è basato Journey Optimizer, offre i massimi livelli di controllo dei dati durante il coinvolgimento e alla fine del coinvolgimento. All’interno di Journey Optimizer, hai il pieno controllo sui dati (che vengono inseriti o generati da Journey Optimizer), sulla governance dei dati e sulle destinazioni a cui vengono inviati i dati.

Tutti i dati sono considerati proprietà dei clienti e possono essere conservati, cifrati, distribuiti o distrutti solo su tua richiesta. L&#39;Adobe agisce come tuo fiduciario, senza alcun diritto ai tuoi dati.

Puoi utilizzare la flessibilità dei dati di Journey Optimizer per soddisfare i requisiti specifici relativi a conservazione, archiviazione o eliminazione dei dati:

* **Estrazione/Esportazione dati**: Puoi avviare l’estrazione dei dati sorgente in qualsiasi momento tramite l’API di accesso ai dati senza penali o ritardi nel tempo. La [API di accesso ai dati](https://experienceleague.adobe.com/docs/experience-platform/data-access/api.html) fornisce agli utenti un’interfaccia RESTful incentrata sulla scoperta e l’accessibilità dei set di dati acquisiti all’interno dell’Experience Platform. <!--In the future (on roadmap), you can use file-based destinations to export and migrate log data from Adobe Journey Optimizer. -->

   Tieni presente che il contenuto utilizzato in percorsi o campagne non può essere estratto tramite i metodi API o Destinazione di cui sopra.

* **Conservazione dei dati del servizio profili**: Per i dati delle serie Comportamento e Tempo aggiunti a qualsiasi profilo, puoi scegliere di utilizzare l’impostazione predefinita di Journey Optimizer per mantenere questi dati per un massimo di 30 giorni dalla data della sua aggiunta a un profilo o fino a un periodo di tempo alternativo selezionato dall’utente. Il momento in cui Adobe conserva questi dati varia da contratto a contratto ed è descritto nei criteri di conservazione dei dati di un&#39;organizzazione.

* **Purgoni e meccanismi di archiviazione**: L&#39;eliminazione dei dati e dell&#39;archiviazione può essere liberamente definita e automatizzata in Journey Optimizer per automatizzare i criteri di conservazione dei dati. È possibile definire strategie di invecchiamento diverse per le diverse entità di dati. È inoltre possibile definire meccanismi di esportazione per esportare automaticamente i dati obsoleti prima che vengano eliminati o archiviati.

* **Data Lake e eliminazioni**: I dati dei clienti memorizzati nel Data Lake possono essere conservati da Journey Optimizer:

   * per 7 giorni per facilitare l’onboarding dei dati dei clienti nei servizi profilo, dopo di che potrebbe essere definitivamente cancellato, o
   * fino a quando scelto per essere cancellato da te

* **Estrazione dati alla cessazione/uscita del coinvolgimento**: Quando il contratto viene terminato, i dati vengono rimossi completamente dallo spazio di archiviazione di Adobe. Inoltre, puoi estrarre estratti completi del profilo prima di terminare un contratto. Questa funzione non comporta costi aggiuntivi. Questo può essere fatto in qualsiasi momento e non solo al termine.

I metodi di cui sopra sono definiti contrattualmente e descritti in dettaglio nell’accordo di elaborazione dei dati (DPA) che l’Adobe concorda con te all’inizio di un impegno. Le applicazioni di Adobe, incluso Journey Optimizer, sono progettate in base al principio che i dati di ciascun cliente devono essere trattati come risorsa di dati proprietaria del cliente.
