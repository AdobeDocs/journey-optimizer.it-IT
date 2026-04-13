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
hide: true
source-git-commit: 3733c9ab401f85b22e1d6e07dbf4db535ff8a96d
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 1%

---

# Domande frequenti sulle integrazioni {#vendor-integration-faq}

>[!BEGINSHADEBOX]

Sommario:

* [Utilizzare le integrazioni](external-sources.md)
* [Introduzione all’integrazione con i fornitori](vendor-integration-gs.md)
* [Fornitori disponibili](vendor-integration.md)
* **[Domande frequenti](vendor-integration-faq.md)**

>[!ENDSHADEBOX]

Di seguito sono riportate le domande frequenti sulle **integrazioni** in Adobe Journey Optimizer.

## Introduzione

+++ Cosa fanno le integrazioni in Journey Optimizer?

Collega origini dati esterne a Journey Optimizer per consentire di richiamare contenuti e dati da sistemi di terze parti nelle campagne e nei percorsi e personalizzare i messaggi utilizzando tali dati.

➡️ [Ulteriori informazioni sulla panoramica delle integrazioni](external-sources.md)

+++

+++ Chi configura le integrazioni e chi le utilizza nel contenuto?

Gli amministratori creano e attivano la configurazione tecnica (**[!UICONTROL Configurazioni]** > **[!UICONTROL Integrazioni]** > **[!UICONTROL Gestione]** > **[!UICONTROL Crea integrazione]**). Gli addetti al marketing utilizzano **[!UICONTROL Aggiungi personalizzazione]** nei componenti Testo o HTML, aprono **[!UICONTROL Integrazioni]**, scelgono un&#39;integrazione attiva e mappano gli attributi.

➡️ [Ulteriori informazioni sui flussi di lavoro dell&#39;amministratore e dell&#39;addetto marketing](external-sources.md)

+++

+++ Dove posso creare o gestire le integrazioni nell’interfaccia utente in qualità di amministratore?

Vai alla sezione **[!UICONTROL Configurations]** nel menu a sinistra, apri **[!UICONTROL Manage]** dalla scheda **[!UICONTROL Integrazioni]**, quindi seleziona **[!UICONTROL Create Integration]**.

➡️ [Ulteriori informazioni sulla creazione di un&#39;integrazione](external-sources.md#configure)

+++

+++ Quali sono i casi d’uso comuni per le integrazioni?

Alcuni esempi includono punti premio da sistemi di fidelizzazione, informazioni sui prezzi dei prodotti, consigli da motori di consigli e aggiornamenti logistici come lo stato di consegna.

➡️ [Ulteriori informazioni sui dati di esempio provenienti da sistemi di terze parti](external-sources.md)

➡️ [Ulteriori informazioni sugli esempi di integrazione dei fornitori](vendor-integration.md)

+++

## Configurazione

+++ Come si configura un’integrazione ad alto livello come amministratore?

Fornisci un nome e una descrizione, un URL dell&#39;endpoint API (facoltativamente con variabili di percorso), valori del modello di percorso, **[!UICONTROL GET]** o **[!UICONTROL POST]**, intestazioni e parametri di query facoltativi, un metodo di autenticazione, impostazioni dei criteri (come timeout e cache facoltativa o nuovo tentativo), una risposta JSON campione ai campi mappa, quindi esegui **[!UICONTROL Send test connection]** e **[!UICONTROL Activate]** se valido.

➡️ [Ulteriori informazioni sulla configurazione dell&#39;integrazione](external-sources.md#configure)

+++

+++ Quali tipi di autenticazione sono supportati?

Sono disponibili i seguenti tipi di autenticazione: **[!UICONTROL Nessuna autenticazione]**, **[!UICONTROL Chiave API]**, **[!UICONTROL Autenticazione di base]** e **[!UICONTROL OAuth 2.0]** (con configurazione del payload per OAuth, se applicabile).

➡️ [Ulteriori informazioni sui tipi di autenticazione](external-sources.md#configure)

+++

+++ Per che cosa viene utilizzato il passaggio di payload di risposta?

Incolla una risposta JSON campione in modo che il sistema possa rilevare i tipi di dati e puoi scegliere quali campi sono esposti per la personalizzazione nei messaggi. Puoi limitare quali campi sono disponibili per gli esperti di marketing durante la creazione.

➡️ [Ulteriori informazioni sulla mappatura del payload di risposta](external-sources.md#configure)

+++

+++ In che modo gli esperti di marketing aggiungono un’integrazione a un messaggio?

Nel contenuto della campagna o del percorso, utilizza **[!UICONTROL Aggiungi personalizzazione]** su un componente Testo o HTML, vai a **[!UICONTROL Integrazioni]**, seleziona un&#39;integrazione e salva. Con la modalità Pillole nell’editor di personalizzazione, puoi mappare i valori alle variabili nella configurazione (ad esempio parametri di intestazione o query o variabili di percorso nell’URL).

➡️ [Ulteriori informazioni sulla personalizzazione con integrazioni](external-sources.md#personalization)

+++

## Funzionalità e casi d’uso

+++ Posso utilizzare le integrazioni in percorsi e campagne?

Sì. La funzione è disponibile sia per i percorsi che per le campagne per **canali in uscita** (ad esempio e-mail, SMS e push), entro i limiti di prodotto correnti.

➡️ [Ulteriori informazioni su percorsi e campagne](external-sources.md#limitations)

+++

+++ È possibile utilizzare le integrazioni in frammenti riutilizzabili?

La funzionalità Integrazioni è **non** supportata nei frammenti. Utilizza le integrazioni nel contenuto di campagne e messaggi di percorso, se il prodotto le supporta.

➡️ [Ulteriori informazioni sui frammenti e sui limiti beta](external-sources.md#limitations)

+++

## Limitazioni

+++ Quali canali supportano le integrazioni?

Sono supportati **canali in uscita** (ad esempio e-mail, SMS e push).

➡️ [Ulteriori informazioni sui canali supportati](external-sources.md#limitations)

+++

+++ Quali formati di risposta API sono supportati?

Per le risposte alle chiamate API, **JSON** è supportato per la mappatura dei campi. L’output di immagine binaria non elaborato e i formati che non sono JSON non sono disponibili per questo flusso di lavoro.

➡️ [Ulteriori informazioni su JSON e formati di risposta](external-sources.md#limitations)

+++

+++ A quali pattern API posso collegarmi?

**Sono supportate le API di recupero** che eseguono il targeting di contenuti specifici. **Le API di elenco** (elenco esteso o pattern di impaginazione) non sono supportate per questo modello di integrazione.

➡️ [Ulteriori informazioni sul recupero e sull&#39;elenco delle API](external-sources.md#limitations)

+++

## Autorizzazioni e funzionalità correlate

+++ Di quali autorizzazioni ho bisogno per configurare le integrazioni?

La configurazione è un flusso di lavoro dell&#39;amministratore in **[!UICONTROL Configurazioni]** > **[!UICONTROL Integrazioni]**. I nomi esatti delle autorizzazioni dipendono dai profili di prodotto Admin Console e Journey Optimizer della tua organizzazione. Conferma con l’amministratore o il rappresentante Adobe.

➡️ [Ulteriori informazioni sulla configurazione delle integrazioni](external-sources.md#configure)

+++

+++ Le integrazioni sostituiscono i connettori Adobe Journey Optimizer con Origini Experience Platform?

No. **Le integrazioni** sono per i campi di personalizzazione nel contenuto dei messaggi che guidi dalle API. **Origini** e altre funzionalità di acquisizione dati hanno scopi diversi (ad esempio l&#39;acquisizione di dati batch e l&#39;arricchimento di profili). Utilizza ciascuna funzionalità per l’ambito previsto.

➡️ [Ulteriori informazioni sulle integrazioni per](external-sources.md)

➡️ [Ulteriori informazioni sulle origini di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=it){target="_blank"}

+++

## Risoluzione dei problemi

+++ Perché la connessione di prova non riesce o rimane non valida?

Verifica l’URL dell’endpoint, il metodo HTTP, i modelli di percorso, le intestazioni e i parametri di query, l’autenticazione e il timeout dei criteri. Utilizza **[!UICONTROL Invia connessione di prova]** dopo le regolazioni. Per i problemi di payload, assicurati che l’esempio rifletta il codice JSON valido e che i campi selezionati corrispondano a quanto restituito dall’API.

➡️ [Ulteriori informazioni sulla verifica della connessione e della convalida del payload](external-sources.md#configure)

+++

+++ Perché gli esperti di marketing non vedono la mia integrazione nel selettore?

Le integrazioni devono essere **attivate** dopo un test riuscito. Quando gli addetti al marketing aprono **[!UICONTROL Integrazioni]** vengono visualizzate solo le integrazioni attive. Se l&#39;integrazione è ancora allo stato Bozza o Inattiva, completare prima l&#39;attivazione.

➡️ [Ulteriori informazioni sulla connessione di prova e sull&#39;attivazione](external-sources.md#configure)

+++

## Fornitori terzi

+++ Quali esempi di fornitori sono disponibili e chi protegge l’API?

È possibile eseguire l’integrazione con qualsiasi piattaforma di terze parti che espone un endpoint API compatibile. **Illustrative** modelli di fornitori ed esempi di configurazione possono aiutarti a modellare API compatibili. La responsabilità di proteggere gli endpoint è della piattaforma di terze parti e del tuo team.

➡️ [Ulteriori informazioni sulle procedure di integrazione fornitore](vendor-integration.md)

+++
