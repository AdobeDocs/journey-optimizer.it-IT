---
solution: Journey Optimizer
product: journey optimizer
title: Attivare campagne tramite API
description: Scopri come attivare le campagne utilizzando le API di Journey Optimizer
topic: Content Management
role: Developer, Admin
level: Intermediate, Experienced
keywords: campagne, attivazione API, REST, ottimizzatore, messaggi
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: d2ce7d7e717ed5fa171cb3de31915830f391d7f9
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 3%

---

# Attivare campagne tramite API {#trigger-campaigns}

## Informazioni sulle campagne attivate dall’API {#about}

Con [!DNL Journey Optimizer], puoi creare campagne e richiamarle da un sistema esterno basato sul trigger dell’utente utilizzando [API REST di esecuzione dei messaggi interattivi](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution). Questo ti consente di soddisfare varie esigenze operative e di messaggistica transazionale, tra cui reimpostazioni di password e token OTP.

A questo scopo, devi prima creare una campagna con attivazione API in Journey Optimizer e quindi avviarne l’esecuzione tramite una chiamata API.

I canali disponibili per le campagne con attivazione API sono messaggi e-mail, SMS e push.

## Creare una campagna con attivazione API {#create}

### Configurare e attivare la campagna {#create-activate}

Il processo di creazione di campagne con attivazione API rimane lo stesso delle campagne pianificate, ad eccezione della selezione del pubblico che viene eseguita nel payload API. Informazioni dettagliate su come creare una campagna sono disponibili in [questa sezione](create-campaign.md).

Per creare una campagna con attivazione API, segui questi passaggi:

1. Crea una nuova campagna con **[!UICONTROL Attivazione dall’API]** digitare.

1. Scegli il canale e la superficie del canale da utilizzare per inviare il messaggio, quindi fai clic su **[!UICONTROL Crea]**.

   ![](assets/api-triggered-type.png)

1. Specifica un titolo e una descrizione per la campagna, quindi configura il messaggio da inviare.

   ![](assets/api-triggered-properties.png)

   >[!NOTE]
   >
   >Puoi trasmettere al payload API dati aggiuntivi che puoi sfruttare per personalizzare il messaggio. [Ulteriori informazioni](#contextual)
   >
   >L’utilizzo di un numero elevato di dati contestuali pesanti nel contenuto potrebbe influire sulle prestazioni.

1. In **[!UICONTROL Pubblico]** Specifica lo spazio dei nomi da utilizzare per identificare gli individui del segmento.

   La **[!UICONTROL Creare nuovi profili]** consente di creare automaticamente profili che non esistono nel database. [Ulteriori informazioni sulla creazione di profili all’esecuzione della campagna](#profile-creation)

1. Configura le date di inizio e di fine della campagna.

   Se configuri una data di inizio e/o di fine specifica per una campagna, questa non verrà eseguita al di fuori di tali date e le chiamate API non riusciranno se la campagna viene attivata dalle API.

1. Fai clic su **[!UICONTROL Rivedi per attivare]** per verificare che la campagna sia configurata correttamente, attivala.

Ora puoi eseguire la campagna dalle API. [Ulteriori informazioni](#execute)

### Eseguire la campagna {#execute}

Una volta che la campagna è stata attivata, devi recuperare la richiesta cURL di esempio generata e utilizzarla nell’API per generare il payload e attivare la campagna.

1. Apri la campagna, quindi copia e incolla la richiesta di esempio da **[!UICONTROL richiesta cURL]** sezione .

   ![](assets/api-triggered-curl.png)

1. Utilizza questa richiesta cURL nelle API per generare il payload e attivare la campagna. Per ulteriori informazioni, consulta la [Documentazione API di esecuzione dei messaggi interattivi](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).

   >[!NOTE]
   >
   >Se hai configurato una data di inizio e/o di fine specifica al momento della creazione della campagna, questa non verrà eseguita al di fuori di queste date e le chiamate API non riusciranno.

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
>Gli attributi contestuali passati nella richiesta non possono superare i 50 kb.
>
>La `context.system` La sintassi è limitata ad Adobe all’uso interno e non deve essere utilizzata per trasmettere attributi contestuali.

Per il momento, non è disponibile alcun attributo contestuale da utilizzare nel menu della barra a sinistra. Gli attributi devono essere inseriti direttamente nell’espressione di personalizzazione, senza che venga eseguito alcun controllo da parte di [!DNL Journey Optimizer].

## Creazione di profili all’esecuzione della campagna {#profile-creation}

In alcuni casi, potrebbe essere necessario inviare messaggi transazionali a profili non esistenti nel sistema. Ad esempio, se un utente sconosciuto tenta di reimpostare la password sul sito web.

Quando un profilo non esiste nel database, Journey Optimizer ti consente di crearlo automaticamente durante l’esecuzione della campagna per consentire l’invio del messaggio a questo profilo.

>[!IMPORTANT]
>
>Questa funzione è disponibile per **creazione di profili di volume molto piccoli** in un caso di utilizzo per l’invio transazionale a volume elevato, con una massa di profili già esistenti in platform.

Per attivare la creazione del profilo durante l’esecuzione della campagna, attiva/disattiva la **[!UICONTROL Creare nuovi profili]** in **[!UICONTROL Pubblico]** sezione .

![](assets/api-triggered-create-profile.png)

>[!NOTE]
>
>I profili sconosciuti vengono creati nel **Set di dati del profilo di messaggistica interattiva AJO** set di dati, rispettivamente in tre namespace predefiniti (e-mail, telefono ed ECID) per ogni canale in uscita (E-mail, SMS e push).
