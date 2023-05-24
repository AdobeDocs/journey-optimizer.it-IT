---
solution: Journey Optimizer
product: journey optimizer
title: Aggiorna profilo
description: Scopri come utilizzare l’attività Aggiorna profilo in un percorso
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: profilo, aggiornamento, percorso, attività
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 9%

---

# Aggiorna profilo {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="Attività Aggiorna profilo"
>abstract="L’attività Aggiorna profilo consente di aggiornare un profilo Adobe Experience Platform esistente con un valore specifico oppure con informazioni provenienti dall’evento o da un’origine dati."

Utilizza il **[!UICONTROL Aggiorna profilo]** attività di azione per aggiornare un profilo Adobe Experience Platform esistente con informazioni provenienti da un evento, un’origine dati o un valore specifico.

## Consigli

* Il **Aggiorna profilo** può essere utilizzata solo nei percorsi che iniziano con un evento che ha uno spazio dei nomi.
* L’azione aggiorna solo i campi esistenti, non crea nuovi campi profilo.
* Non è possibile utilizzare **Aggiorna profilo** azione per generare eventi di esperienza, ad esempio un acquisto.
* Proprio come qualsiasi altra azione, puoi definire un percorso alternativo in caso di errore o timeout e non puoi inserire due azioni in parallelo.
* La richiesta di aggiornamento inviata a Adobe Experience Platform è immediata/entro un secondo. Ci vorrà normalmente qualche secondo, ma a volte di più senza alcuna garanzia. Di conseguenza, ad esempio, se un’azione utilizza il &quot;campo 1&quot; aggiornato da un **Aggiorna profilo** azione posizionata immediatamente prima, non ti aspetti che &quot;campo 1&quot; venga aggiornato nell’azione.
* Il **Aggiorna profilo** L’attività non supporta i campi XDM definiti come enumerazione.

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

Solo i profili di test possono accedere a un percorso in modalità di test. È possibile creare un nuovo profilo di test o trasformare un profilo esistente in un profilo di test. In Adobe Experience Platform, puoi aggiornare gli attributi dei profili tramite un’importazione di file csv o chiamate API. Un metodo più semplice consiste nell&#39;utilizzare un **Aggiorna profilo** attività di azione e modifica il campo booleano del profilo di test da false a true.

Per ulteriori informazioni su come trasformare un profilo esistente in un profilo di test, consulta questa [sezione](../segment/creating-test-profiles.md#create-test-profiles-csv).
