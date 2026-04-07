---
title: Configurazione casella in entrata
description: Configurazione del canale casella in entrata
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
source-git-commit: d84cc0f4d9226876e55e37409a685550fe0c9050
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 4%

---

# Configura casella in entrata {#inbox-configuration}

Prima di poter fornire esperienze con schede di contenuto tramite la Casella in entrata, è necessario definire una configurazione di canale **Casella in entrata** in **[!UICONTROL Configurazioni canale]**. Tale configurazione vincola l’area al consenso, alle etichette di accesso facoltative e a dove viene visualizzata l’esperienza sul web o nell’app iOS o Android. Per creare una configurazione, segui i passaggi seguenti:

1. Accedi al menu **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni generali]** > **[!UICONTROL Configurazioni canale]**, quindi fai clic su **[!UICONTROL Crea configurazione canale]**.

   ![](assets/inbox-configuration-1.png)

1. Immetti un nome e una descrizione (facoltativa) per la configurazione.

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare i caratteri trattino basso `_`, punto `.` e trattino `-`.

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base alla configurazione, è possibile selezionare **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni sul controllo degli accessi a livello di oggetto](../administration/object-based-access.md).

1. Seleziona il canale **[!UICONTROL Posta in arrivo]**.

   ![](assets/inbox-configuration-2.png)

1. Seleziona **[!UICONTROL Azione di marketing]** per associare i criteri di consenso ai messaggi utilizzando questa configurazione. Tutti i criteri di consenso associati all’azione di marketing vengono utilizzati per rispettare le preferenze dei clienti. [Ulteriori informazioni](../action/consent.md#surface-marketing-actions)

1. Seleziona la piattaforma per la quale verrà applicata l’esperienza Casella in entrata.

   ![](assets/inbox-configuration-3.png)

1. Per il Web:

   * In **[!UICONTROL URL pagina]**, immettere o selezionare l&#39;URL della pagina in cui deve essere visualizzata la casella in entrata. Utilizzalo quando l&#39;esperienza è limitata a una pagina.

   * In **[!UICONTROL Posizione a pagina]**, definisci il posizionamento nella pagina, ad esempio l&#39;area o l&#39;identificatore utilizzato dal sito per la superficie della casella in entrata. [Ulteriori informazioni](../web/web-configuration.md)

     ![](assets/inbox-configuration-4.png)

1. Per iOS e Android:

   * In **[!UICONTROL ID app]**, immetti o seleziona l&#39;identificatore dell&#39;app in modo che la configurazione venga applicata alla build corretta di iOS o Android.

   * In **[!UICONTROL Posizione o percorso all&#39;interno dell&#39;app]**, specificare la schermata, il percorso o il contenitore in cui gli utenti devono aprire la cartella Posta in arrivo.

1. Invia le modifiche.

Ora puoi selezionare la configurazione durante la creazione della tua esperienza Casella in entrata.

➡️ [Segui i passaggi descritti in questa pagina](inbox-create.md)
