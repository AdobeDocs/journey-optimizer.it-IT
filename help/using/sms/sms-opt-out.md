---
solution: Journey Optimizer
product: journey optimizer
title: Gestione delle rinunce per i messaggi di testo
description: Scopri come gestire la rinuncia con i messaggi SMS/MMS
feature: SMS
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: 7b1be144776fd11cd4aa90aa315eee60b1acc40f
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 16%

---

# Gestione delle rinunce per i messaggi di testo {#sms-opt-out}

In conformità agli standard e alle normative del settore, tutti i messaggi SMS di marketing devono consentire ai destinatari di annullare facilmente l’iscrizione alla ricezione di messaggi. [Ulteriori informazioni sulla gestione della privacy e della rinuncia](../privacy/opt-out.md)

>[!IMPORTANT]
>
>Le comunicazioni tramite SMS possono essere soggette a vari requisiti legali di conformità a seconda della loro natura, della posizione da cui invii i messaggi e della posizione dei destinatari. Mentre Adobe Journey Optimizer gestisce i messaggi relativi a codici brevi, codici lunghi e numeri gratuiti come descritto di seguito, consulta il tuo consulente legale per assicurarti che le tue comunicazioni tramite SMS siano conformi a tutti i requisiti di conformità legale applicabili.
>

## Parole chiave in entrata native {#sms-native-keywords}

>[!NOTE]
>
> Solo Sinch e Infobip supportano le parole chiave native se utilizzate con Journey Optimizer.

Per impostazione predefinita, Adobe Journey Optimizer gestisce i seguenti messaggi di risposta standard in lingua inglese per i messaggi con codici brevi, gratuiti e a codice lungo:

* **Rinuncia**: INTERROMPI, ESCI, ANNULLA, TERMINA, ANNULLA ISCRIZIONE, NO.
* **Consenso**: SOTTOSCRIVI, SÌ, RIPRENDI, AVVIA, CONTINUA, RIPRENDI, INIZIA.
* **Guida**: GUIDA.

Queste parole chiave in genere attivano una risposta standard automatica dal provider di terze parti. Puoi confermarlo direttamente con il tuo provider o tramite il loro sito di documentazione.

Quando utilizzi Infobip, accertati che l’azione Inoltro sia impostata su Configurazione pull.

Non sono necessari passaggi per garantire che le funzionalità di rinuncia SMS funzionino in Adobe Journey Optimizer, in quanto le risposte alle parole chiave STOP, UNSTOP, START, QUIT, CANCEL, END e UNSUBSCRIBE vengono riconosciute automaticamente. Gli stati di rinuncia dei profili vengono aggiornati in tempo reale in Adobe Journey Optimizer.

Se un cliente risponde STOP a un messaggio di testo, il provider blocca tutti gli SMS successivi provenienti dall’ID mittente specifico (codice breve o numero lungo), inclusi i messaggi transazionali. Per garantire la consegna ininterrotta degli SMS transazionali, utilizza un ID mittente separato che non era stato precedentemente escluso.


>[!NOTE]
>
>Se prevedi di utilizzare SMS a due vie (rispondi con STOP, QUIT, ecc.), accertati di aver inviato almeno un SMS unidirezionale per stabilire il numero di telefono per la mappatura del profilo. Le credenziali del provider scadute o non configurate correttamente impediscono l&#39;aggiornamento del profilo utente da parte delle parole chiave in entrata, causando record di rinuncia mancanti o ritardati.


## Inserisce nell&#39;elenco Bloccati {#sms-blocklists}

Oltre all’interruzione dell’invio da parte di Adobe Journey Optimizer in base allo stato di rinuncia (per le integrazioni dirette con Twilio, Infobip o Sinch), la maggior parte dei provider di gateway SMS mantiene anche un inserisco nell&#39;elenco Bloccati di che ti assicura che non venga inviato un messaggio SMS a una persona che ha scelto di rinunciare. Se utilizzi un provider diverso da Sinch o Twilio e invii un SMS tramite [canale personalizzato](../building-journeys/using-custom-actions.md), devi confermarlo con il tuo provider.


## Codici brevi {#short-codes}

Per impostazione predefinita, le parole chiave opt-in o help per i numeri di codice brevi non vengono gestite da Adobe Journey Optimizer. Per garantire la conformità alle normative di settore e alle regole per la gestione delle rinunce, è essenziale verificare che il codice breve sia conforme a tutte le linee guida.

Tuttavia, Journey Optimizer supporta le rinunce globali basate su parole chiave in arrivo con ID mittente diversi.

## ID mittente alfanumerico {#alphanumeric}

Gli ID mittente alfanumerico sono solo per la messaggistica unidirezionale e non sono in grado di ricevere messaggi in entrata. Di conseguenza, le parole chiave SMS STOP, START e HELP di Adobe Journey Optimizer non sono applicabili agli ID mittente di Alpha. È necessario fornire altre istruzioni, come scrivere al team di supporto, chiamare una linea telefonica di supporto o inviare un messaggio con un altro numero di telefono o codice per consentire agli utenti di rinunciare ai messaggi inviati tramite l’ID mittente alfanumerico.

## Video {#video-sms}

* Il video seguente spiega come configurare il doppio consenso per gli SMS.

  +++ Guarda il video

  >[!VIDEO](https://video.tv.adobe.com/v/3440287/?captions=ita&learn=on)

  +++
