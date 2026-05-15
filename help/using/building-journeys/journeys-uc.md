---
solution: Journey Optimizer
product: journey optimizer
title: Casi di utilizzo dei percorsi
description: Casi di utilizzo dei percorsi
feature: Journeys, Use Cases, Email, Push
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: caso d’uso, multicanale, messaggi, percorso, canale, eventi, push
exl-id: a1bbfcee-2235-4820-a391-d5d35f499cb0
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/o4-7bKdQzB3Yyz22khT4RHNpNvKL0sCg8YPPnaeav9I
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: d8353d85-5da7-453d-bd68-40ad33fa0ab7id: e57d1da4-32c2-4cc6-945c-9feb219156ffid: ebd64fe4-362a-4a1c-9476-b2573ed12a95id: fa683eda-48de-4558-af32-2673edcd44feid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 1060
ht-degree: 1%

---

# Inviare messaggi multicanale {#send-multi-channel-messages}

Questa sezione presenta un caso d’uso che combina un Read Audience, un evento, eventi di reazione e messaggi e-mail/push.

![Flusso di percorso semplice con attività Read Audience, Wait e Email](assets/jo-uc1.png)

## Descrizione del caso d’uso

In questo caso d’uso, l’obiettivo è quello di inviare un primo messaggio e-mail a tutti i clienti appartenenti a un pubblico specifico.

In base alla loro reazione al primo messaggio, vengono inviati messaggi di follow-up specifici.

Se il cliente apre l’e-mail, il sistema attende un acquisto e invia un messaggio push per ringraziare il cliente.

In assenza di reazioni, viene inviata un’e-mail di follow-up.

## Prerequisiti

Affinché questo caso d’uso funzioni, configura quanto segue:

* Un pubblico per tutti i clienti che vivono ad Atlanta, San Francisco o Seattle e sono nati dopo il 1980
* Un evento di acquisto

### Creare il pubblico

In questo percorso, viene utilizzato un pubblico specifico di clienti. Tutti gli individui appartenenti al pubblico entrano nel percorso e seguono i diversi passaggi. In questo esempio, il pubblico esegue il targeting di tutti i clienti che vivono ad Atlanta, San Francisco o Seattle e sono nati dopo il 1980.

Per ulteriori informazioni sui tipi di pubblico, [fai riferimento a questa pagina](../audience/about-audiences.md).

1. Dalla sezione del menu CUSTOMER, seleziona **[!UICONTROL Tipi di pubblico]**.
1. Fai clic sul pulsante **[!UICONTROL Crea pubblico]** in alto a destra nell&#39;elenco del pubblico.
1. Nel riquadro **[!UICONTROL Proprietà pubblico]** immettere un nome per il pubblico.
1. Trascina e rilascia i campi desiderati dal riquadro di sinistra all’area di lavoro centrale e configurali in base alle tue esigenze. In questo esempio, utilizzare i campi attributo **Città** e **Anno di nascita**.
1. Fai clic su **[!UICONTROL Salva]**.

   ![Pannello Attributi aggiuntivi per la selezione dei dati di arricchimento](assets/add-attributes.png)

Il pubblico ora è stato creato ed è pronto per essere utilizzato nel percorso. Utilizzando un&#39;attività **Read Audience**, tutti gli utenti appartenenti al pubblico possono entrare nel percorso.

### Configurare l’evento

Configura un evento inviato al percorso quando un cliente effettua un acquisto. Quando il percorso riceve l&#39;evento, attiva il messaggio di ringraziamento.

Per questo, utilizza un [evento basato su regole](../event/about-events.md).

1. Nella sezione del menu AMMINISTRAZIONE, seleziona **[!UICONTROL Configurazioni]**, quindi fai clic su **[!UICONTROL Eventi]**. Fai clic su **[!UICONTROL Crea evento]** per creare un nuovo evento.

1. Inserisci il nome dell’evento.

1. Nel campo **[!UICONTROL Tipo ID evento]**, seleziona **[!UICONTROL Basato su regole]**.

1. Definisci lo **[!UICONTROL Schema]** e il payload **[!UICONTROL Campi]**. Utilizza diversi campi, ad esempio il prodotto acquistato, la data di acquisto e l’ID acquisto.

1. Nel campo **[!UICONTROL Condizione ID evento]**, definire la condizione utilizzata dal sistema per identificare gli eventi che attivano il percorso. Ad esempio, aggiungere un campo `purchaseMessage` e definire la seguente regola: `purchaseMessage="thank you"`

1. Definisci **[!UICONTROL Spazio dei nomi]** e **[!UICONTROL Identificatore profilo]**.

1. Fai clic su **[!UICONTROL Salva]**.

   ![Percorso con attività Condizione ramificato in membri Gold e altri percorsi](assets/jo-uc2.png)

L’evento è ora configurato e pronto per essere utilizzato nel percorso. Utilizzando l’attività evento corrispondente, è possibile attivare un’azione ogni volta che un cliente effettua un acquisto.

## Progettare il percorso

1. Avvia il percorso con un&#39;attività **Read Audience**. Seleziona il pubblico creato in precedenza. Tutti gli individui appartenenti al pubblico entrano nel percorso.

   ![Verifica delle condizioni meteorologiche se la temperatura è inferiore a 50 gradi](assets/jo-uc4.png)

1. Rilascia un&#39;attività di azione **E-mail** e definisci il contenuto del &quot;primo messaggio&quot;. Questo messaggio viene inviato a tutti i singoli utenti del percorso. Consulta questa [sezione](../email/create-email.md) per scoprire come configurare e progettare un messaggio e-mail.

   ![percorso completo basato sul meteo con condizione di temperatura e azioni e-mail](assets/jo-uc5.png)

1. Aggiungi un evento **Reaction** e seleziona **Email open**. L’evento viene attivato quando una persona appartenente al pubblico apre l’e-mail.

1. Seleziona la casella **Definisci il timeout dell&#39;evento**, definisci una durata (1 giorno in questo esempio) e seleziona **Imposta un percorso di timeout**. In questo modo viene creato un altro percorso per i singoli utenti che non aprono il primo messaggio push o e-mail.

1. Nel percorso di timeout, rilascia un&#39;attività di azione **E-mail** e definisci il contenuto del messaggio di completamento. Questo messaggio viene inviato alle persone che non aprono l’e-mail o non inviano il primo messaggio push entro il giorno successivo. [Scopri come configurare e progettare un&#39;e-mail](../email/create-email.md).

1. Nel primo percorso, aggiungi l’evento di acquisto creato in precedenza. L’evento viene attivato quando un individuo effettua un acquisto.

1. Dopo l&#39;evento, rilascia un&#39;attività di azione **Push** e definisci il contenuto del messaggio di ringraziamento. Consulta questa [sezione](../push/create-push.md) per scoprire come configurare e progettare un push.

## Test e pubblicazione del percorso

1. Prima di eseguire il test del percorso, verificare che sia valido e che non vi siano errori.

1. Utilizza l&#39;interruttore **Test**, che si trova nell&#39;angolo in alto a destra, per attivare la modalità di test. Consulta questa [sezione](testing-the-journey.md) per scoprire come utilizzare la modalità di test.

1. Quando il percorso è pronto, pubblicalo utilizzando il pulsante **Pubblica**, in alto a destra.

## Percorso fedeltà multi-fase {#multi-phase-loyalty}

In questo esempio viene illustrato un pattern di architettura di percorso chiave: la decomposizione di un percorso complesso e multifase in percorsi secondari più piccoli e focalizzati connessi all&#39;attività [**[!UICONTROL Jump]**](jump.md). Un programma fedeltà funge da scenario, ma questo modello si applica a qualsiasi percorso che si estende su più milestone o fasi aziendali.

I percorsi multifase complessi generano rapidamente un gran numero di percorsi cliente univoci. La loro decomposizione in un percorso secondario per fase consente a ciascun percorso di essere gestito, testato e sottoposto a manutenzione in modo indipendente.

### Scenario

Considera un programma fedeltà che guida i clienti attraverso tre milestone utilizzando due canali di marketing ([email](../email/create-email.md) e [push](../push/create-push.md)):

1. **Fase 1 — Scaricare l&#39;app mobile:** Le comunicazioni iniziali incoraggiano i nuovi membri fedeltà a scaricare l&#39;app. Se il cliente non ha agito entro un determinato periodo, viene inviato un promemoria per il follow-up.
1. **Fase 2 - Effettuare una prima transazione:** Una volta scaricata l&#39;app, i messaggi mirati guidano i clienti verso il completamento della prima transazione fedeltà.
1. **Fase 3 - Effettuare una seconda transazione:** Dopo la prima transazione, un set finale di comunicazioni determina una seconda transazione per approfondire il coinvolgimento fedeltà.

Anche con questa semplice strategia, questo percorso espone più di 20 percorsi unici che un cliente può intraprendere. La complessità cresce in modo esponenziale con ogni punto di contatto o canale aggiuntivo.

### Scomposizione di sottogruppi di percorsi

Suddividere il percorso end-to-end in tre percorsi secondari collegati più piccoli:

| Percorso secondario | Condizione di ingresso | Obiettivo aziendale |
|---|---|---|
| Fase 1 — Download delle app | Il cliente aderisce al programma fedeltà | Promuovere il download di app per dispositivi mobili |
| Fase 2 — Prima operazione | Il cliente scarica l’app | Prima transazione fedeltà |
| Fase 3 — Seconda operazione | Il cliente completa la prima transazione | Incentivare la seconda transazione fedeltà |

Connetti i percorsi secondari utilizzando l&#39;attività [**[!UICONTROL Salta]**](jump.md) in modo che i profili passino senza problemi da una fase all&#39;altra. Ogni percorso secondario rimane semplice, leggibile e gestibile in modo indipendente.

<!--
>[!NOTE]
>
>If your goal is to build a gamified loyalty program with challenges, tasks, and built-in reward tracking, Journey Optimizer also offers a dedicated **Loyalty Challenges** capability.
-->

