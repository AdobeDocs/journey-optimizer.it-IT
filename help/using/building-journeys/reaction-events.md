---
solution: Journey Optimizer
product: journey optimizer
title: Eventi di reazione
description: Scopri come utilizzare gli eventi di reazione per rispondere ai dati di tracciamento dei messaggi, come aperture e clic all’interno dei percorsi, e configurare percorsi di timeout per i non-responder.
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: percorso, eventi, reazione, tracciamento, piattaforma
exl-id: 235384f3-0dce-4797-8f42-1d4d01fa42d9
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/6myO49j2-TgkX0-diC8JDePxvMBPjZGnMYdxO466cP4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: d08afb72-92f6-4856-88e3-11ec34313c2fid: d8353d85-5da7-453d-bd68-40ad33fa0ab7id: e57d1da4-32c2-4cc6-945c-9feb219156ffid: ebd64fe4-362a-4a1c-9476-b2573ed12a95id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1030
ht-degree: 7%

---

# Eventi di reazione {#reaction-events}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come utilizzare l&#39;attività Reaction per rispondere ai dati di tracciamento dei messaggi come aperture e clic all&#39;interno dello stesso percorso e configurare percorsi di timeout per gli utenti che non sono coinvolti.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_event_reaction"
>title="Eventi di reazione"
>abstract="Questa attività consente di reagire ai dati di tracciamento relativi a un messaggio inviato nello stesso percorso. Queste informazioni vengono acquisite in tempo reale nel momento in cui sono condivise con [!DNL Adobe Experience Platform]."

## Panoramica {#overview}

Tra le diverse attività degli eventi disponibili nella palette, troverai l&#39;evento integrato **[!UICONTROL Reactions]**. Questa attività consente di reagire ai dati di tracciamento relativi a un messaggio inviato nello stesso percorso. Queste informazioni vengono acquisite in tempo reale nel momento in cui sono condivise con [!DNL Adobe Experience Platform].

Puoi reagire ai messaggi selezionati o aperti. Ad esempio, puoi inviare un altro messaggio se una persona ha aperto l’e-mail precedente o ha fatto clic al suo interno, oppure puoi inviare un messaggio di follow-up diverso se non ha interagito con la tua comunicazione.

Consulta [Attività azione](../building-journeys/about-journey-activities.md#action-activities).

Puoi utilizzare l&#39;attività **[!UICONTROL Reazione]** per eseguire un&#39;azione quando non vi è alcuna reazione ai messaggi. A questo scopo, crea un secondo percorso parallelo all&#39;attività **[!UICONTROL Reaction]** e aggiungi un&#39;attività **[!UICONTROL Wait]**. Se non si verifica alcuna reazione durante il periodo definito nell&#39;attività **[!UICONTROL Wait]**, verrà scelto il secondo percorso. Puoi scegliere di inviare, ad esempio, un messaggio di follow-up.

## Come configurare gli eventi di reazione {#configure}

![Configurazione evento di reazione con selezione canale e opzioni tipo evento](assets/journey45.png)

Per configurare gli eventi di reazione, segui la procedura riportata di seguito:

1. Posiziona un&#39;attività **[!UICONTROL Reazione]** **immediatamente** dopo un&#39;attività [azione canale](journey-action.md) nell&#39;area di lavoro del percorso.
1. Aggiungi un&#39;etichetta **[!UICONTROL Label]** alla reazione. Questo passaggio è facoltativo.
1. Dall’elenco a discesa, seleziona l’attività di azione a cui desideri reagire. Puoi selezionare qualsiasi attività di azione posizionata nei passaggi precedenti del percorso.
1. A seconda dell’azione selezionata, scegli a cosa desideri reagire.
1. Puoi definire un timeout dell’evento (tra 40 secondi e 90 giorni) e un percorso di timeout. Questo crea un secondo percorso per i singoli utenti che non hanno reagito entro la durata definita. Durante il test di un percorso che utilizza un evento di reazione, il valore predefinito e minimo della modalità di test **[!UICONTROL Tempo di attesa]** è di 40 secondi. Vedi [questa sezione](../building-journeys/testing-the-journey.md).

## Guardrail e limitazioni {#guardrails-limitations}

* Un&#39;attività **[!UICONTROL Reaction]** deve essere inserita **immediatamente** dopo un&#39;attività [channel action](journey-action.md) nell&#39;area di lavoro del percorso.
* Non è possibile utilizzare un&#39;attività **[!UICONTROL Reazione]** se prima non è presente alcuna attività di azione del canale.
* Il posizionamento di un&#39;attività **[!UICONTROL Wait]** o di qualsiasi altra attività tra l&#39;azione del canale e l&#39;attività **[!UICONTROL Reaction]** non è supportato e potrebbe impedire il funzionamento previsto dell&#39;attività Reaction.
* Gli eventi di reazione possono tracciare solo i messaggi inviati all’interno dello stesso percorso. Non possono tenere traccia dei messaggi che si verificano in un percorso diverso.
* Gli eventi di reazione tengono traccia dei clic su collegamenti del tipo &quot;tracciato&quot;. L’annullamento dell’abbonamento e i collegamenti alle pagine mirror non vengono presi in considerazione.
* Le aperture delle e-mail vengono tracciate utilizzando un’immagine a 0 pixel inclusa nell’e-mail. Se i client e-mail (come Gmail) bloccano le immagini, le aperture e-mail non verranno prese in considerazione.

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina viene illustrato come utilizzare l&#39;attività evento Reazione incorporata in Adobe Journey Optimizer per diramare i percorsi di percorso in base ai dati di coinvolgimento dei messaggi in tempo reale, ad esempio l&#39;apertura di e-mail e i clic sui collegamenti.

**Intenti:**
* Aggiungere un’attività evento Reazione per rispondere alle aperture dei messaggi o ai clic all’interno di un percorso
* Configurare una durata di timeout e un percorso di fallback per i profili che non coinvolgono
* Creare un percorso parallelo con un’attività Attendi per gestire i non responder
* Seleziona un’attività di azione del canale a monte specifica da ascoltare

**Glossario:**
* **Evento reazione**: attività evento di percorso incorporata che ascolta i dati di tracciamento in tempo reale (aperture, clic) da un messaggio inviato in precedenza nello stesso percorso *(specifico per prodotto)*
* **Percorso timeout**: ramo di percorso secondario seguito dai profili se non producono la reazione prevista entro il periodo di timeout definito *(specifico per prodotto)*

**Guardrail:**
* L’attività Reazione deve essere inserita immediatamente dopo un’attività di azione del canale; non è possibile inserire altre attività tra di esse.
* Non è possibile utilizzare un’attività di reazione se prima nel percorso non è presente alcuna attività di azione del canale.
* Gli eventi di reazione possono tracciare solo i messaggi inviati all’interno dello stesso percorso; il tracciamento tra percorsi non è supportato.
* I collegamenti di annullamento dell’abbonamento e i collegamenti alle pagine mirror non vengono tracciati dagli eventi di reazione.
* Le aperture e-mail si basano su un’immagine di tracciamento a 0 pixel; se il client e-mail blocca le immagini (ad esempio, Gmail), le aperture non verranno registrate.
* L’intervallo di timeout dell’evento è compreso tra 40 secondi e 90 giorni; anche il valore minimo in modalità di test è di 40 secondi.

**Terminologia:**
* Nome canonico: Eventi di reazione — Acronimo: none — varianti: attività di reazione, evento di tracciamento del coinvolgimento
* Sinonimi: &quot;Evento di reazione&quot; = &quot;evento di coinvolgimento del messaggio&quot; = &quot;evento di tracciamento&quot;
* Non confondere: &quot;Evento di reazione&quot; ≠ &quot;Evento esterno&quot; (gli eventi di reazione sono incorporati e legati ai messaggi dello stesso percorso; gli eventi esterni provengono dall’esterno del percorso)

**Domande frequenti:**
* **D: un evento Reazione può tenere traccia di un messaggio inviato in un percorso diverso?** — No; gli eventi di reazione tengono traccia solo dei messaggi inviati nello stesso percorso.
* **D: come posso gestire i profili che non aprono o non fanno clic su un messaggio?** — Aggiungere un percorso parallelo accanto all&#39;attività Reazione con un&#39;attività Attesa. I profili che non reagiscono entro la durata di attesa seguiranno il secondo percorso.
* **Q: i clic del collegamento per l&#39;annullamento dell&#39;abbonamento vengono tracciati dagli eventi di reazione?** — No; vengono acquisiti solo i tipi di collegamento tracciati. I collegamenti di annullamento dell’abbonamento e della pagina speculare sono esclusi.
* **D: cosa succede se un client di posta elettronica blocca le immagini?** — L&#39;e-mail si apre tracciata tramite l&#39;immagine a 0 pixel non verrà registrata per i client che bloccano le immagini, come Gmail.
* **D: qual è l&#39;intervallo di timeout valido per un evento di reazione?** — Tra 40 secondi e 90 giorni.

+++
