---
solution: Journey Optimizer
product: journey optimizer
title: Inviare un messaggio agli iscritti
description: Scopri come creare un percorso per inviare un messaggio agli abbonati di un elenco
feature: Journeys, Use Cases, Subscriptions
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: percorso, caso d’uso, messaggio, abbonati, elenco, lettura
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sDhncesYlIjsj2zjB-QmjWqP--0KDyp-5x5-UGLSjRc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2: []
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 924
ht-degree: 5%

---

# Inviare un messaggio agli abbonati di un elenco {#send-a-message-to-the-subscribers-of-a-list}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come creare un percorso che invia un messaggio agli abbonati di un elenco utilizzando il gruppo di campi Dettagli consenso e preferenze.

>[!ENDSHADEBOX]

Lo scopo di questo caso d’uso è la creazione di un percorso per inviare un messaggio agli abbonati di un elenco.

In questo esempio viene utilizzato il gruppo di campi **[!UICONTROL Dettagli consenso e preferenze]** di [!DNL Adobe Experience Platform]. Per trovare questo gruppo di campi, scegliere **[!UICONTROL Schemi]** dal menu **[!UICONTROL Gestione dati]**. Nella scheda **[!UICONTROL Gruppi di campi]** immettere il nome del gruppo di campi nel campo di ricerca.

![Questo gruppo di campi include l&#39;elemento subscriptions](assets/consent-and-preference-details-field-group.png)

Per configurare il percorso, eseguire la procedura seguente:

1. Crea un percorso che inizia con un&#39;attività **[!UICONTROL Leggi]**. Ulteriori informazioni in [Creare il primo percorso](journey-gs.md).
1. Aggiungi al percorso un&#39;attività di azione **[!UICONTROL E-mail]**. Scopri come [Utilizzare le azioni del canale](journey-action.md).
1. Nella sezione **[!UICONTROL Parametri e-mail]** delle impostazioni dell&#39;attività **[!UICONTROL E-mail]**, sostituisci l&#39;indirizzo e-mail predefinito (`PersonalEmail.adress`) con l&#39;indirizzo e-mail degli iscritti all&#39;elenco:

   1. Fai clic sull&#39;icona **[!UICONTROL Abilita sostituzione parametro]** a destra del campo **[!UICONTROL Indirizzo]**, quindi fai clic sull&#39;icona **[!UICONTROL Modifica]**.

      ![Flusso di Percorso con pubblico di lettura per il targeting dell&#39;elenco degli abbonati](assets/message-to-subscribers-uc-1.png)

   1. Nell’editor espressioni, immetti l’espressione per recuperare gli indirizzi e-mail degli abbonati. [Ulteriori informazioni](expression/expressionadvanced.md).

      Questo esempio mostra un’espressione che include riferimenti ai campi mappa:

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      In questo esempio vengono utilizzate le seguenti funzioni:

      | Funzione | Descrizione | Esempio |
      | --- | --- | --- |
      | `entry` | Fa riferimento a un elemento mappa in base allo spazio dei nomi selezionato | Fai riferimento a un elenco di iscrizioni specifico |
      | `firstEntryKey` | Recupera la prima chiave di ingresso di una mappa | Recupera il primo indirizzo e-mail degli abbonati |

      In questo esempio, l&#39;elenco iscrizioni è denominato `daily-email`. Gli indirizzi di posta elettronica sono definiti come chiavi nella mappa `subscribers`, collegata alla mappa dell&#39;elenco iscrizioni.

      Ulteriori informazioni su [riferimenti ai campi](expression/field-references.md) nelle espressioni.

      ![Configurazione e-mail con contenuti personalizzati per gli abbonati](assets/message-to-subscribers-uc-2.png)

   1. Nella finestra di dialogo **[!UICONTROL Aggiungi espressione]** fare clic su **[!UICONTROL Ok]**.

>[!CAUTION]
>
>La sostituzione dell’indirizzo e-mail deve essere utilizzata solo per casi d’uso specifici. Nella maggior parte dei casi, non è necessario modificare l’indirizzo e-mail perché il valore definito come indirizzo principale nei **[!UICONTROL campi di esecuzione]** è quello che deve essere utilizzato. [Ulteriori informazioni](../configuration/primary-email-addresses.md)

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina viene illustrato come creare un percorso che invia un messaggio e-mail agli abbonati di un elenco ignorando il parametro dell&#39;indirizzo e-mail predefinito tramite un&#39;espressione che legge gli indirizzi degli abbonati da un campo della mappa del consenso.

**Intenti:**

* Creare un percorso che esegue il targeting degli abbonati di un elenco specifico utilizzando un’attività Read audience
* Sostituire l’indirizzo e-mail predefinito in un’attività di azione E-mail utilizzando l’editor di espressioni
* Utilizza le funzioni `entry` e `firstEntryKey` per recuperare gli indirizzi e-mail degli abbonati da una mappa del consenso
* Per accedere ai dati dell’elenco di iscrizioni, fai riferimento al gruppo di campi Dettagli consenso e preferenze

**Glossario:**

* **Sostituzione indirizzo e-mail (sostituzione parametro)**: impostazione di attività di posta elettronica di percorso che sostituisce l&#39;indirizzo e-mail del profilo predefinito con un&#39;espressione personalizzata, utilizzata per casi speciali come il targeting dell&#39;elenco iscrizioni. *(specifico per prodotto)*
* **Gruppo di campi Dettagli consenso e preferenze**: un gruppo di campi dello schema di Adobe Experience Platform che contiene i dati dell&#39;abbonamento e del consenso, inclusa la mappa `subscriptions` utilizzata per memorizzare gli indirizzi e-mail dei sottoscrittori. *(specifico per prodotto)*
* Funzione **`entry`**: funzione di espressione che fa riferimento a un elemento mappa in base alla chiave dello spazio dei nomi, utilizzata in questo caso per fare riferimento a un elenco di sottoscrizioni specifico (ad esempio, `daily-email`). *(specifico per prodotto)*
* Funzione **`firstEntryKey`**: funzione di espressione che recupera la prima chiave di una mappa, utilizzata qui per recuperare il primo indirizzo e-mail dalla mappa degli abbonati di un elenco di iscrizioni. *(specifico per prodotto)*

**Guardrail:**

* La sostituzione dell’indirizzo e-mail deve essere utilizzata solo per casi d’uso specifici, ad esempio il targeting dell’elenco di iscrizioni; nella maggior parte dei casi deve essere utilizzato l’indirizzo principale definito nei campi di esecuzione
* Affinché questo caso d’uso funzioni, il gruppo di campi Consenso e Dettagli preferenze deve essere presente nello schema
* Il nome dell&#39;elenco di sottoscrizioni utilizzato nell&#39;espressione (ad esempio, `daily-email`) deve corrispondere esattamente al nome configurato nei dati

**Terminologia:**

* Nome canonico: sostituzione indirizzo e-mail — Acronimo: none — varianti: sostituzione parametro, sostituzione parametro e-mail
* Sinonimi: &quot;elenco iscrizioni&quot; = &quot;elenco iscrizioni&quot;
* Non confondere: &quot;email address override&quot; ≠ &quot;primary email address&quot; — L&#39;indirizzo e-mail principale è l&#39;indirizzo predefinito utilizzato in tutti i percorsi; l&#39;override è un&#39;espressione per attività utilizzata solo per casi speciali come l&#39;invio di elenchi di abbonamenti

**Domande frequenti:**

* **D: come posso inviare un&#39;e-mail agli abbonati di un elenco di iscrizioni anziché agli indirizzi e-mail del profilo?** — Abilitare la sostituzione del parametro nel campo Address dell&#39;attività Email e immettere un&#39;espressione utilizzando le funzioni `entry` e `firstEntryKey` per recuperare gli indirizzi dalla mappa degli abbonati dell&#39;elenco di abbonamenti di destinazione.
* **D: quale gruppo di campi è necessario per questo caso d&#39;uso?** — Il gruppo di campi Dettagli consenso e preferenze di Adobe Experience Platform, che contiene la struttura di mappe `subscriptions` utilizzata per memorizzare gli indirizzi e-mail degli abbonati.
* **Q: è necessario utilizzare sempre la sostituzione dell&#39;indirizzo di posta elettronica quando si esegue il targeting degli abbonati?** — No; la sostituzione dell&#39;indirizzo e-mail è solo per casi d&#39;uso specifici. Nella maggior parte dei percorsi, deve essere utilizzato l’indirizzo principale definito nei campi di esecuzione.
* **D: quali operazioni esegue la funzione `firstEntryKey` in questo contesto?** : recupera la prima chiave dell&#39;indirizzo e-mail dalla mappa `subscribers` associata a un elenco di iscrizioni specifico, consentendo al percorso di indirizzare i singoli abbonati.

+++
