---
solution: Journey Optimizer
product: journey optimizer
title: Pubblicare il percorso
description: Scopri come creare rapporti sul tuo percorso
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: pubblicazione, percorso, live, validità, verifica
exl-id: 186b061d-0941-48be-8917-bbdfff6dae90
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/pclOxVDnQikU-2nLYMJ8mqEog9QL4WZBC7-NbvhuzIg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44feid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 566
ht-degree: 1%

---

# Rapporto live nell’area di lavoro del percorso {#report-journey}

Dopo la pubblicazione del percorso, all&#39;attivazione della [modalità di esecuzione di prova](journey-dry-run.md), **Live Reporting** fornisce le metriche delle ultime 24 ore direttamente nell&#39;area di lavoro del percorso.


>[!AVAILABILITY]
>
>Se non riesci a visualizzare i dati nel report percorsi Live, devi estendere i tuoi diritti di accesso per includere l&#39;autorizzazione per il report **[!UICONTROL Visualizza percorsi]**. [Ulteriori informazioni](../administration/permissions.md)


Gli eventi visualizzati si sono verificati nelle ultime 24 ore, con un intervallo minimo di due minuti tra l’evento e la visualizzazione, in genere entro cinque minuti.

![Dashboard dei report live dei Percorsi con metriche delle prestazioni in tempo reale](assets/journey_live_report.png)

Per i percorsi in modalità Live o [Dry run](journey-dry-run.md), puoi controllare:

* **[!UICONTROL Profili immessi]**: numero totale di persone che sono entrate nel percorso.
* **[!UICONTROL Profili usciti]**: numero totale di persone che sono uscite dal percorso (compresi gli errori).
* **[!UICONTROL Profili in errore]**: numero totale di persone che hanno riscontrato un errore durante il percorso.
* **[!UICONTROL Profili scartati]**: numero totale di singoli utenti scartati dal percorso per uno dei motivi seguenti:

   * Per le attività **Qualificazione del pubblico**, può verificarsi un&#39;eliminazione se il verbo previsto per la qualifica del pubblico non corrisponde a quello ricevuto dal percorso (ad esempio, &quot;exited&quot; invece di &quot;realized&quot;).
   * Per **percorsi attivati da evento**, può verificarsi un&#39;eliminazione se l&#39;utente ha tentato di rientrare nel percorso troppo presto o quando non è stato consentito il rientro.
   * Nei **percorsi ricorrenti**, viene conteggiato un rifiuto per ogni ricorrenza se l&#39;individuo è già nel percorso e i criteri di rientro non sono impostati su &quot;forzare il rientro&quot;.
   * Nelle attività **Read Audience**, si verifica un&#39;eliminazione se non è impostata alcuna identità per l&#39;individuo esportato o se lo spazio dei nomi dell&#39;identità ricevuta non corrisponde a quello previsto per il percorso.

Per ogni attività di ogni percorso in modalità Live o [Dry run mode](journey-dry-run.md), puoi accedere a:

* **[!UICONTROL Immesso]**: numero totale di singoli utenti che hanno iniziato questa attività. Per le attività **Action**, poiché non vengono eseguite in modalità di esecuzione a secco, questa metrica indica i profili che passano.
* **[!UICONTROL Uscita (ha soddisfatto i criteri di uscita)]**: numero totale di persone che sono uscite dal percorso da tale attività, a causa di un criterio di uscita (inclusi errori).
* **[!UICONTROL Uscita (uscita forzata)]**: numero totale di individui che sono usciti dal percorso mentre era in pausa a causa di una configurazione di percorso da parte di un operatore. Questa metrica è sempre uguale a zero per i percorsi in modalità di esecuzione a secco.
* **[!UICONTROL Errore]**: numero totale di persone che hanno avuto un errore in quell&#39;attività.

## Risoluzione dei problemi relativi a dati di reporting mancanti {#troubleshooting-missing-data}

Se i rapporti sul percorso non contengono i dati previsti, considera quanto segue:

* **Sincronizzazione nome Percorso**: verificare che il nome del percorso in [!DNL Adobe Journey Optimizer] corrisponda al nome archiviato nel set di dati di reporting. Una mancata corrispondenza tra questi nomi può impedire la corretta visualizzazione dei dati di reporting.

* **Intervallo di aggiornamento dati**: dopo aver aggiornato il nome o la configurazione di un percorso, attendere che i dati vengano aggiornati. I dati di reporting vengono generalmente visualizzati entro pochi minuti, ma in alcuni casi possono richiedere più tempo.

* **Autorizzazioni di accesso**: assicurati di disporre delle autorizzazioni necessarie per visualizzare i rapporti sul percorso. Se non trovi dati, verifica con l&#39;amministratore che sia abilitata l&#39;autorizzazione per il rapporto **[!UICONTROL Visualizza percorsi]**. [Ulteriori informazioni sulle autorizzazioni](../administration/permissions.md)

* **Stato Percorso**: i dati di reporting sono disponibili solo per percorsi o percorsi pubblicati in esecuzione in [Modalità di esecuzione di prova](journey-dry-run.md). Le bozze di percorsi non generano dati di reporting.

Se i problemi persistono dopo aver verificato questi elementi, contatta l&#39;amministratore di Adobe o il [supporto Adobe](../start/user-interface.md#support-ticket-guidelines) per assistenza.

>[!MORELIKETHIS]
>
>* [Introduzione al reporting](../reports/gs-reports.md)
>* [Pubblica il tuo percorso](publish-journey.md)
>* [Percorso di prova](journey-dry-run.md)
>* [Configurare e tenere traccia delle metriche di percorso](success-metrics.md)
>* [Rapporti percorso personalizzati](../reports/sharing-overview.md)
