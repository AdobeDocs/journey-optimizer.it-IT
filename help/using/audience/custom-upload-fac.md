---
solution: Journey Optimizer
product: journey optimizer
title: Caricamento personalizzato (CSV) e composizione federata del pubblico
description: Scopri le informazioni chiave e le best practice per l’utilizzo del caricamento personalizzato (CSV) e dei tipi di pubblico con Composizione del pubblico federata.
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
exl-id: d2365e3f-fbef-43c2-bf2a-0a868cb93015
source-git-commit: a98312d9ac5a457bfd6789bf79ad80a24d894a0b
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 1%

---

# Caricamento personalizzato (CSV) e composizione federata del pubblico {#csv-fac}

## Informazioni sul caricamento personalizzato e sulla composizione federata del pubblico {#about}

Oltre alle definizioni dei segmenti e alla composizione del pubblico, [!DNL Journey Optimizer] consente di generare e indirizzare tipi di pubblico importandoli da un file CSV o sfruttando i dati del data warehouse.

* **Caricamento personalizzato**: importa un pubblico utilizzando un file CSV. Scopri come importare i tipi di pubblico nella [documentazione del servizio di segmentazione](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"} di Adobe Experience Platform.

* **Composizione pubblico federato**: unisci i set di dati direttamente dal data warehouse esistente per creare e arricchire tipi di pubblico e attributi di Adobe Experience Platform in un unico sistema. Leggi la guida su [Federated Audience Composition](https://experienceleague.adobe.com/it/docs/federated-audience-composition/using/home).

Puoi indirizzare questi tipi di pubblico in Journey Optimizer o attivarli in qualsiasi destinazione supportata da Adobe Experience Platform

➡️ [Scopri queste funzioni nel video](#video)

## Da leggere {#must-read}

Questa sezione fornisce informazioni chiave da tenere presenti quando si lavora con i tipi di pubblico Caricamento personalizzato (file CSV) e Composizione federata del pubblico.

* **Supporto per anteprima e bozza:** Al momento, l&#39;anteprima e la bozza non sono supportate per i tipi di pubblico creati mediante caricamento CSV o Composizione di pubblico federato. Tieni presente questo aspetto durante la pianificazione delle campagne.

* **Ritardo di attivazione:** i tipi di pubblico sono pronti per essere utilizzati in Journey Optimizer al termine dell&#39;acquisizione. Sebbene questo avvenga in genere entro un’ora, è soggetto ad alcune variabilità.

* **Record attivati e unione identità:** tutti i record nel pubblico vengono attivati, inclusi eventuali duplicati. Durante la prossima esportazione del profilo UPS, questi record passeranno attraverso l’unione delle identità. Di conseguenza, il numero di record attivati può differire dal numero di profili dopo l’unione di identità.

* **Esecuzione del targeting di nuovi profili:** Quando non viene trovata una corrispondenza tra un record e un profilo UPS, viene creato un nuovo profilo vuoto. Questo profilo è collegato agli attributi di arricchimento memorizzati nel data lake. Poiché questo nuovo profilo è vuoto, i campi di targeting utilizzati in genere in Journey Optimizer (ad esempio, personalEmail.address, mobilePhone.number) sono vuoti e quindi non possono essere utilizzati per il targeting.

  Per risolvere questo problema, puoi specificare il &quot;campo di esecuzione&quot; (o &quot;indirizzo di esecuzione&quot; a seconda del canale) nella configurazione del canale come &quot;identityMap&quot;. In questo modo l’attributo scelto come identità nella creazione del pubblico sarà quello utilizzato per il targeting in Journey Optimizer.

## Video sulle procedure {#video}

Scopri come caricare il pubblico in formato CSV in Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/3421714?quality=12)

Ulteriori informazioni su Federated Audience Composition.

>[!VIDEO](https://video.tv.adobe.com/v/3432261?quality=12)
