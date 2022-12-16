---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare i criteri di consenso
description: Scopri come utilizzare i criteri di consenso di Adobe Experience Platform
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 01ca4b3e-3778-4537-81e9-97ef92c9aa9e
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 35%

---

# Utilizzare i criteri di consenso {#consent-management}

Adobe Experience Platform consente di adottare e applicare facilmente i criteri di marketing per rispettare le preferenze di consenso dei clienti. I criteri di consenso sono definiti in Adobe Experience Platform. Fai riferimento a [questa documentazione](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=it#consent-policy).

In Journey Optimizer puoi applicare questi criteri di consenso alle azioni personalizzate. Ad esempio, puoi definire i criteri di consenso per escludere i clienti che non hanno acconsentito a ricevere comunicazioni e-mail, push o SMS.

>[!NOTE]
>
>Le politiche di consenso sono attualmente disponibili solo per le organizzazioni che hanno acquistato l&#39;offerta aggiuntiva Healthcare Shield.

In Journey Optimizer, il consenso è definito a diversi livelli:

* quando **configurazione di un’azione personalizzata**, puoi definire un canale e un’azione di marketing. Vedi questo [sezione](../action/consent.md#consent-custom-action).
* quando si aggiunge il **azione personalizzata in un percorso**, puoi definire un’azione di marketing aggiuntiva. Vedi questo [sezione](../action/consent.md#consent-journey).

## Note importanti {#important-notes}

In Journey Optimizer, il consenso può essere sfruttato nelle azioni personalizzate. Se desideri utilizzarlo con le funzionalità dei messaggi incorporati, devi utilizzare un’attività di condizione per filtrare i clienti nel percorso.

Con la gestione del consenso vengono analizzate due attività percorsi:

* Segmento di lettura: viene preso in considerazione il segmento recuperato.
* Azione personalizzata: la gestione del consenso tiene conto degli attributi utilizzati ([parametri azione](../action/about-custom-action-configuration.md#define-the-message-parameters)) e le azioni di marketing definite (azioni di marketing richieste e azioni di marketing aggiuntive).
* Gli attributi appartenti a un gruppo di campi che utilizzano lo schema di unione predefinito non sono supportati. Questi attributi risulteranno nascosti nell’interfaccia. È necessario creare un altro gruppo di campi utilizzando uno schema diverso.
* I criteri di consenso si applicano solo quando un’azione di marketing (obbligatoria o aggiuntiva) è impostata a livello di azione personalizzata.

Non vengono prese in considerazione tutte le altre attività utilizzate in un percorso. Se avvii il percorso con una qualifica Segmento, il segmento non viene preso in considerazione.

In un percorso, se un profilo viene escluso da un criterio di consenso in un’azione personalizzata, il messaggio non viene inviato a lui, ma lui continua il percorso. Il profilo non passa al percorso di timeout ed errore quando si utilizza una condizione .

Prima di aggiornare i criteri in un&#39;azione personalizzata posizionata in un percorso, assicurati che il percorso non presenti errori.

<!--
There are two types of latency regarding the use of consent policies:

* **User latency**: the delay from the time a profile changes a consent settings to the moment it is applied in Experience Platform. This can take up to 48h. 
* **Consent policy latency**: the delay from the time a consent policy is created or updated to the moment it is applied. This can take up to 6 hours
-->

## Configurazione dell’azione personalizzata {#consent-custom-action}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action_admin"
>title="Definire un’azione di marketing richiesta"
>abstract="L’Azione di marketing richiesta consente di definire l’azione di marketing correlata all’azione personalizzata. Ad esempio, se utilizzi tale azione personalizzata per inviare e-mail, puoi selezionare Targeting e-mail. Se utilizzato in un percorso, tutti i criteri di consenso associati a tale azione di marketing verranno recuperati e utilizzati. Impossibile modificare l&#39;elemento nell&#39;area di lavoro."

Durante la configurazione di un’azione personalizzata, è possibile utilizzare due campi per la gestione del consenso.

Il campo **Canale** consente di selezionare il canale correlato a questa azione personalizzata: **E-mail**, **SMS** oppure **Notifica push**. Il campo **Azione di marketing richiesta** verrà precompilato con l’azione di marketing predefinita per il canale selezionato. Se si seleziona **Altro**, non verrà definita alcuna azione di marketing per impostazione predefinita.

![](assets/consent1.png)

L’**Azione di marketing richiesta** consente di definire l’azione di marketing correlata all’azione personalizzata. Ad esempio, se utilizzi questa azione personalizzata per inviare e-mail, puoi selezionare **Targeting e-mail**. Se utilizzato in un percorso, tutti i criteri di consenso associati a tale azione di marketing verranno recuperati e utilizzati. È selezionata un’azione di marketing predefinita, ma puoi fare clic sulla freccia giù per selezionare dall’elenco le azioni di marketing disponibili.

![](assets/consent2.png)

Per alcuni tipi di comunicazioni importanti, ad esempio un messaggio transazionale inviato per reimpostare la password del cliente, potrebbe non essere necessario applicare un criterio di consenso. Seleziona **Nessuno** in **Azione di marketing necessaria** campo .

Gli altri passaggi per la configurazione di un’azione personalizzata sono descritti in [questa sezione](../action/about-custom-action-configuration.md#consent-management).

### Creazione di un percorso {#consent-journey}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action_canvas"
>title="Azione di marketing necessaria"
>abstract="Durante la creazione di un’azione di marketing personalizzata viene definita un’azione di marketing richiesta. Impossibile rimuovere o modificare l’azione di marketing richiesta."

>[!CONTEXTUALHELP]
>id="ajo_consent_additional_marketing_action_canvas"
>title="Azioni di marketing aggiuntive"
>abstract="Aggiungi un’altra azione di marketing oltre a quella richiesta. Verranno applicati i criteri di consenso relativi a entrambe le azioni di marketing."

>[!CONTEXTUALHELP]
>id="ajo_consent_refresh_policies_canvas"
>title="Visualizzare i criteri di consenso applicabili in fase di runtime"
>abstract="Le azioni di marketing introducono criteri di consenso che combinano parametri di azione e valori di consenso dei singoli profili per filtrare gli utenti. Per ottenere la definizione più recente di questi criteri, fai clic sul pulsante per aggiornarli."

Quando aggiungi l’azione personalizzata in un percorso, diverse opzioni ti consentono di gestire il consenso. Fai clic sul pulsante **Mostra campi di sola lettura** per visualizzare tutti i parametri.

Nella parte superiore dello schermo sono riportati il **Canale** e l’**Azione di marketing richiesta**, definiti durante la configurazione dell’azione personalizzata. Non è possibile modificare questi campi.

![](assets/consent4.png)

Puoi definire un’**Azione di marketing aggiuntiva** per impostare il tipo di azione personalizzata. Questo consente di definire lo scopo dell’azione personalizzata in questo percorso. Oltre all’azione di marketing richiesta, solitamente specifica per un canale, puoi definire un’azione di marketing aggiuntiva specifica per l’azione personalizzata in questo particolare percorso. Ad esempio: una comunicazione di allenamento, una newsletter, una comunicazione fitness, ecc. Verranno applicate sia l’azione di marketing richiesta che quella aggiuntiva.

![](assets/consent3.png)

Fai clic sul pulsante **Aggiorna criteri** , nella parte inferiore della schermata, per aggiornare e controllare l’elenco dei criteri presi in considerazione per questa azione personalizzata. Questo è solo a scopo informativo, durante la costruzione di un percorso. Con i percorsi live, i criteri di consenso vengono recuperati e aggiornati automaticamente ogni 6 ore.

![](assets/consent5.png)

<!--
The following data is taken into account for consent:

* marketing actions and additional marketing actions defined in the custom action
* action parameters defined in the custom action, see this [section](../action/about-custom-action-configuration.md#define-the-message-parameters) 
* attributes used as criteria in a segment when the journey starts with a Read segment, see this [section](../building-journeys/read-segment.md) 

>[!NOTE]
>
>Please note that there can be a latency when updating the list of policies applied, refer to this [this section](../action/consent.md#important-notes).
-->

Gli altri passaggi per configurare un’azione personalizzata in un percorso sono descritti in [questa sezione](../building-journeys/using-custom-actions.md).
