---
solution: Journey Optimizer
product: journey optimizer
title: Gestione delle rinunce per i messaggi mobili
description: Scopri come gestire la rinuncia con i messaggi SMS/MMS
feature: SMS
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
TQID: https://experienceleague.adobe.com/mQVaZ8jb-hBBPxDnztkayDEI4vj0KvMTREI0KxOgAf0
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2: id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: a4c92daab69394e6a736517f2e23a941135f7eb4
workflow-type: tm+mt
source-wordcount: 673
ht-degree: 14%

---

# Gestione delle rinunce per i messaggi mobili {#sms-opt-out}

In conformità agli standard e alle normative del settore, tutti i messaggi SMS di marketing devono consentire ai destinatari di annullare facilmente l’iscrizione alla ricezione di messaggi. [Ulteriori informazioni sulla gestione della privacy e della rinuncia](../privacy/opt-out.md)

>[!IMPORTANT]
>
>Le comunicazioni di messaggi mobili possono essere soggette a vari requisiti di conformità legali a seconda della loro natura, della posizione da cui stai inviando i messaggi mobili e della posizione dei destinatari. Mentre Adobe Journey Optimizer gestisce i messaggi relativi a codici brevi, codici lunghi e numeri gratuiti come descritto di seguito, consulta il tuo consulente legale per assicurarti che le tue comunicazioni di messaggistica mobile siano conformi a tutti i requisiti di conformità legale applicabili.
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

Se definisci parole chiave di rinuncia personalizzate nelle credenziali API SMS, queste sovrascrivono le parole chiave in entrata predefinite elencate sopra. Per mantenere funzionali le parole chiave predefinite, come STOP, QUIT, CANCEL, END e UNSUBSCRIBE, includile esplicitamente insieme alle parole chiave personalizzate nel campo Parole chiave di rinuncia della configurazione SMS. In caso contrario, vengono riconosciute solo le parole chiave personalizzate e le parole chiave predefinite non attivano più le azioni di rinuncia.

Se un cliente risponde STOP a un messaggio Mobile, il provider blocca tutti gli SMS successivi da quel specifico ID mittente (codice breve o numero lungo), inclusi i messaggi transazionali. Per garantire la consegna ininterrotta degli SMS transazionali, utilizza un ID mittente separato che non era stato precedentemente escluso.


>[!NOTE]
>
>Se prevedi di utilizzare SMS a due vie (rispondi con STOP, QUIT, ecc.), accertati di aver inviato almeno un SMS unidirezionale per stabilire il numero di telefono per la mappatura del profilo. Le credenziali del provider scadute o non configurate correttamente impediscono l&#39;aggiornamento del profilo utente da parte delle parole chiave in entrata, causando record di rinuncia mancanti o ritardati. Le risposte in entrata sono archiviate nel set di dati di sistema _AJO Inbound Activity Event_. [Ulteriori informazioni](../data/get-started-datasets.md#system-datasets)


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

  >[!VIDEO](https://video.tv.adobe.com/v/3427129/?learn=on)

  +++
