---
title: Attivare campagne tramite API
description: Scopri come attivare le campagne utilizzando [!DNL Journey Optimizer] API
hide: true
hidefromtoc: true
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 1%

---

# Attivare campagne tramite API {#trigger-campaigns}

## Informazioni sulle campagne attivate dall’API {#about}

>[!NOTE]
>
>L’API di esecuzione dei messaggi interattivi è attualmente in versione beta e potrebbe essere soggetta a frequenti aggiornamenti senza preavviso.

Con [!DNL Journey Optimizer], puoi creare campagne e richiamarle da un sistema esterno basato sul trigger dell’utente utilizzando [API REST di esecuzione dei messaggi interattivi](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution). Questo ti consente di soddisfare varie esigenze operative e di messaggistica transazionale, come reimpostazioni di password, token OTP e altri.

A questo scopo, devi prima creare una campagna con attivazione API in Journey Optimizer e quindi avviarne l’esecuzione tramite una chiamata API.

I canali disponibili per le campagne con attivazione API sono messaggi e-mail, SMS e push.

## Creare una campagna con attivazione API {#create}

Il processo di creazione di campagne con attivazione API rimane lo stesso delle campagne pianificate, ad eccezione della selezione del pubblico che viene eseguita nel payload API. Informazioni dettagliate su come creare una campagna sono disponibili in [questa sezione](create-campaign.md).

Per creare una campagna con attivazione API, segui questi passaggi:

1. Crea una nuova campagna con **[!UICONTROL API-triggered]** digitare.

1. Scegli il canale e la superficie del canale da utilizzare per inviare il messaggio, quindi fai clic su **[!UICONTROL Create]**.

   ![](assets/api-triggered-type.png)

1. Specifica un titolo e una descrizione per la campagna, quindi configura il messaggio da inviare.

   ![](assets/api-triggered-properties.png)

   >[!NOTE]
   >
   >Puoi trasmettere al payload API dati aggiuntivi che puoi sfruttare per personalizzare il messaggio. [Ulteriori informazioni](#contextual)

1. Specifica lo spazio dei nomi da utilizzare per identificare i singoli utenti del segmento.

1. Configura le date di inizio e di fine della campagna.

   Se configuri una data di inizio e/o di fine specifica per una campagna, questa non verrà eseguita al di fuori di tali date e le chiamate API non riusciranno se la campagna viene attivata dalle API.

1. In **[!UICONTROL cURL request]** della sezione , recupera **[!UICONTROL Campaign ID]** da utilizzare nel payload API.

   ![](assets/api-triggered-curl.png)

1. Fai clic su **[!UICONTROL Review to activate]** per verificare che la campagna sia configurata correttamente, attivala.

## Utilizzare attributi contestuali nelle campagne con attivazione API {#contextual}

Con le campagne attivate dall’API, puoi trasmettere dati aggiuntivi nel payload API e utilizzarli all’interno della campagna per personalizzare il messaggio.

Prendiamo questo esempio, in cui i clienti desiderano reimpostare la propria password e si desidera inviare loro un URL di reimpostazione della password generato in uno strumento di terze parti. Con le campagne attivate dall’API, puoi trasmettere questo URL generato al payload API e sfruttarlo nella campagna per aggiungerlo al messaggio.

>[!NOTE]
>
>A differenza degli eventi abilitati per il profilo, i dati contestuali trasmessi nell’API REST vengono utilizzati per la comunicazione una tantum e non memorizzati in base al profilo. Al massimo, il profilo viene creato con i dettagli dello spazio dei nomi, se mancante.

Per utilizzare questi dati nelle campagne, devi passarli al payload API e aggiungerli nel messaggio utilizzando l’editor espressioni. Per eseguire questa operazione, utilizza la variabile `{{context.<contextualAttribute>}}` sintassi, dove `<contextualAttribute>` deve corrispondere al nome della variabile nel payload API contenente i dati da trasmettere.

La `{{context.<contextualAttribute>}}` la sintassi è mappata solo a un tipo di dati String.

![](assets/api-triggered-context.png)

>[!IMPORTANT]
>
>La `context.system` La sintassi è limitata ad Adobe all’uso interno e non deve essere utilizzata per trasmettere attributi contestuali.
Per il momento, non è disponibile alcun attributo contestuale da utilizzare nel menu della barra a sinistra. Gli attributi devono essere inseriti direttamente nell’espressione di personalizzazione, senza che venga eseguito alcun controllo da parte di [!DNL Journey Optimizer].

## Eseguire la campagna {#execute}

Per eseguire una campagna con attivazione API, devi innanzitutto recuperare il relativo ID e passarlo al payload API. A questo scopo, apri la campagna, quindi copia e incolla l’ID dal **[!UICONTROL cURL request]** sezione .

![](assets/api-triggered-id.png)

Puoi quindi utilizzare questo ID nel payload API per attivare la campagna. Fai riferimento a [Documentazione API di esecuzione dei messaggi interattivi](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution) per ulteriori informazioni.

Nota che, se hai configurato una data di inizio e/o di fine specifica durante la creazione della campagna, questa non verrà eseguita al di fuori di queste date e le chiamate API non riusciranno.

>[!NOTE]
>
>In alcuni casi, potrebbe essere necessario inviare messaggi transazionali a profili non esistenti nel sistema. Ad esempio, se un utente sconosciuto tenta di accedere al sito web. In tal caso, il profilo corrispondente viene creato automaticamente in Adobe Experience Platform, nel **Set di dati del profilo di messaggistica interattiva AJO** set di dati.
