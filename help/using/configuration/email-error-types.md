---
solution: Journey Optimizer
product: journey optimizer
title: Tipi di errori e-mail
description: Accedi all’elenco di tutti i possibili errori e-mail durante l’invio di consegne con Journey Optimizer.
feature: Deliverability, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: nuovi tentativi, mancato recapito, morbido, ignorato, rigido, ottimizzatore, errore
hide: true
hidefromtoc: true
exl-id: a8908b11-2288-4d53-897c-3f99cb5ceab4
source-git-commit: 0cb73489981659c3f231b9def40e0e483ed3aef8
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 6%

---

# Tipi di errori e-mail {#email-error-types}

I possibili motivi di un errore di consegna sono molteplici. La tabella seguente descrive tutti gli errori che possono verificarsi durante l&#39;invio di consegne e-mail con [!DNL Journey Optimizer], insieme alla relativa descrizione e al tipo di errore.

Questi errori si trovano nel [Set di dati evento feedback messaggio di AJO](../data/datasets-query-examples.md#message-feedback-event-dataset) che contiene i registri di consegna del messaggio, incluse le informazioni su tutte le consegne del messaggio da [!DNL Journey Optimizer] e i record di feedback dagli ISP e-mail in caso di mancati recapiti.

| Etichetta errore | Tipo di errore | Valore tecnico | Descrizione |
| --- | --- | --- | --- |
| **Indeterminato** | Ignorato | 1 | Impossibile classificare il messaggio SMTP non recapitato ricevuto dall’ISP. |
| **Destinatario non valido** | Mancato recapito permanente | 10 | Indirizzo del destinatario non valido. |
| **Destinatario rifiutato** | Mancato recapito permanente | 15 | L’ISP del destinatario ha rifiutato il messaggio e l’ISP può bloccare il mittente se il destinatario non viene eliminato. |
| **Mancato recapito non permanente** | Mancato recapito morbido | 20 | Si è verificato un errore temporaneo nel messaggio. Potrebbe avere successo in tentativi futuri. |
| **Errore DNS** | Mancato recapito morbido | 21 | Errore DNS temporaneo durante il recapito del messaggio. Potrebbe avere successo in tentativi futuri. |
| **Cassetta postale piena** | Mancato recapito morbido | 22 | Si è verificato un errore di recapito temporaneo del messaggio perché la cassetta postale del destinatario era piena. |
| **Troppo grande** | Ignorato | 23 | Si è verificato un errore di consegna temporaneo del messaggio perché la dimensione del messaggio ha superato il limite del destinatario. |
| **Timeout** | Ignorato | 24 | Consegna del messaggio non riuscita perché la validità del messaggio è scaduta o l&#39;invio all&#39;ISP ha richiesto troppo tempo. |
| **Errore di amministrazione** | Amministrazione | 25 | La consegna non è riuscita a causa di una configurazione dei criteri nell’infrastruttura di invio delle e-mail. |
| **Mancato recapito generico: NESSUNA RICEVUTA** | Ignorato | 30 | Impossibile recapitare il messaggio perché il destinatario non è stato identificato. |
| **Mancato recapito generico** | Ignorato | 40 | Si è verificato un errore di consegna temporaneo per motivi non specificati. |
| **Blocco posta** | Ignorato | 50 | Si è verificato un errore temporaneo della consegna a causa di elevati limiti di volume o frequenza da parte dell’ISP. |
| **Blocco spam** | Ignorato | 51 | Si è verificato un errore temporaneo nella consegna perché l’ISP considerava i domini o gli IP del mittente come una sorgente di spam nota. |
| **Contenuto spam** | Ignorato | 52 | Si è verificato un errore temporaneo nella consegna perché l’ISP ha classificato il contenuto dell’e-mail come spam. |
| **Inoltro negato** | Mancato recapito morbido | 54 | Impossibile accettare il messaggio perché il dominio di destinazione non è inserito nell’elenco Consentiti per l’inoltro. |
| **Risposta automatica** | Ignorato | 60 | Questi messaggi vengono scartati da [!DNL Journey Optimizer] quando vengono ricevuti, a meno che l&#39;inoltro non sia abilitato. |
| **Errore temporaneo** | Ignorato | 70 | La consegna verrà ritentata a una velocità limitata o potrebbe essere differita in caso di sospensione. |
| **Risposta al problema** | Mancato recapito morbido | 100 | La consegna potrebbe non riuscire definitivamente perché [!DNL Journey Optimizer] non supporta un meccanismo di autenticazione di tipo challenge-response. |
