---
title: Guida introduttiva alle identità in Journey Optimizer
description: Scopri come gestire le identità in Adobe Journey Optimizer
feature: Profili
role: User
level: Beginner
source-git-commit: e51be6bf18f2e3dfec11e80d34bf63a8ce8b1012
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Guida introduttiva alle identità {#identities-gs}

Un’identità è un dato univoco per un’entità, in genere una singola persona. Un&#39;identità, ad esempio un ID di accesso, un ECID o un ID fedeltà, viene definita identità nota.

Informazioni personali (PII, Personally Identifiable Information) come indirizzo e-mail e numero di telefono, serve per identificare direttamente un cliente. Di conseguenza, i dati PII vengono utilizzati per far corrispondere le identità multiple di un cliente tra i vari sistemi.

In [!DNL Adobe Journey Optimizer], **Identità** collega i consumatori tra dispositivi e canali, il risultato è un [grafico delle identità](#id-graph). Il grafico dell’identità collegato viene utilizzato per personalizzare le esperienze in base alle interazioni tra tutti i punti di contatto aziendali.

![](assets/identities-home.png)

Ulteriori informazioni su **Servizio identità** in [questa documentazione](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html){target=&quot;_blank&quot;}.

## Namespace Identity

**Gli** spazi dei nomi di identità sono un componente del servizio Identity che funge da indicatori del contesto a cui si riferisce un’identità. Ad esempio, distinguono un valore di `name@email.com` come indirizzo e-mail o `443522` come ID CRM numerico. Per utilizzare i namespace di identità è necessario comprendere i vari servizi Adobe Experience Platform interessati. Prima di iniziare a utilizzare i namespace, controlla la documentazione relativa ai seguenti servizi:

Ulteriori informazioni su **Namespace** in [questa documentazione](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html){target=&quot;_blank&quot;}.

## Grafico di identità{#id-graph}

Il **grafico identità** è una mappa delle relazioni tra identità diverse per un particolare cliente, che fornisce una rappresentazione visiva delle interazioni del cliente con il tuo marchio tra diversi canali. Tutti i grafici dell’identità del cliente vengono gestiti e aggiornati collettivamente da Adobe Experience Platform Identity Service in tempo quasi reale, in risposta all’attività del cliente.

Il visualizzatore del grafico delle identità nell’ interfaccia utente di [!DNL Adobe Journey Optimizer] ti consente di visualizzare e comprendere meglio quali sono le identità dei clienti unite e in che modo. Il visualizzatore consente di trascinare e interagire con diverse parti del grafico, consentendoti di esaminare relazioni di identità complesse, eseguire il debug in modo più efficiente e beneficiare di una maggiore trasparenza nell’utilizzo delle informazioni.

Ulteriori informazioni su **Identity Graph** in [questa documentazione](https://experienceleague.adobe.com/docs/experience-platform/identity/ui/identity-graph-viewer.html){target=&quot;_blank&quot;}.

