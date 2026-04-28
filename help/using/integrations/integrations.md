---
solution: Journey Optimizer
product: journey optimizer
title: Abilita integrazioni esterne
description: Integra integrazioni esterne nel processo di authoring dei canali per arricchire i contenuti con informazioni personalizzate e dinamiche
feature: Integrations
topic: Content Management
role: User
level: Beginner
keywords: integrazione
hide: true
exl-id: 104f283e-f6a5-431b-919a-d97b83d19632
source-git-commit: f40e030e7d14120cdbc118a8f93e2f752d713f6b
workflow-type: tm+mt
source-wordcount: '1227'
ht-degree: 7%

---

# Utilizzare le integrazioni {#external-sources}

>[!BEGINSHADEBOX]

Sommario:

* **[Operazioni con le integrazioni](integrations.md)**
* [Introduzione](vendor-integration-gs.md)
* [Fornitori disponibili](vendor-integration.md)
* [Domande frequenti](vendor-integration-faq.md)

>[!ENDSHADEBOX]

## Panoramica

La funzionalità **Integrazioni** collega Adobe Journey Optimizer a sistemi di terze parti i cui dati e contenuti componibili sono già gestiti altrove. Puoi far emergere tale materiale durante l’authoring e l’invio, il che supporta esperienze più reattive e personalizzate tra i canali utilizzati in Journey Optimizer.

Puoi utilizzare questa funzione per accedere a dati esterni e richiamare contenuti da strumenti di terze parti, ad esempio:

* **Punti premio** da sistemi fedeltà.
* **Informazioni sul prezzo** per i prodotti.
* **Consigli di prodotto** da motori di consigli.
* **Aggiornamenti logistici** come stato di consegna.

Per iniziare a utilizzare le integrazioni, è necessario concedere agli utenti le autorizzazioni **[!UICONTROL Gestisci configurazione integrazione AJO]** e **[!UICONTROL Visualizza integrazione AJO]**. [Ulteriori informazioni sulle autorizzazioni](../administration/permissions.md)

+++ Scopri come assegnare le autorizzazioni correlate alle integrazioni

1. Nel prodotto **[!UICONTROL Autorizzazioni]**, passa alla scheda **[!UICONTROL Ruoli]** e seleziona il **[!UICONTROL Ruolo]** desiderato.

1. Fai clic su **[!UICONTROL Modifica]** per modificare le autorizzazioni.

1. Aggiungi la risorsa **[!UICONTROL Configurazione integrazione AJO]**, quindi seleziona le autorizzazioni di integrazione appropriate dal menu a discesa.

   ![](assets/external-integration-config-9.png)

1. Fai clic su **[!UICONTROL Salva]** per applicare le modifiche.

   Le autorizzazioni degli utenti già assegnati a questo ruolo verranno aggiornate automaticamente.

1. Per assegnare questo ruolo a nuovi utenti, passa alla scheda **[!UICONTROL Utenti]** nella dashboard **[!UICONTROL Ruoli]** e fai clic su **[!UICONTROL Aggiungi utente]**.

1. Immetti il nome o l’indirizzo e-mail dell’utente o sceglilo dall’elenco e fai clic su **[!UICONTROL Salva]**.

Se l&#39;utente non è stato creato in precedenza, consulta [questa documentazione](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/abac/permissions-ui/users).

+++

## Configurare l’integrazione {#configure}

>[!AVAILABILITY]
>
> Questa funzione di integrazione è limitata ai canali in uscita (e-mail, SMS e push) e fornisce dati in formati JSON o HTML. L’API è di sola lettura e supporta solo le operazioni di recupero.

In qualità di amministratore, puoi impostare integrazioni esterne seguendo questi passaggi:

1. Passa alla sezione **[!UICONTROL Configurazioni]** nel menu a sinistra e fai clic su **[!UICONTROL Gestisci]** dalla scheda **[!UICONTROL Integrazioni]**.

   Quindi, fai clic su **[!UICONTROL Crea integrazione]** per avviare una nuova configurazione.

   ![](assets/external-integration-config-1.png)

1. Facoltativamente, incolla un comando **cURL** per compilare automaticamente l&#39;URL, il metodo HTTP, le intestazioni e i parametri di query.

1. Fornisci **[!UICONTROL Nome]** e **[!UICONTROL Descrizione]** per l&#39;integrazione.

   >[!NOTE]
   >
   >Questi campi non possono contenere spazi.

1. Immettere l&#39;endpoint API **[!UICONTROL URL]**, che può includere parametri di percorso con variabili che possono essere definite utilizzando etichette e valori predefiniti.

1. Configura il **[!UICONTROL Modello percorso]** con **[!UICONTROL Nome]** e **[!UICONTROL Valore predefinito]**.

   ![](assets/external-integration-config-2.png)

1. Selezionare il **[!UICONTROL metodo HTTP]** tra GET e POST.

1. Fai clic su **[!UICONTROL Aggiungi intestazione]** e/o **[!UICONTROL Aggiungi parametri di query]** in base alle esigenze per la tua integrazione. Per ogni parametro, fornisci i seguenti dettagli:

   * **[!UICONTROL Parametro]**:: identificatore univoco utilizzato internamente per fare riferimento al parametro.

   * **[!UICONTROL Nome]**: il nome effettivo del parametro come previsto dall&#39;API.

   * **[!UICONTROL Tipo]**: scegliere **Costante** per un valore fisso o **Variabile** per l&#39;input dinamico.

   * **[!UICONTROL Valore]**: immettere il valore direttamente per le costanti oppure selezionare una mappatura variabile.

   * **[!UICONTROL Obbligatorio]**: specificare se questo parametro è obbligatorio.

   ![](assets/external-integration-config-3.png)

1. Scegli un **[!UICONTROL tipo di autenticazione]**:

   * **[!UICONTROL Nessuna autenticazione]**: per le API aperte che non richiedono credenziali.

   * **[!UICONTROL Chiave API]**: autentica le richieste utilizzando una chiave API statica. Immetti il **[!UICONTROL nome chiave API &#x200B;]**, **[!UICONTROL valore chiave API &#x200B;]** e specifica la **[!UICONTROL posizione]**.

   * **[!UICONTROL Autenticazione di base]**: utilizza l&#39;autenticazione di base HTTP standard. Immettere **[!UICONTROL Nome utente]** e **[!UICONTROL Password]**.

   * **[!UICONTROL OAuth 2.0]**: esegui l&#39;autenticazione utilizzando il protocollo OAuth 2.0. Fai clic sull&#39;icona ![modifica](assets/do-not-localize/Smock_Edit_18_N.svg) per configurare o aggiornare il **[!UICONTROL payload]**.

   ![](assets/external-integration-config-4.png)

1. Imposta la **[!UICONTROL configurazione dei criteri]**, ad esempio il periodo di **[!UICONTROL timeout]** per le richieste API e scegli di abilitare la limitazione, la cache e/o un nuovo tentativo.

   Quando la limitazione è abilitata, le tariffe supportate variano da **50** TPS (minimo) a **5000** TPS (massimo).
Quando il nuovo tentativo è abilitato, gli altri errori seguono **tre** tentativi per impostazione predefinita, con **200 ms**, **400 ms** e **800 ms** tra tentativi successivi.

1. Con il campo **[!UICONTROL Payload di risposta]**, puoi decidere quali campi dell&#39;output di esempio devono essere utilizzati per la personalizzazione dei messaggi.

   Fai clic sull&#39;icona ![modifica](assets/do-not-localize/Smock_Edit_18_N.svg) e incolla un payload di risposta JSON di esempio per rilevare automaticamente i tipi di dati.

1. Scegli i campi da esporre per la personalizzazione e specifica i tipi di dati corrispondenti.

   ![](assets/external-integration-config-5.png)

   >[!NOTE]
   >
   >La configurazione del payload **[!UICONTROL Risposta]** definisce la risposta prevista per l&#39;authoring, incluso qualsiasi schema applicato in quel passaggio. Gli addetti al marketing possono fare riferimento solo ai campi esposti; i token per altri percorsi non superano la convalida nell’editor.

1. Utilizza **[!UICONTROL Invia connessione di prova]** per convalidare l&#39;integrazione.

   Una volta convalidata, fai clic su **[!UICONTROL Attiva]**.

### Limiti e comportamento dei tempi di invio {#configure-send-time}

Al momento dell&#39;invio, per impostazione predefinita, le risposte dall&#39;API esterna possono arrivare a **4 MB**. Qualsiasi elemento di dimensioni maggiori viene trattato come un errore di integrazione e **i nuovi tentativi non vengono tentati** quando l&#39;errore è causato dalle dimensioni della risposta.

Le chiamate rispettano la frequenza di **limitazione** configurata: Journey Optimizer pianifica i tentativi fino a tale limite anche quando il sistema esterno è inattivo o restituisce errori. Se **cache** è abilitata, solo **risposte riuscite** vengono archiviate e riutilizzate fino alla scadenza della cache **TTL** definita; le risposte non riuscite non vengono mai memorizzate nella cache.

Ogni messaggio in coda dispone anche di una finestra di validità (TTL). Se l&#39;elaborazione è in ritardo e un messaggio si trova oltre la finestra, il sistema **lo scarta** ed emette un evento **`MessageValidityExclusion`** in modo che il lavoro non aggiornato si cancelli dalla coda e le risorse rimangano disponibili.


## Utilizzo di integrazioni esterne per la personalizzazione {#personalization}

Prima di utilizzare le integrazioni esterne per la personalizzazione, tieni presente che la pianificazione e l’isolamento delle chiamate di integrazione dipendono dal contesto di esecuzione:

* **Esecuzione batch** (campagne batch, campagne orchestrate e campagne marketing attivate da API): ogni esecuzione batch funziona in un ambiente dedicato e isolato. Pertanto, le esecuzioni in batch simultanee che richiamano sistemi esterni non si scontrano né si ostacolano a vicenda.

* **Esecuzione unitaria** (percorsi unitari, percorsi batch e campagne transazionali attivate da API): il traffico di integrazione è isolato per sandbox del brand, pertanto un’API esterna lenta per un brand non ne ritarda un altro. All’interno della sandbox, le integrazioni simultanee possono ritardare brevemente altri messaggi supportati dall’integrazione; ogni messaggio viene tentato fino a 12 ore prima della scadenza.

In qualità di addetto marketing, puoi utilizzare integrazioni configurate per personalizzare il contenuto. Segui questi passaggi:

1. Accedi al contenuto della tua campagna e fai clic su **[!UICONTROL Aggiungi personalizzazione]** dal tuo **[!UICONTROL Componenti]** di testo o HTML.

   [Ulteriori informazioni sui componenti](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. Passa alla sezione **[!UICONTROL Integrazioni]** e fai clic su **[!UICONTROL Apri integrazioni]** per visualizzare tutte le integrazioni attive.

   I frammenti di contenuto sono disponibili con le integrazioni ma supportano solo i canali in uscita. La pubblicazione in entrata non avrà esito positivo. Dopo la pubblicazione di un frammento, l’aggiunta e il salvataggio di nuove integrazioni viene disattivato per evitare un impatto sui percorsi e sulle campagne esistenti.

   ![](assets/external-integration-content-2.png)

1. Seleziona un&#39;integrazione e fai clic su **[!UICONTROL Salva]**.

   ![](assets/external-integration-content-3.png)

1. Attiva la modalità **[!UICONTROL Pillole]** per sbloccare il menu di integrazione avanzato.

   ![](assets/external-integration-content-4.png)

1. Quando si crea la personalizzazione dell&#39;integrazione, l&#39;helper integrazioni include un campo **`required`** che definisce il modo in cui gli errori o i dati mancanti interagiscono con il contenuto predefinito:

   * **`required=true`** (impostazione predefinita): il rendering viene interrotto per il messaggio. L&#39;invio è escluso con **`ExternalDataLookupExclusion`** e tale esclusione è registrata nel **set di dati di feedback del messaggio**.
   * **`required=false`**: la variabile dei risultati è impostata su **`null`** e il rendering continua. Utilizza testo predefinito, fallback o logica condizionale nel modello, in modo che i profili non ricevano contenuto vuoto quando l’integrazione non restituisce dati.

     ![](assets/external-integration-content-8.png)

1. Per completare la configurazione dell&#39;integrazione, definire gli attributi di integrazione specificati in precedenza durante la [configurazione](#configure).

   Puoi assegnare valori a questi attributi utilizzando valori statici, che rimangono costanti, o attributi di profilo, che estraggono informazioni in modo dinamico dai profili utente.

   ![](assets/external-integration-content-5.png)

1. Una volta definiti gli attributi di integrazione, puoi utilizzare i campi di integrazione nel contenuto per la messaggistica personalizzata facendo clic sull&#39;icona ![aggiungi](assets/do-not-localize/Smock_Add_18_N.svg).

   ![](assets/external-integration-content-6.png)

   >[!NOTE]
   >
   >I token nel modello devono utilizzare solo i campi esposti dall&#39;amministratore nella configurazione dell&#39;integrazione. Ad esempio, `{{weatherResponse.temperature}}` è valido quando `temperature` è esposto; `{{weatherResponse.humidity}}` è rifiutato nell&#39;editor se `humidity` non è stato esposto.

1. Fai clic su **[!UICONTROL Salva]**.

La personalizzazione dell’integrazione ora viene applicata correttamente al contenuto, garantendo a ogni destinatario un’esperienza personalizzata e rilevante in base agli attributi configurati.

![](assets/external-integration-content-7.png)

