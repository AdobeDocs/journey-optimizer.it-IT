---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Dividi
description: Scopri come utilizzare l’attività Split in una campagna orchestrata
exl-id: 986bc566-123a-451d-a4a6-bbf5a2798849
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '801'
ht-degree: 88%

---


# Dividi {#split}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split"
>title="Attività Dividi"
>abstract="L’attività **Dividi** consente di segmentare le popolazioni in ingresso in più sottoinsiemi in base a criteri di selezione diversi, ad esempio le regole di filtro o le dimensioni della popolazione."

L’attività **[!UICONTROL Dividi]** è un’attività di **[!UICONTROL targeting]** che consente di segmentare le popolazioni in ingresso in più sottoinsiemi in base a criteri di selezione diversi, ad esempio le regole di filtro o le dimensioni della popolazione.

## Configurare l’attività Dividi {#split-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_segments"
>title="Segmenti per attività Dividi"
>abstract="Aggiungi tutti i sottoinsiemi desiderati per segmentare la popolazione in ingresso.<br/></br>Quando viene eseguita l’attività **Dividi**, la popolazione viene segmentata tra i diversi sottoinsiemi nell’ordine in cui vengono aggiunti all’attività. Prima di avviare la campagna orchestrata, assicurati di aver ordinato i sottoinsiemi nell’ordine più adatto alle tue esigenze utilizzando i pulsanti freccia."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_filter"
>title="Filtro attività Dividi"
>abstract="Per applicare una condizione di filtro al sottoinsieme, fai clic su **[!UICONTROL Crea filtro]** e configura la regola di filtro desiderata utilizzando il generatore di regole. Ad esempio, includi i profili della popolazione in ingresso il cui indirizzo e-mail esiste nel database."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_limit"
>title="Limite attività Dividi"
>abstract="Per limitare il numero di profili selezionati dal sottoinsieme, attiva l’opzione **[!UICONTROL Abilita limite]** e specifica il numero o le percentuali della popolazione da includere."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_sorting"
>title="Ordinamento attività Dividi"
>abstract="Quando imposti un limite di popolazione per un sottoinsieme, puoi classificare i profili selezionati in base a un attributo di profilo specifico, in ordine crescente o decrescente. A tale scopo, attiva l’opzione **Abilita ordinamento**. Ad esempio, puoi limitare un sottoinsieme in modo da includere solo i primi 50 profili con l’importo di acquisto più alto."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_complement"
>title="Complemento generato da suddivisione"
>abstract="Dopo aver configurato tutti i sottoinsiemi, puoi selezionare la popolazione rimanente che non corrisponde a nessuno dei sottoinsiemi e includerli in un’ulteriore transizione in uscita. A tale scopo, attiva l’opzione **Genera complemento**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_generatesubsets"
>title="Generare tutti i sottoinsiemi nella stessa tabella"
>abstract="Attiva questa opzione per raggruppare tutti i sottoinsiemi in una singola transizione di output."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_emptytransition"
>title="Ignora transizione vuota"
>abstract="Attiva l’opzione **[!UICONTROL Ignora transizione vuota]** per disabilitare la transizione di output per questo sottoinsieme se la popolazione in ingresso è vuota."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_enable_overlapping"
>title="Abilita sovrapposizione popolazioni di output"
>abstract=" L’opzione **[!UICONTROL Abilita sovrapposizione popolazioni di output]** consente di gestire le popolazioni appartenenti a diversi sottoinsiemi. Quando questa opzione non è selezionata, l’attività Dividi si assicura che un destinatario non possa essere presente in diverse transizioni di output, anche se soddisfa i criteri di diversi sottoinsiemi. Saranno nella destinazione della prima scheda con i criteri corrispondenti. Quando questa opzione è selezionata, i destinatari possono essere in più sottoinsiemi se soddisfano i rispettivi criteri di filtro."

Per configurare l’attività **[!UICONTROL Dividi]** segui questi passaggi:

1. Aggiungi un&#39;attività **[!UICONTROL Dividi]** alla campagna orchestrata.

1. Il riquadro di configurazione dell’attività si apre con un sottoinsieme predefinito. Fai clic sul pulsante **[!UICONTROL Aggiungi segmento]** per aggiungere tutti i sottoinsiemi desiderati per segmentare la popolazione in ingresso.

   ![](../assets/orchestrated-split-1.png)

   >[!IMPORTANT]
   >
   >L’attività **Dividi** elabora i sottoinsiemi nell’ordine in cui vengono aggiunti. Ad esempio, se il primo sottoinsieme acquisisce il 70% della popolazione, il successivo applica i relativi criteri al restante 30%.
   >
   >Prima di eseguire la campagna orchestrata, assicurati che i sottoinsiemi siano ordinati come previsto. Utilizza i pulsanti freccia per regolarne la posizione.

1. Una volta aggiunti i sottoinsiemi, l’attività mostra tante transizioni di output quanti sono i sottoinsiemi. Si consiglia vivamente di modificare l’etichetta di ciascun sottoinsieme per identificarlo facilmente nell’area di lavoro della campagna orchestrata.

1. Configura i filtri per ciascun sottoinsieme:

   1. Fai clic su un sottoinsieme per aprirne le impostazioni.

   1. Fai clic su **[!UICONTROL Crea filtro]** per definire le regole di filtro utilizzando il generatore di regole, ad esempio per selezionare profili con un indirizzo e-mail valido.

      ![](../assets/orchestrated-split-1.png)

   1. Per limitare il numero di profili selezionati, attiva **[!UICONTROL Abilita limite]** e specifica un numero o una percentuale.

   1. Per ignorare una transizione quando il sottoinsieme è vuoto, abilita **[!UICONTROL Ignora transizione vuota].**

1. Per includere profili non corrispondenti a un sottoinsieme, abilita **[!UICONTROL Genera complemento]**. Questo crea una transizione in uscita aggiuntiva per la popolazione rimanente.

   >[!NOTE]
   >
   >Abilita **[!UICONTROL Genera tutti i sottoinsiemi nella stessa tabella]** per raggruppare tutti i sottoinsiemi in un’unica transizione.

1. Utilizza **[!UICONTROL Abilita la sovrapposizione delle popolazioni di output]** per consentire la visualizzazione dei profili in più sottoinsiemi:

   * **Se non è selezionato**, ogni profilo viene assegnato a un solo sottoinsieme, il primo con il quale corrispondono i criteri anche se è idoneo per altri sottoinsiemi.

   * **Se selezionato**, i profili possono essere inclusi in più sottoinsiemi se soddisfano i criteri per ciascuno di essi.

L’attività adesso è configurata. All’esecuzione della campagna orchestrata, la popolazione verrà segmentata in diversi sottoinsiemi, nell’ordine in cui sono stati aggiunti all’attività.

## Esempio{#split-example}

Nell’esempio seguente, l’attività **[!UICONTROL Dividi]** viene utilizzata per segmentare un pubblico in sottoinsiemi distinti in base al canale di comunicazione che si desidera utilizzare:

* **Sottoinsieme 1 “e-mail”**: include i profili che hanno fornito un numero di telefono.

* **Sottoinsieme 2 “sms”**: esegue il targeting dei profili con un numero di telefono cellulare archiviato nel database.

* **Transizione complemento**: acquisisce tutti i profili rimanenti che non soddisfano i criteri per nessuno dei sottoinsiemi.

![](../assets/orchestrated-split-3.png)
