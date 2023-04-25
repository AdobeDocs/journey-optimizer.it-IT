---
title: Creare i posizionamenti
description: Scopri come creare posizionamenti per le offerte
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: dfaf887e-d4b3-45b0-8297-bffdb0abff4d
source-git-commit: 51f93270c969875e94cc3e98919149d67d764ed1
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 11%

---

# Creare i posizionamenti {#create-placements}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_placement"
>title="Posizionamento"
>abstract="Un posizionamento è un contenitore utilizzato per mostrare le offerte, affinché il contenuto corretto venga visualizzato nella posizione desiderata all’interno del messaggio. I posizionamenti vengono creati dal menu “Componenti”."

Un posizionamento garantisce che il contenuto dell’offerta corretta sia visualizzato nella posizione giusta all’interno del messaggio. Quando aggiungi contenuto a un’offerta, ti verrà chiesto di selezionare un posizionamento in cui visualizzare il contenuto.

➡️ [Scopri come creare posizionamenti in questo video](#video)

Nell’esempio seguente sono presenti tre posizioni, corrispondenti a diversi tipi di contenuto (immagine, testo, HTML).

![](../assets/offers_placement_schema.png)

L’elenco dei posizionamenti è accessibile nella **[!UICONTROL Componenti]** menu. Sono disponibili filtri per recuperare i posizionamenti in base a un canale o contenuto specifico.

![](../assets/placements_filter.png)

Per creare un posizionamento, effettua le seguenti operazioni:

1. Fai clic su **[!UICONTROL Creare un posizionamento]**.

   ![](../assets/offers_placement_creation.png)

1. Definisci le proprietà del posizionamento:

   * **[!UICONTROL Nome]**: Nome del posizionamento. Assicurati di definire un nome significativo per recuperarlo più facilmente.
   * **[!UICONTROL Tipo di canale]**: Canale per il quale verrà utilizzato il posizionamento.
   * **[!UICONTROL Tipo di contenuto]**: Il tipo di contenuto che il posizionamento può visualizzare: Testo, HTML, collegamento immagine o JSON.
   * **[!UICONTROL Descrizione]**: Una descrizione del posizionamento (facoltativo).

   ![](../assets/offers_placement_creation_properties.png)


1. La **[!UICONTROL Impostazioni richieste]** e **[!UICONTROL Formato di risposta]** Le sezioni forniscono parametri aggiuntivi:

   * **[!UICONTROL Consenti duplicati tra posizionamenti]**: Controlla se la stessa offerta può essere proposta più volte in diversi posizionamenti. Se attivato, il sistema considererà la stessa offerta per più posizionamenti. Per impostazione predefinita, il parametro è impostato su false.

      Se questa opzione è impostata su false per qualsiasi posizionamento in una richiesta di decisione, tutti i posizionamenti nella richiesta erediteranno l’impostazione &quot;false&quot;.

   * **[!UICONTROL Richiesta di offerta]**: Per impostazione predefinita, viene restituita un’offerta dell’ambito decisionale per ciascun profilo. Puoi regolare il numero di offerte restituite utilizzando questa opzione. Ad esempio, se selezioni 2, verranno visualizzate le migliori 2 offerte per l’ambito di decisione selezionato.

   * **[!UICONTROL Includi contenuto]** / **[!UICONTROL Includi metadati]**: specifica se il contenuto e i metadati dell’offerta devono essere restituiti nella risposta API. Puoi includere solo tutti i metadati o campi specifici. Per impostazione predefinita, il valore dei metadati Include è impostato su true.
   Questi parametri possono anche essere impostati direttamente nella richiesta API se lavori con [Decisioning API](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/decisioning-api.html). Tuttavia, la loro configurazione nell’interfaccia utente può aiutarti a risparmiare tempo, in quanto non dovrai passarli in ogni richiesta API. Tieni presente che se configuri i parametri sia nell’interfaccia utente che nella richiesta API, i valori della richiesta API prevalgono su quelli dell’interfaccia.

   >[!NOTE]
   >
   >Se lavori con il [API di Edge Decisioning](https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/api-reference/offer-delivery-api/edge-decisioning-api.html?), non puoi impostare questi parametri nella richiesta. È necessario definirli in questa schermata.
   >
   >Se lavori con il [API Batch Decisioning](../api-reference/offer-delivery-api/batch-decisioning-api.md), puoi impostare questi parametri in questa schermata o nella richiesta API. In caso di mancata corrispondenza dei valori dei parametri tra la schermata e la richiesta APi, verranno utilizzati i valori della richiesta.

1. Fai clic su **[!UICONTROL Salva]** per confermare.

1. Una volta creato, il posizionamento viene visualizzato nell’elenco dei posizionamenti. È possibile selezionarlo per visualizzarne le proprietà e modificarlo.

   ![](../assets/placement_created.png)

## Video introduttivo{#video}

Scopri come creare posizionamenti nella gestione delle decisioni.

>[!VIDEO](https://video.tv.adobe.com/v/329372?quality=12)

