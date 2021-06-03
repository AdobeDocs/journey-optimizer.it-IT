---
title: Configurare un evento unitario
description: Scopri come configurare un evento unitario
source-git-commit: 4464ea7169424c1ec6212394b8bda79a9bec1913
workflow-type: tm+mt
source-wordcount: '1636'
ht-degree: 14%

---

# Configurare un evento unitario {#configure-an-event}

![](../assets/do-not-localize/badge.png)

Gli eventi unitari sono collegati a un profilo specifico. Possono essere basati su regole o generati dal sistema.  Ulteriori informazioni sull&#39;evento unitario [questa sezione](../event/about-events.md).

Di seguito sono riportati i primi passaggi per configurare un nuovo evento:

1. Nella sezione AMMINISTRAZIONE, seleziona **[!UICONTROL Configurations]**, quindi fai clic su **[!UICONTROL Events]**. Viene visualizzato l’elenco degli eventi.

   ![](../assets/jo-event1.png)

1. Per creare un nuovo evento, fai clic su **[!UICONTROL Add]**. Il riquadro di configurazione dell’evento si apre sul lato destro dello schermo.

   ![](../assets/jo-event2.png)

1. Inserisci il nome dell’evento. Puoi anche aggiungere una descrizione.

   ![](../assets/jo-event3.png)

   >[!NOTE]
   >
   >Non utilizzare spazi o caratteri speciali. Non usare più di 30 caratteri.

1. Nel campo **[!UICONTROL Type]**, scegli **Eventi unitari**.

   ![](../assets/jo-event3bis.png)

1. Nel campo **[!UICONTROL Event ID type]** , seleziona il tipo di ID evento da utilizzare: **Basato su regole** o **generato dal sistema**. Ulteriori informazioni sui tipi di ID evento in [questa sezione](../event/about-events.md#event-id-type).

   ![](../assets/jo-event4.png)

1. Il numero di percorsi che utilizzano questo evento viene visualizzato nel campo **[!UICONTROL Used in]**. Puoi fare clic sull’icona **[!UICONTROL View journeys]** per visualizzare l’elenco dei percorsi che utilizzano questo evento.

1. Definisci i campi dello schema e del payload: in questo punto è possibile selezionare le informazioni sull’evento (solitamente denominato payload) che i percorsi prevedono di ricevere. Potrai quindi utilizzare queste informazioni nel tuo percorso. Vedi [questa sezione](../event/about-creating.md#define-the-payload-fields).

   ![](../assets/jo-event5.png)

   >[!NOTE]
   >
   >Quando selezioni il tipo **[!UICONTROL System Generated]** , sono disponibili solo gli schemi con il mixin del tipo eventID. Quando selezioni il tipo **[!UICONTROL Rule Based]** , sono disponibili tutti gli schemi Experience Event .

1. Per gli eventi basati su regole, fai clic all’interno del campo **[!UICONTROL Event ID condition]** . Utilizzando l’editor di espressioni semplici, definisci la condizione che verrà utilizzata dal sistema per identificare gli eventi che attiveranno il percorso.
   ![](../assets/jo-event6.png)

   Nel nostro esempio, abbiamo scritto una condizione basata sulla città del profilo. Ciò significa che ogni volta che il sistema riceve un evento che corrisponde a questa condizione (**[!UICONTROL City]** field e **[!UICONTROL Paris]** value), lo trasmette ai percorsi.

1. Aggiungi uno spazio dei nomi. Questo passaggio è facoltativo ma consigliato, poiché l’aggiunta di uno spazio dei nomi consente di sfruttare le informazioni memorizzate nel servizio Profilo cliente in tempo reale, definendo il tipo di chiave di cui dispone l’evento. Vedi [questa sezione](../event/about-creating.md#select-the-namespace).
1. Definisci la chiave: scegli un campo di payload o specifica una formula per identificare la persona associata all’evento. Se selezioni uno spazio dei nomi, questa chiave viene impostata automaticamente, ma può essere comunque modificata. In effetti, percorsi seleziona la chiave che deve corrispondere allo spazio dei nomi (ad esempio, se selezioni uno spazio dei nomi e-mail, verrà selezionata la chiave e-mail). Vedi [questa sezione](../event/about-creating.md#define-the-event-key).

   ![](../assets/jo-event7.png)

1. Per gli eventi generati dal sistema, puoi aggiungere una condizione . Questo passaggio è facoltativo. In tal modo, consenti al sistema di elaborare solo gli eventi che soddisfano la condizione specifica. Tale condizione può essere basata solo sulle informazioni contenute nell’evento. Vedi [questa sezione](../event/about-creating.md#add-a-condition).
1. Fai clic su **[!UICONTROL Save]**.

   ![](../assets/journey7.png)

   L’evento è ora configurato e pronto per essere rilasciato in un percorso. Per poter ricevere gli eventi sono necessari ulteriori passaggi di configurazione. Consulta [questa pagina](../event/additional-steps-to-send-events-to-journey-orchestration.md).

## Definire i campi payload {#define-the-payload-fields}

La definizione del payload ti consente di scegliere le informazioni che il sistema prevede di ricevere dall’evento nel tuo percorso e la chiave per identificare quale persona è associata all’evento. Il payload si basa sulla definizione del campo XDM di Experience Cloud. Per ulteriori informazioni su XDM, consulta [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it).

1. Seleziona uno schema XDM dall’elenco e fai clic sul campo **[!UICONTROL Payload]** o sull’icona **[!UICONTROL Edit]**.

   ![](../assets/journey8.png)

   Vengono visualizzati tutti i campi definiti nello schema. L’elenco dei campi varia da uno schema all’altro. È possibile cercare un campo specifico o utilizzare i filtri per visualizzare tutti i nodi e i campi o solo i campi selezionati. In base alla definizione dello schema, alcuni campi possono essere obbligatori e preselezionati. Non è possibile deselezionarli. Per impostazione predefinita, tutti i campi obbligatori affinché l’evento possa essere ricevuto correttamente dai percorsi sono selezionati.

   >[!NOTE]
   >
   >Accertati di aver aggiunto il mixin &quot;orchestrazione&quot; allo schema XDM. Questo assicurerà che lo schema contenga tutte le informazioni necessarie per funzionare con [!DNL Journey Optimizer].

   ![](../assets/journey9.png)

1. Seleziona i campi che si prevede di ricevere dall’evento. Questi sono i campi che l&#39;utente aziendale sfrutterà nel percorso. Devono inoltre includere la chiave che verrà utilizzata per identificare la persona associata all&#39;evento (consulta [questa sezione](../event/about-creating.md#define-the-event-key)).

   ![](../assets/journey10.png)

   >[!NOTE]
   >
   >Per gli eventi generati dal sistema, il campo **[!UICONTROL eventID]** viene aggiunto automaticamente nell’elenco dei campi selezionati in modo che [!DNL Journey Optimizer] possa identificare l’evento. Il sistema che preme l’evento non deve generare un ID, ma deve utilizzare quello disponibile nell’anteprima del payload. Vedi [questa sezione](../event/about-creating.md#preview-the-payload).

1. Dopo aver selezionato i campi necessari, fai clic su **[!UICONTROL Save]** o premi **[!UICONTROL Enter]**.

   ![](../assets/journey11.png)

   Il numero di campi selezionati viene visualizzato nel campo **[!UICONTROL Payload]** .

   ![](../assets/journey12.png)

## Seleziona lo spazio dei nomi {#select-the-namespace}

Lo spazio dei nomi ti consente di definire il tipo di chiave utilizzata per identificare la persona associata all’evento. La configurazione è facoltativa. È richiesto se desideri recuperare, nei tuoi percorsi, informazioni aggiuntive provenienti dal [Profilo del cliente in tempo reale](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html). La definizione dello spazio dei nomi non è necessaria se utilizzi solo dati provenienti da un sistema di terze parti tramite un’origine dati personalizzata.

È possibile utilizzare uno dei predefiniti oppure crearne uno nuovo utilizzando il servizio Namespace Identity. Fai riferimento a questa [pagina](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html).

Se selezioni uno schema con un&#39;identità primaria, i campi **[!UICONTROL Key]** e **[!UICONTROL Namespace]** sono precompilati. Se non è definita alcuna identità, selezioniamo _identityMap > id_ come chiave primaria. Quindi devi selezionare uno spazio dei nomi e la chiave verrà precompilata (sotto il campo **[!UICONTROL Namespace]** ) utilizzando _identityMap > id_.

Durante la selezione dei campi, i campi di identità principali vengono contrassegnati con tag.

![](../assets/primary-identity.png)


Seleziona uno spazio dei nomi dall’elenco a discesa.

![](../assets/journey17.png)

È consentito un solo spazio dei nomi al percorso. Se utilizzi più eventi nello stesso percorso, è necessario che utilizzino lo stesso namespace. Consulta [questa pagina](../building-journeys/journey.md).

## Definire la chiave evento {#define-the-event-key}

La chiave è il campo o la combinazione di campi che fa parte dei dati di payload dell’evento e che consentirà al sistema di identificare la persona associata all’evento. La chiave può essere, ad esempio, l&#39;ID Experience Cloud, un ID CRM o un indirizzo e-mail.

Se prevedi di sfruttare i dati memorizzati nel database Profilo cliente in tempo reale, devi selezionare, come chiave evento, le informazioni definite come identità del profilo nel [Servizio Profilo cliente in tempo reale](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html).

Consentirà al sistema di eseguire la riconciliazione tra l’evento e il profilo del singolo utente. Se selezioni uno schema con un&#39;identità primaria, i campi **[!UICONTROL Key]** e **[!UICONTROL Namespace]** sono precompilati. Se non è definita alcuna identità, selezioniamo _identityMap > id_ come chiave primaria. Quindi devi selezionare uno spazio dei nomi e la chiave verrà precompilata (sotto il campo **[!UICONTROL Namespace]** ) utilizzando _identityMap > id_.

Durante la selezione dei campi, i campi di identità principali vengono contrassegnati con tag.

![](../assets/primary-identity.png)

Se devi utilizzare una chiave diversa, ad esempio un ID CRM o un indirizzo e-mail, devi aggiungerla manualmente:

1. Fai clic all’interno del campo **[!UICONTROL Key]** o sull’icona della matita.

   ![](../assets/journey16.png)

1. Seleziona il campo scelto come chiave nell’elenco dei campi payload. Puoi anche passare all’editor di espressioni avanzate per creare chiavi più complesse (ad esempio, una concatenazione di due campi degli eventi). Vedi sotto, in questa sezione.

   ![](../assets/journey20.png)

Quando l’evento viene ricevuto, il valore della chiave consentirà al sistema di identificare la persona associata all’evento. Associata a uno spazio dei nomi (consulta [questa sezione](../event/about-creating.md#select-the-namespace)), può essere utilizzata per eseguire query su Adobe Experience Platform. Consulta [questa pagina](../building-journeys/about-journey-activities.md#orchestration-activities).
La chiave viene utilizzata anche per verificare che una persona si trovi in un percorso. Infatti, una persona non può trovarsi in due luoghi diversi nello stesso percorso. Di conseguenza, il sistema non consente che la stessa chiave, ad esempio la chiave CRMID=3224, si trovi in luoghi diversi nello stesso percorso.

Puoi anche accedere alle funzioni di espressione avanzate (**[!UICONTROL Advanced mode]**) per eseguire ulteriori manipolazioni. Queste funzioni consentono di manipolare i valori utilizzati per eseguire query specifiche, ad esempio la modifica dei formati, l’esecuzione di concatenazioni di campi, tenendo conto solo di una parte di un campo (ad esempio i 10 primi caratteri). Consulta [questa pagina](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html).

## Aggiungi una condizione {#add-a-condition}

La condizione è disponibile solo per gli eventi generati dal sistema. Puoi definire una condizione di evento che consente al sistema di filtrare l’elaborazione degli eventi. Se la condizione è true, l’evento viene elaborato. Se la condizione non è vera, l’evento viene ignorato.

La condizione relativa agli eventi può essere basata solo sui dati passati nel payload dell’evento. La condizione definita a livello di evento non può essere modificata nell’area di lavoro da un addetto al marketing. Lo scopo è quello di indurire questa condizione quando viene utilizzato questo evento. Ad esempio, se non vuoi che gli esperti di marketing utilizzino eventi di abbandono carrello se il valore del carrello è troppo piccolo, puoi creare una condizione sul campo evento &quot;valore del carrello&quot; e imporre un valore superiore a 100 dollari.

Puoi utilizzare l’editor di espressioni semplici o l’editor di espressioni avanzate per impostare le condizioni sugli eventi. Consulta [questa pagina](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html).

Ad esempio, puoi definire una condizione per elaborare solo gli eventi di un tipo di evento specifico e ignorare gli altri tipi. Oppure, se l’evento è un abbandono del carrello e il payload include il campo del valore del carrello, puoi definire una condizione di evento per elaborare gli eventi solo se il valore del carrello è maggiore di 100 dollari.

![](../assets/journey78.png)

## Anteprima del payload {#preview-the-payload}

L’anteprima del payload ti consente di convalidare la definizione del payload.

>[!NOTE]
>
>Per gli eventi generati dal sistema, quando crei un evento, prima di visualizzare l’anteprima del payload, salva l’evento e riaprilo. Questo passaggio è necessario per generare un ID evento nel payload.

1. Fai clic sull&#39;icona **[!UICONTROL View Payload]** per visualizzare in anteprima il payload previsto dal sistema.

   ![](../assets/journey13.png)

   I campi selezionati vengono visualizzati.

   ![](../assets/journey14.png)

1. Seleziona l’anteprima per convalidare la definizione del payload.

1. Quindi, puoi condividere l’anteprima del payload con la persona responsabile dell’invio dell’evento. Questo payload può aiutarlo a progettare la configurazione di un evento che preme su [!DNL Journey Optimizer]. Consulta [questa pagina](../event/additional-steps-to-send-events-to-journey-orchestration.md).
