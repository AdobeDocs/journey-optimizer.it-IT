---
title: Introduzione a Decisioning
description: Ulteriori informazioni su Decisioning
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilità limitata"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 19%

---

# Introduzione a Decisioning {#get-started-experience-decisioning}

>[!AVAILABILITY]
>
>Decisioning è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.
>
>Adobe Per il momento, la funzionalità non è disponibile per i clienti che hanno acquistato il componente aggiuntivo **Healthcare Shield** e **Privacy and Security Shield**.

## Che cos’è Decisioning {#about}

Decisioning semplifica la personalizzazione offrendo un catalogo centralizzato di offerte di marketing note come &quot;elementi decisionali&quot; e un motore decisionale sofisticato. Questo motore sfrutta le regole e i criteri di classificazione per selezionare e presentare a ogni persona gli elementi decisionali più rilevanti.

Questi elementi decisionali vengono integrati direttamente in un&#39;ampia gamma di superfici in entrata tramite il [nuovo canale di esperienza basato su codice](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/code-based-experience/get-started-code-based), ora accessibile nelle campagne Journey Optimizer. I criteri decisionali sono disponibili per l’utilizzo solo nelle campagne di esperienza basate su codice.


## Decisioning dei passaggi chiave {#steps}

I passaggi principali per lavorare con Decisioning sono i seguenti:

1. **Assegna le autorizzazioni appropriate**. Decisioning è disponibile solo per gli utenti con accesso a un **[!UICONTROL ruolo]** correlato a Decisioning, ad esempio i responsabili delle decisioni. Se non riesci ad accedere a Decisioning, devi estendere le autorizzazioni.

   +++Scopri come assegnare il ruolo Responsabili delle decisioni

   1. Per assegnare un ruolo a un utente nel prodotto [!DNL Permissions], passare alla scheda **[!UICONTROL Ruoli]** e selezionare Responsabili delle decisioni.

      ![](assets/decision_permission_1.png)

   1. Dalla sezione **[!UICONTROL Utenti]**, fai clic su **[!UICONTROL Aggiungi utente]**.

      ![](assets/decision_permission_2.png)

   1. Digita il nome o l’indirizzo e-mail dell’utente o selezionalo dall’elenco e fai clic su **[!UICONTROL Salva]**.

      Se l’utente non è stato creato in precedenza, consulta la [documentazione Aggiungere utenti](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/ui/users).

      ![](assets/decision_permission_3.png)

   L’utente dovrebbe quindi ricevere un messaggio e-mail di reindirizzamento all’istanza.

+++

1. **Configurare gli attributi personalizzati**: personalizzare il catalogo degli elementi in base alle proprie esigenze impostando gli attributi personalizzati nello schema del catalogo.

1. **Crea elementi decisionali** da mostrare al pubblico di destinazione.

1. **Organizza con le raccolte**: utilizza le raccolte per categorizzare gli elementi decisionali in base a regole basate su attributi. Incorpora le raccolte nelle strategie di selezione per determinare quale raccolta di elementi decisionali deve essere considerata.

1. **Crea regole di decisione**: le regole di decisione vengono utilizzate negli elementi di decisione e/o nelle strategie di selezione per determinare a chi può essere visualizzato un elemento di decisione.

1. **Implementare metodi di classificazione**: creare metodi di classificazione e applicarli nelle strategie di decisione per determinare l&#39;ordine di priorità per la selezione degli elementi di decisione.

1. **Creare strategie di selezione**: creare strategie di selezione che sfruttano raccolte, regole di decisione e metodi di classificazione per identificare gli elementi di decisione adatti alla visualizzazione nei profili.

1. **Incorpora un criterio di decisione nella campagna basata su codice**: i criteri di decisione combinano più strategie di selezione per determinare gli elementi di decisione idonei da visualizzare al pubblico previsto.
