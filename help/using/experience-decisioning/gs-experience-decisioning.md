---
title: Inizia a usare la funzione Decisioni
description: Ulteriori informazioni sulle funzioni decisionali
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 22%

---

# Inizia a usare la funzione Decisioni {#get-started-experience-decisioning}

>[!CONTEXTUALHELP]
>id="ajo_email_enable_experience_decisioning"
>title="Cos’è la funzione Decisioni?"
>abstract="La funzione Decisioni è un nuovo strumento che, insieme alla gestione delle decisioni, consente di scegliere gli elementi migliori dal motore decisionale e di consegnarli a ogni persona. Per utilizzarla, è necessaria una configurazione aggiuntiva."

## Che cos’è Decisioning {#about}

La funzione Decisioni semplifica la personalizzazione proponendo un catalogo centralizzato di offerte di marketing note come “elementi decisionali” e un motore decisionale sofisticato. Questo motore sfrutta le regole e i criteri di classificazione per selezionare e presentare a ogni singolo utente gli elementi decisionali più rilevanti.

Questi elementi decisionali vengono integrati direttamente in un&#39;ampia gamma di superfici in entrata tramite il [nuovo canale di esperienza basato su codice](../code-based/get-started-code-based.md), accessibile nelle campagne Journey Optimizer.

>[!IMPORTANT]
>
>I criteri decisionali sono disponibili per l’utilizzo solo nelle campagne e-mail e nelle esperienze basate su codice.

➡️ Un caso d&#39;uso end-to-end che mostra come creare decisioni e utilizzarle in esperimenti di contenuto con il canale di esperienza basato sul codice è presentato in [questa sezione](experience-decisioning-uc.md).

## Decisioning dei passaggi chiave {#steps}

I passaggi principali per lavorare con Decisioning sono i seguenti:

1. **Assegna le autorizzazioni appropriate**. Decisioning è disponibile solo per gli utenti con accesso a un **[!UICONTROL ruolo]** correlato a Decisioning, ad esempio i responsabili delle decisioni. Se non riesci ad accedere a Decisioning, devi estendere le autorizzazioni.

   +++Scopri come assegnare il ruolo Responsabili delle decisioni

   1. Per assegnare un ruolo a un utente nel prodotto [!DNL Permissions], passare alla scheda **[!UICONTROL Ruoli]** e selezionare Responsabili delle decisioni.

      ![](assets/decision_permission_1.png)

   1. Dalla sezione **[!UICONTROL Utenti]**, fai clic su **[!UICONTROL Aggiungi utente]**.

      ![](assets/decision_permission_2.png)

   1. Digita il nome o l&#39;indirizzo e-mail dell&#39;utente o selezionalo dall&#39;elenco e fai clic su **[!UICONTROL Salva]**.

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

1. **Crea un criterio di decisione e incorporalo nel tuo percorso/campagna basata su codice o e-mail**: i criteri di decisione combinano più strategie di selezione per determinare gli elementi di decisione idonei da visualizzare al pubblico previsto.

   ➡️ [Scopri come utilizzare i criteri di decisione](create-decision.md)
➡️ Per consegnare correttamente l&#39;offerta tramite il canale di esperienza basato su codice, segui i passaggi di implementazione in [questa sezione](../code-based/code-based-implementation-samples.md).

