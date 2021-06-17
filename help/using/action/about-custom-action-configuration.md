---
solution: Journey Orchestration
title: Informazioni sulla configurazione delle azioni personalizzata
description: Scopri come configurare un’azione personalizzata
feature: Azioni
topic: Amministrazione
role: Administrator
level: Intermediate
source-git-commit: 265e15f3b56dfac7a5c35bf6817a5ff2da1d744a
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 9%

---

# Configurare un’azione {#configure-an-action}

Se utilizzi un sistema di terze parti per l’invio di messaggi o se desideri che i percorsi inviino chiamate API a un sistema di terze parti, puoi configurare la relativa connessione ai percorsi in questo punto. L’azione personalizzata definita dagli utenti tecnici sarà quindi disponibile nella palette a sinistra del percorso, nella categoria **[!UICONTROL Action]** (consulta [questa pagina](../building-journeys/about-journey-activities.md#action-activities). Di seguito sono riportati alcuni esempi di sistemi a cui è possibile connettersi con azioni personalizzate: Epsilon, Facebook, Adobe.io, Firebase, ecc.
Le limitazioni sono elencate in [questa pagina](../building-journeys/limitations.md).

Di seguito sono riportati i passaggi principali necessari per configurare un’azione personalizzata:

1. Nella sezione del menu AMMINISTRAZIONE, selezionare **[!UICONTROL Configurations]**. Nella sezione **[!UICONTROL Actions]**, fai clic su **[!UICONTROL Manage]**. Fai clic su **[!UICONTROL Create Action]** per creare una nuova azione. Il riquadro di configurazione delle azioni si apre sul lato destro dello schermo.

   ![](../assets/custom2.png)

1. Immetti un nome per l’azione.

   >[!NOTE]
   >
   >Non utilizzare spazi o caratteri speciali. Non usare più di 30 caratteri.

1. Aggiungi una descrizione all’azione. Questo passaggio è facoltativo.
1. Il numero di percorsi che utilizzano questa azione viene visualizzato nel campo **[!UICONTROL Used in]** . Fai clic sul pulsante **[!UICONTROL View journeys]** per visualizzare l’elenco dei percorsi che utilizzano questa azione.
1. Definisci i diversi parametri **[!UICONTROL URL Configuration]**. Consulta [questa pagina](../action/about-custom-action-configuration.md#url-configuration).
1. Configura la sezione **[!UICONTROL Authentication]** . Questa configurazione è la stessa delle origini dati.  Vedi [questa sezione](../datasource/external-data-sources.md#section_wjp_nl5_nhb).
1. Definisci il **[!UICONTROL Action parameters]**. Consulta [questa pagina](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Fai clic su **[!UICONTROL Save]**.

   L’azione personalizzata è ora configurata ed è pronta per essere utilizzata nei percorsi. Consulta [questa pagina](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Quando un&#39;azione personalizzata viene utilizzata in un percorso, la maggior parte dei parametri è di sola lettura. È possibile modificare solo i campi **[!UICONTROL Name]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** e la sezione **[!UICONTROL Authentication]**.

## Configurazione URL {#url-configuration}

Quando configuri un’azione personalizzata, devi definire i seguenti parametri **[!UICONTROL URL Configuration]**:

![](../assets/journeyurlconfiguration.png)

1. Aggiungi il **[!UICONTROL URL]** del servizio esterno.

   >[!NOTE]
   >
   >Per motivi di sicurezza, è consigliabile utilizzare HTTPS. Non consentiamo l’uso di indirizzi di Adobe che non sono pubblici e l’uso di indirizzi IP.

1. Seleziona la chiamata **[!UICONTROL Method]**: può essere **[!UICONTROL POST]** o **[!UICONTROL PUT]**.
1. Nella sezione **[!UICONTROL Headers]**, fai clic su **[!UICONTROL Add a header field]** per definire una nuova coppia chiave/valore. Corrispondono alle intestazioni HTTP della richiesta effettuata al servizio esterno. Per eliminare le coppie chiave/valore, posiziona il cursore sul campo intestazione e fai clic sull’icona **[!UICONTROL Delete]** .

   **[!UICONTROL Content-Type]** e  **[!UICONTROL Charset]** sono impostati per impostazione predefinita e non possono essere eliminati o ignorati.

   >[!NOTE]
   >
   >Le intestazioni vengono convalidate in base alle seguenti [regole di analisi](https://tools.ietf.org/html/rfc7230#section-3.2.4).

## Definisci i parametri delle azioni {#define-the-message-parameters}

![](../assets/messageparameterssection.png)

Nella sezione **[!UICONTROL Action parameters]** , incolla un esempio del payload JSON da inviare al servizio esterno.

![](../assets/customactionpayloadmessage.png)

>[!NOTE]
>
>I nomi di campo nel payload non possono contenere un &quot;.&quot; aggiuntivo.

Puoi definire il tipo di parametro (ad esempio: (stringa, numero intero, ecc.).

Puoi anche scegliere se specificare se un parametro è una costante o una variabile:

* Costante significa che il valore del parametro è definito nel riquadro di configurazione dell&#39;azione da un utente tecnico. Il valore sarà sempre lo stesso in tutti i percorsi. Non varia e l’addetto al marketing non lo vedrà quando utilizza l’azione personalizzata nel percorso. Potrebbe trattarsi, ad esempio, di un ID previsto dal sistema di terze parti. In tal caso, il valore passato è rappresentato dal campo a destra della costante/variabile di attivazione/disattivazione.
* Variabile indica che il valore del parametro varia. L’addetto al marketing che utilizza questa azione personalizzata in un percorso sarà libero di trasmettere il valore desiderato o di specificare dove recuperare il valore per questo parametro (ad esempio dall’evento, da Adobe Experience Platform, ecc.). In tal caso, il campo a destra della costante/variabile di attivazione è l’etichetta che l’addetto al marketing vedrà nel percorso per denominare questo parametro.

![](../assets/customactionpayloadmessage2.png)
