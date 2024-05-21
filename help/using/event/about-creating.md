---
solution: Journey Optimizer
product: journey optimizer
title: Configurare un evento unitario
description: Scopri come configurare un evento unitario
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: evento, unitario, creazione, percorso
exl-id: e22e2bc7-0c15-457a-8980-97bea5da7784
source-git-commit: 0f1c4b96e930e8e473463002c1d8ef66341a07c4
workflow-type: tm+mt
source-wordcount: '1609'
ht-degree: 12%

---

# Configurare un evento unitario {#configure-an-event}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_unitary"
>title="Eventi unitari"
>abstract="La configurazione dell’evento consente di definire le informazioni che Journey Optimizer riceverà sotto forma di eventi. All’interno dei vari passaggi di un percorso puoi utilizzare più eventi, e uno stesso evento può essere utilizzato in più percorsi. Gli eventi unitari sono collegati a un profilo specifico. Possono essere basati su regole o generati dal sistema."

Gli eventi unitari sono collegati a un profilo specifico. Possono essere basate su regole o generate dal sistema.  Ulteriori informazioni sull’evento unitario [questa sezione](../event/about-events.md).

Di seguito sono riportati i primi passaggi per configurare un nuovo evento:

1. Nella sezione del menu ADMINISTRATION, selezionare **[!UICONTROL Configurazioni]**. In  **[!UICONTROL Eventi]** , fare clic su **[!UICONTROL Gestisci]**. Viene visualizzato l’elenco degli eventi.

   ![](assets/jo-event1.png)

1. Clic **[!UICONTROL Crea evento]** per creare un nuovo evento. Il riquadro di configurazione dell’evento si apre sul lato destro dello schermo.

   ![](assets/jo-event2.png)

1. Inserisci il nome dell’evento. Puoi anche aggiungere una descrizione.

   ![](assets/jo-event3.png)

   >[!NOTE]
   >
   >Sono consentiti solo caratteri alfanumerici e trattini bassi. La lunghezza massima è di 30 caratteri.

1. In **[!UICONTROL Tipo]** campo, scegli **Unitario**.

   ![](assets/jo-event3bis.png)

1. In **[!UICONTROL Tipo ID evento]** , seleziona il tipo di ID evento che desideri utilizzare: **Basato su regole** o **Generato dal sistema**. Ulteriori informazioni sui tipi di ID evento in [questa sezione](../event/about-events.md#event-id-type).

   ![](assets/jo-event4.png)

1. Il numero di percorsi che utilizzano questo evento viene visualizzato nel **[!UICONTROL Utilizzato in]** campo. Puoi fare clic su **[!UICONTROL Visualizza percorsi]** per visualizzare l’elenco dei percorsi che utilizzano questo evento.

1. Definisci i campi dello schema e del payload: in questo punto è possibile selezionare le informazioni sull’evento, solitamente denominato payload, che i percorsi prevedono di ricevere. Potrai quindi utilizzare queste informazioni nel tuo percorso. Consulta [questa sezione](../event/about-creating.md#define-the-payload-fields).

   ![](assets/jo-event5.png)

   >[!NOTE]
   >
   >Quando selezioni il **[!UICONTROL Generato dal sistema]** tipo, sono disponibili solo gli schemi che hanno il campo tipo eventID. Quando selezioni il **[!UICONTROL Basato su regole]** Tipo, sono disponibili tutti gli schemi Experience Event.

1. Per gli eventi basati su regole, fai clic su all’interno del **[!UICONTROL Condizione ID evento]** campo. Utilizzando l’editor di espressioni semplice o avanzato, definisci la condizione che verrà utilizzata dal sistema per identificare gli eventi che attiveranno il percorso.
   ![](assets/jo-event6.png)

   >[!NOTE]
   >
   >L’editor di espressioni avanzate nella configurazione degli eventi è disponibile in Disponibilità limitata per alcuni clienti selezionati.

   Nel nostro esempio, abbiamo scritto una condizione basata sulla città del profilo. Ciò significa che ogni volta che il sistema riceve un evento che corrisponde a questa condizione (**[!UICONTROL Città]** campo e **[!UICONTROL Parigi]** ), la trasmetterà ai percorsi.

   >[!NOTE]
   >
   >Nell’editor delle espressioni semplici non tutti gli operatori sono disponibili, ma dipendono dal tipo di dati. Ad esempio, per un tipo di stringa di campo, puoi utilizzare &quot;contains&quot; o &quot;equal to&quot;.
   >
   >Se modifichi lo schema con nuovi valori di enumerazione dopo aver creato l’evento, segui questi passaggi per applicare le modifiche all’evento esistente: deseleziona il campo di enumerazione dai campi dell’evento, conferma la selezione, quindi seleziona nuovamente il campo di enumerazione. Viene ora visualizzato il nuovo valore di enumerazione.

1. Aggiungi uno spazio dei nomi. Questo passaggio è facoltativo ma consigliato, poiché l’aggiunta di uno spazio dei nomi consente di sfruttare le informazioni memorizzate nel servizio Profilo cliente in tempo reale, definendo il tipo di chiave di cui dispone l’evento. Consulta [questa sezione](../event/about-creating.md#select-the-namespace).

1. Definire l’identificatore del profilo: scegli un campo dai campi del payload o definisci una formula per identificare la persona associata all’evento. Se selezioni uno spazio dei nomi, questa chiave viene impostata automaticamente, ma può essere comunque modificata. In effetti, i percorsi selezionano la chiave che deve corrispondere allo spazio dei nomi, ad esempio, se scegli uno spazio dei nomi e-mail, verrà selezionata la chiave e-mail. Consulta [questa sezione](../event/about-creating.md#define-the-event-key).

   ![](assets/jo-event7.png)

1. Fai clic su **[!UICONTROL Salva]**.

   L’evento è ora configurato e pronto per essere rilasciato in un percorso. Per poter ricevere gli eventi sono necessari ulteriori passaggi di configurazione. Consulta [questa pagina](../event/additional-steps-to-send-events-to-journey.md).

## Definire i campi payload {#define-the-payload-fields}

La definizione del payload consente di scegliere le informazioni che il sistema si aspetta di ricevere dall’evento nel percorso e la chiave per identificare quale persona è associata all’evento. Il payload si basa sulla definizione del campo XDM di Experience Cloud. Per ulteriori informazioni su XDM, consulta [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.

1. Seleziona uno schema XDM dall’elenco e fai clic sul pulsante **[!UICONTROL Campi]** campo o sul **[!UICONTROL Modifica]** icona.

   ![](assets/journey8.png)

   Vengono visualizzati tutti i campi definiti nello schema. L’elenco dei campi varia da uno schema all’altro. Puoi cercare un campo specifico o utilizzare i filtri per visualizzare tutti i nodi e i campi o solo i campi selezionati. In base alla definizione dello schema, alcuni campi possono essere obbligatori e preselezionati. Non è possibile deselezionarli. Per impostazione predefinita, vengono selezionati tutti i campi obbligatori per consentire la corretta ricezione dell’evento da parte dei percorsi.

   >[!NOTE]
   >
   >Per gli eventi generati dal sistema, accertati di aver aggiunto il gruppo di campi &quot;orchestrazione&quot; allo schema XDM. In questo modo lo schema conterrà tutte le informazioni necessarie per lavorare con [!DNL Journey Optimizer].

   ![](assets/journey9.png)

1. Seleziona i campi che prevedi di ricevere dall’evento. Questi sono i campi che l’utente aziendale sfrutterà nel percorso. Devono inoltre includere la chiave che verrà utilizzata per identificare la persona associata all’evento (vedi [questa sezione](../event/about-creating.md#define-the-event-key)).

   >[!NOTE]
   >
   >Per gli eventi generati dal sistema, **[!UICONTROL eventID]** viene aggiunto automaticamente nell’elenco dei campi selezionati in modo che [!DNL Journey Optimizer] può identificare l’evento. Il sistema che trasmette l’evento non deve generare un ID, deve utilizzare quello disponibile nell’anteprima del payload. Consulta [questa sezione](../event/about-creating.md#preview-the-payload).

1. Dopo aver selezionato i campi necessari, fai clic su **[!UICONTROL Ok]** o premere **[!UICONTROL Invio]**.

   Il numero di campi selezionati viene visualizzato nel **[!UICONTROL Campi]** campo.

   ![](assets/journey12.png)

## Selezionare lo spazio dei nomi {#select-the-namespace}

>[!CONTEXTUALHELP]
>id="ajo_journey_namespace"
>title="Spazio dei nomi identità"
>abstract="Seleziona la chiave per identificare il profilo cliente associato all’evento."

Lo spazio dei nomi consente di definire il tipo di chiave utilizzato per identificare la persona associata all’evento. La sua configurazione è facoltativa. È necessario se desideri recuperare nei tuoi percorsi informazioni aggiuntive provenienti da [Profilo cliente in tempo reale](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target="_blank"}. La definizione dello spazio dei nomi non è necessaria se utilizzi solo dati provenienti da un sistema di terze parti tramite un’origine dati personalizzata.

Puoi utilizzare uno dei predefiniti o crearne uno nuovo utilizzando il servizio Identity Namespace. Fai riferimento a [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=it){target="_blank"}.

Se selezioni uno schema con un’identità primaria, il **[!UICONTROL Identificatore profiler]** e **[!UICONTROL Namespace]** i campi sono precompilati. Se non è stata definita alcuna identità, selezioniamo _identityMap > id_ come chiave primaria. Quindi devi selezionare uno spazio dei nomi e la chiave verrà precompilata (sotto il **[!UICONTROL Namespace]** field) utilizzando _identityMap > id_.

Quando selezioni i campi, vengono taggati i campi di identità primari.

![](assets/primary-identity.png)

Seleziona uno spazio dei nomi dall’elenco a discesa.

![](assets/journey17.png)

È consentito un solo spazio dei nomi per percorso. Se utilizzi più eventi nello stesso percorso, è necessario che utilizzino lo stesso namespace. Consulta [questa pagina](../building-journeys/journey.md).

>[!NOTE]
>
>È possibile selezionare solo uno spazio dei nomi delle identità basato su persone. Se hai definito uno spazio dei nomi per una tabella di ricerca (ad esempio: Spazio dei nomi ProductID per una ricerca di prodotto), questo non sarà disponibile nella **Namespace** elenco a discesa.

## Definire l’identificatore del profilo {#define-the-event-key}

La chiave è il campo, o la combinazione di campi, che fa parte dei dati di payload dell’evento e che consente al sistema di identificare la persona associata all’evento. La chiave può essere, ad esempio, l’ID Experience Cloud, un ID del sistema di gestione delle relazioni con i clienti o un indirizzo e-mail.

Per utilizzare i dati memorizzati nel database Real-time Customer Profile di Adobe, la chiave dell’evento deve essere costituita dalle informazioni definite come identità di un profilo nel [Servizio Profilo cliente in tempo reale](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target="_blank"}.

L’identificatore di profilo consente al sistema di eseguire la riconciliazione tra l’evento e il profilo dell’individuo. Se selezioni uno schema con un’identità primaria, il **[!UICONTROL Identificatore profilo]** e **[!UICONTROL Namespace]** i campi sono precompilati. Se non è stata definita alcuna identità, il _identityMap > id_ è la chiave primaria. Quindi devi selezionare uno spazio dei nomi e la chiave viene automaticamente precompilata utilizzando _identityMap > id_.

Quando selezioni i campi, vengono taggati i campi di identità primari.

![](assets/primary-identity.png)

Se devi utilizzare una chiave diversa, ad esempio un ID CRM o un indirizzo e-mail, devi aggiungerla manualmente, come spiegato di seguito:

1. Fai clic all’interno del **[!UICONTROL Identificatore profilo]** o sull&#39;icona della matita.

   ![](assets/journey16.png)

1. Seleziona il campo scelto come chiave nell’elenco dei campi del payload. Puoi anche passare all’editor di espressioni avanzate per creare chiavi più complesse (ad esempio, una concatenazione di due campi degli eventi).

   ![](assets/journey20.png)

Quando l’evento viene ricevuto, il valore della chiave consente al sistema di identificare la persona associata all’evento. Associato a uno spazio dei nomi (vedere [questa sezione](../event/about-creating.md#select-the-namespace)), la chiave può essere utilizzata per eseguire query su Adobe Experience Platform. Consulta [questa pagina](../building-journeys/about-journey-activities.md#orchestration-activities).
La chiave viene utilizzata anche per verificare che una persona appartenga a un percorso. Infatti, una persona non può trovarsi in due luoghi diversi nello stesso percorso. Di conseguenza, il sistema non consente che la stessa chiave, ad esempio la chiave CRMID=3224, si trovi in luoghi diversi nello stesso percorso.

È inoltre possibile accedere alle funzioni di espressione avanzate (**[!UICONTROL Modalità avanzata]**) se desideri eseguire ulteriori manipolazioni. Queste funzioni ti consentono di manipolare i valori utilizzati per eseguire query specifiche, ad esempio per modificare i formati e eseguire concatenazioni di campi, tenendo conto solo di una parte di un campo (ad esempio i primi 10 caratteri). Consulta questa [pagina](../building-journeys/expression/expressionadvanced.md).

## Anteprima del payload {#preview-the-payload}

L’anteprima del payload consente di convalidare la definizione del payload.

>[!NOTE]
>
>Per gli eventi generati dal sistema, quando crei un evento, prima di visualizzare l’anteprima del payload, salva l’evento e riaprilo. Questo passaggio è necessario per generare un ID evento nel payload.

1. Fai clic su **[!UICONTROL Visualizza payload]** per visualizzare in anteprima il payload previsto dal sistema.

   ![](assets/journey13.png)

   È possibile notare che vengono visualizzati i campi selezionati.

   ![](assets/journey14.png)

1. Controlla l’anteprima per convalidare la definizione del payload.

1. Quindi, puoi condividere l’anteprima del payload con alla persona responsabile dell’invio dell’evento. Questo payload può aiutarli a progettare la configurazione di un evento che invia a [!DNL Journey Optimizer]. Consulta [questa pagina](../event/additional-steps-to-send-events-to-journey.md).
