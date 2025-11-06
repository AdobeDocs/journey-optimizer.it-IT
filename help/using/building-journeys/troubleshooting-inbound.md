---
solution: Journey Optimizer
product: journey optimizer
title: Guida alla risoluzione dei problemi per le azioni in entrata nei percorsi
description: Scopri come eseguire il debug e risolvere i problemi relativi alle azioni in entrata in percorsi Adobe Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: azioni in entrata, risoluzione dei problemi, percorso, debug, supporto autonomo, controllo, errori
exl-id: 5c56786f-da22-4558-b2ae-01f762175a7f
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '1654'
ht-degree: 1%

---

# Risoluzione dei problemi relativi alle azioni in entrata nei percorsi {#troubleshooting-inbound-actions}

Le azioni in entrata, ad esempio le esperienze in-app, web e basate su codice, sono componenti critici di [!DNL Journey Optimizer] in quanto consentono un coinvolgimento personalizzato con gli utenti durante il percorso. Tuttavia, possono verificarsi comportamenti imprevisti, ad esempio contenuto in entrata mancante o consegna continua dopo che un profilo esce dal percorso.

Questa guida fornisce una procedura dettagliata per eseguire il debug dei problemi relativi alle azioni in entrata in un percorso, per aiutarti a identificarli e risolverli in modo indipendente prima di contattare il supporto tecnico.

<!--This guide addresses the two most common scenarios with inbound actions in a journey. They are as follows:

* A profile enters the inbound step, but the user does not receive the expected inbound content.
* A user continues to receive inbound content even after the profile exits the journey.
-->

## Prerequisiti {#prerequisites}

Prima di iniziare la risoluzione dei problemi, verificare quanto segue:

1. Configura una sessione **Assurance**. Scopri come fare nella [documentazione di Adobe Experience Platform Assurance](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/tutorials/using-assurance){target="_blank"}.

1. Passa al percorso contenente l’azione in entrata per recuperare il nome del percorso e l’ID della versione.

   >[!NOTE]
   >
   >L&#39;ID versione percorso si trova nell&#39;URL dopo &#39;percorso/&#39; (ad esempio: *86232fb1-2932-4036-8198-55dfec606fd7*).

   ![](assets/troubleshoot-inbound-retrieve-journey-id.png)

1. Fai clic sull’azione in entrata per visualizzarne i dettagli. Recupera l’etichetta e l’ID dell’azione in entrata.

   ![](assets/troubleshoot-inbound-retrieve-action-id.png)

1. Ottieni lo spazio dei nomi e l’ID del profilo per identificare il profilo che incontra problemi. In base alla configurazione, ad esempio, lo spazio dei nomi può essere ECID, e-mail o ID cliente. Scopri come cercare un profilo nella [documentazione di Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide#browse-identity){target="_blank"}.

## Scenario 1: l’utente non ha ricevuto il contenuto in entrata {#scenario-1}

In questo scenario, un profilo ha inserito l’azione in entrata nel percorso, ma anche dopo 30 minuti, il contenuto in entrata corrispondente non viene visualizzato nel dispositivo/client al passaggio dell’attivazione della configurazione.


### Controlli preliminari {#pre-checks}

1. **Il set di dati in entrata del Percorso è abilitato per l&#39;acquisizione del profilo**

   L&#39;azione in entrata utilizza il set di dati **Percorso in entrata** per gli aggiornamenti del profilo durante l&#39;esecuzione. Assicurati che il set di dati sia abilitato per i profili nella sandbox corrente. [Ulteriori informazioni sui set di dati](../data/get-started-datasets.md)

2. Identità &#39;joai&#39; **definita nelle identità della piattaforma**

   L&#39;azione in entrata utilizza lo spazio dei nomi **joai** nel profilo `segmentMembership` per attivare il profilo per il passaggio in entrata. Assicurati che sia stato definito in Platform Identities per la sandbox. Ulteriori informazioni su [Servizio Experience Platform Identity](https://experienceleague.adobe.com/en/docs/experience-platform/identity/home){target="_blank"}

### Passaggi del debug {#debugging-steps}

Il grafico seguente mostra la sequenza dei passaggi di debug che puoi seguire:

![](assets/troubleshoot-inbound-scenario-1-steps.png){width="70%" align="center"}

### Passaggio 1: verifica se il dispositivo/client riceve il contenuto da Edge Network {#step-1}

Per prima cosa, controlla se il dispositivo/client riceve il contenuto previsto.

>[!BEGINTABS]

>[!TAB Canale in-app]

1. Vai alla sessione [Assurance](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/tutorials/using-assurance){target="_blank"} e seleziona la sezione **[!UICONTROL Messaggistica in-app]** dal pannello a sinistra.

1. Nella scheda **[!UICONTROL Messaggi sul dispositivo]**, fare clic sull&#39;elenco a discesa **[!UICONTROL Messaggi]**.

   ![](assets/troubleshoot-inbound-assurance-in-app.png){width="80%"}

1. Cerca un messaggio con il nome del percorso seguito da &quot;- Messaggio in-app&quot;. Se presente, significa che il messaggio in-app è presente sul dispositivo/client e il problema potrebbe essere correlato al trigger in-app.

1. Se il messaggio non viene trovato, significa che il dispositivo o il client non ha ricevuto il messaggio in-app. <!--Go to the [next step](#step-2) for further debugging.-->

>[!TAB Canale web]

Visita la pagina e controlla la scheda di rete oppure controlla il payload di risposta di Edge nella sezione **[!UICONTROL Edge Delivery]** della sessione [Assurance](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/tutorials/using-assurance){target="_blank"}.

>[!TAB Canale esperienza basato su codice]

Esegui una richiesta curl utilizzando [API di Adobe](https://developer.adobe.com/data-collection-apis/docs/api/) e controlla il payload di risposta di Edge nella sezione **[!UICONTROL Edge Delivery]** della sessione [Assurance](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/tutorials/using-assurance){target="_blank"}.

>[!ENDTABS]

### Passaggio 2: verifica se Edge Network restituisce il contenuto {#step-2}

Questo passaggio consente di assicurarsi che Edge Network restituisca il contenuto in entrata previsto da riprodurre sul dispositivo/client.

Quando un profilo entra in un&#39;azione in entrata in un percorso, viene automaticamente qualificato in un segmento di pubblico speciale (nello spazio dei nomi **joai**) corrispondente all&#39;azione del percorso in entrata.

Quando un client effettua una richiesta all&#39;Edge Network per un profilo e una superficie specifici, il profilo è idoneo a ricevere il contenuto per le azioni del percorso in entrata che hanno come destinazione tale superficie, solo se il profilo è attualmente membro del segmento **joai** corrispondente.

Per eseguire il debug del comportamento di Edge Network, segui i passaggi seguenti.

1. Apri la visualizzazione **[!UICONTROL Edge Delivery]** nella sessione di Assurance. Questa vista fornisce informazioni sull’esecuzione dell’azione in entrata sul server Edge Network. Per ulteriori informazioni, consulta la [documentazione di Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}.

1. Verifica se l&#39;attività Edge corrispondente all&#39;azione in entrata è elencata nelle sezioni **[!UICONTROL Attività qualificate]** o **[!UICONTROL Attività non qualificate]**.

   ![](assets/troubleshoot-inbound-edge-delivery.png)

   * Se nella sezione **Attività qualificate**, il profilo è qualificato per l&#39;azione di percorso in entrata e il contenuto deve essere restituito.
   * Se nella sezione **Attività non qualificate** il profilo non è idoneo per l&#39;azione di percorso in entrata. Per ulteriori dettagli, consulta i motivi di esclusione.
   * Se in **nessuna sezione** si è verificato un problema con la pubblicazione dell&#39;azione di percorso in entrata in Edge Network oppure l&#39;URI della superficie richiesta non corrisponde alle impostazioni di configurazione del canale per l&#39;azione in entrata.

   >[!NOTE]
   >
   >Per trovare l&#39;attività Edge nella sessione **Assurance**, cerca l&#39;attività in cui **[!UICONTROL audienceNamespace]** è **joai** e **[!UICONTROL audienceSegmentId]** è &lt;*JourneyVersionID*>_&lt;*JourneyActionID*> (ad esempio: *86232fb1-2932-4036-8198-55dfec606fd7_708f718d-8503-4427-ad8d-8e28979b554c*).

   ![](assets/troubleshoot-inbound-edge-delivery-unqualified.png){width="70%"}

1. Se l&#39;attività si trova nella sezione **[!UICONTROL Attività non qualificate]** e il motivo dell&#39;esclusione è *&#39;Il segmento non è attivo&#39;*, significa che il server di consegna Edge Network non ritiene che il profilo faccia parte del segmento di pubblico **joai** rilevante.

   Puoi verificare se il segmento **joai** è presente nella vista del profilo del server di consegna Edge Network aprendo l&#39;elemento **segmentsMap** della sezione Profile e cercando la presenza dell&#39;ID del segmento **joai**.

1. Se il server di consegna Edge Network non visualizza il profilo come nel segmento **joai** pertinente, passa al passaggio successivo.<!--use the Platform Profile viewer UI to check if the expected **joai** segment is in a realized state in the Edge profile. Learn more in the [Experience Platform Profile UI documentation](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide){target="_blank"}-->

### Passaggio 3: verifica se l’iscrizione al pubblico &quot;joai&quot; è stata propagata ad Edge Network {#step-3}

Questo passaggio consente di verificare che il profilo Edge sia stato aggiornato correttamente quando il profilo è entrato nell&#39;azione del percorso in entrata e che sia stato qualificato nel segmento **joai** corrispondente.

Quando un profilo viene qualificato per un segmento **joai**, viene prima aggiornato nell&#39;hub e quindi l&#39;appartenenza al segmento viene proiettata nel profilo Edge per l&#39;utilizzo da parte del server di consegna Edge Network.

>[!NOTE]
>
>La propagazione dall’hub ad Edge può richiedere fino a 15-30 minuti dal momento in cui il profilo viene aggiornato sull’hub.

Per verificare la presenza del segmento **joai** nell&#39;attributo `segmentMembership` del profilo di Edge, eseguire la procedura seguente.

1. Passa al menu **[!UICONTROL Cliente]** > **[!UICONTROL Profili]** nel riquadro di navigazione sinistro di [!DNL Journey Optimizer] e individua il profilo utilizzando lo spazio dei nomi e l&#39;ID. Ulteriori informazioni su [Profili cliente in tempo reale](../audience/get-started-profiles.md)

1. Selezionare la scheda **[!UICONTROL Attributi]** e scegliere la visualizzazione **[!UICONTROL Edge]**.

1. Fare clic su **[!UICONTROL Visualizza JSON]** per aprire la visualizzazione JSON per il profilo.

   ![](assets/troubleshoot-inbound-profile-view-json.png){width="80%"}

1. Vai all&#39;attributo `segmentMembership` e controlla se l&#39;ID segmento &lt;*JourneyVersionID>*_&lt;*JourneyActionID*> è presente nello spazio dei nomi **joai** e se in **[!UICONTROL realized]** <!--or existing?-->status.

   ![](assets/troubleshoot-inbound-profile-json-realized.png){width="90%"}

   * Se presente, il segmento **joai** corrispondente all&#39;azione del percorso in entrata è stato propagato correttamente al profilo Edge.

   * Se non viene visualizzata nella vista del profilo del server di consegna Edge Network, potrebbe essersi verificato un problema con il modo in cui il server di consegna carica il profilo Edge.

1. Se l&#39;ID segmento **joai** non è presente o è nello stato **[!UICONTROL exited]**, significa che non è stato (ancora) propagato ad Edge.

   Attendere 15-30 minuti per la propagazione dei valori `segmentMembership` dall&#39;hub ad Edge. Se non è ancora presente, andare al passaggio successivo.

<!--The next step is to check whether the audience segment is present in the profile on the Hub.-->

### Passaggio 4: verifica se l’iscrizione al pubblico &quot;joai&quot; è presente nel profilo sull’hub {#step-4}

Questo passaggio consente di verificare che il profilo Hub sia stato aggiornato correttamente quando il profilo è entrato nell&#39;azione del percorso in entrata e che sia stato qualificato nel segmento **joai** corrispondente.

>[!NOTE]
>
>L&#39;acquisizione dell&#39;appartenenza al segmento **joai** nel profilo Hub può richiedere fino a 15-30 minuti dal momento in cui il profilo è entrato nell&#39;azione di percorso in entrata.

Per verificare la presenza del segmento **joai** nell&#39;attributo `segmentMembership` del profilo Hub, eseguire la procedura seguente.

1. Passa al menu **[!UICONTROL Cliente]** > **[!UICONTROL Profili]** nel riquadro di navigazione sinistro di [!DNL Journey Optimizer] e individua il profilo utilizzando lo spazio dei nomi e l&#39;ID. Ulteriori informazioni su [Profili cliente in tempo reale](../audience/get-started-profiles.md)

1. Seleziona la scheda **[!UICONTROL Attributi]** e scegli la visualizzazione **[!UICONTROL Hub]**.

1. Fare clic su **[!UICONTROL Visualizza JSON]** per aprire la visualizzazione JSON per il profilo.

1. Vai all&#39;attributo **[!UICONTROL segmentMembership]** e controlla se l&#39;ID segmento &lt;*JourneyVersionID>*_&lt;*JourneyActionID*> è presente nello spazio dei nomi **joai** e se è nello stato **[!UICONTROL realized]** <!--or existing?-->.

   * Se presente, il segmento **joai** corrispondente all&#39;azione del percorso in entrata è stato correttamente acquisito nel profilo Hub.

   * Se non viene trovato nel profilo di Edge dopo almeno 30 minuti, potrebbe essersi verificato un problema con il sistema di proiezione di Edge.

1. Se l&#39;ID del segmento **joai** non è presente o è nello stato **[!UICONTROL exited]**, significa che il profilo non è stato (ancora) qualificato correttamente nel segmento di pubblico **joai** speciale al momento dell&#39;immissione nell&#39;azione del percorso in entrata corrispondente.

   Attendere 15-30 minuti per l&#39;acquisizione dei valori `segmentMembership` nel profilo sull&#39;hub. Se non è ancora presente, andare al passaggio successivo.

### Passaggio 5: se il client/dispositivo non riceve ancora il contenuto previsto {#step-5}

Se hai eseguito tutti i passaggi precedenti e non vedi il comportamento previsto dopo 30-60 minuti di attesa che l’iscrizione al segmento si propaghi ad Edge Network, contatta l’Assistenza clienti di Adobe o il tuo rappresentante Adobe.

Includi tutti i dettagli possibili dai passaggi di debug, ad esempio:

* il passaggio in cui si verifica il comportamento imprevisto;
* l’ID versione del percorso;
* l’ID dell’azione del percorso;
* la traccia completa di Assurance;
* la vista JSON del profilo Edge;
* la vista JSON del profilo dell’hub;
* ecc.

## Scenario 2: l’utente sta ancora ricevendo il contenuto in entrata {#scenario-2}

Questo scenario è inverso a [Scenario 1](#scenario-1): il profilo è uscito dal percorso, ma l&#39;utente sta ancora ricevendo il contenuto in entrata.

Tuttavia, quando un profilo esce da un percorso, non dovrebbe più essere idoneo per i segmenti di pubblico **joai** corrispondenti alle azioni in entrata nel percorso.

Segui gli stessi passaggi di debug dello [Scenario 1](#debugging-steps) per verificare se il profilo Hub, il profilo Edge e il server di consegna Edge Network riflettono correttamente lo stato di appartenenza al segmento del segmento **joai** pertinente e se il client non riceve più il contenuto in entrata.

<!--

## Reference Section {#reference-section}

- [Assurance Setup Guide](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/tutorials/using-assurance)
- [Adobe Experience Platform Documentation](https://experienceleague.adobe.com/docs/experience-platform/home.html)
- [Streaming Ingestion APIs Troubleshooting](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html)

-->
