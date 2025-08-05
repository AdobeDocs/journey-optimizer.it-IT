---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Deduplica
description: Scopri come utilizzare l’attività Deduplica
exl-id: 4aa79448-f75a-48d5-8819-f4cb4baad5c7
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 98%

---


# Deduplica {#deduplication}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_fields"
>title="Campi per identificare i duplicati"
>abstract="Nella sezione **Campi per identificare i duplicati** , fai clic sul pulsante **Aggiungi attributo** per specificare i campi per i quali i valori identici consentono l’identificazione dei duplicati, ad esempio: indirizzo e-mail, nome, cognome e così via. L’ordine dei campi consente di specificare quali elaborare per primi."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication"
>title="Attività Deduplica"
>abstract="L’attività **Deduplica** consente di eliminare i duplicati nei risultati delle attività in entrata. Viene utilizzato principalmente dopo le attività di targeting e prima delle attività che consentono l’utilizzo di dati mirati."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_complement"
>title="Generare un complemento"
>abstract="Puoi generare una transizione in uscita aggiuntiva con la popolazione rimanente, che è stata esclusa come duplicato. A tale scopo, attiva l’opzione **Genera complemento**"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_deduplication_settings"
>title="Impostazioni di deduplica"
>abstract="Per eliminare i duplicati nei dati in arrivo, definisci il metodo di deduplica nei campi seguenti. Per impostazione predefinita, viene mantenuto un solo record. Devi anche selezionare la modalità di deduplica in base a un’espressione o a un attributo. Per impostazione predefinita, il record da escludere dai duplicati viene selezionato in modo casuale."

L’attività **[!UICONTROL Deduplica]** è un’attività di **[!UICONTROL targeting]**. Questa attività consente di eliminare i duplicati nei risultati delle attività in entrata, ad esempio i profili duplicati nell’elenco dei destinatari. L’attività **[!UICONTROL Deduplica]** viene generalmente utilizzata dopo le attività di targeting e prima delle attività che consentono l’utilizzo di dati mirati.

## Configurare l’attività Deduplica{#deduplication-configuration}

Per configurare l’attività **[!UICONTROL Deduplica]** segui questi passaggi:


1. Aggiungi un&#39;attività **[!UICONTROL Deduplicazione]** alla campagna orchestrata.

1. Nella sezione **[!UICONTROL Campi per identificare i duplicati]** , fai clic sul pulsante **[!UICONTROL Aggiungi attributo]** per specificare i campi per i quali i valori identici consentono l’identificazione dei duplicati, ad esempio: indirizzo e-mail, nome, cognome e così via. L’ordine dei campi consente di specificare quali elaborare per primi.

   ![](../assets/deduplication-1.png)

1. Nella sezione **[!UICONTROL Impostazioni deduplica]**, scegli il numero di record univoci per continuare a utilizzare il campo Duplicati da mantenere. Il valore predefinito è 1, che mantiene un record per gruppo duplicato. Impostalo su 0 per mantenere tutti i duplicati.

   Ad esempio, se i record A e B sono considerati duplicati del record Y e il record C è considerato un duplicato del record Z:

   * **Se il valore del campo è 1**: vengono conservati solo i record Y e Z.
   * **Se il valore del campo è 0**: vengono conservati tutti i record (A, B, C, Y, Z).
   * **Se il valore del campo è 2**: vengono mantenuti C e Z, più due valori da A, B e Y, in modo casuale o in base al metodo di deduplica utilizzato.

1. Scegli un **[!UICONTROL metodo di deduplica]**, che definisce il modo in cui il sistema decide quali record mantenere da ogni gruppo di duplicati:

   * **[!UICONTROL Selezione casuale]**: seleziona in modo casuale il record da escludere dai duplicati.
   * **[!UICONTROL Utilizzo di un’espressione]**: mantiene i record con il valore più alto o più basso in base a un’espressione definita dall’utente.
   * **[!UICONTROL Valori non vuoti]**: mantiene i record in cui il campo selezionato non è vuoto, ad esempio mantiene solo i profili con un numero di telefono.
   * **[!UICONTROL In base a un elenco di valori]**: consente di assegnare priorità a valori specifici per uno o più campi. Ad esempio è possibile assegnare priorità ai record con “Paese” impostato su Francia. Fai clic su **[!UICONTROL Attributo]** per scegliere un campo o creare un’espressione personalizzata. Utilizza il **[!UICONTROL pulsante Aggiungi]** per immettere i valori preferiti in ordine di priorità.

   ![](../assets/deduplication-2.png)

1. Se desideri sfruttare la popolazione rimanente, seleziona l’opzione **[!UICONTROL Genera complemento]**. Il complemento è costituito da tutti i duplicati. Verrà quindi aggiunta all’attività un’ulteriore transizione.

## Esempio{#deduplication-example}

Nell’esempio seguente viene utilizzata un’attività **[!UICONTROL Deduplica]** per rimuovere i record duplicati dal pubblico target prima di inviare una consegna. Il pubblico viene innanzitutto filtrato in modo da includere solo i profili con un campo E-mail non vuoto. L’attività **[!UICONTROL Deduplica]** utilizza quindi l’indirizzo e-mail per identificare ed escludere i duplicati.

![](../assets/deduplication-3.png)
