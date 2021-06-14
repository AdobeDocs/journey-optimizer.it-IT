---
title: Configurare un’origine dati
description: Informazioni su come configurare un’origine dati
feature: 'Origini dati '
topic: Amministrazione
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 8%

---

# Configurare un’origine dati {#configure-data-source}

![](../assets/do-not-localize/badge.png)

Di seguito sono riportati i passaggi principali per la configurazione dell’origine dati:

>[!NOTE]
>
>La configurazione dell’origine dati viene sempre eseguita da un **utente tecnico**.

1. Selezionare il menu **[!UICONTROL Admin]** / **[!UICONTROL Data Sources]**.

   Viene visualizzato l’elenco delle origini dati. Per ulteriori informazioni sull&#39;interfaccia, consulta [questa pagina](../user-interface.md) .

   ![](../assets/journey18.png)

1. Quindi è possibile aggiungere gruppi di campi all&#39;origine dati incorporata (vedere [questa pagina](../datasource/adobe-experience-platform-data-source.md)) oppure creare una nuova origine dati esterna (vedere [questa pagina](../datasource/external-data-sources.md)) e i gruppi di campi associati (vedere [questa pagina](../datasource/configure-data-sources.md#define-field-groups)).

   ![](../assets/journey23.png)

1. Fai clic su **[!UICONTROL Save]**.

   Adesso l’origine dati è configurata ed è pronta per essere utilizzata nei percorsi.

## Definire i gruppi di campi {#define-field-groups}

I gruppi di campi sono insiemi di campi che è possibile recuperare da un’origine dati e utilizzare in un percorso.

Per ogni origine dati, puoi definire diversi gruppi di campi, ciascuno dei quali con una specifica durata della cache.

Ad esempio, puoi creare un gruppo di campi con il numero di telefono, l’e-mail, il nome e l’indirizzo del profilo. Potrai quindi utilizzare questi dati nel tuo percorso per creare condizioni. Ad esempio, puoi decidere di inviare un SMS solo se il numero di telefono del profilo non è vuoto. Se è vuoto, puoi inviare un’e-mail.

Anche se viene aggiunto automaticamente un nome predefinito, ti consigliamo di assegnare un nome al gruppo di campi. In effetti, il nome del gruppo di campi sarà visibile agli altri utenti in [!DNL Journey Optimizer]. È consigliabile assegnare un nome pertinente ai gruppi di campi.

Quando un campo origine dati viene utilizzato in un percorso, il sistema recupererà tutti i campi definiti per quel gruppo di campi. Pertanto, è consigliabile selezionare solo i campi necessari per i percorsi. Questo ridurrà la latenza della richiesta nei percorsi aumentando così le prestazioni. È possibile aggiungere facilmente più campi nei gruppi di campi in un secondo momento.

**[!UICONTROL Cache duration]** è importante anche in quanto ti aiuterà a ottimizzare le prestazioni. La durata della cache indica che in un percorso, se i dati di un gruppo di campi vengono recuperati una volta, il sistema li memorizzerà temporaneamente nella cache. Se gli stessi dati sono richiesti più avanti nello stesso percorso, il sistema non effettuerà un&#39;altra richiesta all&#39;origine dati. La configurazione della durata della cache deve essere adattata per ogni caso d’uso. Se devi recuperare dati in tempo reale, ad esempio lo stato della prenotazione dell’hotel, le informazioni meteo o il numero di punti fedeltà, associ il gruppo di campi contenente questi campi a una breve durata della cache (ad esempio 1 secondo). Per i campi che vengono aggiornati meno frequentemente (nome, genere), creerai un secondo gruppo di campi con una durata della cache più lunga (ad esempio, 5 giorni).

Il numero di percorsi che utilizzano un gruppo di campi viene visualizzato nel campo **[!UICONTROL Used in]** . Puoi fare clic sul pulsante **[!UICONTROL View journeys]** per visualizzare l’elenco dei percorsi che utilizzano questo gruppo di campi.

>[!NOTE]
>
>Tieni presente che se un gruppo di campi non ha un campo, non verrà visualizzato nell’editor espressioni.

![](../assets/journey3bis.png)

## Ciclo di vita del gruppo di campi {#field-group-lifecycle}

È possibile aggiungere o rimuovere campi da un gruppo di campi non utilizzato in alcuna bozza o in un percorso live.

Puoi aggiungere ma non rimuovere un campo da un gruppo di campi utilizzato in uno o più percorsi di bozza o live. In questo modo si evitano percorsi di rottura.

Per eliminare un campo da un gruppo di campi utilizzato in uno o più percorsi, procedere come segue. Utilizziamo un esempio di gruppo di campi denominato &quot;Gruppo di campi A&quot;.

1. Nell’elenco dei gruppi di campi, posiziona il cursore su &quot;Gruppo di campi A&quot; e fai clic sull’icona **[!UICONTROL Duplicate]** situata a destra. Ad esempio, denominare il gruppo di campi duplicato &quot;Gruppo di campi B&quot;.
1. In &quot;Gruppo di campi B&quot;, rimuovere i campi che non si desidera più.
1. In &quot;Gruppo di campi A&quot;, controlla dove viene utilizzato questo gruppo di campi. Queste informazioni vengono visualizzate nel campo **[!UICONTROL Used in]** .
1. Aprire tutti i percorsi che utilizzano &quot;Gruppo di campi A&quot;.
1. Crea nuove versioni di ciascuno di questi percorsi. Modifica tutte le attività utilizzando &quot;Gruppo di campi A&quot; e seleziona &quot;Gruppo di campi B&quot;.
1. Arrestare le vecchie versioni di percorsi che utilizzano &quot;Gruppo di campi A&quot;. Non dovrebbe quindi essere presente alcun percorso che utilizzi &quot;Gruppo di campi A&quot;.
1. Rimuovere il &quot;Gruppo di campi A&quot; in quanto non è più utilizzato.
