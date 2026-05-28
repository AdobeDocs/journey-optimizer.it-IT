---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzo di attributi con più valori
description: Scopri come utilizzare gli attributi calcolati.
feature: Audiences, Profiles
role: User
level: Intermediate
exl-id: 5402a179-263f-46a7-bddf-5b7017cf0f82
TQID: https://experienceleague.adobe.com/bH8UDdjWsh1Kle1ltVP2ltgXcNJDfVIdTuFdGWSZv6Y
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: f42b4d14-fe8a-428b-b62e-e7995eaab1b3
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
  - id: e95b6013-acbe-46e9-a3b5-b80e14088d7d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 520
ht-degree: 3%

---

# Utilizzo di attributi con più valori {#computed-attributes}

Gli attributi calcolati riepilogano i singoli eventi comportamentali in attributi di profilo calcolati disponibili in Adobe Experience Platform. Questi attributi si basano sui set di dati Experience Event abilitati per il profilo acquisiti in Adobe Experience Platform e fungono da punti dati aggregati memorizzati nei profili dei clienti.

Ogni attributo calcolato è un attributo di profilo che puoi sfruttare per la segmentazione, la personalizzazione e l’attivazione in percorsi e campagne. Questa semplificazione migliora la capacità di fornire ai clienti esperienze personalizzate tempestive e significative.


![](../rn/assets/do-not-localize/computed-attributes.gif)


>[!NOTE]
>
>Per accedere agli attributi calcolati, assicurati di disporre delle autorizzazioni appropriate (**Visualizza attributi calcolati** e **Gestisci attributi calcolati**).

## Creare attributi calcolati {#manage}

Per creare attributi calcolati, passare alla scheda **[!UICONTROL Attributi calcolati]** nel menu **[!UICONTROL Profili]** situato sul lato sinistro.

Da questa schermata, puoi creare attributi calcolati creando regole che combinano attributi evento, funzioni di aggregazione, insieme a un periodo di lookback specificato. Ad esempio, puoi calcolare la somma degli acquisti effettuati negli ultimi tre mesi, identificare l’articolo più recente visualizzato da un profilo che non ha effettuato un acquisto nell’ultima settimana o sommare il totale dei punti premio accumulati da ciascun profilo.

![](assets/computed-attributes.png)

Quando la regola è pronta, pubblica l’attributo calcolato per renderlo disponibile in altri servizi a valle, incluso Journey Optimizer.

Informazioni dettagliate sulla creazione e la gestione degli attributi calcolati sono disponibili nella [documentazione relativa agli attributi calcolati](https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html?lang=it)

## Aggiungere attributi calcolati all&#39;origine dati Adobe Experience Platform {#source}

Per sfruttare gli attributi calcolati in Journey Optimizer, aggiungili all&#39;origine dati Journey Optimizer **Experience Platform**.

L’origine dati Adobe Experience Platform definisce la connessione ad Adobe Real-time Customer Profile. Questa origine dati recupera i dati del profilo e i dati di Experience Events da Real-time Customer Profile Service.

Per aggiungere attributi calcolati all&#39;origine dati, eseguire la procedura seguente:

1. Passa al menu a sinistra **[!UICONTROL Configurazioni]**, quindi fai clic sulla scheda **[!UICONTROL Origini dati]**.

1. Selezionare l&#39;origine dati **[!UICONTROL Experience Platform]**.

   ![](assets/computed-attributes-add.png)

1. Aggiungi il gruppo di campi **[!UICONTROL SystemComputedAttributes]** contenente tutti gli attributi calcolati creati.

   ![](assets/computed-attributes-fieldgroup.png)

Gli attributi calcolati sono ora disponibili per l’utilizzo in Journey Optimizer. [Scopri come utilizzare gli attributi calcolati in Journey Optimizer](#use)

Informazioni dettagliate sull&#39;aggiunta di gruppi di campi all&#39;origine dati di Adobe Experience Platform sono disponibili in [questa sezione](../datasource/adobe-experience-platform-data-source.md).

## Utilizzare attributi calcolati in Journey Optimizer {#use}

>[!NOTE]
>
>Prima di iniziare, assicurati di aver aggiunto gli attributi calcolati all’origine dati Adobe Experience Platform. [Scopri come in questa sezione](#source).

Gli attributi calcolati forniscono funzionalità versatili in Journey Optimizer. Utilizzali per vari scopi, come personalizzare il contenuto dei messaggi, creare nuovi tipi di pubblico o suddividere i percorsi in base a uno specifico attributo calcolato. Ad esempio, dividi il percorso di un percorso in base agli acquisti totali di un profilo nelle ultime tre settimane aggiungendo un singolo attributo calcolato in un’attività Condizione. Puoi anche personalizzare un’e-mail visualizzando l’elemento visualizzato più di recente per ciascun profilo.

Poiché gli attributi calcolati sono campi di attributi di profilo creati nello schema di unione profili, puoi accedervi dall&#39;editor di personalizzazione nel gruppo di campi **SystemComputedAttributes**. A questo punto, aggiungi attributi calcolati nelle espressioni, trattandole come qualsiasi altro attributo di profilo per eseguire le operazioni desiderate.

![](assets/computed-attributes-ajo.png)
