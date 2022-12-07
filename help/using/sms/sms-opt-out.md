---
solution: Journey Optimizer
product: journey optimizer
title: Gestione della rinuncia agli SMS
description: Scopri come gestire la rinuncia con i messaggi SMS
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 96%

---

# Gestione della rinuncia agli SMS {#sms-opt-out}

In conformità agli standard e alle normative del settore, tutti i messaggi SMS di marketing devono consentire ai destinatari di annullare facilmente l’iscrizione alla ricezione di messaggi. [Ulteriori informazioni sulla privacy e la gestione delle rinunce](../privacy/opt-out.md)

Per impostazione predefinita, Adobe Journey Optimizer gestisce i messaggi di risposta standard in lingua inglese, come ad esempio STOP, UNSTOP e START per i messaggi a numeri gratuiti e con codice lungo, in conformità agli standard di settore per l’integrazione nativa come Sinch e Twilio. Queste parole chiave solitamente attivano una risposta standard automatica dal tuo provider di terze parti (ad esempio Twilio, Sinch, ecc.). Puoi confermarlo direttamente con il tuo provider o tramite il loro sito di documentazione.

Non sono necessari passaggi per garantire che le funzionalità di rinuncia SMS funzionino in Adobe Journey Optimizer in quanto le risposte alle parole chiave STOP, UNSTOP e START verranno riconosciute automaticamente.

Inoltre Adobe Journey Optimizer interrompe l’invio in base allo stato di rinuncia (per le integrazioni dirette con Twilio o Sinch), e la maggior parte dei provider di gateway SMS gestisce anche un elenco Bloccati che ti assicura che non venga inviato un messaggio SMS a una persona che ha scelto la rinuncia. Se utilizzi un provider diverso da Sinch o Twilio e invii un SMS tramite un [canale personalizzato](../building-journeys/using-custom-actions.md), è necessario confermarlo con il tuo provider.

>[!IMPORTANT]
>
>Le campagne di messaggi possono essere soggette a vari requisiti di conformità legali a seconda della natura della campagna di messaggi di testo, della posizione da cui stai inviando i messaggi di testo e della posizione dei destinatari. <br>Anche se Adobe Journey Optimizer gestirà i messaggi relativi ai codici lunghi e ai numeri gratuiti come descritto in precedenza, è necessario consultare il proprio consulente legale per assicurarsi che la campagna di messaggi di testo sia conforme a tutti i requisiti di conformità legale applicabili.

## Codici brevi {#short-codes}

Per impostazione predefinita, Adobe Journey Optimizer non gestirà le parole chiave di rinuncia, consenso o aiuto per i numeri con codice breve.

Devi accertarti che il tuo codice breve sia conforme a tutte le regole e le normative del settore per la gestione delle rinunce.

## ID mittente alfanumerico {#alphanumeric}

Gli ID mittente alfanumerico sono solo per la messaggistica unidirezionale e non sono in grado di ricevere messaggi in entrata. Di conseguenza, le parole chiave SMS STOP, START e HELP di Adobe Journey Optimizer non sono applicabili agli ID mittente alfanumerico. È necessario fornire altre istruzioni, come scrivere al team di supporto, chiamare una linea telefonica di supporto o inviare un messaggio con un altro numero di telefono o codice per consentire agli utenti di rinunciare ai messaggi inviati tramite l’ID mittente alfanumerico.

## Video {#video-sms}

Per ulteriori informazioni sul funzionamento del supporto nativo per parole chiave in entrata (START, STOP e UNSTOP) per SMS, guarda il seguente video:

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
