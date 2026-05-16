---
solution: Journey Optimizer
product: journey optimizer
title: Esportazione di messaggi in Journey Optimizer
description: Scopri come esportare i messaggi
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: esportazione, messaggi, HIPAA, e-mail, SMS, configurazione
exl-id: 7b50c933-9738-4b1b-acae-08f0a8d41dab
TQID: https://experienceleague.adobe.com/4i6dFByqNizhrMeQrr32twEPVrg4Jz8J-rgA-sR70Ho
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: cc84ad59f4233967c484c99651edb0558518c58c
workflow-type: tm+mt
source-wordcount: 1398
ht-degree: 0%

---

# Esportare il contenuto del messaggio {#message-export}

>[!CONTEXTUALHELP]
>id="ajo_admin_msg_export"
>title="Conserva ed esporta i contenuti inviati"
>abstract="Selezionando questa opzione è possibile scrivere il contenuto dei messaggi e-mail o SMS inviati utilizzando questa configurazione in un set di dati [!DNL Experience Platform]. I record vengono conservati per 7 giorni di calendario dall’acquisizione, durante i quali puoi esportarli nel tuo archivio."

>[!AVAILABILITY]
>
>Questa funzionalità è disponibile solo per il canale e-mail e SMS, per le organizzazioni che hanno acquistato l’offerta del componente aggiuntivo Esportazione messaggi. Per ulteriori informazioni, contatta il rappresentante Adobe.

**Esportazione messaggi** consente di trasferire il contenuto dei messaggi e-mail e SMS inviati da [!DNL Journey Optimizer] al tuo archivio tramite [[!DNL Adobe Experience Platform] destinazioni](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/home){target="_blank"}, che ti consentono di inviare dati da [!DNL Experience Platform] agli endpoint esterni.

Con questa funzione, il contenuto dei messaggi e-mail e SMS inviati tramite [!DNL Journey Optimizer] che sono stati contrassegnati per l&#39;esportazione viene scritto nel [!DNL Experience Platform] [set di dati di esportazione messaggi di AJO](message-export-schema.md).

I record vengono quindi conservati nel set di dati per sette giorni di calendario dall’acquisizione, durante i quali puoi esportarli nel sistema esterno desiderato.

➡️ Per le domande e le risposte più comuni, vedere [Domande frequenti sull&#39;esportazione dei messaggi](#message-export-faq).

## Guardrail

* Questa funzionalità supporta solo i canali **Email** e **SMS**.
* I record nel set di dati di esportazione dei messaggi di AJO vengono conservati **per sette giorni di calendario** dall&#39;acquisizione.
* Il backfill non è supportato per i messaggi inviati prima di abilitare l’esportazione dei messaggi come descritto di seguito.

## Abilita esportazione messaggi {#enable-message-export}

Il processo di onboarding per la funzione Esportazione messaggi è costituito da due passaggi:

1. [Imposta il flusso di dati di esportazione](#set-up-export-dataflow) in [!DNL Experience Platform];
1. [Abilita esportazione messaggi](#config-message-export) nella configurazione del canale in [!DNL Journey Optimizer].

>[!WARNING]
>
>Verranno visualizzati solo i nuovi record dopo l’abilitazione delle esportazioni e l’invio dei messaggi. I backfill per il contenuto prima di impostare il processo di esportazione e di abilitare l’opzione Esporta messaggio non sono supportati.

### Configurare il flusso di dati di esportazione {#set-up-export-dataflow}

Prima di poter esportare i dati, impostare il processo di esportazione definendo la destinazione [!DNL Experience Platform] e il flusso di esportazione del set di dati.

Per i passaggi dettagliati, le destinazioni cloud supportate, le autorizzazioni richieste e ulteriori informazioni, vedi [questa sezione](../data/export-datasets.md#export-datasets).

>[!NOTE]
>
>Questa configurazione deve essere configurata per ogni sandbox.

1. Scegli un tipo di destinazione [Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/destination-types){target="_blank"}. Un elenco delle piattaforme di destinazione disponibili pronte per la ricezione dei dati è disponibile in [questa pagina](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/overview){target="_blank"}.

1. In [!DNL Experience Platform], configura la destinazione definendo credenziali, bucket/contenitore, prefisso percorso e opzioni di sicurezza. [Scopri come](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets){target="_blank"}

1. Crea un flusso di esportazione di set di dati utilizzando i seguenti dati:

   * Set di dati di Source: seleziona **Set di dati esportazione messaggi di AJO**.
   * Formato file: seleziona JSON o Parquet (scegli uno in base agli strumenti a valle).
   * Pianificazione: assicurati che venga eseguito entro l’intervallo di conservazione di 7 giorni.

### Abilitare l’esportazione dei messaggi nella configurazione del canale {#config-message-export}

Per applicare l’esportazione dei messaggi alle campagne e ai percorsi, devi abilitare l’opzione dedicata a livello di configurazione del canale. Segui i passaggi seguenti.

1. In [!DNL Journey Optimizer], modificare o creare la configurazione del [canale](channel-surfaces.md#create-channel-surface) e-mail o SMS desiderata.

1. Selezionare l&#39;opzione **[!UICONTROL Abilita esportazione messaggi]**.

   ![](assets/config-message-export.png)

1. Salva le modifiche e invia la configurazione del canale.

Dopo aver inviato messaggi tramite campagne o percorsi utilizzando questa configurazione di canale, i messaggi e-mail e SMS vengono scritti nel **set di dati di esportazione messaggi di AJO**. Potrai quindi [accedere ai record](#access-exported-data) nel set di dati ed esportarli nella destinazione di archiviazione selezionata in base al flusso di dati di esportazione definito.

>[!NOTE]
>
>Se si disabilita l&#39;opzione **[!UICONTROL Abilita esportazione messaggi]**, i nuovi record per questa configurazione del canale non verranno acquisiti nel set di dati. I record esistenti rimangono fino alla scadenza della conservazione.

## Accedere ai dati dei messaggi esportati {#access-exported-data}

Dopo aver inviato i messaggi utilizzando una configurazione di canale con Esportazione messaggi abilitata, puoi accedere ai dati esportati e rivederli nel **Set di dati di esportazione messaggi di AJO**.

Per visualizzare i dati del messaggio esportato:

1. In [!DNL Journey Optimizer], passa a **[!UICONTROL Gestione dati]** > **[!UICONTROL Set di dati]** nell&#39;area di navigazione a sinistra. [Ulteriori informazioni sui set di dati](../data/get-started-datasets.md)

1. Assicurati di visualizzare i set di dati generati dal sistema.

1. Selezionare il **set di dati di esportazione messaggi di AJO** dall&#39;elenco.

   ![](assets/datasets-list.png)

1. Nella pagina dei dettagli del set di dati fare clic su **[!UICONTROL Anteprima set di dati]** per visualizzare i record più recenti.

   ![](assets/ajo-message-export-dataset.png)

Il set di dati contiene informazioni complete per ogni messaggio inviato tramite la configurazione del canale con Esportazione messaggi abilitata, tra cui: oggetto, corpo del messaggio, indirizzo e-mail o numero di telefono del destinatario, indirizzo del mittente o numero di telefono, data e ora di invio, dati di personalizzazione e altro ancora.

➡️ Per una visualizzazione completa della struttura del set di dati e di tutti i campi disponibili, vedere [Schema di esportazione dei messaggi di AJO](message-export-schema.md).

Tutti i record nel set di dati vengono conservati per **sette giorni di calendario** dall&#39;acquisizione. Durante questo periodo di conservazione, è possibile accedere ai dati per i controlli di conformità, le indagini legali o esportarli nel proprio sistema di storage tramite la destinazione Experience Platform configurata.

## Esempio di JSON esportato {#sample-exported-json}

Gli esempi seguenti mostrano la forma complessiva dei record scritti nel set di dati di esportazione dei messaggi di AJO per SMS ed e-mail. Valori come identificatori, riferimenti a schemi, marche temporali e contenuto sono illustrativi; le esportazioni riflettono sandbox, schema e messaggi inviati.

Espandi ogni sezione per visualizzare il JSON campione completo.

+++ Esempio di esportazione SMS

```json
{
  "header": {
    "msgId": "f06d2a6d-65c3-472b-9ca7-cc4224af2df4",
    "xactionId": "9ccd6e76-9ee5-4a12-bff3-fea240228121",
    "msgType": "xdmEntityCreate",
    "imsOrgId": "906E3A095DC834230A495FD6@AdobeOrg",
    "sandboxId": "db3adc95-dcf6-49c3-badc-95dcf639c345",
    "sandboxName": "ajo-e2e",
    "createdAt": 1773591102107,
    "datasetId": "689653509dd3432b92f6323f",
    "schemaRef": {
      "id": "https://ns.adobe.com/aemonacpprodcampaign/schemas/64cb5d9d26c2aae6b08bdc9b7882deb90202439ec53836e7",
      "contentType": "application/vnd.adobe.xed-full+json;version=1"
    },
    "source": {
      "name": "message-execution-service"
    },
    "originalTimestamp": 1773591102107,
    "tags": [
      "ups:segmentation=false"
    ]
  },
  "body": {
    "xdmEntity": {
      "_experience": {
        "customerJourneyManagement": {
          "messageExecution": {
            "messageExecutionID": "CSM-09561055",
            "messageID": "15fe77c8-ab73-49e4-abbb-c25b859162ff-0",
            "messageType": "marketing",
            "campaignID": "5638ce57-5264-4a96-995f-5ae34eddafd7",
            "campaignVersionID": "f9019155-3d6a-44a1-9b6f-5f9cd49e7cf5",
            "campaignActionID": "dfa7f59f-477c-42ec-9db2-831d294b5779",
            "batchInstanceID": "5e23a286fb72411f1cdf1443a81ad2eb",
            "messagePublicationID": "15fe77c8-ab73-49e4-abbb-c25b859162ff",
            "audience": {
              "id": "4c339f63-b66e-4e72-8d56-db624b5277f2",
              "type": "targeted"
            }
          },
          "messageProfile": {
            "channel": {
              "_id": "https://ns.adobe.com/xdm/channels/sms",
              "_type": "https://ns.adobe.com/xdm/channel-types/sms"
            },
            "messageProfileID": "7ff5aefb-7583-38c4-8c32-b63cced94aa7",
            "variant": "5c1092da-5ba2-4bcc-b591-713ee7999f7d"
          },
          "messageRenderedContent": {
            "smsContent": {
              "message": "AJO Campaigns - Prod - E2E Test Text VA7"
            }
          },
          "messageDeliveryMetadata": {
            "smsMetadata": {
              "recipient": {
                "number": "+19256260201"
              },
              "sender": {
                "numbers": [
                  "12345678"
                ]
              }
            }
          }
        }
      },
      "identityMap": {
        "email": [
          {
            "id": "rlyajoqa+messageExport1@adobe.com",
            "primary": true
          }
        ]
      },
      "_id": "b0001846-cafa-379a-be96-1d8ee973e047",
      "timestamp": "2026-03-15T16:11:42.184Z"
    }
  }
}
```

+++

+++ Esempio di esportazione e-mail

```json
{
  "header": {
    "msgId": "1e64d2c4-7887-4f80-8b28-5c20d3da8baf",
    "xactionId": "5yfSV2Gs7VJM5TKo1uEkbiDd4iuakgzQ",
    "msgType": "xdmEntityCreate",
    "imsOrgId": "745F37C35E4B776E0A49421B@AdobeOrg",
    "sandboxId": "068abf40-575e-11ea-8512-9b1bfdb82603",
    "sandboxName": "prod",
    "createdAt": 1754489661211,
    "datasetId": "68912b8881572a2b267380c1",
    "schemaRef": {
      "id": "https://ns.adobe.com/cjmstage/schemas/1684477c0160376b8bb6975a80b5e5bd384696329faa1c42",
      "contentType": "application/vnd.adobe.xed-full+json;version=1"
    },
    "source": {
      "name": "message-execution-service"
    },
    "originalTimestamp": 1754489659000,
    "tags": [
      "ups:segmentation=false"
    ]
  },
  "body": {
    "xdmEntity": {
      "_experience": {
        "customerJourneyManagement": {
          "messageExecution": {
            "messageExecutionID": "HUMA-62208933",
            "messageID": "d0d02f68-afea-42fc-b898-6819cee643e6-0",
            "messageType": "transactional",
            "campaignID": "ce2331c2-c259-47ff-a1dd-f6d1eae08801",
            "campaignVersionID": "4272bb9f-e154-44e9-89f1-6548c77d1455",
            "batchInstanceID": "03587190-72cf-11f0-938b-31e7c9f96d89",
            "messagePublicationID": "d0d02f68-afea-42fc-b898-6819cee643e6",
            "audience": {
              "type": "all"
            }
          },
          "messageProfile": {
            "channel": {
              "_id": "https://ns.adobe.com/xdm/channels/email",
              "_type": "https://ns.adobe.com/xdm/channel-types/email"
            },
            "messageProfileID": "5yfSV2Gs7VJM5TKo1uEkbiDd4iuakgzQ",
            "variant": "11cc5796-8017-4738-aa66-ca5db967dfcc"
          },
          "messageRenderedContent": {
            "emailContent": {
              "subject": "test",
              "html": "xxx"
            }
          },
          "messageDeliveryMetadata": {
            "emailMetadata": {
              "recipient": {
                "email": "himanshig@adobe.com"
              },
              "sender": {
                "email": "cjm-team@e2e-personalisation.test.cjmadobe.com",
                "name": "CJM team",
                "replyToEmail": "replyto@marketing.adobecjm.com",
                "replyToName": "replyto",
                "errorEmail": "replyto@e2e-personalisation.test.cjmadobe.com"
              }
            }
          }
        }
      },
      "identityMap": {
        "email": [
          {
            "id": "chijain@adobe.com",
            "primary": true
          }
        ]
      },
      "_id": "ea48ce1b-80c9-3c6a-b05f-d1c998989e02",
      "timestamp": "2025-08-06T14:14:22.814Z"
    }
  }
}
```

+++

## Domande frequenti sull’esportazione dei messaggi {#message-export-faq}

+++ Cos’è l’esportazione di messaggi?

L’esportazione dei messaggi consente ai clienti di esportare messaggi completamente renderizzati (e-mail e SMS) inviati agli utenti finali. I dati esportati possono essere consegnati a destinazioni esterne utilizzando le funzionalità di esportazione standard [!DNL Adobe Experience Platform] (AEP) e utilizzati per scopi quali l&#39;archiviazione, la revisione della conformità, l&#39;analisi o le integrazioni a valle.

+++

+++ Quali canali sono supportati?

L’esportazione dei messaggi supporta:

* E-mail
* SMS

+++

+++ Quali dati genera l’esportazione dei messaggi?

Esportazione messaggi crea un set di dati generato dal sistema in [!DNL Adobe Experience Platform] che contiene uno snapshot del messaggio al momento dell&#39;invio. Questo set di dati può quindi essere esportato nelle destinazioni supportate (ad esempio, archiviazione cloud o sistemi di terze parti).

L&#39;esportazione dei messaggi è progettata come un meccanismo che consente ai clienti di trasferire i dati dei messaggi dai sistemi Adobe. I clienti sono responsabili della trasformazione, dell&#39;archiviazione e della gestione dei dati nelle proprie soluzioni di archiviazione o di conformità.

+++

+++ L’esportazione dei messaggi acquisisce messaggi completamente personalizzati?

Sì. L’esportazione dei messaggi acquisisce il messaggio completamente renderizzato inviato a ciascun destinatario, inclusi la personalizzazione e il contenuto dinamico renderizzato al momento dell’invio.

+++

+++ È possibile utilizzare Esportazione messaggi per riprodurre il messaggio originale?

Sì. Il HTML esportato può essere utilizzato per riprodurre il messaggio originale inviato in un browser.

Tuttavia, la riproduzione dipende dalla disponibilità di risorse esterne (come le immagini). L’esportazione dei messaggi non incorpora i file multimediali direttamente nell’esportazione.

+++

+++ Le immagini e i supporti sono inclusi nell&#39;esportazione?

L’esportazione dei messaggi include contenuti HTML con riferimenti (URL) a immagini e altri contenuti multimediali. Le risorse multimediali non sono incorporate nell’esportazione.

Se l’URL di un’immagine o di una risorsa non è più valido, se viene limitato o non viene pubblicata dopo l’ora di invio, non sarà possibile recuperare la risorsa.

+++

+++ Come vengono gestiti i collegamenti nell’esportazione dei messaggi?

I messaggi esportati contengono collegamenti tracciati crittografati, in modo coerente con il modo in cui i collegamenti vengono gestiti al momento dell’invio. Questi collegamenti crittografati vengono mantenuti nell’esportazione e possono essere risolti come progettato dalla piattaforma.

+++

+++ Come vengono gestiti i dati PII e di personalizzazione?

I dati vengono memorizzati esattamente come appaiono nel messaggio sottoposto a rendering:

* I valori Personalization visualizzati nel messaggio (ad esempio, nome) vengono visualizzati come testo.
* Gli elementi crittografati (come i collegamenti tracciati) rimangono crittografati.
* L’esportazione dei messaggi non rende automaticamente anonimo o reagisce al contenuto del messaggio sottoposto a rendering.

+++

+++ Qual è il periodo di conservazione per i dati di esportazione dei messaggi?

I dati di esportazione dei messaggi seguono un intervallo di conservazione di 7 giorni entro [!DNL Adobe Experience Platform].

I clienti devono esportare i dati entro questo periodo e memorizzarli nei propri sistemi, qualora sia necessaria una conservazione più lunga.

+++

+++ I clienti possono testare l’esportazione dei messaggi prima dell’acquisto?

Non esiste alcuna opzione di prova o &quot;try-before-you-buy&quot; per l’esportazione dei messaggi.

I clienti possono convalidare i propri sistemi a valle utilizzando file di esportazione di esempio, poiché l’esportazione dei messaggi si basa sul set di dati standard di AEP e sulla funzionalità di destinazione.

+++

+++ Lo schema Esportazione messaggi è disponibile prima dell’acquisto?

No. Il set di dati e lo schema di esportazione dei messaggi diventano disponibili nel prodotto solo dopo l’acquisto e l’abilitazione del componente aggiuntivo Esportazione messaggi.

+++

+++ L&#39;esportazione dei messaggi è una soluzione completa per l&#39;archiviazione o la conformità?

No. L&#39;esportazione dei messaggi è un attivatore, non un prodotto di archiviazione o conformità completo.

I clienti devono:

* Esportare i dati del messaggio da Adobe
* Trasforma o arricchisci in base alle esigenze
* Archiviazione e gestione dei dati nei propri sistemi di archiviazione o di conformità

+++

+++ Quali sono i casi d’uso comuni?

In genere i clienti utilizzano l’esportazione di messaggi per:

* Revisione della conformità o delle normative
* Archiviazione dei messaggi
* Integrazione con sistemi di terze parti
* Audit interno o flussi di lavoro di supporto
* Analisi oltre le applicazioni Adobe

+++

+++ Quali funzioni non vengono svolte dall’esportazione dei messaggi

L’esportazione dei messaggi non:

* Incorporare immagini o risorse multimediali esterne
* Conservazione dei dati illimitata o a lungo termine nei sistemi Adobe
* Offrire un ambiente di prova
* Archiviare automaticamente i messaggi all’esterno di Adobe

+++

