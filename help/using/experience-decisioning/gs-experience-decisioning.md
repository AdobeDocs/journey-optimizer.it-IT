---
title: Introduzione a Experience Decisioning
description: Ulteriori informazioni su Experience Decisioning
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilità limitata"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 19%

---

# Introduzione a Experience Decisioning {#get-started-experience-decisioning}

>[!AVAILABILITY]
>
>La funzione Decisioni per le esperienze è attualmente disponibile solo per alcune organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.
>
>Per il momento, la funzione non è disponibile per i clienti che hanno acquistato l’Adobe **Healthcare Shield** e **Privacy e sicurezza** offerte aggiuntive.

## Cos’è Experience Decisioning {#about}

La funzione Decisioni per le esperienze semplifica la personalizzazione proponendo un catalogo centralizzato di offerte di marketing note come “elementi decisionali” e un motore decisionale sofisticato. Questo motore sfrutta le regole e i criteri di classificazione per selezionare e presentare a ogni persona gli elementi decisionali più rilevanti.

Questi elementi decisionali vengono integrati direttamente in un’ampia gamma di superfici in entrata tramite il nuovo canale di esperienza basato su codice, ora accessibile nelle campagne Journey Optimizer. I criteri decisionali di Experience Decisioning sono disponibili solo per l’utilizzo in campagne di esperienza basate su codice.

## Passaggi chiave di Experience Decisioning {#steps}

I passaggi principali per lavorare con Experience Decisioning sono i seguenti:

1. **Assegnare le autorizzazioni appropriate**. Experience Decisioning è disponibile solo per gli utenti con accesso a un correlato a Experience Decisioning **[!UICONTROL ruolo]** come i responsabili delle decisioni. Se non riesci ad accedere ad Experience Decisioning, devi estendere le autorizzazioni.

   +++Scopri come assegnare il ruolo Responsabili delle decisioni

   1. Per assegnare un ruolo a un utente in [!DNL Permissions] prodotto, passare alla **[!UICONTROL Ruoli]** e selezionare Responsabili delle decisioni.

      ![](assets/decision_permission_1.png)

   1. Dalla sezione **[!UICONTROL Utenti]** , fare clic su **[!UICONTROL Aggiungi utente]**.

      ![](assets/decision_permission_2.png)

   1. Digita il nome o l’indirizzo e-mail dell’utente o selezionalo dall’elenco e fai clic su **[!UICONTROL Salva]**.

      Se l’utente non è stato creato in precedenza, consulta [Aggiungi documentazione utenti](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   L’utente dovrebbe quindi ricevere un messaggio e-mail di reindirizzamento all’istanza.

+++

1. **Configurare gli attributi personalizzati**: personalizza il catalogo articoli in base alle tue esigenze impostando attributi personalizzati nello schema del catalogo.

1. **Creare elementi decisionali** per mostrarlo al pubblico di destinazione.

1. **Organizzare con le raccolte**: utilizza le raccolte per categorizzare gli elementi decisionali in base a regole basate su attributi. Incorpora le raccolte nelle strategie di selezione per determinare quale raccolta di elementi decisionali deve essere considerata.

1. **Creare regole di decisione**: le regole di decisione vengono utilizzate negli elementi di decisione e/o nelle strategie di selezione per determinare a chi può essere visualizzato un elemento di decisione.

1. **Implementare metodi di classificazione**: crea metodi di classificazione e applicali all’interno di strategie decisionali per determinare l’ordine prioritario per la selezione degli elementi decisionali.

1. **Creare strategie di selezione**: crea strategie di selezione che sfruttano raccolte, regole di decisione e metodi di classificazione per identificare gli elementi di decisione adatti per la visualizzazione nei profili.

1. **Incorporare un criterio di decisione nella campagna basata su codice**: i criteri di decisione combinano più strategie di selezione per determinare gli elementi di decisione idonei da visualizzare al pubblico previsto.
