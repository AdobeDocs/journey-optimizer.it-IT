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
source-git-commit: 676e2d6788c8110b76a38e857a62ba9c1be5842c
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 45%

---

# Gestione della rinuncia agli SMS {#sms-opt-out}

In conformità agli standard e alle normative del settore, tutti i messaggi SMS di marketing devono consentire ai destinatari di annullare facilmente l’iscrizione alla ricezione di messaggi. [Ulteriori informazioni sulla privacy e la gestione delle rinunce](../privacy/opt-out.md)

>[!IMPORTANT]
>
>Le comunicazioni tramite SMS possono essere soggette a vari requisiti di conformità legali a seconda della natura, della posizione da cui stai inviando i messaggi di testo e della posizione dei destinatari. Mentre Adobe Journey Optimizer gestisce i messaggi relativi ai codici lunghi e ai numeri verdi come descritto di seguito, consulta il tuo consulente legale per assicurarti che le comunicazioni di SMS siano conformi a tutti i requisiti legali applicabili in materia di conformità.

## Parole chiave native in entrata{#sms-native-keywords}

Per impostazione predefinita, Adobe Journey Optimizer gestisce i messaggi di risposta standard in lingua inglese, come ad esempio STOP, UNSTOP e START per i messaggi a numeri gratuiti e con codice lungo, in conformità agli standard di settore per l’integrazione nativa come Sinch e Twilio.

Queste parole chiave solitamente attivano una risposta standard automatica dal tuo provider di terze parti (come Twilio o Sinch). Puoi confermarlo direttamente con il tuo provider o tramite il loro sito di documentazione.

Non sono necessari passaggi per garantire che le funzionalità di rinuncia SMS funzionino in Adobe Journey Optimizer in quanto le risposte alle parole chiave STOP, UNSTOP e START vengono riconosciute automaticamente. Gli stati di rinuncia ai profili vengono aggiornati in tempo reale in Adobe Journey Optimizer.


## Inserire nell&#39;elenco Bloccati{#sms-blocklists}

Oltre a interrompere l’invio in base allo stato di rinuncia (per le integrazioni dirette con Twilio o Sinch), la maggior parte dei provider di gateway SMS mantiene anche un inserire nell&#39;elenco Bloccati Adobe Journey Optimizer che ti assicura che non venga consegnato un messaggio SMS a una persona che ha scelto di rinunciare. Se utilizzi un provider diverso da Sinch o Twilio e invii un SMS tramite [canale personalizzato](../building-journeys/using-custom-actions.md), devi confermarlo con il tuo provider.


## Codici brevi {#short-codes}

Per impostazione predefinita, Adobe Journey Optimizer non gestisce le parole chiave di rinuncia, consenso o aiuto per i numeri di codice brevi. Devi accertarti che il tuo codice breve sia conforme a tutte le regole e le normative del settore per la gestione delle rinunce.

## ID mittente alfanumerico {#alphanumeric}

Gli ID mittente alfanumerico sono solo per la messaggistica unidirezionale e non sono in grado di ricevere messaggi in entrata. Di conseguenza, le parole chiave SMS STOP, START e HELP di Adobe Journey Optimizer non sono applicabili agli ID mittente alfanumerico. È necessario fornire altre istruzioni, come scrivere al team di supporto, chiamare una linea telefonica di supporto o inviare un messaggio con un altro numero di telefono o codice per consentire agli utenti di rinunciare ai messaggi inviati tramite l’ID mittente alfanumerico.

## Video {#video-sms}

Per ulteriori informazioni sul funzionamento del supporto nativo per parole chiave in entrata (START, STOP e UNSTOP) per SMS, guarda il seguente video:

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
