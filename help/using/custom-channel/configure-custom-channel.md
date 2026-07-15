---
title: 'Configurare un canale personalizzato: panoramica'
description: Scopri i passaggi che un amministratore deve completare per configurare un canale personalizzato in Adobe Journey Optimizer, dalla creazione del canale alla configurazione di un canale.
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Disponibilità limitata" type="Informative"
source-git-commit: 4556e8b50fe71cf9d703d034a3c5772b8fea9d33
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 9%

---


# Configurare un canale personalizzato {#custom-channel-configuration}

>[!AVAILABILITY]
>
>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.

La configurazione di un canale personalizzato è un’attività di amministratore che viene eseguita una volta per canale. Dopo aver configurato il canale, gli addetti al marketing possono selezionarlo immediatamente in campagne, percorsi e campagne orchestrate, proprio come qualsiasi canale nativo [!DNL Journey Optimizer].

Il processo di configurazione prevede quattro passaggi: definizione del canale stesso (endpoint, autenticazione, payload), gestione delle credenziali API utilizzate per autenticare le richieste, delega facoltativa di un sottodominio per il tracciamento dei collegamenti e infine creazione di una configurazione di canale che verrà selezionata dagli addetti al marketing al momento dell’authoring.

>[!NOTE]
>
>Prima di iniziare, controlla i prerequisiti e i guardrail per i canali personalizzati, incluse le autorizzazioni richieste e i metodi di autenticazione supportati.

## Passaggi di configurazione {#steps}

Il processo di configurazione di un canale personalizzato è costituito da quattro passaggi. Ogni passaggio è descritto in dettaglio negli articoli collegati di seguito.

| Passaggio | Operazioni eseguite | Perché è importante | Collegamento |
| --- | --- | --- | --- |
| **1. Crea il canale personalizzato** | Definisci l’URL dell’endpoint, le intestazioni, i criteri di limitazione, il tipo di autenticazione e la struttura del payload del messaggio nel Channel Builder. | Questa è la definizione principale del tuo canale. Indica a [!DNL Journey Optimizer] come inviare un messaggio e come si presenta. | [Ulteriori informazioni](create-custom-channel.md) |
| **2. Gestisci credenziali API** | Crea e gestisci i set di credenziali utilizzati per autenticare le richieste nell’endpoint. | I set di credenziali multipli consentono di riutilizzare la stessa definizione di canale tra marchi o ambienti diversi senza duplicare il canale. | [Ulteriori informazioni](custom-channel-api-credentials.md) |
| **3. Delega un sottodominio** *(facoltativo)* | Delega un sottodominio specifico per il canale personalizzato. | Obbligatorio solo se il payload del messaggio contiene collegamenti tracciabili. Senza un sottodominio delegato, il tracciamento dei collegamenti non è disponibile per questo canale. | [Ulteriori informazioni](custom-channel-subdomains.md) |
| **4. Crea una configurazione di canale** | Crea un predefinito denominato che collega il canale personalizzato a un set specifico di credenziali, a un sottodominio e alle impostazioni predefinite facoltative del payload. | Durante la creazione di campagne o percorsi, gli addetti al marketing selezionano un canale personalizzato e una configurazione di canale associata. Puoi creare più configurazioni per lo stesso canale (ad esempio, una per marchio o regione). | [Ulteriori informazioni](custom-channel-configuration.md) |

<!--
## Get started {#get-started}

1. [Create the custom channel](create-custom-channel.md) by defining its endpoint, authentication method, and message payload structure in the Channel Builder.
1. [Set up API credentials](custom-channel-api-credentials.md) to authenticate requests sent to your endpoint — required for all authentication types other than **None**.
1. [Delegate a subdomain](custom-channel-subdomains.md) if your message payload includes trackable links and you want them served from a branded domain.
1. [Create a channel configuration](custom-channel-configuration.md) to produce the named preset that marketers will select when building campaigns and journeys.


-->