---
solution: Journey Optimizer
product: journey optimizer
title: Gestione della rinuncia agli SMS
description: Scopri come gestire la rinuncia con i messaggi SMS
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: 63237c02f632d289dba845acdcd0859f2d6de9c9
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 31%

---

# Gestione della rinuncia agli SMS {#sms-opt-out}

In conformità agli standard e alle normative del settore, tutti i messaggi SMS di marketing devono consentire ai destinatari di annullare facilmente l’iscrizione alla ricezione di messaggi. [Ulteriori informazioni sulla privacy e la gestione delle rinunce](../privacy/opt-out.md)

>[!IMPORTANT]
>
>Le comunicazioni tramite SMS possono essere soggette a vari requisiti di conformità legali a seconda della natura, della posizione da cui stai inviando i messaggi di testo e della posizione dei destinatari. Mentre Adobe Journey Optimizer gestisce i messaggi relativi ai codici lunghi e ai numeri verdi come descritto di seguito, consulta il tuo consulente legale per assicurarti che le comunicazioni di SMS siano conformi a tutti i requisiti legali applicabili in materia di conformità.

## Parole chiave native in entrata{#sms-native-keywords}

Per impostazione predefinita, Adobe Journey Optimizer gestisce i seguenti messaggi di risposta in lingua inglese standard per i messaggi Toll-Free e Long Code: INTERROMPI, INTERROMPI, INIZIA, ESCI, ANNULLA, FINE E ANNULLA ABBONAMENTO. Tieni presente che solo Sinch supporta le parole chiave native quando viene utilizzato con Journey Optimizer.

Queste parole chiave solitamente attivano una risposta standard automatica dal provider di terze parti. Puoi confermarlo direttamente con il tuo provider o tramite il loro sito di documentazione.

Non sono necessari passaggi per garantire che le funzionalità di rinuncia SMS funzionino in Adobe Journey Optimizer in quanto le risposte alle parole chiave STOP, UNSTOP, START, QUIT, CANCEL, END e UNSUBSCRIBE vengono automaticamente riconosciute. Gli stati di rinuncia ai profili vengono aggiornati in tempo reale in Adobe Journey Optimizer.


## Inserire nell&#39;elenco Bloccati{#sms-blocklists}

Oltre a interrompere l’invio in base allo stato di rinuncia (per le integrazioni dirette con Twilio o Sinch), la maggior parte dei provider di gateway SMS mantiene anche un inserire nell&#39;elenco Bloccati Adobe Journey Optimizer che ti assicura che non venga consegnato un messaggio SMS a una persona che ha scelto di rinunciare. Se utilizzi un provider diverso da Sinch o Twilio e invii un SMS tramite [canale personalizzato](../building-journeys/using-custom-actions.md), devi confermarlo con il tuo provider.


## Codici brevi {#short-codes}

Per impostazione predefinita, Adobe Journey Optimizer non gestisce le parole chiave di consenso o aiuto per i numeri di codice brevi. Per garantire la conformità alle normative e alle regole del settore per la gestione delle rinunce, è essenziale verificare che il codice breve sia conforme a tutte le linee guida.

Tuttavia, Journey Optimizer supporta le rinunce globali basate su parole chiave in entrata con diversi ID mittente.

## ID mittente alfanumerico {#alphanumeric}

Gli ID mittente alfanumerico sono solo per la messaggistica unidirezionale e non sono in grado di ricevere messaggi in entrata. Di conseguenza, le parole chiave SMS STOP, START e HELP di Adobe Journey Optimizer non sono applicabili agli ID mittente alfanumerico. È necessario fornire altre istruzioni, come scrivere al team di supporto, chiamare una linea telefonica di supporto o inviare un messaggio con un altro numero di telefono o codice per consentire agli utenti di rinunciare ai messaggi inviati tramite l’ID mittente alfanumerico.

## Video {#video-sms}

Per ulteriori informazioni sul funzionamento del supporto nativo per parole chiave in entrata (START, STOP e UNSTOP) per SMS, guarda il seguente video:

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
