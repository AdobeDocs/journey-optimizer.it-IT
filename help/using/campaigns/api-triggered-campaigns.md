---
solution: Journey Optimizer
product: journey optimizer
title: Attivare campagne tramite API
description: Scopri come attivare le campagne utilizzando le API di Journey Optimizer
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagne, attivate da API, REST, ottimizzatore, messaggi
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: 280238fb3f41cef08c4e5a8720839aff5b767cf5
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 2%

---

# Attivare campagne tramite API {#trigger-campaigns}

## Informazioni sulle campagne attivate da API {#about}

Con [!DNL Journey Optimizer] è possibile creare campagne e quindi eseguirle da un sistema esterno basato sull&#39;attivatore utente utilizzando l&#39;[API REST di esecuzione interattiva dei messaggi](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution). Questo ti consente di soddisfare varie esigenze di marketing e messaggistica transazionale, tra cui reimpostazioni di password e token OTP.

A tal fine, devi innanzitutto creare una campagna attivata da API in Journey Optimizer e quindi avviarne l’esecuzione tramite una chiamata API.

![](../rn/assets/do-not-localize/api-triggered.gif)

I canali disponibili per le campagne attivate da API sono e-mail, SMS e messaggi push.

>[!NOTE]
>
>Al momento, la modalità Consegna rapida non è supportata per le campagne attivate dall’API per le notifiche push.

➡️ [Scopri questa funzione nel video](#video)

## Creare una campagna attivata da API {#create}

### Configurare e attivare la campagna {#create-activate}

Per creare una campagna attivata da API, segui i passaggi seguenti. Informazioni dettagliate su come creare una campagna sono disponibili in [questa sezione](create-campaign.md).

1. Crea una nuova campagna con il tipo **[!UICONTROL Attivato da API]**.

1. Scegli la categoria **[!UICONTROL Marketing]** o **[!UICONTROL Transazionale]** a seconda del tipo di comunicazione che desideri inviare.

1. Scegli uno dei canali supportati e la relativa configurazione di canale da utilizzare per inviare il messaggio, quindi fai clic su **[!UICONTROL Crea]**.

   ![](assets/api-triggered-type.png)

1. Specifica un titolo e una descrizione per la campagna, quindi fai clic su **[!UICONTROL Modifica contenuto]** per configurare il messaggio da inviare.

   >[!NOTE]
   >
   >Puoi trasmettere dati aggiuntivi nel payload API che puoi sfruttare per personalizzare il messaggio. [Ulteriori informazioni](#contextual)
   >
   >L’utilizzo di un numero elevato o di dati contestuali pesanti nel contenuto può influire sulle prestazioni.

1. Nella sezione **[!UICONTROL Pubblico]**, specifica lo spazio dei nomi da utilizzare per identificare i singoli utenti.

   * Se stai creando una campagna di tipo **transazionale**, i profili target devono essere definiti nella chiamata API. L&#39;opzione **[!UICONTROL Crea nuovi profili]** consente di creare automaticamente profili che non esistono nel database. [Ulteriori informazioni sulla creazione del profilo durante l&#39;esecuzione della campagna](#profile-creation)

     >[!NOTE]
     >
     >Una singola chiamata API supporta fino a 20 destinatari univoci. Ogni destinatario deve avere un ID utente univoco; gli ID utente duplicati non sono consentiti. Ulteriori informazioni sono disponibili nella [documentazione dell&#39;API di esecuzione messaggi interattiva](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution/operation/postIMUnitaryMessageExecution){target="_blank"}

   * Per campagne di tipo **marketing**, fai clic sul pulsante **[!UICONTROL Pubblico]** per scegliere il pubblico di destinazione.

1. Configura le date di inizio e di fine della campagna.

   Se configuri una data di inizio e/o di fine specifica per una campagna, questa non verrà eseguita al di fuori di tali date e le chiamate API non riusciranno se la campagna viene attivata dalle API.

1. Fai clic su **[!UICONTROL Rivedi per attivare]** per verificare che la campagna sia configurata correttamente, quindi attivala.

Ora puoi eseguire la campagna dalle API. [Ulteriori informazioni](#execute)

### Eseguire la campagna {#execute}

Una volta attivata la campagna, devi recuperare la richiesta cURL di esempio generata e utilizzarla nell’API per generare il payload e attivare la campagna.

1. Apri la campagna, quindi copia e incolla la richiesta di payload dalla sezione **[!UICONTROL richiesta cURL]**. Questo payload include tutte le variabili di personalizzazione (profilo e contesto) utilizzate nel messaggio. È disponibile una volta che la campagna è in diretta.

   ![](assets/api-triggered-curl.png)

1. Utilizza questa richiesta cURL nelle API per generare il payload e attivare la campagna. Per ulteriori informazioni, consulta la [documentazione dell&#39;API di esecuzione interattiva dei messaggi](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).


   Esempi di chiamate API sono disponibili anche in [questa pagina](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).

   >[!NOTE]
   >
   >Se hai configurato una data di inizio e/o di fine specifica durante la creazione della campagna, questa non verrà eseguita al di fuori di queste date e le chiamate API avranno esito negativo.

## Utilizzare attributi contestuali in campagne attivate da API {#contextual}

Con le campagne attivate da API, puoi trasmettere dati aggiuntivi nel payload API e utilizzarli all’interno della campagna per personalizzare il messaggio.

Prendiamo questo esempio, in cui i clienti vogliono reimpostare la propria password e desideri inviare loro un URL di reimpostazione della password generato in uno strumento di terze parti. Con le campagne attivate da API, puoi passare l’URL generato nel payload API e sfruttarlo nella campagna per aggiungerlo al messaggio.

>[!NOTE]
>
>A differenza degli eventi abilitati per il profilo, i dati contestuali passati nell’API REST vengono utilizzati per una comunicazione una tantum e non memorizzati rispetto al profilo. Al massimo, il profilo viene creato con i dettagli dello spazio dei nomi, se questo è stato trovato mancante.

Per utilizzare questi dati nelle campagne, devi passarli nel payload API e aggiungerli nel messaggio utilizzando l’editor di personalizzazione. A questo scopo, utilizza la sintassi `{{context.<contextualAttribute>}}`, in cui `<contextualAttribute>` deve corrispondere al nome della variabile nel payload API contenente i dati che desideri trasmettere.

La sintassi `{{context.<contextualAttribute>}}` è mappata solo a un tipo di dati String.

![](assets/api-triggered-context.png)


>[!IMPORTANT]
>
>Gli attributi contestuali trasmessi nella richiesta non possono superare i 200 kb e sono sempre considerati di tipo stringa.
>
>La sintassi `context.system` è limitata solo all&#39;utilizzo interno di Adobe e non deve essere utilizzata per trasmettere attributi contestuali.

Per il momento non è disponibile alcun attributo contestuale da utilizzare nel menu della barra a sinistra. Gli attributi devono essere digitati direttamente nell&#39;espressione di personalizzazione, senza alcun controllo eseguito da [!DNL Journey Optimizer].

## Creazione di profili durante l’esecuzione della campagna {#profile-creation}

In alcuni casi, potrebbe essere necessario inviare messaggi transazionali a profili che non esistono nel sistema. Ad esempio, se un utente sconosciuto tenta di reimpostare la password sul sito web.

Se nel database non esiste un profilo, Journey Optimizer ti consente di crearlo automaticamente durante l’esecuzione della campagna per consentire l’invio del messaggio a questo profilo.

>[!IMPORTANT]
>
>In caso di messaggi transazionali, questa funzione viene fornita per **la creazione di profili di volume molto piccoli** in un caso di utilizzo di invio transazionale di volumi elevati, con la maggior parte dei profili già esistenti in Platform.

Per attivare la creazione del profilo durante l&#39;esecuzione della campagna, attiva l&#39;opzione **[!UICONTROL Crea nuovi profili]** nella sezione **[!UICONTROL Pubblico]**. Se questa opzione è disabilitata, i profili sconosciuti verranno rifiutati per qualsiasi invio e la chiamata API avrà esito negativo.

![](assets/api-triggered-create-profile.png)

>[!NOTE]
>
>I profili sconosciuti vengono creati nel set di dati del profilo di messaggistica interattiva **AJO**, in tre spazi dei nomi predefiniti (e-mail, telefono e ECID) rispettivamente per ogni canale in uscita (e-mail, SMS e push). Tuttavia, se utilizzi uno spazio dei nomi personalizzato, l’identità viene creata con lo stesso spazio dei nomi personalizzato.

## Video introduttivo {#video}

Scopri come creare una campagna e attivarla da un sistema esterno basato sulle interazioni dell’utente, utilizzando l’API REST di Esecuzione interattiva dei messaggi.

>[!VIDEO](https://video.tv.adobe.com/v/3425358?quality=12)
