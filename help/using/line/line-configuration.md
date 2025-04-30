---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il canale LINE
description: Scopri come configurare il tuo ambiente per inviare messaggi LINE con Journey Optimizer
feature: Line, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: 8714ac6b2fd76ec859c358535fa322f0ac333a82
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 4%

---

# Configurare il canale LINE in Journey Optimizer {#line-configuration}

1. Accedi al menu **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni generali]** > **[!UICONTROL Configurazioni canale]**, quindi fai clic su **[!UICONTROL Crea configurazione canale]**.

   ![](assets/line-config-1.png)

1. Immetti un nome e una descrizione (facoltativa) per la configurazione, quindi seleziona il canale da configurare.

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare i caratteri trattino basso `_`, punto `.` e trattino `-`.

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base alla configurazione, è possibile selezionare **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni sul controllo degli accessi a livello di oggetto](../administration/object-based-access.md).

1. Seleziona il canale **LINE**.

   ![](assets/line-config-2.png)

1. Seleziona **[!UICONTROL Azione di marketing]** per associare i criteri di consenso ai messaggi utilizzando questa configurazione. Tutti i criteri di consenso associati all’azione di marketing vengono utilizzati per rispettare le preferenze dei clienti. [Ulteriori informazioni](../action/consent.md#surface-marketing-actions)

1. Seleziona il tipo di messaggio per la configurazione:

   * **Marketing**: per messaggi promozionali, ad esempio promozioni settimanali per un negozio al dettaglio. Questi messaggi richiedono il consenso dell’utente e devono essere conformi alla politica di LINE relativa alle opzioni di consenso dell’utente.
   * **Transazionale**: per messaggi non commerciali, ad esempio conferme di ordini, notifiche di reimpostazione della password o aggiornamenti di consegna. Questi messaggi possono essere inviati anche agli utenti che hanno annullato l’abbonamento alle comunicazioni di marketing, ma sono strettamente limitati a contesti transazionali specifici.

1. Seleziona le **[!UICONTROL impostazioni canale]**.

   Rivolgiti al tuo rappresentante Adobe per configurare le **[!UICONTROL impostazioni del canale]**.

   ![](assets/line-config-2.png)

1. Seleziona il tuo **[!UICONTROL ID utente LINE]** da mappare. Questo è l’identificatore utilizzato per collegare i messaggi a singoli utenti all’interno del tuo canale LINE.

1. Digita il **[!UICONTROL Nome mittente]**, ad esempio il nome del tuo marchio.

1. Invia le modifiche.

Ora puoi selezionare la configurazione durante la creazione del messaggio LINE.
