---
title: Catalogo articoli
description: Scopri come utilizzare il catalogo degli elementi
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilità limitata"
exl-id: 2d118f5a-32ee-407c-9513-fe0ebe3ce8f0
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Catalogo articoli {#catalog}

In Decisioning, i cataloghi fungono da contenitori centrali per l’organizzazione degli elementi decisionali. Ogni catalogo è collegato a uno schema Adobe Experience Platform, che include tutti gli attributi assegnabili a un elemento decisionale.

Per il momento, tutti gli elementi decisionali creati sono consolidati in un unico catalogo &quot;Offerte&quot;, accessibile tramite il menu **[!UICONTROL Cataloghi]**.

![](assets/catalogs-list.png)

Per accedere allo schema del catalogo in cui sono memorizzati gli attributi degli elementi decisionali, effettua le seguenti operazioni:

1. Nell&#39;elenco degli elementi fare clic sul pulsante **[!UICONTROL Modifica schema]** accanto al pulsante **[!UICONTROL Crea elemento]**.

1. Lo schema del catalogo viene aperto in una nuova scheda, seguendo la struttura riportata di seguito:

   * Il nodo **`_experience`** include attributi di elementi decisionali standard quali nome, data di inizio e di fine e descrizione.
   * Il nodo **`_<imsOrg>`** ospita gli attributi degli elementi decisionali personalizzati. Per impostazione predefinita, non sono configurati attributi personalizzati, ma puoi aggiungerne quanti ne servono in base alle tue esigenze. Al termine, gli attributi personalizzati vengono visualizzati nella schermata di creazione dell’elemento decisionale insieme agli attributi standard.

   ![](assets/catalogs-schema.png)

1. Per aggiungere un attributo personalizzato allo schema, espandere il nodo **`_<imsOrg>`** e fare clic sul pulsante &quot;+&quot; nella posizione desiderata nella struttura.

   ![](assets/catalogs-add.png)

1. Compila i campi necessari per l&#39;attributo aggiunto e fai clic su **[!UICONTROL Applica]**.

   >[!CAUTION]
   >
   >Per il momento, Decisioning supporta esclusivamente i seguenti tipi di dati: String, Integer, Boolean, Date, DateTime e Decisioning Assets. Eventuali campi che non rientrano in questi tipi di dati non saranno disponibili per l’utilizzo durante la creazione di un elemento decisionale o di un catalogo.

   Il valore immesso in un attributo con l’attributo di risorsa decisioning è un URL pubblico. Nella maggior parte dei casi, questo richiama un’immagine.

   Informazioni dettagliate su come utilizzare gli schemi di Adobe Experience Platform sono disponibili nella [documentazione del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=it).

1. Una volta aggiunti gli attributi personalizzati desiderati, salva lo schema. Il nuovo campo è ora disponibile nella schermata di creazione delle decisioni sugli elementi, nella sezione **[!UICONTROL Attributi personalizzati]**.
