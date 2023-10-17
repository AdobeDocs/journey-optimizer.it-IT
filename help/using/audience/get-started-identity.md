---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle identità in Journey Optimizer
description: Scopri come gestire le identità in Adobe Journey Optimizer
feature: Profiles, Identities
role: User
level: Beginner
exl-id: 90e892e9-33c2-4da5-be1d-496b42572897
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: ht
source-wordcount: '342'
ht-degree: 100%

---

# Introduzione alle identità {#identities-gs}

Un’identità è un dato univoco per un’entità, in genere una singola persona. Un’identità, ad esempio un ID di accesso, un ECID o un ID fedeltà, viene definita identità nota.

Le informazioni personali (PII, Personally Identifiable Information) come indirizzo e-mail e numero di telefono, servono per identificare direttamente un cliente. Di conseguenza, i dati PII vengono utilizzati per far corrispondere le identità multiple di un cliente tra i vari sistemi.

In [!DNL Adobe Journey Optimizer], le **Identità** collegano i consumatori tra dispositivi e canali creando un [grafico delle identità](#id-graph). Il grafico delle identità collegato viene utilizzato per personalizzare le esperienze in base alle interazioni tra tutti i punti di contatto aziendali.

![](assets/identities-home.png)

Ulteriori informazioni su **Identity Service** in [questa documentazione](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=it){target="_blank"}.

## Spazio dei nomi delle identità {#identity-namespaces}

Gli **spazi dei nomi dele identità** sono un componente di Identity Service che fungono da indicatori del contesto a cui si riferisce un’identità. Ad esempio, distinguono un valore di `name@email.com` come indirizzo e-mail o `443522` come ID CRM numerico. Per utilizzare gli spazi dei nomi delle identità è necessario comprendere i vari servizi Adobe Experience Platform interessati. Prima di iniziare a utilizzare gli spazi dei nomi, controlla la documentazione relativa ai seguenti servizi:

Ulteriori informazioni su **Spazio dei nomi delle identità** in [questa documentazione](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=it){target="_blank"}.

## Grafico delle identità{#id-graph}

Il **Grafico delle identità** è una mappa delle relazioni tra identità diverse per un particolare cliente, che fornisce una rappresentazione visiva di come il cliente interagisce con il tuo marchio su diversi canali. Tutti i grafici dell’identità del cliente vengono gestiti e aggiornati collettivamente da Adobe Experience Platform Identity Service in tempo quasi reale, in risposta all’attività del cliente.

Il visualizzatore del grafico delle identità nell’interfaccia utente [!DNL Adobe Journey Optimizer] ti consente di visualizzare e comprendere meglio quali identità dei clienti sono unite e in che modo. Il visualizzatore consente di trascinare e interagire con diverse parti del grafico, consentendoti di esaminare relazioni di identità complesse, eseguire il debug in modo più efficiente e beneficiare di una maggiore trasparenza nell’utilizzo delle informazioni.

Ulteriori informazioni sul **Grafico delle identità** in [questa documentazione](https://experienceleague.adobe.com/docs/experience-platform/identity/ui/identity-graph-viewer.html?lang=it){target="_blank"}.
