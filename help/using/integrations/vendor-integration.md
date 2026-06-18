---
solution: Journey Optimizer
product: journey optimizer
title: Integrazione fornitore
description: Utilizza le integrazioni Adobe Journey Optimizer con qualsiasi piattaforma esterna che espone un’API valida e i pattern di fornitori testati dagli ingegneri per garantirne l’affidabilità durante la progettazione della configurazione.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: integrazione, fornitore, terze parti
subfeature_v2: []
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
source-git-commit: bfb28a935dffca7c381fe72339abc840d2ab297b
workflow-type: tm+mt
source-wordcount: 10185
ht-degree: 5%

---

# Configurazioni fornitore di esempio {#vendor-integration}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come utilizzare le integrazioni Adobe Journey Optimizer con qualsiasi piattaforma esterna che espone un&#39;API compatibile, con guardrail operativi e modelli di fornitori illustrativi per guidare la configurazione.

>[!ENDSHADEBOX]

>[!BEGINSHADEBOX]

I clienti sono responsabili di garantire che l’utilizzo della funzione Integrazioni di AJO e di eventuali fornitori o integrazioni di terze parti associati sia conforme a tutte le leggi e le normative applicabili, come HIPAA.

>[!ENDSHADEBOX]

## Navigazione rapida {#quick-navigation}

Utilizza questi collegamenti raggruppati per passare rapidamente al modello del fornitore pertinente:

* **Sistema di gestione dei contenuti:** [Contentful](#contentful), [Sitecore](#sitecore), [Salsify](#salsify), [Contentstack](#contentstack), [Akeneo](#akeneo), [Magnolia](#magnolia)
* **Fedeltà e premi:** [Voucherify](#voucherify), [Talon.One](#talon-one), [Antavo](#antavo), [Fedeltà Salesforce](#salesforce-loyalty), [Capillare](#capillary)
* **Modelli, personalizzazione e consigli:** [Stensul](#stensul), [Marigold](#marigold), [Consigli di Adobe Target](#adobe-target-recommendations)
* **Dati, meteo e operazioni:** [AccuWeather](#accuweather), [ShipStation](#shipstation), [RevenueCat](#revenuecat), [Databricks](#databricks)
* **Recensioni, consenso e social:** [Bynder](#bynder), [Trustpilot](#trustpilot), [Bazaarvoice](#bazaarvoice), [OneTrust](#onetrust), [Meta](#meta), [Aprimo](#aprimo), [Epsilon (Epsilon3)](#epsilon)

## Contenuto e CMS {#content-and-cms}

### Contentoso {#contentful}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è gestito da o formalmente supportato da Contentful. Conferma i dettagli API correnti con la relativa documentazione.

>[!BEGINSHADEBOX]

Contentful è un CMS headless per voci e risorse strutturate su REST o GraphQL, per cui Journey Optimizer può estrarre contenuti in fase di invio o apertura.

I casi d’uso tipici includono blocchi hero localizzati, testo alt e CTA nelle e-mail, nonché voci di prodotto o promo nei moduli dinamici. Un altro pattern comune è il recupero di una voce specifica per ID per la messaggistica personalizzata.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni di Content.

Si applicano i seguenti prerequisiti:

* Spazio esaustivo con accesso all’API di consegna e chiave API di lettura.
* Cancella tipi di contenuto e ID campo; accesso amministratore in Journey Optimizer per creare integrazioni.

Si applicano le seguenti limitazioni ed esclusioni:

* Le API per elenchi ampi o per contenuti impaginati non si adattano bene a questo pattern; preferiscono le chiamate di recupero che hanno come target una voce o una risorsa specifica.
* La sincronizzazione write-back o bidirezionale non rientra nell&#39;ambito di questo esempio.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Configura **GET** con l&#39;API di distribuzione dei contenuti e il token di consegna, incolla il JSON di esempio, mappa i campi, verifica, attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configurare l&#39;endpoint utilizzando l&#39;URL CDA (Content Delivery API): `https://cdn.contentful.com/spaces/{space_id}/environments/{environment_id}/entries/{entry_id}`

1. Selezionare il metodo HTTP: **GET**.

1. Aggiungi autenticazione. Imposta il parametro **`access_token`** **query** sul token API Content Delivery, come mostrato nei **Campi di integrazione di esempio** di seguito. Contentful accetta anche lo stesso token in un&#39;intestazione `Authorization: Bearer`. Utilizza qualsiasi campo di integrazione supporti.

1. Se necessario, aggiungi le variabili di percorso (ad esempio, ID voce, impostazioni locali).

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi obbligatori per la personalizzazione.

1. Configura il timeout e la memorizzazione in cache in base alle esigenze.

1. Verifica la connessione e attiva.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

Campi di integrazione di esempio (allinea con [API Content Delivery](https://www.contentful.com/developers/docs/references/content-delivery-api/){target="_blank"} per il tuo Windows Live Spaces e il tuo ambiente):

| Campo | Valore |
| -- | -- |
| **URL** | `https://cdn.contentful.com/spaces/{{spaceID}}/environments/{{environment_id}}/entries/{{entry_id}}` |
| Payload di risposta | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |
| Policy | Configura i dettagli a livello di criterio in base alle tue esigenze. |
| **metodo HTTP** | `GET` |

**Parametri percorso**

| Parametro percorso | Nome | Valore predefinito |
| --- | --- | --- |
| `spaceID` | `spaceID` | `<YOUR_SPACE_ID>` |
| `environment_id` | `environment_id` | `<YOUR_ENV_ID>` |
| `entry_id` | `entry_id` | `<YOUR_ENTRY_ID>` |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Content-Type (predefinito) | Content-Type | Costante | application/json | Sì (attivato) |

**Autenticazione**

| Tipo | Nome chiave API | Valore chiave API | Posizione |
| --- | --- | --- | --- |
| Chiave API | `access_token` | `<YOUR_API_KEY>` | Parametro query |

+++

### Sitecore {#sitecore}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è gestito da Sitecore o formalmente supportato da Sitecore. Conferma i dettagli API correnti con la documentazione di Sitecore.

>[!BEGINSHADEBOX]

Sitecore Content Hub e le relative API cloud supportano i flussi di download e metadati in stile DAM; il modello di esempio seguente è incentrato su un ordine di download per ID.

I casi d’uso tipici includono i metadati di risorse o download nel contenuto delle e-mail e l’allineamento con i flussi di lavoro DAM gestiti in Sitecore.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni di Sitecore.

Si applicano i seguenti prerequisiti:

* URL e credenziali del tenant (bearer o token in base alla superficie API).
* Accesso amministratore in Journey Optimizer per creare integrazioni.

Si applicano le seguenti limitazioni ed esclusioni:

* I nomi host e i percorsi variano a seconda del prodotto Sitecore. Utilizza solo endpoint esposti dal tenant.
* I token di accesso, l’aggiornamento e la durata di OAuth devono rispettare i criteri di sicurezza di Sitecore.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Configura **GET** nel percorso dell&#39;ordine di download, imposta le intestazioni di autorizzazione per Sitecore, mappa `id` dal contesto, incolla JSON di esempio, mappa i campi e ottimizza i timeout per la latenza delle risorse.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando l’API di Content Hub (ad esempio: ordine di download per ID). Esempio di pattern URL:

   `https://xmapps-api.sitecorecloud.io/api/v1/downloadorders/{id}`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

Utilizza i campi seguenti per configurare questa chiamata di esempio in Journey Optimizer. Conferma il nome host e la versione API per il tuo prodotto (Content Hub, XM Cloud e così via) nella [documentazione di Sitecore](https://doc.sitecore.com/){target="_blank"}.

| Campo | Valore |
| --- | --- |
| **URL** | `https://xmapps-api.sitecorecloud.io/api/v1/downloadorders/{{id}}` |
| **metodo HTTP** | `GET` |
| Payload di risposta | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |
| Policy | Configura i dettagli a livello di criterio in base alle tue esigenze. |

**Parametri percorso**

| Parametro percorso | Nome | Valore predefinito |
| --- | --- | --- |
| `id` | `id` | `<id_of_download_order>` |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Content-Type (predefinito) | Content-Type | Costante | application/json | Sì (attivato) |
| Authorization | Authorization | Costante | Bearer `<token>` | Sì (attivato) |
| If-Modified-Since | If-Modified-Since | Variable | 2019-08-24T14:15:22Z | No (disattivato) |

**Autenticazione**

| Tipo | Nome chiave API | Valore chiave API | Posizione |
| --- | --- | --- | --- |
| Chiave API | X-Auth-Token | `<token>` | Header |

+++

### Salsefrica {#salsify}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è mantenuto da Salsify o formalmente sostenuto da quest&#39;ultimo. Conferma i dettagli API correnti con la documentazione di Salsify.

>[!BEGINSHADEBOX]

Salsify è un PIM con API per prodotti, canali e risorse digitali.

I casi d’uso tipici includono attributi di prodotto o URL multimediali nelle e-mail e nella messaggistica allineati con i dati del catalogo in syndication.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni di Salsify.

Si applicano i seguenti prerequisiti:

* Token API e contesto organizzazione; ID prodotto risolvibili dal profilo o contesto.
* Accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* Cataloghi molto grandi: evita gli endpoint di elenco in blocco se le integrazioni prevedono il recupero per entità.
* La visibilità degli attributi può essere limitata dalle autorizzazioni per il ruolo Salsifica.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Preferisci il recupero di un singolo prodotto rispetto alle chiamate di catalogo in blocco, imposta l’autenticazione bearer, incolla il JSON di esempio, mappa i campi, verifica, attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando l’API di prodotto Salsify. Esempio di pattern URL:

   `https://api.salsify.com/v1/...`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

Alcuni riferimenti meno recenti riutilizzavano un percorso di stile dell&#39;ordine di download per Salsify; il tenant potrebbe invece utilizzare `https://app.salsify.com/api/v1/orgs/{org_id}/products/{salsify_id}` o simili. Conferma in [Sviluppatori Salsify](https://developers.salsify.com/){target="_blank"}.

| Campo | Valore |
| --- | --- |
| **URL** | `https://app.salsify.com/api/v1/orgs/{{org_id}}/products/{{salsify_id}}` |
| **metodo HTTP** | `GET` |
| **Criterio** | Configura i dettagli a livello di criterio in base alle tue esigenze. |
| **Payload di risposta** | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |

**Parametri percorso**

| Parametro percorso | Nome | Valore predefinito |
| --- | --- | --- |
| `org_id` | `org_id` | `<org_id>` |
| `salsify_id` | `salsify_id` | `<salsify_id>` |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Content-Type (parametro predefinito) | Content-Type | Costante | application/json | Sì (attivato) |
| Authorization | Authorization | Costante | `Bearer <YOUR_TOKEN_HERE>` | Sì (attivato) |
| If-Modified-Since | If-Modified-Since | Variable | 2019-08-24T14:15:22Z | No (disattivato) |

**Autenticazione**

| Tipo | Nome chiave API | Valore chiave API | Posizione |
| --- | --- | --- | --- |
| Chiave API | `apiKey` | `<your_api_key>` | Header |

+++

### Stack di contenuti {#contentstack}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è gestito da o formalmente supportato da Contentstack. Conferma i dettagli API correnti con la documentazione di Contentstack.

>[!BEGINSHADEBOX]

Contentstack è un CMS headless; la distribuzione REST è tipica per la mappatura dei campi JSON in Journey Optimizer.

Un caso d’uso tipico prevede l’utilizzo di voci per banner o promozioni con parametri che includono la lingua.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni di Contentstack.

Si applicano i seguenti prerequisiti:

* Stack di chiavi API, token di consegna, nome dell’ambiente e UID del tipo di contenuto.
* Accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* Questo modello utilizza il JSON REST per la mappatura dei campi; la distribuzione GraphQL segue un percorso di integrazione diverso.
* Utilizza token di consegna appropriati per la produzione; i flussi di anteprima e pubblicati non sono intercambiabili.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Aggiungi entrambe le intestazioni `api_key` e `access_token` come richiesto da Contentstack, includi il parametro di query `environment`, incolla JSON di esempio, mappa i campi, verifica, attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando l’API di distribuzione dei contenuti. Esempio di pattern URL:

   `https://cdn.contentstack.io/v3/content_types/{content_type_uid}/entries/{entry_uid}`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

Campi di integrazione di esempio. Vedi [API di distribuzione dei contenuti dello stack di contenuti](https://www.contentstack.com/docs/developers/apis/content-delivery-api/){target="_blank"}.

| Campo | Valore |
| --- | --- |
| **URL** | `https://cdn.contentstack.io/v3/content_types/{{content_type_uid}}/entries/{{entry_uid}}` |
| **metodo HTTP** | `GET` |
| Payload di risposta | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |
| Policy | Configura i dettagli a livello di criterio in base alle tue esigenze. |
| Intestazioni | Non sono necessarie intestazioni aggiuntive. |

**Parametri percorso**

| Parametro percorso | Nome | Valore predefinito |
| --- | --- | --- |
| `content_type_uid` | Tipo di contenuto UID | `<your_content_type_uid>` |
| `entry_uid` | UID entry-level | `<your_entry_uid>` |

**Autenticazione**

| Nome chiave | Valore chiave | Aggiungi a |
| --- | --- | --- |
| `api_key` | `<YOUR_STACK_API_KEY>` | Header |
| `access_token` | `<YOUR_DELIVERY_TOKEN>` | Header |

Lo stack di contenuti prevede **entrambe** chiavi come intestazioni per le richieste di consegna.

**Parametri query**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| `environment` | Nome dell’ambiente | Variable | `<your_environment_name>` | Sì (attivato) |

+++

### Akeneo {#akeneo}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è mantenuto da Akeneo o formalmente supportato da Akeneo. Conferma i dettagli API correnti con la documentazione di Akeneo.

>[!BEGINSHADEBOX]

Akeneo PIM espone le API REST per prodotti, attributi e file multimediali.

I casi d’uso tipici includono i dati di prodotto gestiti nei moduli e-mail e gli attributi per un dato canale nei percorsi.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni di Akeneo.

Si applicano i seguenti prerequisiti:

* URL di base PIM e client OAuth; UUID prodotto o strategia di identificazione.
* Accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* Le risposte PIM possono essere grandi. Mappa solo gli attributi richiesti per la personalizzazione.
* Le operazioni di scrittura non rientrano nell’ambito dei tipici esempi di personalizzazione in sola lettura.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Usa **GET** con token Bearer, richiedi solo le opzioni attributo necessarie nei flag di query, incolla il JSON di esempio, mappa un set di attributi minimo, verifica, attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando l’API REST di Akeneo. Esempio di pattern URL:

   `https://{pim-host}/api/rest/v1/...`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

Esempio di pattern: `https://{pim-host}/api/rest/v1/products-uuid/{uuid}` con `Accept: application/json`. Vedi [API Akeneo](https://api.akeneo.com/){target="_blank"}.

| Campo | Valore |
| --- | --- |
| **URL** | `https://{{your-akeneo-domain}}.com/api/rest/v1/products-uuid/{{uuidProduct}}` |
| **metodo HTTP** | `GET` |
| **Criterio** | Configura i dettagli a livello di criterio in base alle tue esigenze. |
| **Payload di risposta** | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |

**Parametri percorso**

| Parametro percorso | Nome | Valore predefinito |
| --- | --- | --- |
| `uuidProduct` | UUID | `<product_uuid>` |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Authorization | Authorization | Costante | `Bearer <YOUR_TOKEN>` | Sì (attivato) |
| Accetta | Accetta | Costante | application/json | Sì (attivato) |

**Parametri query**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| `with_attribute_options` | Includi opzioni attributo | Variable | falso | No (disattivato) |
| `with_quality_scores` | Includi punteggi di qualità | Variable | falso | No (disattivato) |
| `with_completenesses` | Includi completezza | Variable | falso | No (disattivato) |

**Autenticazione**

| Tipo | Nome chiave API | Valore chiave API | Posizione |
| --- | --- | --- | --- |
| Chiave API | Authorization | `Bearer <YOUR_ACCESS_TOKEN>` | Header |

+++

### Magnolia {#magnolia}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è mantenuto da Magnolia o formalmente sostenuto da Magnolia. Conferma i dettagli API correnti con la documentazione di Magnolia.

>[!BEGINSHADEBOX]

Magnolia offre endpoint di consegna headless e REST a seconda della distribuzione.

Un caso d’uso tipico è la distribuzione di nodi o frammenti di contenuto per i moduli di marketing.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni di Magnolia.

Si applicano i seguenti prerequisiti:

* URL e token dell’istanza o autenticazione di base; area di lavoro e percorsi per la consegna.
* Accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* Gli URL di consegna REST dipendono dai moduli e dalla configurazione di Magnolia installati.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Utilizza il pattern dell’URL di consegna pubblico esposto dai moduli, esegui l’autenticazione secondo le indicazioni di Magnolia (consegna anonima vs token per contenuto protetto), incolla JSON di esempio, mappa i campi, verifica, attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando Magnolia REST (consegna). Esempio di pattern URL:

   `https://{author-or-public}/.rest/delivery/...`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

Esempio di pattern: `https://{domain}/magnoliaAuthor/.rest/delivery/...` o URL pubblici in stile tour di consegna. I percorsi dipendono dai moduli installati. Consulta la [documentazione di Magnolia](https://docs.magnolia-cms.com/){target="_blank"}.

| Campo | Valore |
| --- | --- |
| **URL** | `http://{{your-domain}}/magnoliaAuthor/.rest/delivery/<myEndpoint>/travel/@nodes` |
| **metodo HTTP** | `GET` |
| **Criterio** | Configura i dettagli a livello di criterio in base alle tue esigenze. |
| **Payload di risposta** | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Content-Type | Content-Type | Costante | application/json | Sì (attivato) |
| Accetta | Accetta | Costante | application/json | Sì (attivato) |

**Autenticazione**

| Tipo | Nome chiave API | Valore chiave API | Posizione |
| --- | --- | --- | --- |
| Chiave API | Authorization | `<bearer_token>` | Header |

Nota: l’API di consegna utilizza il ruolo resto anonimo per i contenuti che non richiedono un accesso. Per un accesso sicuro ai dati protetti, è preferibile un metodo più affidabile, come i token API o OAuth 2.0.

+++


## Fedeltà e premi {#loyalty-and-rewards}

### Voucherify {#voucherify}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è mantenuto da o formalmente supportato da Voucherify. Conferma i dettagli API correnti con la documentazione di Voucherify.

>[!BEGINSHADEBOX]

Voucherify fornisce promozioni e API REST per la fidelizzazione (campagne, voucher, programmi fedeltà).

I casi d’uso tipici includono la fedeltà di lettura o lo stato di promozione per le offerte nel contenuto e la visualizzazione di livello o saldo, se appropriato.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e i limiti di Voucherify.

Si applicano i seguenti prerequisiti:

* ID applicazione e segreto (per area geografica/cluster); chiarezza sugli endpoint di fidelizzazione o campagna da chiamare.
* Accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* Evita di esporre gli identificatori interni di campagne o promozioni negli errori rivolti al cliente o nel contenuto dei messaggi.
* Si applicano limiti di velocità a livello di applicazione. Configura nuovi tentativi e memorizzazione in cache secondo le linee guida di Voucherify.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Imposta l&#39;URL di base per il cluster, aggiungi le intestazioni richieste (`X-APP-ID`, `X-APP-TOKEN`), vincola gli endpoint di elenco con filtri o ID, incolla JSON di esempio, mappa i campi, verifica, attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando le API Loyalty/REST. Per [Voucherify](https://docs.voucherify.io/){target="_blank"}, imposta l&#39;host **cluster** e i percorsi per la tua area geografica. Esempio di pattern URL:

   `https://{cluster}.voucherify.io/`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

Campi di integrazione di esempio. Riferimento completo: [API Voucherify](https://docs.voucherify.io/reference/introduction){target="_blank"}.

| Campo | Valore |
| --- | --- |
| **URL** | `https://{{cluster}}.voucherify.io/v1/loyalties/{{campaignId}}/members` |
| **metodo HTTP** | `GET` |
| Payload di risposta | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |
| Policy | Configura i dettagli a livello di criterio in base alle tue esigenze. |

**Parametri percorso**

| Parametro percorso | Nome | Valore predefinito |
| --- | --- | --- |
| `cluster` | `cluster` | `<your_cluster>` |
| `campaignId` | `campaignId` | `<loyalty_campaign_Id>` |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Content-Type (predefinito) | Content-Type | Costante | application/json | Sì (attivato) |
| X-APP-ID | X-APP-ID | Costante | `<YOUR-APP-ID>` | Sì (attivato) |
| X-Voucherify-Channel | X-Voucherify-Channel | Costante | Documentazione di Voucherify | No (disattivato) |

**Parametri query**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| `limit` | `limit` | Variable | 10 | No (disattivato) |
| `page` | `page` | Variable | 1 | No (disattivato) |
| `customer` | `customer` | Variable | `<customer_identifier>` | No (disattivato) |
| `created_at` | `created_at` | Variable | `<iso8601_date>` | No (disattivato) |
| `updated_at` | `updated_at` | Variable | `<iso8601_date>` | No (disattivato) |
| `order` | `order` | Variable | `<sort_field>` | No (disattivato) |
| `code` | `code` | Variable | `<loyalty_card_code>` | No (disattivato) |
| `ids` | `ids` | Variable | `<array_of_ids>` | No (disattivato) |

**Autenticazione**

| Tipo | Nome chiave API | Valore chiave API | Posizione |
| --- | --- | --- | --- |
| Chiave API | X-APP-TOKEN | `<YOUR-APP-TOKEN>` | Header |

+++

### Talon.One {#talon-one}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è mantenuto da Talon.One o formalmente supportato da Talon.One. Conferma i dettagli API correnti con la documentazione di Talon.One.

>[!BEGINSHADEBOX]

Talon.One è un motore di regole per la promozione e la fedeltà con API REST per sessioni, effetti e profili.

I casi d’uso tipici includono promozioni a livello di carrello o profilo in contenuti personalizzati e visualizzazione di progressi o premi di fedeltà.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni di Talon.One.

Si applicano i seguenti prerequisiti:

* Chiave API e URL di base specifico per la distribuzione; identificatori per l’ambito di applicazione o campagna.
* Accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* I flussi che coinvolgono più sessioni possono richiedere un’attenta mappatura al modello di richiesta Integrazioni.
* Osservare i limiti di velocità di Talon.One e la guida idempotenza.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Utilizza **GET** nel profilo o nel percorso di raggiungimento richiesto, imposta `Authorization: ApiKey-v1 <key>` come documentato, incolla JSON di esempio, mappa i campi, verifica, attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando l’API di integrazione Talon.One. Esempio di pattern URL:

   `https://{your-domain}.talon.one/v1/...`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

| Campo | Valore |
| --- | --- |
| **URL** | `https://{{your-deployment}}.talon.one/v1/customer_profiles/{{integrationId}}/achievements/{{achievementId}}` |
| **metodo HTTP** | `GET` |

**Parametri percorso**

| Parametro percorso | Nome | Valore predefinito |
| --- | --- | --- |
| `your-deployment` | `your-deployment` | `<your_deployment>` |
| `integrationId` | `integrationId` | `<integrationId>` |
| `achievementId` | `achievementId` | `<achievementId>` |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Content-Type (predefinito) | Content-Type | Costante | application/json | Sì (attivato) |

**Parametri query**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| `progressStatus` | `progressStatus` | Variable | in corso / completato / scaduto | No (disattivato) |
| `startDate` | `startDate` | Variable | 2024-05-29T15:04:05+07:00 | No (disattivato) |
| `endDate` | `endDate` | Variable | 2024-05-29T15:04:05+07:00 | No (disattivato) |
| `pageSize` | `pageSize` | Variable | `<default_page_size>` | No (disattivato) |
| `skip` | `skip` | Variable | `<items_to_skip>` | No (disattivato) |

**Autenticazione**

| Tipo | Nome chiave API | Valore chiave API | Posizione |
| --- | --- | --- | --- |
| Chiave API | Authorization | ApiKey-v1 `<YOUR_API_KEY>` | Header |

+++

### Antavo {#antavo}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è mantenuto da Antavo o formalmente supportato da Antavo. Conferma i dettagli API correnti con la documentazione di Antavo.

>[!BEGINSHADEBOX]

Antavo è una piattaforma di fidelizzazione aziendale con API REST per membri, premi ed eventi.

I casi d’uso tipici includono punti, livelli o premi nelle e-mail o nelle notifiche push e nelle offerte guidate dallo stato di fedeltà.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni di Antavo.

Si applicano i seguenti prerequisiti:

* Stack di credenziali URL e API; identificatori di programma o negozio, come richiesto.
* Accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* I dati PII del cliente devono essere gestiti in base agli accordi Antavo e alle politiche sulla privacy.
* Conferma le versioni API e gli endpoint stabili con Antavo per il tuo ambiente.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Configura **GET** con l&#39;autenticazione del fornitore (ad esempio, chiave API nella query), evita di esporre PII rispetto ai criteri, incolla JSON di esempio, mappa i campi, prova, attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando l’API Enterprise di Antavo.

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

I campi di integrazione di esempio utilizzano l&#39;host **staging**; la produzione utilizza il nome host dello stack Antavo. Consulta la [documentazione di Antavo](https://antavo.com/docs/){target="_blank"}.

| Campo | Valore |
| --- | --- |
| **URL** | `https://api.staging.antavo.com/customers/{{customer_id}}/activities/offers` |
| **metodo HTTP** | `GET` |
| **Criterio** | Configura i dettagli a livello di criterio in base alle tue esigenze. |
| **Payload di risposta** | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |

**Parametri percorso**

| Parametro percorso | Nome | Valore predefinito |
| --- | --- | --- |
| `customer_id` | `customer_id` | `<customer_id>` |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Content-Type (predefinito) | Content-Type | Costante | application/json | Sì (attivato) |
| Accetta | Accetta | Costante | application/json | No (disattivato) |

**Autenticazione**

| Tipo | Nome chiave API | Valore chiave API | Posizione |
| --- | --- | --- | --- |
| Chiave API | `api_key` | `<YOUR_API_KEY>` | Parametri query |

+++

### Fedeltà Salesforce {#salesforce-loyalty}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è gestito da Salesforce né è formalmente supportato da. Conferma i dettagli API correnti con la documentazione di Salesforce.

>[!BEGINSHADEBOX]

Salesforce Loyalty Management espone API REST sulla piattaforma Salesforce per membri, programmi e transazioni.

I casi d’uso tipici includono il superamento di livelli, punti o vantaggi nei percorsi e l’allineamento della messaggistica con i dati di gestione delle relazioni con i clienti e i dati fedeltà.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e i limiti per la fedeltà a Salesforce.

Si applicano i seguenti prerequisiti:

* l’istanza Salesforce, l’app connessa o l’utente dell’integrazione e OAuth appropriati per la tua organizzazione.
* Accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* I limiti dell’API Salesforce e l’aggiornamento del token OAuth devono essere progettati nell’integrazione.
* Le regole di sicurezza e condivisione a livello di campo determinano quali campi vengono visualizzati nelle risposte API.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Utilizza l’endpoint di integrazione della fedeltà approvato dal team, completa Salesforce OAuth, incolla il JSON di esempio, mappa i campi, rispetta i limiti dell’API composita, verifica, attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configurare l’endpoint utilizzando Salesforce Loyalty Management REST. Esempio di pattern URL:

   `https://{instance}.salesforce.com/services/data/vXX.X/...`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

Utilizzare l&#39;operazione GET del **profilo membro** di Gestione della fedeltà documentata per la versione API dell&#39;organizzazione; i percorsi includono gli identificatori di programma e membro. Consulta [Sviluppatori Salesforce](https://developer.salesforce.com/){target="_blank"}.

| Campo | Valore |
| --- | --- |
| **URL** | `https://{{your-instance}}.my.salesforce.com/services/data/{{version}}/connect/loyalty/management/members` |
| **metodo HTTP** | `GET` |
| **Criterio** | Configura i dettagli a livello di criterio in base alle tue esigenze. |
| **Payload di risposta** | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |

**Parametri percorso**

| Parametro percorso | Nome | Valore predefinito |
| --- | --- | --- |
| `your-instance` | `your-instance` | `<your_instance>` |
| `version` | `version` | `version` |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Content-Type (predefinito) | Content-Type | Costante | application/json | Sì (attivato) |
| Accetta | Accetta | Costante | application/json | No (disattivato) |

**Parametri query**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| `membershipNumber` | `membershipNumber` | Variable | `<membership_number>` | No (disattivato)* |
| `membershipId` | `membershipId` | Variable | `<membership_id>` | No (disattivato)* |
| `posMemId` | `posMemId` | Variable | `<pos_mem_id>` | No (disattivato)* |

\* È richiesto almeno uno dei tre.

**Autenticazione**

| Tipo | Nome chiave API | Valore chiave API | Posizione |
| --- | --- | --- | --- |
| Chiave API | Authorization | `<access_token>` | Header |

+++

### Capillare {#capillary}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è mantenuto da o formalmente supportato da Capillary. Conferma i dettagli API correnti con la documentazione di Capillary.

>[!BEGINSHADEBOX]

Capillary fornisce API di fidelizzazione e coinvolgimento comuni negli stack di vendita al dettaglio.

I casi d’uso tipici includono punti, livelli o offerte all’interno di percorsi personalizzati.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni di Capillary.

Si applicano i seguenti prerequisiti:

* Host API e autenticazione (richieste spesso firmate; segui i documenti Capillary).
* Identificatori di programma per l’endpoint.

Si applicano le seguenti limitazioni ed esclusioni:

* Gli schemi di autenticazione e gli host regionali variano a seconda della distribuzione. Conferma con Capillary per lo stack.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Configura le intestazioni come `CAP-API-ACCESS-TOKEN` come richiesto, incolla il JSON campione, mappa i campi, prova, attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando le API Capillary.

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

Esempio: `https://ushc.intouch.capillarytech.com/api/v3/rewards/{reward_id}` (l&#39;host varia in base all&#39;area geografica). Convalida lo schema host e di autenticazione con [Capillary](https://capillarytech.com/){target="_blank"}.


| Campo | Valore |
| --- | --- |
| **URL** | `https://ushc.intouch.capillarytech.com/api/v3/rewards/{{reward_id}}` |
| **metodo HTTP** | `GET` |
| **Criterio** | Configura i dettagli a livello di criterio in base alle tue esigenze. |
| **Payload di risposta** | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |

**Parametri percorso**

| Parametro percorso | Nome | Valore predefinito |
| --- | --- | --- |
| `reward_id` | ID premio | `<your_reward_id>` |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Content-Type | Content-Type | Costante | application/json | Sì (attivato) |
| CAP-API-ACCESS-TOKEN | Token di accesso | Costante | `<YOUR_ACCESS_TOKEN>` | Sì (attivato) |

**Autenticazione**

| Tipo | Nome chiave API | Valore chiave API | Posizione |
| --- | --- | --- | --- |
| Chiave API | CAP-API-ACCESS-TOKEN | `<YOUR_ACCESS_TOKEN>` | Header |

+++


## Modelli e messaggi {#templates-and-messaging}

### Stensul {#stensul}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è mantenuto da Stensul o formalmente supportato da Stensul. Conferma i dettagli API correnti con la documentazione di Stensul.

>[!BEGINSHADEBOX]

Stensul è una piattaforma per la creazione di e-mail per modelli approvati; Journey Optimizer può utilizzare metadati di modelli e aree strutturate tramite la sua API.

I casi d’uso tipici includono l’importazione di modelli approvati e le aree di mappatura agli attributi di profilo, nonché il riutilizzo di blocchi governati per le build scalabili delle campagne.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni di Stensul.

Si applicano i seguenti prerequisiti:

* Account permanente con accesso API e modelli pubblicati con token definiti.
* Accesso amministratore in Journey Optimizer per creare integrazioni.

Si applicano le seguenti limitazioni ed esclusioni:

* La modifica diretta in WYSIWYG dei modelli Stensul in Journey Optimizer non è trattata qui.
* I HTML di grandi dimensioni o complessi nei payload dei modelli possono richiedere l’analisi della sicurezza e la bonifica.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione.

1. Configura l’endpoint utilizzando l’URL dell’API per modelli Stensul. Esempio di pattern URL:

   `https://api.stensul.com/v1/templates/{template_id}`

1. Configurare l’autenticazione (chiave API o OAuth in base alla documentazione API di Stensul).

1. Definisci le variabili di percorso , ad esempio l’ID modello.

1. Incolla una risposta JSON campione per il rilevamento del campo.

1. Mappa i campi modello richiesti ai campi di personalizzazione Journey Optimizer.

1. Verifica la connessione e attiva.

### Marigold {#marigold}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è mantenuto da Marigold o formalmente supportato da Marigold. Conferma i dettagli API correnti con la documentazione di Marigold.

>[!BEGINSHADEBOX]

Marigold espone le API di fidelizzazione e coinvolgimento; gli host differiscono in base alla geografia (nomi host del modulo UE vs US).

Un caso d’uso tipico consiste nell’arricchire i messaggi con dati di fidelizzazione o preferenze provenienti dai programmi Marigold.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e sulle limitazioni di Marigold.

Si applicano i seguenti prerequisiti:

* URL di base e credenziali dal contratto; utente API con privilegi minimi, quando possibile.
* Accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* Gli endpoint variano in base al prodotto Marigold. Esegui la convalida con il supporto Marigold per la distribuzione.
* I dati personali contenuti nelle risposte devono essere conformi all’accordo sulla protezione dei dati e alle politiche di conservazione.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Puntare all&#39;host Marigold per la propria regione, impostare l&#39;autenticazione (l&#39;esempio seguente utilizza `X-Api-Key` con chiave e segreto), incollare JSON campione, mappare i campi, testare, attivare.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando l’API REST Marigold.

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

1. Marigold utilizza 2 endpoint in base all’area geografica per la quale è attiva l’istanza del cliente:

   * Europa: `https://{{customername}}.module.slgnt.eu`
   * USA: `https://{{customername}}.module.slgnt.us`

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

L&#39;host di base dipende dalla regione (ad esempio `https://{{customername}}.module.slgnt.eu` o `https://{{customername}}.module.slgnt.us`). Conferma i percorsi con Marigold per la distribuzione.

| Campo | Valore |
| --- | --- |
| **URL** | `https://{{customername}}.module.slgnt.{{locale}}/Portal/Api/organizations/{{organization}}/content/{{api_name}}` |
| **metodo HTTP** | `GET` |
| Payload di risposta | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |
| Policy | Configura i dettagli a livello di criterio in base alle tue esigenze. |

**Parametri percorso**

| Parametro percorso | Nome | Valore predefinito |
| --- | --- | --- |
| `customername` | `customername` | `<your_name>` |
| `locale` | `locale` | `eu` / `us` |
| `organization` | `organization` | `<your_organization>` |
| `api_name` | `api_name` | `<api_name>` |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Content-Type (predefinito) | Content-Type | Costante | application/json | Sì (attivato) |

**Autenticazione**

| Tipo | Nome chiave API | Valore chiave API | Posizione |
| --- | --- | --- | --- |
| Chiave API | X-Api-Key | `<apiKey>:<apiSecret>` | Header |

+++

### Consigli di Adobe Target {#adobe-target-recommendations}

>[!IMPORTANT]
>
>Questa configurazione è un modello illustrativo testato dal team Adobe Journey Optimizer. La funzione Consigli di Adobe Target è un prodotto Adobe separato con un proprio ciclo di rilascio e un controllo delle versioni API. Prima di distribuire in produzione, conferma sempre i dettagli API correnti con la [documentazione per gli sviluppatori di Adobe Target](https://experienceleague.adobe.com/en/docs/target-dev/developer/overview).

>[!BEGINSHADEBOX]

Adobe Target include Recommendations e API di consegna per esperienze lato server o integrate, in base ai diritti.

I casi d’uso tipici includono l’inserimento di consigli nelle esperienze create in Journey Optimizer e l’allineamento delle chiavi con il profilo o il contesto Experience Platform.

<!--
➡️ After you activate the integration, learn how to [use Adobe Target data in message templates](integrations-personalization.md#use-adobe-target-in-templates).
-->

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni per la funzione Consigli di Adobe Target.

Si applicano i seguenti prerequisiti:

* Target con Recommendations; organizzazione IMS e autenticazione supportata.
* Accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* Le API per la generazione di consigli e consegne richiedono parametri specifici (ad esempio mbox o identificatori di prodotto). Segui la documentazione di Adobe Target.
* Ottimizza la latenza e il caching per il volume di invio e il caso d’uso.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Le chiamate di consegna sono spesso **POST** con un corpo JSON. Configura OAuth per [autenticazione Target](https://experienceleague.adobe.com/en/docs/target-dev/developer/api/configure-authentication){target="_blank"}, incolla una risposta di esempio, mappa i campi e verifica nel volume previsto.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando le API di consegna/Recommendations di Target.

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

| Campo | Valore |
| --- | --- |
| **URL** | `https://{{client}}.tt.omtrdc.net/rest/v1/delivery` |
| Policy | Configura i dettagli a livello di criterio in base alle tue esigenze. |
| **metodo HTTP** | `POST` |

**Parametri percorso**

| Parametro percorso | Nome | Valore predefinito |
| --- | --- | --- |
| `client` | `client` | `<client_name>` |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Content-Type (predefinito) | Content-Type | Costante | application/json | Sì (attivato) |

**Parametri query**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| client | client | Variable | `<customer_client_code>` | Sì (attivato) |
| sessionId | sessionId | Variable | ` <session_identifier>` | Sì (attivato) |

**Autenticazione**

Fai riferimento a [Configurazione autenticazione di destinazione](https://experienceleague.adobe.com/en/docs/target-dev/developer/api/configure-authentication) e aggiungi JSON al payload.

**Richiedi payload**

```Sample Request Payload JSON
{
  "id": {
    "tntId": "<YOUR_TENANT_ID>"
  },
  "context": {
    "channel": "web",
    "address": {
      "url": "https://example.com/store.html"
    },
    "screen": {
      "width": 1200,
      "height": 1400
    }
  },
  "experienceCloud": {
    "analytics": {
      "logging": "server_side",
      "supplementalDataId": "<supDataId>",
      "trackingServer": "sstats.adobe.com"
    }
  },
  "execute": {
    "pageLoad": {
      "parameters": {
        "pageType": "checkout",
        "preferredCurrency": "$"
      }
    },
    "mboxes": [
      {
        "index": 1,
        "name": "orderConfirmPage"
      }
    ]
  },
  "prefetch": {
    "views": [
      {
        "parameters": {
          "ad": "view"
        }
      }
    ],
    "mboxes": {
      "index": 1,
      "name": "SummerOffer"
    }
  }
}
```

+++


## Dati, meteo e operazioni {#data-weather-and-operations}

### AccuWeather {#accuweather}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è mantenuto da o formalmente supportato da AccuWeather. Conferma i dettagli API correnti con la documentazione di AccuWeather.

>[!BEGINSHADEBOX]

AccuWeather espone previsioni e posizione API REST in modo che i messaggi possano includere snippet in base al meteo.

I casi d’uso tipici includono previsioni brevi per e-mail o push e contenuti personalizzati utilizzando valori di previsione legati al profilo o al contesto.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni di AccuWeather.

Si applicano i seguenti prerequisiti:

* Abbonamento API e chiave; chiave di posizione o flusso di ricerca della città.
* Accesso amministratore in Journey Optimizer per creare integrazioni.

Si applicano le seguenti limitazioni ed esclusioni:

* Conferma la forma di risposta JSON per il livello di abbonamento AccuWeather; le integrazioni mappano i campi dalle risposte JSON.
* Osserva i limiti di velocità di AccuWeather e il caching consigliato.
* La risoluzione di `locationKey` richiede spesso una richiesta di geolocalizzazione o di ricerca di città separata prima delle chiamate di previsione.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Utilizza **GET** a meno che la sottoscrizione non richieda diversamente, allega il parametro di query `apiKey`, mappa `locationKey` e altre variabili dal profilo/contesto, incolla JSON di esempio, mappa i campi, quindi verifica.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando l’API Daily Forecasts. Esempio di pattern URL:

   `https://dataservice.accuweather.com/forecasts/v1/daily/{days}day/{locationKey}`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++Campi di integrazione di esempio

Campi di integrazione di esempio. Dettagli e livelli sono descritti in [API AccuWeather](https://developer.accuweather.com/apis){target="_blank"}. Risolvi spesso `locationKey` con una chiamata di ricerca posizioni separata (ad esempio `.../locations/v1/cities/search?q={{cityName}}`).

| Campo | Valore |
| --- | --- |
| **URL** | `https://dataservice.accuweather.com/forecasts/v1/daily/{{days}}day/{{locationKey}}` |
| **metodo HTTP** | `GET` |
| Payload di risposta | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |
| Policy | Configura i dettagli a livello di criterio in base alle tue esigenze. |

**Parametri percorso**

| Parametro percorso | Nome | Valore predefinito |
| --- | --- | --- |
| `days` | `days` | `15` |
| `locationKey` | `locationKey` | `<desired_location_key>` |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Content-Type (predefinito) | Content-Type | Costante | application/json | Sì (attivato) |

**Parametri query**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| `format` | `format` | Variable | json | No (disattivato) |
| `language` | `language` | Variable | en-US | No (disattivato) |
| `details` | `details` | Variable | False | No (disattivato) |
| `metric` | `metric` | Variable | False | No (disattivato) |

**Autenticazione**

| Tipo | Nome chiave API | Valore chiave API | Posizione |
| --- | --- | --- | --- |
| Chiave API | `apiKey` | `<YOUR_API_KEY>` | Parametri query |

+++

### ShipStation {#shipstation}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è gestito da o formalmente supportato da ShipStation. Conferma i dettagli API correnti con la documentazione di ShipStation.

>[!BEGINSHADEBOX]

ShipStation offre API per la spedizione e l&#39;ordine di vettori, etichette e tracciamento.

I casi d’uso tipici includono lo stato degli ordini, i collegamenti di tracciamento o le ETA di consegna nei messaggi transazionali.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni di ShipStation.

Si applicano i seguenti prerequisiti:

* Chiave API e segreto (autenticazione di base per documenti ShipStation).
* Accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* Non esporre le chiavi API ShipStation nel contenuto del messaggio; mantieni le credenziali solo nella configurazione dell’integrazione.
* Gli endpoint di elenco impaginati possono non essere adatti alle integrazioni; preferisci GET a risorsa singola, quando possibile.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Eseguire il targeting della risorsa necessaria (ordini e spedizioni), autenticarla per [API ShipStation](https://www.shipstation.com/docs/api/){target="_blank"}, incollare JSON di esempio, mappare i campi, testare, attivare.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando l’API REST ShipStation. Esempio di pattern URL:

   `https://ssapi.shipstation.com/...`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

Nell&#39;esempio di **Ottieni timer** seguente viene illustrata una chiamata di temporizzazione per l&#39;automazione ShipStation. Utilizzare il percorso esatto e l&#39;autenticazione della guida all&#39;integrazione di ShipStation durante la riproduzione in Journey Optimizer.

| Campo | Valore |
| --- | --- |
| **URL** | `https://dashboard.sendtric.com/api/v1/timers/{{id}}` |
| **metodo HTTP** | `POST` |
| **Criterio** | Configura i dettagli a livello di criterio in base alle tue esigenze. |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Content-Type (predefinito) | Content-Type | Costante | application/json | Sì (attivato) |

**Autenticazione**

| Tipo | Nome chiave API | Valore chiave API | Posizione |
| --- | --- | --- | --- |
| Chiave API | apiKey | `<your_api_key>` | Header |

**Richiedi payload**

```Sample Request Payload
{
    "external_batch_id": "se-28529731",
    "batch_notes": "This is my batch",
    "shipment_ids": [
      "se-28529731"
    ],
    "rate_ids": [
      "se-28529731"
    ]
}
```

+++

### RevenueCat {#revenuecat}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è gestito da RevenueCat o formalmente supportato da quest’ultimo. Conferma i dettagli API correnti con la documentazione RevenueCat.

>[!BEGINSHADEBOX]

RevenueCat fornisce le API per lo stato degli abbonamenti e i diritti per le app.

Un caso d’uso tipico riflette lo stato di abbonamento nelle campagne del ciclo di vita in cui i criteri lo consentono.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e sulle limitazioni di RevenueCat.

Si applicano i seguenti prerequisiti:

* Chiave API segreta e identificatori di app; mappatura stabile tra profili e ID cliente RevenueCat.
* Accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* Proteggi le chiavi API segrete e segui i tuoi criteri di rotazione.
* I dati relativi all’abbonamento e all’adesione sono sensibili. Rispetta i requisiti sulla privacy e sul consenso.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Chiama il REST **GET** modellato di seguito, esegui l&#39;autenticazione con l&#39;intestazione della chiave segreta, incolla il JSON di esempio, mappa i campi, verifica, attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando l’API REST RevenueCat. Esempio di pattern URL:

   `https://api.revenuecat.com/v1/...`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

Esempio di pattern: utilizza **Get a Product** di RevenueCat (o GET equivalente a prodotto/diritto) dai [documenti RevenueCat](https://docs.revenuecat.com/){target="_blank"} con l&#39;URL e la versione di base del progetto.

| Campo | Valore |
| --- | --- |
| **URL** | `https://api.revenuecat.com/projects/{{project_id}}/products/{{product_id}}` |
| **metodo HTTP** | `GET` |
| **Criterio** | Configura i dettagli a livello di criterio in base alle tue esigenze. |
| **Payload di risposta** | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |

**Parametri percorso**

| Parametro percorso | Nome | Valore predefinito |
| --- | --- | --- |
| `project_id` | `project_id` | `<project_id>` |
| `product_id` | `product_id` | `<product_id>` |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Content-Type (predefinito) | Content-Type | Costante | application/json | Sì (attivato) |

**Parametri query**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| `country` | `country` | Variable | `<iso_country_code>` | No (disattivato) |
| `locale` | `locale` | Variable | `<locale_code>` | No (disattivato) |
| `parentId` | `parentId` | Variable | `<parent_category_id>` | No (disattivato) |

**Autenticazione**

| Tipo | Nome chiave API | Valore chiave API | Posizione |
| --- | --- | --- | --- |
| Chiave API | Authorization | `Bearer <token>` | Header |

+++

### Databricks {#databricks}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è gestito da o formalmente supportato dalle banche dati. Conferma i dettagli API correnti con la documentazione Databricks.

>[!BEGINSHADEBOX]

Databricks fornisce API SQL e REST sui dati di lakehouse; le bozze precedenti combinavano le indicazioni di esecuzione delle istruzioni con un esempio di **processi/get**.

Un caso d’uso tipico prevede l’utilizzo di attributi piccoli e denormalizzati da tabelle gestite per la personalizzazione con il minimo privilegio.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni per le banche dati.

Si applicano i seguenti prerequisiti:

* Host Workspace, token o OAuth per criterio organizzazione; entità servizio con ambito minimo.
* Accesso amministratore in Journey Optimizer.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Preferisci percorsi di lettura ristretti; se utilizzi l&#39;esecuzione dell&#39;istruzione **POST**, includi il corpo JSON richiesto dall&#39;API, incolla una risposta di successo campione per la mappatura, verifica attentamente la latenza, attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configurare l&#39;endpoint utilizzando l&#39;API di esecuzione delle istruzioni SQL Databricks. Esempio di pattern URL:

   `https://{workspace-host}/api/2.0/sql/statements/...`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++Campi di integrazione di esempio

L&#39;esempio di processo **GET** di seguito è illustrativo; per la personalizzazione basata su SQL, preferisci il modello [API di esecuzione istruzione](https://docs.databricks.com/api/workspace/statementexecution){target="_blank"} supportato dall&#39;area di lavoro.

| Campo | Valore |
| --- | --- |
| **URL** | `https://<databricks-instance>/api/2.0/jobs/get` |
| **metodo HTTP** | `GET` |
| Payload di risposta | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |
| Policy | Configura i dettagli a livello di criterio in base alle tue esigenze. |
| Autenticazione | OAuth |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Accetta | Accetta | Costante | application/json | Sì (attivato) |

**Parametri query**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| `job_id` | `job_id` | Variable | `12` | Sì |

+++

## Recensioni, consenso e social network {#reviews-consent-and-social}

### Bynder {#bynder}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è mantenuto da Bynder o formalmente supportato da Bynder. Conferma i dettagli API correnti con la documentazione di Bynder.

>[!BEGINSHADEBOX]

Bynder è un DAM con API REST; le integrazioni comunemente utilizzano OAuth 2.0 per metadati di sola lettura o URL di risorse.

I casi d’uso tipici includono l’estrazione dei metadati di risorse o degli URL di consegna nei messaggi e il mantenimento dell’allineamento della creatività approvata in Bynder con i percorsi.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni di Bynder.

Si applicano i seguenti prerequisiti:

* Dominio portale e client OAuth (o approccio token approvato).
* Ambiti per l’accesso in sola lettura; accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* L’aggiornamento della paginazione e del token OAuth deve seguire le regole API di Bynder.
* Risposte impaginate di grandi dimensioni: mappa solo i campi necessari per la personalizzazione.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Configura **GET** sull&#39;endpoint scelto (un modello comune è l&#39;elenco degli utenti), completa OAuth per [Bynder](https://developer.bynder.com/){target="_blank"}, evita di richiamare pagine di dati non necessarie, mappa i campi, verifica, quindi attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando l’API Bynder v4. Esempio di pattern URL:

   `https://{your-bynder-domain}/api/v4/users/`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

Campi di integrazione di esempio. Consulta la [documentazione dell&#39;API Bynder](https://developer.bynder.com/){target="_blank"} per i dettagli del payload di OAuth 2.0.

| Campo | Valore |
| --- | --- |
| **URL** | `https://{{your-bynder-domain}}/api/v4/users/` |
| **metodo HTTP** | `GET` |
| Payload di risposta | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |
| Policy | Configura i dettagli a livello di criterio in base alle tue esigenze. |

**Parametri percorso**

| Parametro percorso | Nome | Valore predefinito |
| --- | --- | --- |
| `your-bynder-domain` | `your-bynder-domain` | `<your-bynder-domain>` |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Content-Type (predefinito) | Content-Type | Costante | application/json | Sì (attivato) |
| Authorization | Authorization | Costante | Bearer `<token>` | Sì (attivato) |

**Parametri query**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| `includeInActive` | `includeInActive` | Variable | False | No (disattivato) |
| `limit` | `limit` | Variable | 100 | No (disattivato) |
| `page` | `page` | Variable | 1 | No (disattivato) |

**Autenticazione**

| Tipo | Payload |
| --- | --- |
| OAuth 2.0 | Payload OAuth 2.0 (consulta la documentazione di Bynder) |

```
{
    "type": "oauth2",
    "endpoint": {
        "uri": ""
    },
    "method": "get",
    "response": {
        "type": "json"
    },
    "request": {
        "header": [
            {
                "key": "client_id",
                "value": ""
            },
            {
                "key": "client_secret",
                "value": ""
            }
        ],
        "queryParams": [
            {
                "key": "grant_type",
                "value": ""
            },
            {
                "key": "scope",
                "value": ""
            }
        ],
        "payload": {
            "type": "json",
            "content": {}
        }
    },
    "credentialPaths": [
        "header.client_id",
        "header.client_secret",
        "queryParam.scope"
    ],
    "tokenPath": "message.token",
    "policy": {
        "timeoutInMilliseconds": 30000,
        "cache": {
            "enabled": true,
            "ttlInSeconds": 300
        },
        "retry": {
            "enabled": false
        }
    },
    "locationConfig": {
        "key": "x-token",
        "location": "query"
    }
}
```

+++

### Trustpilot {#trustpilot}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è gestito da Trustpilot né formalmente sostenuto da quest&#39;ultimo. Conferma i dettagli API correnti con la documentazione Trustpilot.

>[!BEGINSHADEBOX]

Trustpilot fornisce API per i dati di riepilogo aziendali e di revisione laddove il caso d’uso e il contratto lo consentono.

Un caso d’uso tipico mostra conteggi o valutazioni di recensioni in contenuti di marketing conformi ai termini di Trustpilot.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni di Trustpilot.

Si applicano i seguenti prerequisiti:

* Chiave API e caso d’uso approvato; identificatori aziendali per le query.
* Accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* L’utilizzo dei dati Trustpilot deve essere conforme alle politiche di branding e uso dei dati Trustpilot.
* I limiti di tasso si applicano al riepilogo delle revisioni e agli endpoint correlati.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Configura **GET** con l&#39;autenticazione della query richiesta, mappa gli identificatori dal profilo o dal contesto, incolla il JSON di esempio, mappa i campi, verifica, attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando le API Trustpilot. Esempio di pattern URL:

   `https://api.trustpilot.com/v1/...`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

Utilizza l&#39;operazione di elenco categorie di [sviluppatori Trustpilot](https://developers.trustpilot.com/){target="_blank"} per il tuo modello di integrazione; i parametri variano in base alla risorsa.

| Campo | Valore |
| --- | --- |
| **URL** | `https://api.trustpilot.com/v1/categories` |
| **metodo HTTP** | `GET` |
| **Criterio** | Configura i dettagli a livello di criterio in base alle tue esigenze. |
| **Payload di risposta** | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Content-Type (predefinito) | Content-Type | Costante | application/json | Sì (attivato) |

**Parametri query**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| `country` | `country` | Variable | `<iso_country_code>` | No (disattivato) |
| `locale` | `locale` | Variable | `<locale_code>` | No (disattivato) |
| `parentId` | `parentId` | Variable | `<parent_category_id>` | No (disattivato) |

**Autenticazione**

| Tipo | Nome chiave API | Valore chiave API | Posizione |
| --- | --- | --- | --- |
| Chiave API | apiKey | `<your_api_key>` | Header |

+++

### Bazaarvoice {#bazaarvoice}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è gestito da o formalmente supportato da Bazarvoice. Conferma i dettagli API correnti con la documentazione di Bazarvoice.

>[!BEGINSHADEBOX]

Bazarvoice fornisce valutazioni, recensioni e API UGC.

Un caso d’uso tipico consiste nel mostrare riepiloghi di revisione o valutazioni nelle e-mail quando la policy lo consente.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni di Bazarvoice.

Si applicano i seguenti prerequisiti:

* La passkey API e gli identificatori client del contratto.
* Accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* La visualizzazione delle valutazioni e delle recensioni deve rispettare le policy sui contenuti Bazarvoice.
* I limiti di frequenza e le regole di caching si applicano per chiave API.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Utilizza **GET** con `passkey` come parametro di query nell&#39;API delle conversazioni, imposta `Accept: application/json`, incolla JSON di esempio, mappa i campi, verifica, attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando l’API per conversazioni Bazarvoice. Esempio di pattern URL:

   `https://api.bazaarvoice.com/...`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

Punto di ingresso di esempio: `https://api.bazaarvoice.com/data/products.json` con parametri di query versione e filtro. Vedi [Sviluppatore Bazaarvoice](https://developer.bazaarvoice.com/){target="_blank"}.

| Campo | Valore |
| --- | --- |
| **URL** | `https://api.bazaarvoice.com/data/products.json` |
| **metodo HTTP** | `GET` |
| **Criterio** | Configura i dettagli a livello di criterio in base alle tue esigenze. |
| **Payload di risposta** | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Accetta | Accetta | Costante | application/json | Sì (attivato) |

**Autenticazione**

| Tipo | Valore chiave | Posizione |
| --- | --- | --- |
| passkey | `<YOUR_ACCESS_TOKEN>` | Parametri query |

**Parametri query**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| `apiversion` | apiversionNumber | Costante | 5.4 | Sì (attivato) |
| `filter` | `filter` | Variable | Id:47950830 | No (disattivato) |
| `stats` | `stats` | Variable | tutto | No (disattivato) |

+++

### OneTrust {#onetrust}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è gestito da o formalmente supportato da OneTrust. Conferma i dettagli API correnti con la documentazione di OneTrust.

>[!BEGINSHADEBOX]

OneTrust espone le API per la privacy e il consenso (URL e schemi specifici del prodotto).

Un caso d’uso tipico è la lettura dei segnali di consenso o di preferenza per i contenuti condizionali consentiti dall’architettura e dalla revisione legale.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni di OneTrust.

Si applicano i seguenti prerequisiti:

* Credenziali API e URL di base regionale; approvazione legale per i campi utilizzati nei messaggi.
* Accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* I dati sul consenso e sulle preferenze sono altamente regolamentati. Coordina con la privacy e i team legali.
* I percorsi e i payload API sono diversi a seconda del prodotto OneTrust. Utilizza la documentazione per l’abbonamento.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Utilizza lo schema pubblicato o il percorso del centro preferenze per i documenti di abbonamento, completa OAuth se necessario, incolla JSON di esempio, mappa i campi, verifica, attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l&#39;endpoint utilizzando l&#39;API OneTrust. Il tenant, il prodotto e il percorso provengono dalla documentazione di [OneTrust](https://developer.onetrust.com/){target="_blank"} per la sottoscrizione. Esempio di pattern URL:

   `https://{tenant}.my.onetrust.com/api/...`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

| Campo | Valore |
| --- | --- |
| **URL** | `https://customer.my.onetrust.com/api/consentmanager/v2/preferencecenters/{{preferencecenterid}}/schema` |
| **metodo HTTP** | `GET` |
| **Criterio** | Configura i dettagli a livello di criterio in base alle tue esigenze. |
| **Payload di risposta** | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |
| **Autenticazione** | OAuth |

**Parametri percorso**

| Parametro | Nome | Elemento “value” |
| --- | --- | --- |
| `preferencecenterid` | `preferencecenterid` | `<pref-id>` |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Accetta | Accetta | Costante | application/json | Sì (attivato) |

**Parametri query**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| `state` | `state` | costante | PUBBLICATO | Sì |

+++

#### Schema del centro preferenze (pubblicato)

Esempio di pattern (frammento): `https://{tenant}.my.onetrust.com/api/consentmanager/v2/preferencecenters/{preferencecenterid}/schema?state=PUBLISHED`. Conferma il percorso esatto in [OneTrust Developer](https://developer.onetrust.com/){target="_blank"}.

### Meta {#meta}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è gestito da Meta né è formalmente supportato da. Conferma i dettagli API correnti con la documentazione di Meta.

>[!BEGINSHADEBOX]

Le API di Meta Graph e Marketing espongono gli oggetti catalogo e campagna per le integrazioni aziendali autorizzate.

Un caso d’uso tipico è arricchire il contenuto con attributi da Meta laddove i token e i criteri lo consentono.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni di Meta.

Si applicano i seguenti prerequisiti:

* Token utente o app di sistema con autorizzazioni corrette; allineamento di Business Manager.
* Accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* I token di accesso di breve durata richiedono un rinnovo o una strategia di lunga durata adatta alle integrazioni lato server.
* Rispetta i termini della piattaforma Meta; non registrare token o altri segreti nei payload dei messaggi.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Le chiamate al grafico sono spesso **GET** con un percorso con versione; gestisci la scadenza del token, incolla il JSON di esempio, mappa i campi, verifica, attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando l’API di Meta Graph. Esempio di pattern URL:

   `https://graph.facebook.com/vXX.X/...`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

Campi di integrazione di esempio. Consulta [Graph API](https://developers.facebook.com/docs/graph-api){target="_blank"} per il controllo delle versioni e i token di accesso.

| Campo | Valore |
| --- | --- |
| **URL** | `https://graph.facebook.com/{{API_VERSION}}/{{PRODUCT_CATALOG_ID}}/products` |
| **metodo HTTP** | `GET` |
| Payload di risposta | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |
| Policy | Configura i dettagli a livello di criterio in base alle tue esigenze. |
| Autenticazione | OAuth |

**Parametri percorso**

| Parametro percorso | Nome | Valore predefinito |
| --- | --- | --- |
| `API_VERSION` | `API_VERSION` | `v19.0` |
| `PRODUCT_CATALOG_ID` | `PRODUCT_CATALOG_ID` | `12345` |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Accetta | Accetta | Costante | application/json | Sì (attivato) |

**Parametri query**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| `fields` | `fields` | Variable | ID | No |
| `filter` | `filter` | Variable | — | No |

+++

### Aprimo {#aprimo}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è mantenuto da Aprimo o formalmente supportato da Aprimo. Conferma i dettagli API correnti con la documentazione di Aprimo.

>[!BEGINSHADEBOX]

Aprimo combina operazioni di marketing e API DAM per record, risorse e metadati.

I casi d’uso tipici includono campi di record o risorse approvati in contenuti dinamici e flussi di lavoro DAM gestiti in settori regolamentati.

>[!ENDSHADEBOX]

+++ Scopri i prerequisiti e le limitazioni di Aprimo.

Si applicano i seguenti prerequisiti:

* URL e credenziali tenant (OAuth o chiave API in base alla configurazione).
* Accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* La sicurezza a livello di campo di Aprimo deve essere allineata con gli attributi mappati in Journey Optimizer.
* Payload HAL o JSON di grandi dimensioni: limita i campi mappati al set minimo richiesto.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Utilizza **GET** nel percorso del record necessario, invia le intestazioni richieste come `API-VERSION`, incolla il file JSON di esempio (HAL o JSON restituito), mappa un set di campi minimo, verifica, attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando l’API DAM/Records di Aprimo. Utilizza l&#39;URL di base API e il percorso dei record per il **tenant** (secondo Aprimo). Esempio di pattern URL:

   `https://{tenant}.dam.aprimo.com/`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

| Campo | Valore |
| --- | --- |
| **URL** | `https://productstrategy1.dam.aprimo.com/api/core/record/{{recordID}}` |
| **metodo HTTP** | `GET` |

**Parametri percorso**

| Parametro percorso | Nome | Valore predefinito |
| --- | --- | --- |
| `recordId` | `recordId` | `<record_identifier>` |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Content-Type (predefinito) | Content-Type | Costante | application/json | Sì (attivato) |
| VERSIONE API | VERSIONE API | Costante | 1 | Sì (attivato) |
| Accetta | Accetta | Costante | application/hal+json OR application/json | No (disattivato) |
| select-record | select-record | Variable | `<selection_type>` | No (disattivato) |
| select-record-fields | select-record-fields | Variable | `<field_list>` | No (disattivato) |
| select-field | select-field | Variable | `<field_selection>` | No (disattivato) |

**Autenticazione**

| Tipo | Nome chiave API | Valore chiave API | Posizione |
| --- | --- | --- | --- |
| Chiave API | Authorization | Bearer `<token>` | Header |

+++

### Epsilon (Epsilon3) {#epsilon}

>[!IMPORTANT]
>
>Questo esempio di configurazione è stato testato in modo indipendente da Adobe come modello di esempio. Non è mantenuto da Epsilon o formalmente supportato da Epsilon. Conferma i dettagli API correnti con la documentazione di Epsilon.

>[!BEGINSHADEBOX]

Epsilon espone le API per contratto aziendale; gli URL di base e l’autenticazione provengono dal team del tuo account (l’esempio di API degli eventi riportato di seguito è illustrativo).

Un caso d’uso tipico espone gli attributi di fidelizzazione o offerta tramite API JSON supportate.

>[!ENDSHADEBOX]

+++ Ulteriori informazioni sui prerequisiti e le limitazioni di Epsilon (Epsilon3).

Si applicano i seguenti prerequisiti:

* Credenziali ed endpoint da Epsilon; accesso amministratore in Journey Optimizer.

Si applicano le seguenti limitazioni ed esclusioni:

* Endpoint e host sono specifici del cliente. Non distribuire senza la documentazione fornita dal team dell&#39;account Epsilon.

+++

Utilizza la procedura seguente per configurare questa integrazione in Journey Optimizer. Per i dettagli della richiesta, vedi **Campi di integrazione di esempio** e conferma questi valori con la documentazione del fornitore per il tuo ambiente.

1. Segui [Operazioni con le integrazioni](integrations.md). Non indovinare gli URL pubblici. Utilizza le specifiche di Epsilon, incolla il JSON di esempio, mappa i campi, verifica, attiva.

1. In Journey Optimizer, vai a **[!UICONTROL Configurazioni]** > **[!UICONTROL Gestisci]**, quindi seleziona **[!UICONTROL Crea integrazione]**.

1. Immetti un nome di integrazione senza spazi.

1. Configura l’endpoint utilizzando l’API Epsilon (in base alle specifiche di integrazione). L’URL di base e i percorsi delle risorse sono forniti dal team dell’account Epsilon. Esempio di pattern URL:

   `https://{your-instance}.epsilon3.io/api/...`

1. Seleziona il metodo HTTP mostrato nella tabella di configurazione, in genere GET, a meno che non venga indicato diversamente.

1. Configura l’autenticazione (intestazioni, parametri di query o OAuth) esattamente come specificato nella tabella e nella documentazione del fornitore.

1. Definisci i parametri di percorso, query ed intestazione e mappa le variabili su dati di profilo o contestuali, se necessario.

1. Incolla una risposta JSON campione in modo da poter rilevare e mappare i campi.

1. Seleziona i campi richiesti per la personalizzazione nella mappatura del payload di risposta.

1. Configura i criteri di timeout, nuovo tentativo e caching in base al volume previsto.

1. Verifica la connessione, quindi attiva l’integrazione.

La tabella seguente elenca alcuni valori di esempio per questa richiesta di integrazione.

+++ Campi di integrazione di esempio

Esempio di pattern: `https://{your-instance}.epsilon3.io/api/v1/planning/events` con `start` e `end` parametri di query e chiave API basata su intestazione. Verificare con Epsilon prima della produzione.

| Campo | Valore |
| --- | --- |
| **URL** | `https://{{your-instance}}.epsilon3.io/api/v1/planning/events` |
| **metodo HTTP** | `GET` |
| **Criterio** | Configura i dettagli a livello di criterio in base alle tue esigenze. |
| **Payload di risposta** | Seleziona e configura i campi di risposta desiderati da utilizzare durante l’authoring, in base alla risposta API. |

**Parametri percorso**

| Parametro percorso | Nome | Valore predefinito |
| --- | --- | --- |
| `your-instance` | `your-instance` | `<your_instance>` |

**Intestazioni**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| Content-Type (predefinito) | Content-Type | Costante | application/json | Sì (attivato) |

**Parametri query**

| Parametro | Nome | Tipo | Valore | Obbligatorio |
| --- | --- | --- | --- | --- |
| `start` | `start` | Variable | 2019-08-24T14:15:22Z | Sì (attivato)* |
| `end` | `end` | Variable | 2019-08-24T14:15:22Z | Sì (attivato)* |
| `eventType` | `eventType` | Variable | pianificato/non pianificato | No (disattivato) |
| `exclude_recurrences` | `exclude_recurrences` | Variable | true / false | No (disattivato) |

\* Facoltativo per `eventType` = `unscheduled` e per `exclude_recurrences` = `true`.

**Autenticazione**

| Tipo | Nome chiave API | Valore chiave API | Posizione |
| --- | --- | --- | --- |
| Chiave API | `<your_username>` | `<EPSILON3_API_KEY>` | Header |

+++

