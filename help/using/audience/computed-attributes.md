---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzo di attributi con più valori
description: Scopri come utilizzare gli attributi calcolati.
feature: Audiences, Profiles
role: User
level: Intermediate
exl-id: 5402a179-263f-46a7-bddf-5b7017cf0f82
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 4%

---

# Utilizzo di attributi con più valori {#computed-attributes}

Gli attributi calcolati consentono di riepilogare i singoli eventi comportamentali in attributi di profilo calcolati disponibili in Adobe Experience Platform. Questi attributi calcolati si basano sui set di dati Experience Event abilitati per il profilo acquisiti in Adobe Experience Platform e fungono da punti di dati aggregati memorizzati nei profili dei clienti.

Ogni attributo calcolato è un attributo di profilo che puoi sfruttare per la segmentazione, la personalizzazione e l’attivazione in percorsi e campagne. Questa semplificazione migliora la capacità di fornire ai clienti esperienze personalizzate tempestive e significative.


![](../rn/assets/do-not-localize/computed-attributes.gif)


>[!NOTE]
>
>Per accedere agli attributi calcolati, devi disporre delle autorizzazioni appropriate (**Visualizza attributi calcolati** e **Gestisci attributi calcolati**).

## Creare attributi calcolati {#manage}

Per creare attributi calcolati, passare alla scheda **[!UICONTROL Attributi calcolati]** nel menu **[!UICONTROL Profili]** situato sul lato sinistro.

Da questa schermata, puoi creare attributi calcolati creando regole che combinano attributi evento, funzioni di aggregazione e un periodo di lookback specificato. Ad esempio, puoi calcolare la somma degli acquisti effettuati negli ultimi tre mesi, identificare l’articolo più recente visualizzato da un profilo che non ha effettuato un acquisto nell’ultima settimana o sommare il totale dei punti premio accumulati da ciascun profilo.

![](assets/computed-attributes.png)

Quando la regola è pronta, pubblica l’attributo calcolato per renderlo disponibile in altri servizi a valle, incluso Journey Optimizer.

Informazioni dettagliate su come creare e gestire attributi calcolati sono disponibili nella [documentazione sugli attributi calcolati](https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html?lang=it)

## Aggiungere attributi calcolati all&#39;origine dati Adobe Experience Platform {#source}

Per poter sfruttare gli attributi calcolati in Journey Optimizer, devi innanzitutto aggiungerli all&#39;origine dati Journey Optimizer **Experience Platform**.

L’origine dati di Adobe Experience Platform definisce la connessione ad Adobe Real-Time Customer Profile. Questa origine dati è progettata per recuperare i dati del profilo e i dati di Experience Events da Real-time Customer Profile Service.

Per aggiungere attributi calcolati all&#39;origine dati, eseguire la procedura seguente:

1. Passa al menu a sinistra delle **[!UICONTROL configurazioni]**, quindi fai clic sulla scheda **[!UICONTROL Origini dati]**.

1. Selezionare l&#39;origine dati **[!UICONTROL Experience Platform]**.

   ![](assets/computed-attributes-add.png)

1. Aggiungi il gruppo di campi **[!UICONTROL SystemComputedAttributes]** contenente tutti gli attributi calcolati creati.

   ![](assets/computed-attributes-fieldgroup.png)

Gli attributi calcolati sono ora disponibili per l’utilizzo in Journey Optimizer. [Scopri come utilizzare gli attributi calcolati in Journey Optimizer](#use)

Informazioni dettagliate su come aggiungere gruppi di campi all&#39;origine dati di Adobe Experience Platform sono disponibili in [questa sezione](../datasource/adobe-experience-platform-data-source.md).

## Utilizzare attributi calcolati in Journey Optimizer {#use}

>[!NOTE]
>
>Prima di iniziare, assicurati di aver aggiunto gli attributi calcolati all’origine dati di Adobe Experience Platform. [Scopri come in questa sezione](#source).

Gli attributi calcolati offrono un set versatile di funzionalità all’interno di Percorsi Optimizer. Puoi utilizzarli per vari scopi, ad esempio per personalizzare il contenuto dei messaggi, creare nuovi tipi di pubblico o suddividere i percorsi in base a uno specifico attributo calcolato. Ad esempio, puoi dividere il percorso di un percorso in base agli acquisti totali di un profilo nelle ultime tre settimane, aggiungendo un singolo attributo calcolato in un’attività Condizione. Puoi anche personalizzare un’e-mail visualizzando l’elemento visualizzato più di recente per ciascun profilo.

Poiché gli attributi calcolati sono campi di attributi di profilo creati nello schema di unione profili, puoi accedervi dall&#39;editor di personalizzazione nel gruppo di campi **SystemComputedAttributes**. Da qui, puoi aggiungere un attributo calcolato alle espressioni, trattandole come qualsiasi altro attributo di profilo per eseguire le operazioni desiderate.

![](assets/computed-attributes-ajo.png)
