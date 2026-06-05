---
title: Introduzione alla funzione Decisioni
description: Ulteriori informazioni sulle funzioni decisionali
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/z-9FSXpQNMyy0KcGaLWgDYHqAx-BWhIEJYAq4wVqmv4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: 1b4e12b9433a819a3be34c4f01c489af1d6091ed
workflow-type: tm+mt
source-wordcount: 751
ht-degree: 22%

---

# Introduzione alla funzione Decisioni {#get-started-experience-decisioning}

>[!CONTEXTUALHELP]
>id="ajo_email_enable_experience_decisioning"
>title="Cos’è la funzione Decisioni?"
>abstract="La funzione Decisioni è un nuovo strumento che, insieme alla gestione delle decisioni, consente di scegliere gli elementi migliori dal motore decisionale e di consegnarli a ogni persona. Per utilizzarla, è necessaria una configurazione aggiuntiva."

## Che cos’è Decisioning {#about}

La funzione Decisioni semplifica la personalizzazione proponendo un catalogo centralizzato di offerte di marketing note come “elementi decisionali” e un motore decisionale sofisticato. Questo motore sfrutta le regole e i criteri di classificazione per selezionare e presentare a ogni singolo utente gli elementi decisionali più rilevanti.

Questi elementi decisionali vengono integrati perfettamente nei messaggi e nelle esperienze su [!DNL Adobe Journey Optimizer] canali: [esperienza basata su codice](../code-based/get-started-code-based.md), e-mail, SMS, notifiche push e [direct mailing](batch-decisioning-direct-mail.md) per le decisioni in batch e le esportazioni di direct mailing personalizzate. Il supporto di Experience Decisioning per la direct mailing è una nuova funzionalità; in precedenza, il motore Decisioning non era disponibile per i file di estrazione della direct mailing.

>[!IMPORTANT]
>
>I criteri delle decisioni sono disponibili per tutti i clienti per i canali **Esperienza basata su codice**, **E-mail**, **Notifica push**, **SMS** e **Direct mail**.

➡️ [Scopri questa funzione nel video](#video)

➡️ Un caso d&#39;uso end-to-end che mostra come creare decisioni e utilizzarle in esperimenti di contenuto con il canale di esperienza basato sul codice è presentato in [questa sezione](experience-decisioning-uc.md).

## Decisioning dei passaggi chiave {#steps}

I passaggi principali per lavorare con Decisioning sono i seguenti:

1. **Assegna le autorizzazioni appropriate**. Decisioning è disponibile solo per gli utenti con accesso a un **[!UICONTROL ruolo]** correlato a Decisioning, ad esempio i responsabili delle decisioni. Se non riesci ad accedere a Decisioning, devi estendere le autorizzazioni.

   +++Scopri come assegnare il ruolo Responsabili delle decisioni

   1. Per assegnare un ruolo a un utente nel prodotto [!DNL Permissions], passare alla scheda **[!UICONTROL Ruoli]** e selezionare Responsabili delle decisioni.

      ![](assets/decision_permission_1.png)

   1. Dalla scheda **[!UICONTROL Utenti]**, fai clic su **[!UICONTROL Aggiungi utente]**.

      ![](assets/decision_permission_2.png)

   1. Digita il nome o l’indirizzo e-mail dell’utente o selezionalo dall’elenco e fai clic su **[!UICONTROL Salva]**.

      Se l’utente non è stato creato in precedenza, consulta la [documentazione Aggiungere utenti](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   L’utente dovrebbe quindi ricevere un messaggio e-mail di reindirizzamento all’istanza.

   +++

1. **Configurare gli attributi personalizzati**: personalizzare il catalogo degli elementi in base alle proprie esigenze impostando gli attributi personalizzati nello schema del catalogo.

   ➡️ [Scopri come configurare il catalogo elementi](catalogs.md)

1. **Crea elementi decisionali** da mostrare al pubblico di destinazione.

   ➡️ [Scopri come creare elementi decisionali](items.md) nell&#39;interfaccia utente (e nella [documentazione API](api-reference/decisions-items/create.md))

1. **Organizza con le raccolte**: utilizza le raccolte per categorizzare gli elementi decisionali in base a regole basate su attributi. Incorpora le raccolte nelle strategie di selezione per determinare quale raccolta di elementi decisionali deve essere considerata.

   ➡️ [Scopri come gestire le raccolte di elementi](collections.md) nell&#39;interfaccia utente (e nella [documentazione API](api-reference/items-collections/create.md))

1. **Crea regole di decisione**: le regole di decisione vengono utilizzate negli elementi di decisione e/o nelle strategie di selezione per determinare a chi può essere visualizzato un elemento di decisione.

   ➡️ [Scopri come creare regole di decisione](rules.md)

1. **Implementare i metodi di classificazione**: creare metodi di classificazione e applicarli nelle strategie di selezione per determinare l&#39;ordine di priorità per la selezione degli elementi decisionali.

   ➡️ [Scopri come creare metodi di classificazione](ranking/ranking.md)

1. **Creare strategie di selezione**: creare strategie di selezione che sfruttano raccolte, regole di decisione e metodi di classificazione per identificare gli elementi di decisione adatti alla visualizzazione nei profili.

   ➡️ [Scopri come creare strategie di selezione nell&#39;interfaccia utente](selection-strategies.md) nell&#39;interfaccia utente (e nella [documentazione API](api-reference/selection-strategies/create.md))

1. **Creare un criterio di decisione e incorporarlo nel percorso o nella campagna** (esperienza basata su codice, e-mail, SMS o push): i criteri di decisione combinano più strategie di selezione per determinare gli elementi di decisione idonei da visualizzare al pubblico previsto.

   ➡️ [Scopri come utilizzare i criteri di decisione](create-decision.md)
➡️ Per consegnare correttamente l&#39;offerta tramite il canale di esperienza basato su codice, segui i passaggi di implementazione in [questa sezione](../code-based/code-based-implementation-samples.md).

## Processo decisionale {#process}

Il grafico seguente riepiloga il processo decisionale end-to-end, dalla gestione degli elementi decisionali e la configurazione delle strategie di selezione, fino all’incorporamento dei criteri decisionali in un percorso di esperienza o una campagna basati sul codice.

![](assets/decisioning-process.png){zoomable="yes"}

## Risorse aggiuntive {#additional-resources}

* **[Crea elementi decisionali](items.md)** - Scopri come creare e gestire elementi decisionali tra cui offerte, varianti di contenuto ed esperienze.
* **[Configurare i cataloghi delle decisioni](catalogs.md)** - Informazioni su come organizzare gli elementi decisionali in cataloghi per una migliore gestione.
* **[Definire le strategie di selezione](selection-strategies.md)** - Scopri come creare strategie di selezione con regole di idoneità e metodi di classificazione.
* **[Creare criteri di decisione](create-decision-policy.md)** - Scopri come creare criteri di decisione che combinano strategie e vincoli.
* **[Modelli di classificazione e IA](ranking/ranking.md)** - Formule di classificazione principali e modelli di IA per il decisioning personalizzato.
* **[Migra da Gestione decisioni](migrate-to-decisioning.md)** - Comprendi i vantaggi della migrazione a Decisioning e utilizza le API degli strumenti di migrazione.
* **[Guardrail di decisioning](decisioning-guardrails.md)**: rivedi limitazioni importanti e best practice per l&#39;implementazione del decisioning.
* **[Tutorial su Decisioning](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/decision-capabilities/decisioning/introduction-to-decisioning){target="_blank"}**: esplora esercitazioni video dettagliate sulle funzioni decisionali e sulle best practice.

## Video introduttivo {#video}

Scopri le funzionalità Decisioning di Adobe Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/3451101?quality=12)
