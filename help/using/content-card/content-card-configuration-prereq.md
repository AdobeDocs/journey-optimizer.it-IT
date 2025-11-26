---
title: Configurazione delle schede di contenuto
description: Prerequisiti per il canale delle schede di contenuto
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: df92e319-1e42-486f-b688-595964a762c9
source-git-commit: 3d5ed7c5efd76616c8dbc89078f7368eedc5f1af
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 3%

---

# Prerequisiti per le schede di contenuto {#content-card-configuration-prereq}

Affinché Adobe Journey Optimizer visualizzi correttamente le schede di contenuto, devi configurare le seguenti impostazioni Adobe Experience Platform:

* **Raccolta dati di Adobe Experience Platform**

  [Crea uno stream di dati](https://experienceleague.adobe.com/it/docs/experience-platform/datastreams/configure){target="_blank"} e [aggiungi il servizio Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/datastreams/configure#aep){target="_blank"}. Abilita le opzioni **[!UICONTROL Segmentazione Edge]** e **[!UICONTROL Adobe Journey Optimizer]**. In questo modo gli eventi Journey Optimizer vengono gestiti da Adobe Experience Platform Edge Network.
Aggiungi il gruppo di campi **Evento esperienza - Interazione proposta** al set di dati per includere i dati nei rapporti. [Ulteriori informazioni sugli stream di dati](https://experienceleague.adobe.com/it/docs/experience-platform/datastreams/configure){target="_blank"}

* **Adobe Experience Platform**

  Verifica che il criterio di unione predefinito abbia **Criterio di unione attivo su Edge** abilitato nel menu Experience Platform **[!UICONTROL Cliente]** > **[!UICONTROL Profili]** > **[!UICONTROL Criteri di unione]**. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=it#configure){target="_blank"}

  >[!NOTE]
  >
  >Quando utilizzi un criterio di unione personalizzato **[!UICONTROL Preferenza set di dati]**, assicurati di aggiungere il set di dati **[!UICONTROL Percorso in entrata]** all&#39;interno del criterio di unione specificato.

* **Adobe Experience Platform Mobile o Platform Web SDK**

  Per le applicazioni per dispositivi mobili e Web, per aggiungere modifiche alle pagine Web o alle app per dispositivi mobili, devi implementare [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/it/docs/platform-learn/implement-web-sdk/overview){target="_blank"} sul tuo sito Web o [Adobe Experience Platform Mobile SDK](https://developer.adobe.com/client-sdks/home/){target="_blank"} nelle tue app per dispositivi mobili.

* **Journey Optimizer**

  Crea una [configurazione scheda di contenuto](#content-card-configuration).

* **Risoluzione dei problemi**

  Utilizza la visualizzazione **Edge Delivery** in **Adobe Experience Platform Assurance** per risolvere i problemi delle esperienze mobili. Può esaminare le richieste, verificare le chiamate edge ed esaminare i dati del profilo. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}

* **Esperimenti contenuto**

  Assicurati che il set di dati utilizzato nello [stream di dati](https://experienceleague.adobe.com/it/docs/experience-platform/datastreams/overview#_blank){target="_blank"} dell&#39;app sia incluso anche nella configurazione di reporting dell&#39;esperimento sui contenuti. I dati dell’app non vengono visualizzati nei rapporti se i set di dati non corrispondono.

  Scopri come aggiungere set di dati per i rapporti sull’esperimento dei contenuti in [questa sezione](../reports/reporting-configuration.md).

## Guardrail di gestione del profilo {#profile-management-guardrail}

Le schede di contenuto [!DNL Journey Optimizer] possono essere indirizzate a profili pseudonimi, ovvero profili non autenticati o non ancora noti perché non sono stati precedentemente attivati su altri canali. Questo è il caso, ad esempio, quando si esegue il targeting di tutti i visitatori o tipi di pubblico in base a ID temporanei come ECID.

Questo aumenta il numero totale di profili coinvolgibili, il che può avere implicazioni di costo se viene superato il numero contrattuale di profili coinvolgibili acquistati. Le metriche di licenza per ciascun pacchetto sono elencate nella pagina [Descrizione del prodotto Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}. Puoi controllare il numero di profili coinvolgibili nel [dashboard di utilizzo delle licenze](../audience/license-usage.md).

Per mantenere i profili coinvolgibili entro limiti ragionevoli, Adobe consiglia di impostare un valore TTL (Time-To-Live) per eliminare automaticamente i profili pseudonimi dal profilo cliente in tempo reale se non sono stati visualizzati o coinvolti in un intervallo di tempo specifico.

>[!NOTE]
>
>Scopri come configurare la scadenza dei dati per i profili pseudonimi nella [documentazione di Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}.

Adobe consiglia di impostare il valore TTL su 14 giorni, in modo che corrisponda al valore TTL del profilo Edge corrente.