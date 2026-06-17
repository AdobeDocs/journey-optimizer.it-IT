---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il canale delle attività live
description: Scopri come configurare il tuo ambiente per inviare attività live con Journey Optimizer
feature: Channel Configuration
role: Admin
level: Intermediate
exl-id: db85a563-9630-4d87-bf10-9f2515fe8a45
TQID: https://experienceleague.adobe.com/LThNKcpBCCkin2G-y4n-tty4bcGLxMA4ObiodBrpBwY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: e30b0a1a-b594-47b8-af94-1e3a2be6df11id: c96d2aa5-76a2-443d-8d23-5de95577c909id: ed2fba79-65cb-4680-96d2-2ad5d851714did: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0977b7c36d8556d4aaed43f4b94abb4ccacd2305
workflow-type: tm+mt
source-wordcount: 557
ht-degree: 1%

---

# Introduzione alla configurazione delle attività live {#mobile-live-config}

>[!BEGINSHADEBOX]

**In questa pagina:** configura le tue credenziali push e la configurazione del canale attività live in modo da poter autorizzare Adobe Journey Optimizer a distribuire aggiornamenti in tempo reale alla tua app iOS.

>[!ENDSHADEBOX]

Prima di inviare attività live, devi configurare l’ambiente Adobe Journey Optimizer. Per eseguire questa operazione:

## Passaggio 1: aggiungere le credenziali push dell’app in Journey Optimizer (facoltativo){#push-credentials-launch}

La registrazione delle credenziali push dell’app mobile è necessaria per autorizzare Adobe a inviare notifiche push per tuo conto.

Il passaggio 1 è facoltativo se le credenziali push sono già state configurate, in quanto possono essere riutilizzate per la configurazione del canale attività live. Se non è stata definita alcuna credenziale, devi creare nuove credenziali push per l’app. Consulta i passaggi descritti di seguito:

1. Accedi al menu **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni push]** > **[!UICONTROL Credenziali push]**.

1. Fare clic su **[!UICONTROL Crea credenziali push]**.

   ![](assets/credential-1.png)

1. Dal menu a discesa **[!UICONTROL Platform]**, seleziona il sistema operativo:

1. Immetti l&#39;app mobile **[!UICONTROL ID app]**.

   ![](assets/credential-2.png)

1. Abilita l&#39;opzione **[!UICONTROL Applica a tutte le sandbox]** per rendere queste credenziali push disponibili in tutte le sandbox. Se una sandbox specifica ha le proprie credenziali per la stessa coppia Platform e App ID, queste avranno la precedenza.

1. Attivato il pulsante **[!UICONTROL Immetti manualmente le credenziali push]** per aggiungere le tue credenziali.

1. Trascina e rilascia il file .p8 Apple Push Notification Authentication Key. Questa chiave può essere acquisita dalla pagina **Certificati**, **Identificatori** e **Profili**.

1. Fornisci l&#39;**ID chiave**. Si tratta di una stringa di 10 caratteri assegnata durante la creazione del tasto di autenticazione p8. È disponibile nella scheda **Chiavi** in **Certificati**, **Identificatori** e **Profili** pagina.

1. Fornisci **ID team**. Si tratta di un valore stringa che si trova nella scheda Appartenenza.

1. Fai clic su **[!UICONTROL Invia]** per creare la configurazione dell&#39;app.

## Passaggio 2: creare la configurazione dell’attività live {#config-live-activity}

1. Nella barra a sinistra, passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** e seleziona **[!UICONTROL Impostazioni generali]** > **[!UICONTROL Configurazioni canale]**. Fare clic sul pulsante **[!UICONTROL Crea configurazione canale]**.

   ![](assets/config-1.png)

1. Immetti un nome e una descrizione (facoltativa) per la configurazione, quindi seleziona il canale dell’attività Live.

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare i caratteri trattino basso `_`, punto `.` e trattino `-`.

1. Seleziona **[!DNL Live activity]** come tuo canale.

   ![](assets/config-2.png)

1. Seleziona **[!UICONTROL Azioni di marketing]** per associare i criteri di consenso ai messaggi utilizzando questa configurazione. Tutti i criteri di consenso associati all’azione di marketing vengono utilizzati per rispettare le preferenze dei clienti. Ulteriori informazioni

1. Scegli iOS come **[!UICONTROL piattaforma]**.

1. Seleziona dall&#39;elenco a discesa lo stesso **[!UICONTROL ID app]** come per le [credenziali push](#push-credentials-launch) configurate in precedenza o scegline uno esistente.

   ![](assets/config-3.png)

1. Una volta configurati tutti i parametri, fai clic su **[!UICONTROL Invia]** per confermare. Puoi anche salvare la configurazione del canale come bozza e riprenderla in un secondo momento.

1. Una volta creata, la configurazione del canale viene visualizzata nell&#39;elenco con lo stato **[!UICONTROL Elaborazione]**.

   >[!NOTE]
   >
   >Se i controlli non hanno esito positivo, ulteriori informazioni sui possibili motivi di errore in [questa sezione](../configuration/channel-surfaces.md).

1. Una volta completati i controlli, la configurazione del canale ottiene lo stato **[!UICONTROL Attivo]**. È pronto per essere utilizzato per inviare messaggi.

Ora puoi avviare l’integrazione con Adobe Experience Platform Mobile SDK per abilitare gli aggiornamenti dinamici in tempo reale sullo schermo Bloccato e su Dynamic Island.

➡️ [Ulteriori informazioni sull&#39;integrazione di Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)

>[!TIP]
>
>Se riscontri problemi con la configurazione o la consegna di attività Live, consulta [Risoluzione dei problemi relativi alle attività Live](troubleshoot-mobile-live.md) per i passaggi di debug.