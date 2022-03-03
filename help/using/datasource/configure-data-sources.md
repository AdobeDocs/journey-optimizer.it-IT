---
title: Configurare un’origine dati
description: Informazioni su come configurare un’origine dati
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: 9b0dcffb-f543-4066-850c-67ec33f74a31
source-git-commit: bd35bf2ec4c1b2898007d670fc20626f06cc3750
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 10%

---

# Configurare un’origine dati {#configure-data-source}

Di seguito sono riportati i passaggi principali per la configurazione dell’origine dati:

>[!NOTE]
>
>La configurazione dell’origine dati viene sempre eseguita da un **utente tecnico**.

1. Nella sezione del menu AMMINISTRAZIONE, seleziona **[!UICONTROL Configurations]**. In  **[!UICONTROL Data Sources]** sezione, fai clic su **[!UICONTROL Manage]**. Viene visualizzato l’elenco delle origini dati. Vedi [questa pagina](../start/user-interface.md) per ulteriori informazioni sull’interfaccia.

   ![](assets/journey18.png)

1. È quindi possibile aggiungere gruppi di campi all’origine dati incorporata (consulta [questa pagina](../datasource/adobe-experience-platform-data-source.md)) o crea una nuova origine dati esterna (vedi [questa pagina](../datasource/external-data-sources.md)) e i gruppi di campi associati (vedi [questa pagina](../datasource/configure-data-sources.md#define-field-groups)).

   ![](assets/journey23.png)

1. Fai clic su **[!UICONTROL Save]**.

   Adesso l’origine dati è configurata ed è pronta per essere utilizzata nei percorsi.

## Definire i gruppi di campi {#define-field-groups}

I gruppi di campi sono insiemi di campi che è possibile recuperare da un’origine dati e utilizzare in un percorso.

Per ogni origine dati puoi definire diversi gruppi di campi.

Ad esempio, puoi creare un gruppo di campi con il numero di telefono, l’e-mail, il nome e l’indirizzo del profilo. Potrai quindi utilizzare questi dati nel tuo percorso per creare condizioni. Ad esempio, puoi decidere di inviare un SMS solo se il numero di telefono del profilo non è vuoto. Se è vuoto, puoi inviare un’e-mail.

Anche se viene aggiunto automaticamente un nome predefinito, ti consigliamo di assegnare un nome al gruppo di campi. In effetti, il nome del gruppo di campi sarà visibile agli altri utenti in [!DNL Journey Optimizer]. È consigliabile assegnare un nome pertinente ai gruppi di campi.

Quando un campo origine dati viene utilizzato in un percorso, il sistema recupererà tutti i campi definiti per quel gruppo di campi. Pertanto, è consigliabile selezionare solo i campi necessari per i percorsi. Questo ridurrà la latenza della richiesta nei percorsi aumentando così le prestazioni. È possibile aggiungere facilmente più campi nei gruppi di campi in un secondo momento.

Il numero di percorsi che utilizzano un gruppo di campi viene visualizzato nella **[!UICONTROL Used in]** campo . Puoi fare clic su **[!UICONTROL View journeys]** per visualizzare l’elenco dei percorsi che utilizzano questo gruppo di campi.

>[!NOTE]
>
>Tieni presente che se un gruppo di campi non ha un campo, non verrà visualizzato nell’editor espressioni.

![](assets/journey3bis.png)

## Ciclo di vita del gruppo di campi {#field-group-lifecycle}

È possibile aggiungere o rimuovere campi da un gruppo di campi non utilizzato in alcuna bozza o in un percorso live.

Puoi aggiungere ma non rimuovere un campo da un gruppo di campi utilizzato in uno o più percorsi di bozza o live. In questo modo si evitano percorsi di rottura.

Per eliminare un campo da un gruppo di campi utilizzato in uno o più percorsi, procedere come segue. Utilizziamo un esempio di gruppo di campi denominato &quot;Gruppo di campi A&quot;.

1. Nell’elenco dei gruppi di campi, posiziona il cursore su &quot;Gruppo di campi A&quot; e fai clic sul pulsante **[!UICONTROL Duplicate]** a destra. Ad esempio, denominare il gruppo di campi duplicato &quot;Gruppo di campi B&quot;.
1. In &quot;Gruppo di campi B&quot;, rimuovere i campi che non si desidera più.
1. In &quot;Gruppo di campi A&quot;, controlla dove viene utilizzato questo gruppo di campi. Queste informazioni vengono visualizzate nel **[!UICONTROL Used in]** campo .
1. Aprire tutti i percorsi che utilizzano &quot;Gruppo di campi A&quot;.
1. Crea nuove versioni di ciascuno di questi percorsi. Modifica tutte le attività utilizzando &quot;Gruppo di campi A&quot; e seleziona &quot;Gruppo di campi B&quot;.
1. Arrestare le vecchie versioni di percorsi che utilizzano &quot;Gruppo di campi A&quot;. Non dovrebbe quindi essere presente alcun percorso che utilizzi &quot;Gruppo di campi A&quot;.
1. Rimuovere il &quot;Gruppo di campi A&quot; in quanto non è più utilizzato.
