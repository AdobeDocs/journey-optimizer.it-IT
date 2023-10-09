---
title: Catalogo articoli
description: Scopri come utilizzare il catalogo degli elementi
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 2d118f5a-32ee-407c-9513-fe0ebe3ce8f0
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 16%

---

# Catalogo articoli {#catalog}

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione:

* [Introduzione a Offer Decisioning](gs-experience-decisioning.md)
* Gestire gli elementi decisionali
   * **[Configurare il catalogo degli elementi](catalogs.md)**
   * [Creare elementi decisionali](items.md)
   * [Gestire le raccolte di elementi](collections.md)
* Configurare la selezione degli elementi
   * [Creare regole di decisione](rules.md)
   * [Creare metodi di classificazione](ranking.md)
* [Creare strategie di selezione](selection-strategies.md)
* [Creare criteri di decisione](create-decision.md)

>[!ENDSHADEBOX]

In Experience Decisioning, i cataloghi fungono da contenitori centrali per l’organizzazione degli elementi decisionali. Ogni catalogo è collegato a uno schema Adobe Experience Platform, che include tutti gli attributi assegnabili a un elemento decisionale.

Per il momento, tutti gli elementi decisionali creati sono consolidati in un unico catalogo &quot;Offerte&quot;, accessibile tramite **[!UICONTROL Elementi]** menu.

![](assets/catalogs-list.png)

Per accedere allo schema del catalogo in cui sono memorizzati gli attributi degli elementi decisionali, effettua le seguenti operazioni:

1. Nell&#39;elenco Elementi fare clic sul pulsante **[!UICONTROL Modifica schema]** accanto al pulsante **[!UICONTROL Crea elemento]** pulsante.

1. Lo schema del catalogo viene aperto in una nuova scheda, seguendo la struttura riportata di seguito:

   * Il **`_experience`** Il nodo include gli attributi standard degli elementi decisionali come nome, data di inizio e di fine e descrizione.
   * Il **`_<imsOrg>`** il nodo ospita gli attributi degli elementi decisionali personalizzati. Per impostazione predefinita, non sono configurati attributi personalizzati, ma puoi aggiungerne quanti ne servono in base alle tue esigenze. Al termine, gli attributi personalizzati vengono visualizzati nella schermata di creazione dell’elemento decisionale insieme agli attributi standard.

   ![](assets/catalogs-schema.png)

1. Per aggiungere un attributo personalizzato allo schema, espandi la **`_<imsOrg>`** e fare clic sul pulsante &quot;+&quot; nella posizione desiderata nella struttura.

   ![](assets/catalogs-add.png)

1. Inserisci i campi necessari per l’attributo aggiunto e fai clic su **[!UICONTROL Applica]**.

   >[!CAUTION]
   >
   >Per il momento, Experience Decisioning supporta esclusivamente i tipi di dati elencati di seguito. Eventuali campi che non rientrano in questi tipi di dati non saranno disponibili per l’utilizzo durante la creazione di un elemento decisionale.
   >* Stringa
   >* Booleano
   >* Numero

   Informazioni dettagliate su come lavorare con gli schemi di Adobe Experience Platform sono disponibili nella sezione [Documentazione del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=it).

1. Una volta aggiunti gli attributi personalizzati desiderati, salva lo schema. Il nuovo campo è ora disponibile nella schermata di creazione delle decisioni sugli elementi, all’interno di **[!UICONTROL Attributi personalizzati]** sezione.
