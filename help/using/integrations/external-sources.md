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
hidefromtoc: true
exl-id: 104f283e-f6a5-431b-919a-d97b83d19632
source-git-commit: 26f0bdd9f67648d0a382fd67c296bf44f0ea42df
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 1%

---

# Utilizzare le integrazioni {#external-sources}

## Panoramica

La funzionalità **Integrazioni** consente l&#39;integrazione diretta di origini dati di terze parti in Adobe Journey Optimizer. Questa funzione semplifica l’integrazione di dati esterni e origini di contenuto nelle campagne, consentendoti di fornire messaggi altamente personalizzati e dinamici su più canali.

Puoi utilizzare questa funzione per accedere a dati esterni e richiamare contenuti da strumenti di terze parti, ad esempio:

* **Punti premio** da sistemi fedeltà.
* **Informazioni sul prezzo** per i prodotti.
* **Consigli di prodotto** da motori di consigli.
* **Aggiornamenti logistici** come stato di consegna.

## Limitazioni della versione Beta {#limitations}

La versione beta presenta le seguenti limitazioni:

* I canali in uscita sono supportati solo.

* Per le risposte alle chiamate API è supportato solo il formato JSON. Le uscite di immagine HTML e raw binarie non sono disponibili.

* Sono supportate solo le API di recupero che hanno come target contenuti specifici; le API di elenco non sono disponibili.

* La funzione Integrazioni è disponibile sia per i Percorsi che per le campagne, ma non è supportata nei frammenti.

## Configurare l’integrazione {#configure}

In qualità di amministratore, puoi impostare integrazioni esterne seguendo questi passaggi:

1. Passa alla sezione **[!UICONTROL Configurazioni]** nel menu a sinistra e fai clic su **[!UICONTROL Gestisci]** dalla scheda **[!UICONTROL Integrazioni]**.

   Quindi, fai clic su **[!UICONTROL Crea integrazione]** per avviare una nuova configurazione.

   ![](assets/external-integration-config-1.png)

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

1. Con il campo **[!UICONTROL Payload di risposta]**, puoi decidere quali campi dell&#39;output di esempio devono essere utilizzati per la personalizzazione dei messaggi.

   Fai clic sull&#39;icona ![modifica](assets/do-not-localize/Smock_Edit_18_N.svg) e incolla un payload di risposta JSON di esempio per rilevare automaticamente i tipi di dati.

1. Scegli i campi da esporre per la personalizzazione e specifica i tipi di dati corrispondenti.

   ![](assets/external-integration-config-5.png)

1. Utilizza **[!UICONTROL Invia connessione di prova]** per convalidare l&#39;integrazione.

   Una volta convalidata, fai clic su **[!UICONTROL Attiva]**.

## Utilizzo di integrazioni esterne per la personalizzazione {#personalization}

In qualità di addetto marketing, puoi utilizzare integrazioni configurate per personalizzare il contenuto. Segui questi passaggi:

1. Accedi al contenuto della tua campagna e fai clic su **[!UICONTROL Aggiungi personalizzazione]** dal tuo **[!UICONTROL Componenti]** di testo o HTML.

[Ulteriori informazioni sui componenti](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. Passa alla sezione **[!UICONTROL Integrazioni]** e fai clic su **[!UICONTROL Apri integrazioni]** per visualizzare tutte le integrazioni attive.

   ![](assets/external-integration-content-2.png)

1. Seleziona un&#39;integrazione e fai clic su **[!UICONTROL Salva]**.

   ![](assets/external-integration-content-3.png)

1. Attiva la modalità **[!UICONTROL Pillole]** per sbloccare il menu di integrazione avanzato.

   ![](assets/external-integration-content-4.png)

1. Per completare la configurazione dell&#39;integrazione, definire gli attributi di integrazione specificati in precedenza durante la [configurazione](#configure).

   Puoi assegnare valori a questi attributi utilizzando valori statici, che rimangono costanti, o attributi di profilo, che estraggono informazioni in modo dinamico dai profili utente.

   ![](assets/external-integration-content-5.png)

1. Una volta definiti gli attributi di integrazione, puoi utilizzare i campi di integrazione nel contenuto per la messaggistica personalizzata facendo clic sull&#39;icona ![aggiungi](assets/do-not-localize/Smock_Add_18_N.svg).

   ![](assets/external-integration-content-6.png)

1. Fai clic su **[!UICONTROL Salva]**.

La personalizzazione dell’integrazione ora viene applicata correttamente al contenuto, garantendo a ogni destinatario un’esperienza personalizzata e rilevante in base agli attributi configurati.

![](assets/external-integration-content-7.png)
