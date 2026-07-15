---
title: Creare un canale personalizzato
description: Scopri come creare e configurare un canale personalizzato in Adobe Journey Optimizer utilizzando Channel Builder.
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Disponibilità limitata" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '1555'
ht-degree: 1%

---


# Configurare un canale personalizzato {#create-custom-channel}

>[!CONTEXTUALHELP]
>id="ajo_custom_channel_settings"
>title="Informazioni sui canali personalizzati"
>abstract="Un canale personalizzato consente a Adobe Journey Optimizer di inviare messaggi personalizzati a un sistema esterno tramite il tuo endpoint API. Definisci le proprietà generali, l’endpoint, l’autenticazione e il payload, quindi testa e attiva il nuovo canale personalizzato. Al termine, puoi utilizzarla durante la creazione di una configurazione di canale in modo che gli addetti al marketing possano utilizzarla in percorsi e campagne."
>additional-url="" text="Introduzione ai canali personalizzati"

<!--Contextual help final location TBC (here or in Settings subsection-->

Per poter utilizzare un canale personalizzato in campagne e percorsi, un amministratore deve prima crearlo. Ciò comporta la definizione dell’endpoint, dell’autenticazione, dei criteri di limitazione e della struttura del payload dei messaggi.

La sezione **Channel Builder** è l&#39;interfaccia centrale per la definizione di nuovi canali personalizzati. <!--It is accessible to users with the **[!UICONTROL Administrator]** role. -->Consente di creare e configurare canali personalizzati, ma anche di gestire le credenziali API e delegare i sottodomini.

>[!IMPORTANT]
>
>Per accedere a Channel Builder, creare e gestire canali personalizzati, è necessario disporre delle autorizzazioni **Visualizza canali personalizzati** e **Gestisci canali personalizzati** concesse. <!--[Learn more](../administration/high-low-permissions.md)--> Scopri come gestire le autorizzazioni in [questa sezione](../administration/permissions.md).

## Accedere e gestire i canali personalizzati {#access-channel-builder}

Per accedere a **Channel Builder** e gestire i tuoi canali personalizzati, segui la procedura riportata di seguito.

1. Vai a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** nella barra di navigazione a sinistra.

1. Seleziona **[!UICONTROL Canali personalizzati]** nella sezione **[!UICONTROL Generatore di canali]**.

   ![Inventario canali personalizzato](assets/custom_channels_inventory.png){width="70%"}

1. L’inventario elenca tutti i canali personalizzati nella sandbox, compreso il loro stato corrente e il tipo di autenticazione utilizzato per connettersi all’endpoint esterno.

1. Puoi filtrare i canali personalizzati in base allo stato (**Bozza**, **Attivo** o **Archiviato**), chi li ha creati e cercare per nome.

1. Per modificare un canale, fai clic sul nome nell’inventario, apporta le modifiche e salva. Per i canali attivi, puoi modificare solo alcuni campi - [ulteriori informazioni](#test-activate).

   >[!CAUTION]
   >
   >La modifica delle impostazioni di limitazione o di nuovo tentativo su un canale attivo ha effetto immediato per tutte le esecuzioni in volo e future.

1. Per archiviare un canale, aprirlo dall&#39;inventario e fare clic su **[!UICONTROL Archivia]**.

   Quando si archivia un canale attivo, questo viene rimosso da tutti i menu a discesa di selezione: selettore delle azioni della campagna, palette delle azioni di percorso, elenco dei canali delle campagne orchestrate, configurazioni dei canali e modelli di contenuto. I percorsi e le campagne esistenti che utilizzano già il canale continuano a funzionare normalmente.

## Creare un canale personalizzato {#create-channel}

Per creare un nuovo canale personalizzato, segui la procedura riportata di seguito.

1. Fai clic sul pulsante **[!UICONTROL Crea canale personalizzato]** per aprire il modulo di creazione del canale. Inizia definendo le impostazioni generali per il canale personalizzato.

   ![Impostazioni generali](assets/custom_channel_properties.png){width="70%"}

1. Nella sezione **[!UICONTROL Proprietà]**, immetti un **[!UICONTROL Nome]** per il tuo canale personalizzato. Questo nome verrà visualizzato nell’area di lavoro percorsi, nel selettore delle azioni della campagna e nell’elenco dei canali delle campagne orchestrate.

   >[!NOTE]
   >
   >Il nome deve essere univoco, iniziare con una lettera (A-Z), includere solo caratteri alfanumerici o caratteri speciali ( _, ., -) e deve essere maggiore di 1 carattere.

1. È possibile selezionare un&#39;icona dalla libreria di icone predefinita oppure selezionare un file SVG dal computer.

   >[!NOTE]
   >
   >Il file non deve superare i 150 KB.

   Questa icona verrà visualizzata accanto al nome del canale nell’area di lavoro del percorso. Se non viene caricata alcuna icona, viene utilizzata quella predefinita.

1. Immettere una **[!UICONTROL Descrizione]** facoltativa.

<!--
1. Optionally, assign **[!UICONTROL Access labels]** to restrict access to this channel based on data usage policies. Learn more
-->

## Impostare la configurazione dell’endpoint {#endpoint-configuration}

Devi configurare l’endpoint, che è l’URL HTTP del sistema di messaggistica esterno. [!DNL Journey Optimizer] invia una richiesta POST a questo endpoint con il payload personalizzato quando un profilo è idoneo in una campagna o in un percorso.

![Configurazione endpoint](assets/custom_channel_endpoint_configuration.png){width="70%"}

1. Nella sezione **[!UICONTROL Configurazione endpoint]**, immetti l&#39;host **[!UICONTROL URL]** del sistema di messaggistica esterno.

   <!--The HTTP method to is currently set to **POST**.-->

   >[!IMPORTANT]
   >Il sistema di messaggistica esterno deve esporre un endpoint HTTPS che [!DNL Journey Optimizer] può chiamare tramite HTTP POST. L’endpoint deve:
   >
   >* Accetta il formato di payload definito dal canale (JSON).
   >* Supporta uno dei metodi di autenticazione disponibili nel Channel Builder. [Ulteriori informazioni](#authentication-settings)
   >* Restituisce una risposta HTTP 2xx per confermare la ricezione della richiesta.

1. Aggiungi **[!UICONTROL Intestazioni]** in base alle esigenze. Le intestazioni sono coppie chiave-valore trasmesse a livello di richiesta HTTP. Vengono inviate insieme a ogni richiesta all’endpoint e vengono in genere utilizzate per token di autenticazione, specifiche del tipo di contenuto o altri metadati richiesti dal sistema esterno.

   <!--At minimum, `Content-Type` and `Charset` are available as default headers.-->

   ![Configurazione intestazioni](assets/custom_channel_endpoint_headers.png)

   Per ogni intestazione, puoi definire se il relativo valore è:

   * **[!UICONTROL Costante]** - Valore statico impostato una volta e incluso in ogni richiesta. Ad esempio, è possibile definire il parametro `Content-Type` con il valore `application/json` o il parametro `Charset` con il valore `UTF-8`.
   * **[!UICONTROL Variabile]** - Se viene immesso un valore predefinito, questo viene utilizzato a meno che non venga sostituito nella configurazione del canale. Ad esempio, puoi definire una variabile per l’ID utente che viene risolta in fase di esecuzione. [Ulteriori informazioni](custom-channel-configuration.md) <!--From Custom actions section: For these parameters, you can define where to get this information (example: events, data sources), pass values manually or use the advanced expression editor for advanced use cases. Advanced uses cases can be data manipulation and other function usage. Refer to this [page](expression/expressionadvanced.md).-->

1. Se necessario, aggiungere **[!UICONTROL Parametri query]** utilizzando lo stesso pattern costante/variabile. I parametri di query vengono aggiunti all’URL dell’endpoint al momento della consegna. I parametri costanti vengono sempre aggiunti con lo stesso valore; i parametri variabili vengono risolti al momento dell’invio, ad esempio per trasmettere un identificatore utente dal profilo.

   ![Parametri query](assets/custom_channel_endpoint_query_param.png){width="70%"}

1. Nella sezione **[!UICONTROL Configurazione dei criteri]**, definire il modo in cui [!DNL Journey Optimizer] gestisce la velocità effettiva delle richieste e gli errori. Questo è importante per garantire che il sistema esterno possa gestire il volume di richieste ed evitare di sovraccaricarlo.

   ![Configurazione criterio](assets/custom_channel_endpoint_policy_config.png)

   * **[!UICONTROL Abilita limitazione]** - Disabilitata per impostazione predefinita. Imposta il numero massimo di richieste al secondo (impostazione predefinita: **5.000c**). Una volta raggiunto il limite, le richieste vengono messe in coda e inviate il prima possibile.
   * **[!UICONTROL Abilita nuovo tentativo]** - Abilitato per impostazione predefinita. Impostare il numero massimo di tentativi (impostazione predefinita: **3**, intervallo configurabile: 0-10) per le richieste non riuscite. Questo aiuta a evitare di sopraffare l’endpoint durante errori transitori.
   * **[!UICONTROL Timeout]** - Impostazione predefinita: **5.000 millisecondi**. Imposta il tempo massimo di attesa di una risposta dall’endpoint prima di considerare la richiesta non riuscita.     <!--* **[!UICONTROL Enable cache]** – Disabled by default. Set the caching duration (default TTL: **600 seconds**). After the TTL (Time To Live) expires, the next request is sent to the endpoint. Caching is useful for endpoints that return the same response for identical requests, reducing load and improving performance.-->

## Impostazioni di autenticazione {#authentication-settings}

>[!CONTEXTUALHELP]
>id="ajo_custom_channel_authentication"
>title="Definisci il tipo di autenticazione"
>abstract="L’autenticazione garantisce che solo le richieste autorizzate vengano inviate al sistema di messaggistica esterno. Puoi scegliere tra diversi metodi di autenticazione, tra cui Chiave API, Autenticazione di base e OAuth 2.0. Al momento dell’attivazione, Adobe Journey Optimizer genera automaticamente un set iniziale di credenziali API per il canale, che possono essere gestite nell’inventario delle credenziali API. Tuttavia, anche se è possibile modificare le credenziali in un secondo momento, è necessario fornire i dettagli di autenticazione qui per verificare la connessione all’endpoint prima di attivare il canale."
>additional-url="" text="Ulteriori informazioni sulle credenziali API"

Selezionare il **[!UICONTROL tipo di autenticazione]** da utilizzare per questo canale. Le opzioni disponibili dipendono dai metodi di autenticazione supportati dal sistema di messaggistica esterno.

![Tipo di autenticazione](assets/custom_channel_authentication_type.png){width="70%"}

Fornisci i dettagli di autenticazione richiesti dall’endpoint.

* **[!UICONTROL Nessuno]** - La richiesta viene inviata senza credenziali.
* **[!UICONTROL Chiave API]** - Fornisci il nome, il valore e la posizione della chiave (parametro o intestazione di query).
* **[!UICONTROL Autenticazione di base]** - Specificare nome utente e password.
* **[!UICONTROL OAuth 2.0]** - Configura il payload per l&#39;autenticazione OAuth 2.0.
  <!--* **[!UICONTROL Custom]** – Define the authentication configuration using a JSON payload.-->

Se il tipo di autenticazione è diverso da **None**, [!DNL Journey Optimizer] genera automaticamente un set iniziale di credenziali API per questo canale quando viene attivato. Puoi modificare queste credenziali e crearne di nuove nell’inventario delle credenziali API. [Ulteriori informazioni](custom-channel-api-credentials.md) <!--TBC-->

Tuttavia, i dettagli di autenticazione sono necessari qui per testare la connessione all’endpoint prima di attivare il canale. È disponibile un pulsante **[!UICONTROL Verifica connessione]** per convalidare la configurazione dell&#39;autenticazione. [Ulteriori informazioni](#test-activate)

## Configurazione payload {#payload-configuration}

>[!CONTEXTUALHELP]
>id="ajo_custom_channel_payload_config"
>title="Abilita campo per configurazione canale"
>abstract="Se attivati, i campi in questa colonna vengono visualizzati nella configurazione del canale, consentendo agli amministratori di impostare valori diversi per configurazione (ad esempio, un ID mittente diverso per marchio o area geografica). Ciò è utile per i campi che possono variare in base al contesto della campagna o del percorso, ad esempio le informazioni sul mittente o i modelli di messaggio."
>additional-url="" text="Configurare i parametri dinamici nella configurazione del canale personalizzata"

<!--Create a page on Custom channel config to explain how to use the payload in a channel configuration.-->

Il payload viene inviato all’endpoint quando un profilo si qualifica in una campagna o in un percorso.

Nella configurazione del payload, definisci la struttura del payload del messaggio e quali campi gli addetti al marketing possono creare e personalizzare.

1. Fare clic su **[!UICONTROL Definisci payload]** e scegliere come definire il payload:

   * **[!UICONTROL Incolla payload JSON di esempio]**. Incolla un oggetto JSON rappresentativo e [!DNL Journey Optimizer] ne deduce automaticamente uno schema.
   * **[!UICONTROL Importa schema JSON]** (disponibile a breve). Carica un file di schema JSON completo.

     >[!AVAILABILITY]
     >
     >Questa funzionalità non è ancora disponibile. Sarà aggiunto in una versione futura.

1. Dopo la generazione dello schema, [!DNL Journey Optimizer] visualizza tutti i campi rilevati in una visualizzazione modulo.

   ![](assets/custom_channel_payload_configuration.png)

1. Per ogni campo, configura le seguenti impostazioni:

   | Impostazione | Descrizione |
   | --- | --- |
   | **[!UICONTROL Valore predefinito]** | Facoltativo. Utilizzato se non viene fornito un valore personalizzato al momento dell’authoring. |
   | **[!UICONTROL Tipo]** | Di sola lettura, derivato dal payload. Tipi supportati: `string`, `integer`, `decimal`, `boolean`, `dateTime`, `dateTimeOnly`, `dateOnly`, `listObject`, `listString`, `listInteger`, `listDecimal`, `listBoolean`, `listDateTime`, `listDateTimeOnly`, `listDateOnly`. |
   | **[!UICONTROL Obbligatorio]** | Se abilitato, il campo deve contenere un valore quando il canale viene utilizzato in una campagna o in un percorso. I campi obbligatori mancanti causano un errore di convalida che impedisce l’attivazione. |
   | **[!UICONTROL Configurazione canale]** | Se attivato, il campo viene visualizzato nella configurazione del canale, consentendo agli amministratori di impostare valori diversi per configurazione (ad esempio, un ID mittente diverso per marchio o area geografica). [Scopri come](custom-channel-configuration.md) |

   I campi nidificati sono rappresentati utilizzando la notazione del punto (ad esempio, `image.id`).<!--TBC-->

## Test e attivazione {#test-activate}

Mentre il canale è nello stato **[!UICONTROL Bozza]**, utilizza il pulsante **[!UICONTROL Verifica connessione]** nella parte superiore dello schermo per inviare una richiesta di test all&#39;endpoint e convalidare la connessione end-to-end.

![Verifica pulsante connessione](assets/custom_channel_test_connection.png){width="70%"}

Controlla i registri del sistema esterno per verificare che la richiesta sia stata ricevuta con l’autenticazione e il payload previsti.

Una volta che il test è riuscito, puoi salvare o attivare il canale.

* Fai clic su **[!UICONTROL Salva come bozza]** per salvare l&#39;avanzamento senza rendere disponibile il canale.
* Fai clic su **[!UICONTROL Attiva]** per rendere il canale disponibile per l&#39;utilizzo in configurazioni di canale, campagne e percorsi.

>[!IMPORTANT]
>
>Dopo l’attivazione di un canale, rimangono modificabili solo i seguenti campi: nome, descrizione, icona, limitazione e configurazione di un nuovo tentativo. L&#39;URL dell&#39;endpoint, le intestazioni, i parametri di query, l&#39;autenticazione e la struttura del payload sono bloccati.<!--TBC-->

<!--TBC: An activated channel can be **archived** (hidden from all selection drop-downs while existing journeys and campaigns continue to function), but it cannot be **deleted**. Deletion is only possible while the channel is in **[!UICONTROL Draft]** status.TBC-->

## Passaggi successivi {#next-steps}

È stato creato il tuo canale personalizzato. Completa la configurazione seguendo i passaggi rimanenti:

* [Imposta credenziali API](custom-channel-api-credentials.md) (se il canale utilizza l&#39;autenticazione)
* [Delega un sottodominio](custom-channel-subdomains.md) (facoltativo, obbligatorio per il tracciamento dei collegamenti)
* [Creare una configurazione dei canali](custom-channel-configuration.md)
