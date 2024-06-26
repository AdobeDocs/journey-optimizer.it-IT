---
solution: Journey Optimizer
product: journey optimizer
title: Aggiornare il profilo
description: Scopri come utilizzare l’attività Aggiorna profilo in un percorso
feature: Journeys, Profiles, Activities
topic: Content Management
role: User
level: Intermediate
keywords: profilo, aggiornamento, percorso, attività
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 6%

---

# Aggiornare il profilo {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="Attività Aggiorna profilo"
>abstract="L’attività Aggiorna profilo consente di aggiornare un profilo Adobe Experience Platform esistente con un valore specifico oppure con informazioni provenienti dall’evento o da un’origine dati."

Utilizza il **[!UICONTROL Aggiorna profilo]** attività di azione per aggiornare un profilo Adobe Experience Platform esistente con informazioni provenienti da un evento, un’origine dati o un valore specifico.

## Raccomandazioni

* Il **Aggiorna profilo** può essere utilizzato solo in percorsi che hanno uno spazio dei nomi.
* L’azione aggiorna solo i campi esistenti, non crea nuovi campi profilo.
* Non è possibile utilizzare **Aggiorna profilo** azione per generare eventi di esperienza, ad esempio un acquisto.
* Proprio come qualsiasi altra azione, puoi definire un percorso alternativo in caso di errore o timeout e non puoi inserire due azioni in parallelo.
* La richiesta di aggiornamento inviata a Adobe Experience Platform è immediata/entro un secondo. Ci vorrà normalmente qualche secondo, ma a volte di più senza alcuna garanzia. Di conseguenza, ad esempio, se un’azione utilizza il &quot;campo 1&quot; aggiornato da un **Aggiorna profilo** azione posizionata immediatamente prima, non ti aspetti che &quot;campo 1&quot; venga aggiornato nell’azione.
* Il **Aggiorna profilo** L’attività non supporta i campi XDM definiti come enumerazione.
* Il **[!UICONTROL Aggiorna profilo]** l’attività aggiorna solo il [Archivio profili](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html#profile-data-store){target="_blank"}, non il Data Lake.
* Quando selezioni un set di dati in **[!UICONTROL Aggiorna profilo]** attività, si consiglia di utilizzare un’attività non interessata dai flussi di acquisizione dei dati. Perché **Aggiorna profilo** Gli aggiornamenti vengono memorizzati solo in [Archivio profili](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html#profile-data-store){target="_blank"}, esiste il rischio di sovrascrivere tali modifiche con un flusso di acquisizione dati.

  Inoltre, il **Aggiorna profilo** la configurazione dell’attività non richiede uno spazio dei nomi delle identità. Di conseguenza, assicurati che il set di dati selezionato utilizzi lo stesso spazio dei nomi Identity utilizzato dall’azione che ha avviato il percorso, in quanto questo spazio dei nomi verrà utilizzato da questi aggiornamenti. La mappa delle identità può essere utilizzata anche dal set di dati selezionato. Se non si seleziona un set di dati con lo spazio dei nomi corretto o uno che utilizza la mappa di identità, si verifica la **Aggiorna profilo** l&#39;attività non superata.



## Utilizzo dell’aggiornamento del profilo

1. Progetta il percorso iniziando con un evento. Consulta questa [sezione](../building-journeys/journey.md).

1. In **Azione** nella palette, rilascia la sezione **Aggiorna profilo** attività nell’area di lavoro.

   ![](assets/profileupdate0.png)

1. Seleziona uno schema dall’elenco.

1. Fai clic su **Campo** per selezionare il campo da aggiornare. È possibile selezionare un solo campo.

   ![](assets/profileupdate2.png)

1. Seleziona un set di dati dall’elenco.

   >[!NOTE]
   >
   >Il **Aggiorna profilo** azione aggiorna i dati del profilo in tempo reale, ma non i set di dati. La selezione del set di dati è necessaria in quanto il profilo è un record correlato a un set di dati.

1. Fai clic sul pulsante **Valore** per definire il valore da utilizzare:

   * Utilizzando l’editor di espressioni semplici, puoi selezionare un campo da un’origine dati o dall’evento in ingresso.

     ![](assets/profileupdate4.png)

   * Se desideri definire un valore specifico o sfruttare funzioni avanzate, fai clic su **Modalità avanzata**.

     ![](assets/profileupdate3.png)

Il **Aggiorna profilo** è ora configurato.

![](assets/profileupdate1.png)


## Utilizzo della modalità di test {#using-the-test-mode}

In modalità di test, l’aggiornamento del profilo non verrà simulato. L’aggiornamento verrà eseguito sul profilo di test.

Solo i profili di test possono entrare in un percorso in modalità di test. È possibile creare un nuovo profilo di test o trasformare un profilo esistente in un profilo di test. In Adobe Experience Platform, puoi aggiornare gli attributi dei profili tramite un’importazione di file csv o chiamate API. Un metodo più semplice consiste nell&#39;utilizzare un **Aggiorna profilo** attività di azione e modifica il campo booleano del profilo di test da false a true.

Per ulteriori informazioni su come trasformare un profilo esistente in un profilo di test, consulta questa [sezione](../audience/creating-test-profiles.md#create-test-profiles-csv).
