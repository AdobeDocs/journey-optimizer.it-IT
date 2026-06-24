---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare e assegnare sandbox
description: Scopri come gestire le sandbox
feature: Sandboxes
topic: Administration
role: Admin, Developer
level: Experienced
keywords: sandbox, virtuale, ambienti, organizzazione, piattaforma
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
TQID: https://experienceleague.adobe.com/8vcaHkqHeyoP-TZltCkjpBhvZIifuiPbKy-Whoj74Z8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
subfeature_v2: []
source-git-commit: c46ce04b47a3576e6373cbe788f2bbccf6ddbed0
workflow-type: tm+mt
source-wordcount: 919
ht-degree: 12%

---

# Utilizzare e assegnare sandbox {#sandboxes}

>[!BEGINSHADEBOX]

**In questa pagina:** utilizza e assegna sandbox per suddividere l&#39;istanza di Adobe Journey Optimizer in ambienti isolati, in modo da poter sviluppare, testare ed eseguire in produzione senza influire su altri lavori.

>[!ENDSHADEBOX]

Le **Sandbox** sono ambienti virtuali che suddividono l&#39;istanza di Adobe Journey Optimizer in aree di lavoro separate e isolate, per lo sviluppo, il test o la produzione. La gestione della sandbox si trova in **Amministrazione** > **Canali** > **Connetti i sistemi e gli ambienti** (o tramite il selettore sandbox in alto a destra nell&#39;interfaccia). Le sandbox consentono di sperimentare in modo sicuro, assegnare un accesso diverso per ruolo e mantenere il contenuto organizzato. In questa pagina viene illustrato come utilizzare e assegnare sandbox, configurare l&#39;accesso al contenuto e, nell&#39;articolo [Esportare oggetti in un&#39;altra sandbox](../configuration/copy-objects-to-sandbox.md), come copiare percorsi e modelli tra sandbox.

## Utilizzare le sandbox {#using-sandbox}

[!DNL Journey Optimizer] consente di suddividere l&#39;istanza in ambienti virtuali separati denominati sandbox. Le sandbox vengono assegnate tramite i ruoli in Autorizzazioni. [Scopri come assegnare le sandbox](permissions.md#create-product-profile).

[!DNL Journey Optimizer] riflette le sandbox di Adobe Experience Platform create per una determinata organizzazione. Le sandbox di Adobe Experience Platform possono essere create o reimpostate dall’istanza di Adobe Experience Platform. [Ulteriori informazioni sono disponibili nella guida utente sulle sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=it){target="_blank"}.

Puoi trovare il controllo del commutatore sandbox in alto a destra dello schermo, accanto al nome della tua organizzazione. Per passare da una sandbox all’altra, fai clic sulla sandbox attualmente attiva nel commutatore e selezionane un’altra dall’elenco a discesa.

![](assets/sandbox_5.png)

➡️ [Ulteriori informazioni sulle sandbox in questo video](#video)

## Assegna sandbox {#assign-sandboxes}

>[!IMPORTANT]
>
> La gestione delle sandbox può essere eseguita solo da un amministratore **[!UICONTROL Product]** o **[!UICONTROL System]**.

Puoi scegliere di assegnare sandbox diverse a **[!UICONTROL Ruoli]** predefiniti o personalizzati.

Per assegnare le sandbox:

1. In [!DNL Permissions], dalla scheda **[!UICONTROL Ruoli]**, selezionare un **[!UICONTROL Ruolo]**.

   ![](assets/sandbox_1.png)

1. Fai clic su **[!UICONTROL Modifica]**.

1. Dall&#39;elenco a discesa delle risorse **[!UICONTROL Sandbox]**, seleziona la sandbox che verrà assegnata al tuo ruolo.

   ![](assets/sandbox_3.png)

1. Se necessario, fai clic sull&#39;icona X accanto ad essa per rimuovere l&#39;accesso alla sandbox dal tuo **[!UICONTROL Ruolo]**.

   ![](assets/sandbox_4.png)

1. Fai clic su **[!UICONTROL Salva]**.

## Accesso al contenuto {#content-access}

Per configurare l’accessibilità dei contenuti, assegna una cartella condivisa di contenuto a ciascuna sandbox. Puoi creare e configurare le cartelle condivise nella scheda **[!UICONTROL Archiviazione]** visualizzata in [!DNL Admin Console] per gli amministratori. Se hai accesso a [!DNL Admin Console] come amministratore di sistema, puoi creare cartelle condivise e aggiungere delegati con diversi livelli di accesso alle cartelle condivise.

![](assets/do-not-localize/content_access.png)

Per sincronizzare i contenuti con la sandbox corretta, è necessario seguire la stessa sintassi della sandbox. Ad esempio, se la sandbox è denominata &quot;sviluppo&quot;, la cartella condivisa deve avere lo stesso nome.

[Scopri come gestire le cartelle condivise](https://helpx.adobe.com/it/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target="_blank"}.

## Video introduttivo{#video}

Scopri cosa sono le sandbox e come distinguere le sandbox di sviluppo da quelle di produzione. Scopri come creare, reimpostare ed eliminare le sandbox.

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

- **TL;DR:** Le sandbox suddividono l&#39;istanza di Journey Optimizer in aree di lavoro virtuali isolate per lo sviluppo, il test e la produzione. Vengono assegnate agli utenti tramite i ruoli nel prodotto Autorizzazioni e l&#39;accesso ai contenuti viene configurato tramite cartelle condivise in Admin Console.

**Intenti:**

- Passare da una sandbox all’altra nell’interfaccia di Journey Optimizer utilizzando il commutatore sandbox
- Assegnare una o più sandbox a un ruolo nel prodotto Autorizzazioni
- Rimuovere l’accesso sandbox da un ruolo
- Configurare l’accesso al contenuto (cartelle condivise) per una sandbox
- Comprendere la correlazione delle sandbox con ruoli e autorizzazioni

**Glossario:**

- **Sandbox**: ambiente virtuale che suddivide l&#39;istanza di Journey Optimizer in aree di lavoro separate e isolate per lo sviluppo, il test o l&#39;utilizzo in produzione *(specifico per prodotto)*
- **Commutatore sandbox**: il controllo in alto a destra dell&#39;interfaccia di Journey Optimizer, accanto al nome dell&#39;organizzazione, utilizzato per passare dalle sandbox *(specifiche del prodotto)*
- **Cartella condivisa**: cartella di archiviazione configurata in Admin Console per una sandbox che consente l&#39;accesso al contenuto; il nome deve corrispondere al nome della sandbox per consentire la corretta sincronizzazione del contenuto *(specifico per prodotto)*

**Guardrail:**

- La gestione delle sandbox può essere eseguita solo da un amministratore di prodotto o di sistema (prerequisito difficile, come indicato nella nota importante sulla pagina)
- I nomi delle cartelle condivise devono seguire la stessa sintassi del nome della sandbox per il contenuto da sincronizzare con la sandbox corretta (come indicato nella pagina)

**Terminologia:**

- Non confondere: &quot;Utilizzo di una sandbox&quot; (passaggio a essa nell’interfaccia utente utilizzando il commutatore sandbox) ≠ &quot;Assegnazione di una sandbox&quot; (aggiunta di una sandbox a un ruolo nel prodotto Autorizzazioni) ≠ &quot;Creazione di una sandbox&quot; (eseguito in Adobe Experience Platform, non in Journey Optimizer)
- Sinonimi: &quot;sandbox&quot; = &quot;ambiente virtuale&quot; nel contesto di questa pagina
- Da non confondere: &quot;Assegnare sandbox&quot; (aggiunta di sandbox a un ruolo in Autorizzazioni) ≠ &quot;Gestire sandbox&quot; (creazione, reimpostazione o eliminazione di sandbox — operazione eseguita in Adobe Experience Platform)

**Domande frequenti:**

- **D: come posso passare da una sandbox all&#39;altra in Journey Optimizer?** — Utilizza il selettore sandbox in alto a destra dello schermo, accanto al nome dell’organizzazione; fai clic sulla sandbox attiva e selezionane un’altra dall’elenco a discesa.
- **D: chi può assegnare le sandbox ai ruoli?** — Solo amministratori di prodotto o di sistema.
- **D: In che modo le sandbox vengono rese disponibili agli utenti?** — Le sandbox vengono assegnate tramite i ruoli nel prodotto Autorizzazioni.
- **D: quale convenzione di denominazione deve seguire una cartella condivisa?** — La cartella condivisa deve avere lo stesso nome della sandbox a cui è associata (ad esempio, se la sandbox è denominata &quot;sviluppo&quot;, anche la cartella condivisa deve essere denominata &quot;sviluppo&quot;).

+++
<!-- ai-accordion-version: 1 | source-hash: 0a5ada9b -->