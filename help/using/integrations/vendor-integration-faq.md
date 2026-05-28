---
solution: Journey Optimizer
product: journey optimizer
title: Domande frequenti sulle integrazioni
description: Domande frequenti sulle integrazioni di Journey Optimizer per dati e contenuti esterni nei messaggi.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: integrazione, domande frequenti, dati esterni, personalizzazione
subfeature_v2: []
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 852
ht-degree: 1%

---

# Domande frequenti sulle integrazioni {#vendor-integration-faq}

Di seguito sono riportate le domande frequenti sulle **integrazioni** in Adobe Journey Optimizer.


## Introduzione

+++ Cosa fanno le integrazioni in Journey Optimizer?

Collega origini dati esterne a Journey Optimizer per consentire di richiamare contenuti e dati da sistemi di terze parti nelle campagne e nei percorsi e personalizzare i messaggi utilizzando tali dati.

➡️ [Ulteriori informazioni sulla panoramica delle integrazioni](integrations.md)

+++

+++ Chi configura le integrazioni e chi le utilizza nel contenuto?

Gli amministratori creano e attivano la configurazione tecnica (**[!UICONTROL Configurazioni]** > **[!UICONTROL Integrazioni]** > **[!UICONTROL Gestione]** > **[!UICONTROL Crea integrazione]**). Gli addetti al marketing utilizzano **[!UICONTROL Aggiungi personalizzazione]** nei componenti Testo o HTML, aprono **[!UICONTROL Integrazioni]**, scelgono un&#39;integrazione attiva e mappano gli attributi.

➡️ [Ulteriori informazioni sui flussi di lavoro dell&#39;amministratore e dell&#39;addetto marketing](integrations.md)

+++

+++ Dove posso creare o gestire le integrazioni nell’interfaccia utente in qualità di amministratore?

Vai alla sezione **[!UICONTROL Configurations]** nel menu a sinistra, apri **[!UICONTROL Manage]** dalla scheda **[!UICONTROL Integrazioni]**, quindi seleziona **[!UICONTROL Create Integration]**.

➡️ [Ulteriori informazioni sulla creazione di un&#39;integrazione](integrations.md#configure)

+++

+++ Quali sono i casi d’uso comuni per le integrazioni?

Alcuni esempi includono punti premio da sistemi di fidelizzazione, informazioni sui prezzi dei prodotti, consigli da motori di consigli e aggiornamenti logistici come lo stato di consegna.

➡️ [Ulteriori informazioni sui dati di esempio provenienti da sistemi di terze parti](integrations.md)

➡️ [Ulteriori informazioni sugli esempi di integrazione dei fornitori](vendor-integration.md)

+++

## Configurazione

+++ Come si configura un’integrazione ad alto livello come amministratore?

Fornisci un nome e una descrizione, un URL dell&#39;endpoint API (facoltativamente con variabili di percorso), valori del modello di percorso, **[!UICONTROL GET]** o **[!UICONTROL POST]**, intestazioni e parametri di query facoltativi, un metodo di autenticazione, impostazioni dei criteri (come timeout e cache facoltativa o nuovo tentativo), una risposta JSON campione ai campi mappa, quindi esegui **[!UICONTROL Send test connection]** e **[!UICONTROL Activate]** se valido.

➡️ [Ulteriori informazioni sulla configurazione dell&#39;integrazione](integrations.md#configure)

+++

+++ Quali tipi di autenticazione sono supportati?

Sono disponibili i seguenti tipi di autenticazione: **[!UICONTROL Nessuna autenticazione]**, **[!UICONTROL Chiave API]**, **[!UICONTROL Autenticazione di base]** e **[!UICONTROL OAuth 2.0]** (con configurazione del payload per OAuth, se applicabile).

➡️ [Ulteriori informazioni sui tipi di autenticazione](integrations.md#configure)

+++

+++ Per che cosa viene utilizzato il passaggio di payload di risposta?

Incolla una risposta JSON campione in modo che il sistema possa rilevare i tipi di dati e puoi scegliere quali campi sono esposti per la personalizzazione nei messaggi. Puoi limitare quali campi sono disponibili per gli esperti di marketing durante la creazione.

➡️ [Ulteriori informazioni sulla mappatura del payload di risposta](integrations.md#configure)

+++

+++ In che modo gli esperti di marketing aggiungono un’integrazione a un messaggio?

Nel contenuto della campagna o del percorso, utilizza **[!UICONTROL Aggiungi personalizzazione]** su un componente Testo o HTML, vai a **[!UICONTROL Integrazioni]**, seleziona un&#39;integrazione e salva. Con la modalità Pillole nell’editor di personalizzazione, puoi mappare i valori alle variabili nella configurazione (ad esempio parametri di intestazione o query o variabili di percorso nell’URL).

➡️ [Ulteriori informazioni sulla personalizzazione con integrazioni](integrations.md#personalization)

+++

## Funzionalità e casi d’uso

+++ Posso utilizzare le integrazioni in percorsi e campagne?

Sì. La funzione è disponibile sia per i percorsi che per le campagne per **canali in uscita** (ad esempio e-mail, SMS e push), entro i limiti di prodotto correnti.

➡️ [Ulteriori informazioni su percorsi e campagne](integrations.md#limitations)

+++

+++ È possibile utilizzare le integrazioni in frammenti riutilizzabili?

La funzione Integrazioni è supportata in Frammenti.

➡️ [Ulteriori informazioni sui frammenti](aem-fragments-gs.md)

+++

## Limitazioni

+++ Quali canali supportano le integrazioni?

Sono supportati **canali in uscita** (ad esempio e-mail, SMS e push).

➡️ [Ulteriori informazioni sui canali supportati](integrations.md#limitations)

+++

+++ Quali formati di risposta API sono supportati?

Per le risposte alle chiamate API, **JSON** e **HTML** sono supportati per la mappatura dei campi. L’output di immagine binaria non elaborato e i formati che non sono JSON non sono disponibili per questo flusso di lavoro.

➡️ [Ulteriori informazioni su JSON e formati di risposta](integrations.md#limitations)

+++

+++ A quali pattern API posso collegarmi?

**Sono supportate le API di recupero** che eseguono il targeting di contenuti specifici. **Le API di elenco** (elenco esteso o pattern di impaginazione) non sono supportate per questo modello di integrazione.

➡️ [Ulteriori informazioni sul recupero e sull&#39;elenco delle API](integrations.md#limitations)

+++

## Autorizzazioni e funzionalità correlate

+++ Di quali autorizzazioni ho bisogno per configurare le integrazioni?

Per iniziare a utilizzare le integrazioni, è necessario concedere agli utenti le autorizzazioni **[!UICONTROL Gestisci configurazione integrazione AJO]** e **[!UICONTROL Visualizza configurazione integrazione AJO]**.

➡️ [Ulteriori informazioni sulle autorizzazioni di integrazione](integrations.md#overview)

+++

+++ Le integrazioni sostituiscono i connettori Adobe Journey Optimizer con Origini Experience Platform?

No. **Le integrazioni** sono per i campi di personalizzazione nel contenuto dei messaggi che guidi dalle API. **Origini** e altre funzionalità di acquisizione dati hanno scopi diversi (ad esempio l&#39;acquisizione di dati batch e l&#39;arricchimento di profili). Utilizza ciascuna funzionalità per l’ambito previsto.

➡️ [Ulteriori informazioni sulle integrazioni per](integrations.md)

➡️ [Ulteriori informazioni sulle origini di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=it){target="_blank"}

+++

## Risoluzione dei problemi

+++ Perché la connessione di prova non riesce o rimane non valida?

Verifica l’URL dell’endpoint, il metodo HTTP, i modelli di percorso, le intestazioni e i parametri di query, l’autenticazione e il timeout dei criteri. Utilizza **[!UICONTROL Invia connessione di prova]** dopo le regolazioni. Per i problemi di payload, assicurati che l’esempio rifletta il codice JSON valido e che i campi selezionati corrispondano a quanto restituito dall’API.

➡️ [Ulteriori informazioni sulla verifica della connessione e della convalida del payload](integrations.md#configure)

+++

+++ Perché gli esperti di marketing non vedono la mia integrazione nel selettore?

Le integrazioni devono essere **attivate** dopo un test riuscito. Quando gli addetti al marketing aprono **[!UICONTROL Integrazioni]** vengono visualizzate solo le integrazioni attive. Se l&#39;integrazione è ancora allo stato Bozza o Inattiva, completare prima l&#39;attivazione.

➡️ [Ulteriori informazioni sulla connessione di prova e sull&#39;attivazione](integrations.md#configure)

+++

## Fornitori terzi

+++ Quali esempi di fornitori sono disponibili e chi protegge l’API?

È possibile eseguire l’integrazione con qualsiasi piattaforma di terze parti che espone un endpoint API compatibile. **Illustrative** modelli di fornitori ed esempi di configurazione possono aiutarti a modellare API compatibili. La responsabilità di proteggere gli endpoint è della piattaforma di terze parti e del tuo team.

➡️ [Ulteriori informazioni sulle procedure di integrazione fornitore](vendor-integration.md)

+++
