---
solution: Journey Optimizer
product: journey optimizer
title: Testare un’azione personalizzata
description: Scopri come risolvere i problemi di un’azione personalizzata
badge: label="Disponibilità limitata"
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: azione, terze parti, personalizzato, percorsi, API
source-git-commit: 5ce76bd61a61e1ed5e896f8da224fc20fba74b53
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 2%

---


# Risolvere i problemi relativi alle azioni personalizzate {#troubleshoot-a-custom-action}

>[!AVAILABILITY]
>
>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.
>

## Panoramica

La funzionalità **Invia richiesta di test** consente agli amministratori di convalidare le configurazioni delle azioni personalizzate effettuando chiamate API reali direttamente da Adobe Journey Optimizer (AJO). Questa funzione assicura che la struttura della richiesta, le intestazioni, l’autenticazione e il payload siano formattati correttamente prima di essere utilizzati in un percorso.

![](assets/send-test-request.png){width="70%" align="left"}

## Prerequisiti

- **Accesso amministratore richiesto:**
   - Gli utenti devono disporre dell&#39;autorizzazione **&quot;Gestisci eventi percorsi, origini dati e azioni&quot;**.
   - Questa autorizzazione è inclusa nel ruolo *Amministratori di Percorso*.
   - L&#39;autorizzazione **&quot;Visualizza eventi di percorsi...&quot;** da sola non è sufficiente.
- Una **Azione personalizzata** deve essere preconfigurata con un URL, intestazioni e impostazioni di autenticazione.

## Come utilizzare la funzione Invia richiesta di test

1. Passa alla schermata di configurazione **Azioni personalizzate**.
1. Fare clic sul pulsante **&quot;Invia richiesta test&quot;**.
1. Viene visualizzata una finestra popup che consente di specificare i parametri della richiesta:
   - Se il metodo di azione personalizzato **è GET**, non è richiesto alcun payload.
   - Se il metodo di azione personalizzato **è POST**, è necessario fornire un payload JSON.

     >[!NOTE]
     >
     >AJO genererà un errore se la struttura di questo JSON non è corretta, ma non lo farà in caso di mancata corrispondenza con un tipo di dati. Ad esempio, non si verifica alcun errore se si utilizza un parametro intero per quella che deve essere una stringa.

   - Se è definita l&#39;autenticazione, verrà richiesto di immettere i dettagli di autenticazione.

1. Fai clic su **Invia** per eseguire la richiesta.
1. La risposta dall’API, incluse le intestazioni e i codici di stato, verrà visualizzata nell’interfaccia.

## Gestione dell’autenticazione

Quando un’azione personalizzata include l’autenticazione, AJO richiede all’utente di inserire i dettagli di autenticazione per ogni richiesta di test:

- **Autenticazione di base:** L&#39;utente deve fornire la *password*.
- **Autenticazione chiave API:** L&#39;utente deve immettere la chiave API *value*.
- **Autenticazione personalizzata:** L&#39;utente deve fornire i parametri di autenticazione nella richiesta *bodyParam*. In questo caso vengono aggiunte due sezioni da completare: **Richiesta di autenticazione** e **Risposta di autenticazione**.

## Differenze chiave dagli strumenti di test esterni (ad esempio, Postman)

- La richiesta di test viene eseguita da **AJO Percorsi**, ovvero:
   - Viene utilizzata la struttura esatta della richiesta (comprese le intestazioni specifiche per AJO).
   - L’IP sorgente e le intestazioni corrispondono a quelle utilizzate nei percorsi live.
- Può essere utilizzato per la risoluzione dei problemi di **percorsi live** in cui l&#39;azione personalizzata è già distribuita.
- Elimina la necessità di copiare manualmente i dettagli di configurazione tra gli strumenti, riducendo il rischio di errori.

## Risoluzione dei problemi

- Se la richiesta non riesce, verifica:
   - Credenziali di autenticazione immesse nel test.
   - Il metodo di richiesta (GET vs. POST) e il payload corrispondente.
   - L’endpoint API e le intestazioni definiti nell’azione personalizzata.
- Utilizza i dati di risposta per identificare potenziali configurazioni errate.

Questa funzione semplifica il processo di test e convalida, garantendo il corretto funzionamento delle azioni personalizzate nei percorsi live di AJO.

