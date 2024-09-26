---
solution: Journey Optimizer
product: journey optimizer
title: Publish il percorso
description: Scopri come creare rapporti sul tuo percorso
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: pubblicazione, percorso, live, validità, verifica
source-git-commit: 59a597a563074fa4daa74c64e97f6bb5c0f6834d
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---

# Rapporto live nell’area di lavoro del percorso {#report-journey}

>[!NOTE]
>
>Se non riesci a visualizzare i dati nel report percorsi Live, devi estendere i tuoi diritti di accesso per includere l&#39;autorizzazione per il report **[!UICONTROL Visualizza percorsi]**. [Ulteriori informazioni](../administration/permissions.md)

Dopo la pubblicazione del percorso, **Live Reporting** fornisce le metriche delle ultime 24 ore, direttamente nell&#39;area di lavoro del percorso.

Gli eventi visualizzati si sono verificati nelle ultime 24 ore, con un intervallo minimo di due minuti tra l’evento e la visualizzazione, in genere entro cinque minuti.

![](assets/journey_live_report.png)

Per il tuo percorso live, puoi accedere a:

* **[!UICONTROL Profili immessi]**: numero totale di singoli utenti che sono entrati in questa attività.
* **[!UICONTROL Chiuso con profilo]**: numero totale di persone che sono uscite dal percorso da tale attività, a causa di un criterio di uscita.
* **[!UICONTROL Profili in errore]**: numero totale di persone che hanno riscontrato un errore durante il percorso.
* **[!UICONTROL Profili scartati]**: numero totale di singoli utenti scartati dal percorso per uno dei motivi seguenti:

   * Per le attività **Qualificazione del pubblico**, può verificarsi un&#39;eliminazione se il verbo previsto per la qualifica del pubblico non corrisponde a quello ricevuto dal percorso (ad esempio, &quot;exited&quot; invece di &quot;realized&quot;).
   * Per **percorsi attivati da evento**, può verificarsi un&#39;eliminazione se l&#39;utente ha tentato di rientrare nel percorso troppo presto o quando non è stato consentito il rientro.
   * Nei **percorsi ricorrenti**, viene conteggiato un rifiuto per ogni ricorrenza se l&#39;individuo è già nel percorso e i criteri di rientro non sono impostati su &quot;forzare il rientro&quot;.
   * Nelle attività **Read Audience**, si verifica un&#39;eliminazione se non è impostata alcuna identità per l&#39;individuo esportato o se lo spazio dei nomi dell&#39;identità ricevuta non corrisponde a quello previsto per il percorso.

Per ogni attività all’interno di ogni percorso live, puoi accedere a:

* **[!UICONTROL Profili immessi]**: numero totale di singoli utenti che sono entrati in questa attività.
* **[!UICONTROL Profilo di uscita]**: numero totale di persone che sono uscite dal percorso da tale attività, a causa di un criterio di uscita.
* **[!UICONTROL Errore]**: numero totale di persone che hanno avuto un errore in quell&#39;attività.
