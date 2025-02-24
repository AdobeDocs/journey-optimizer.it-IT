---
solution: Journey Optimizer
product: journey optimizer
title: Configurare l’annullamento di iscrizione a mailing list
description: Scopri come includere un URL per l’annullamento dell’iscrizione con un solo clic nell’intestazione delle e-mail quando imposti la configurazione del canale
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: impostazioni, e-mail, configurazione
exl-id: c6c77975-ec9c-44c8-a8d8-50ca6231fea6
source-git-commit: b3655506dff97756a59a63d5b8f0c358dc7c7510
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 100%

---

# Annullamento iscrizione a mailing list{#list-unsubscribe}

<!--Do not modify - Legal Review Done -->

Durante una nuova configurazione del canale e-mail, quando si [seleziona un sottodominio](email-settings.md#subdomains-and-ip-pools) dall’elenco, viene visualizzata l’opzione **[!UICONTROL Abilita annullamento iscrizione a mailing list]**.

![](assets/preset-list-unsubscribe.png)

## Abilitare l’annullamento di iscrizione a mailing list {#enable-list-unsubscribe}

Questa opzione è abilitata per impostazione predefinita per includere un URL di annullamento iscrizione con un solo clic nell’intestazione dell’e-mail, ad esempio:

![](assets/preset-list-unsubscribe-header.png)

>[!NOTE]
>
>Se disabiliti questa opzione, nell’intestazione dell’e-mail non viene visualizzato alcun URL di annullamento iscrizione con un solo clic.

L’intestazione per l’annullamento dell’iscrizione a mailing list offre due opzioni che sono abilitate per impostazione predefinita, a meno che non vengano deselezionate:

![](assets/surface-list-unsubscribe.png){width="80%"}

* Un indirizzo **[!UICONTROL Indirizzo Mailto (annulla iscrizione)]**, che è l’indirizzo di destinazione a cui vengono indirizzate le richieste di annullamento iscrizione per l’elaborazione automatica.

  In [!DNL Journey Optimizer], l’indirizzo e-mail per l’annullamento dell’iscrizione è l’**[!UICONTROL Indirizzo Mailto (annulla iscrizione)]** predefinito visualizzato nella configurazione del canale, in base al [sottodominio selezionato](#subdomains-and-ip-pools). <!--With this method, clicking the Unsubscribe link sends a pre-filled email to the unsubscribe address specified in the email header.-->

* L’**[!UICONTROL URL per annullamento iscrizione con un solo clic]**, che per impostazione predefinita è l’intestazione per l’annullamento dell’iscrizione alla mailing list generato con URL di rinuncia con un solo clic, in base al sottodominio impostato e configurato nelle impostazioni di configurazione del canale. <!--With this method, clicking the Unsubscribe link directly unsubscribes the user, requiring only a single action to unsubscribe.-->

Puoi selezionare il **[!UICONTROL Livello di consenso]** dall’elenco a discesa corrispondente. Può essere specifico per il canale o per l’identità del profilo. In base a questa impostazione, quando un utente annulla l’iscrizione utilizzando l’URL di annullamento iscrizione alla mailing list nell’intestazione di un’e-mail, il consenso viene aggiornato in [!DNL Adobe Journey Optimizer] a livello di canale o di ID.

Le funzioni **[!UICONTROL Indirizzo Mailto (annulla iscrizione)]** e **[!UICONTROL URL di annullamento iscrizione con un solo clic]** sono facoltative.

Se non desideri utilizzare l’URL predefinito di annullamento iscrizione con un solo clic generato, puoi deselezionare la funzione. Nello scenario in cui l’opzione **[!UICONTROL Abilita annullamento di iscrizione a mailing list]** sia attivata e la funzione **[!UICONTROL URL di annullamento iscrizione con un solo clic]** sia deselezionata, se viene aggiunto un [collegamento di rinuncia con un solo clic](../email/email-opt-out.md#one-click-opt-out) a un messaggio creato utilizzando questa configurazione, l’intestazione Annullamento iscrizione alla mailing list rileva tale collegamento, inserito nel corpo dell’e-mail, e lo utilizza come valore dell’URL di annullamento iscrizione con un solo clic.

![](assets/preset-list-unsubscribe-opt-out-url.png)

>[!NOTE]
>
>Se non aggiungi un collegamento di rinuncia con un solo clic nel contenuto del messaggio e l’**[!UICONTROL URL di annullamento iscrizione con un solo clic]** predefinito è deselezionato nelle impostazioni di configurazione dei canali, nessun URL verrà trasferito nell’intestazione dell’e-mail come parte dell’intestazione per l’annullamento dell’iscrizione alla mailing list.

Ulteriori informazioni sulla gestione delle funzionalità di annullamento dell’iscrizione nei messaggi sono disponibili in [questa sezione](../email/email-opt-out.md#unsubscribe-header).

## Gestire esternamente i dati di annullamento iscrizione {#custom-managed}

>[!CONTEXTUALHELP]
>id="ajo_email_config_unsubscribe_custom"
>title="Definire la modalità di gestione dei dati di annullamento iscrizione"
>abstract="**Gestito da Adobe**: i dati sul consenso vengono gestiti da te all’interno del sistema Adobe.<br>**Gestito da cliente**: i dati sul consenso vengono gestiti da te in un sistema esterno e la sincronizzazione dei dati sul consenso non viene aggiornata nel sistema Adobe, a meno che questa non venga avviata da te."

Se gestisci il consenso al di fuori di Adobe, seleziona l’opzione **[!UICONTROL Gestito da cliente]** per immettere un indirizzo e-mail personalizzato per l’annullamento dell’iscrizione e l’URL personalizzato per l’annullamento con un clic.

![](assets/surface-list-unsubscribe-custom.png){width="80%"}

>[!WARNING]
>
>Se utilizzi l’opzione **[!UICONTROL Gestito da cliente]**, Adobe non archivia i dati sul consenso o di annullamento dell’iscrizione. Con l’opzione **[!UICONTROL Gestito da cliente]**, le organizzazioni scelgono di utilizzare un sistema esterno e saranno responsabili della gestione dei dati sul consenso in tale sistema esterno. Non esiste alcuna sincronizzazione automatica dei dati sul consenso tra il sistema esterno e [!DNL Journey Optimizer]. Qualsiasi sincronizzazione dei dati sul consenso, originata dal sistema esterno per aggiornare i dati sul consenso dell’utente in [!DNL Journey Optimizer], deve essere avviata dall’organizzazione come trasferimento di dati per inviare nuovamente i dati sul consenso in [!DNL Journey Optimizer].

### Configurare l’API di decrittografia {#configure-decrypt-api}

Con l’opzione **[!UICONTROL Gestito da cliente]** selezionata, se immetti endpoint personalizzati e li utilizzi in una campagna o in un percorso, [!DNL Journey Optimizer] aggiunge alcuni parametri predefiniti specifici del profilo all’evento di aggiornamento del consenso <!--sent to the custom endpoint --> quando i destinatari fanno clic sul collegamento Annulla iscrizione.

Questi parametri vengono inviati all’endpoint in modo crittografato. Pertanto, il sistema di consenso esterno deve implementare un’API specifica tramite [Adobe Developer](https://developer.adobe.com){target="_blank"} per decrittografare i parametri inviati da Adobe.

La chiamata GET per recuperare questi parametri dipende dall’opzione Annullamento iscrizione a mailing list in uso: **[!UICONTROL URL per annullamento iscrizione con un solo clic]** o **[!UICONTROL Indirizzo Mailto (annulla iscrizione)]**.

<!--To configure the API to send back the information to [!DNL Adobe Journey Optimizer] when a recipient has unsubscribed using the List unsubscribe option with custom endpoints, follow the steps below.-->

+++ URL di annullamento iscrizione con un solo clic

Con l’opzione **[!UICONTROL URL per annullamento iscrizione con un solo clic]**, facendo clic sul collegamento Annulla iscrizione l’utente viene subito rimosso.

La chiamata GET è la seguente:

Endpoint: https://platform.adobe.io/journey/imp/consent/decrypt

Parametri query:

* **parametri**: contiene il payload crittografato
* **pid**: ID profilo crittografato

Questi due parametri verranno inclusi nell’evento di aggiornamento del consenso inviato agli endpoint personalizzati.

Requisiti dell’intestazione:

* x-api-key
* x-gw-ims-org-id
* autorizzazione (token utente dal tuo account tecnico)

+++

+++ Indirizzo Mailto (annulla iscrizione)

Con l’opzione **[!UICONTROL Indirizzo Mailto (annulla iscrizione)]**, quando si fa clic sul collegamento Annulla iscrizione viene inviata un’e-mail precompilata all’indirizzo di annullamento dell’iscrizione specificato.

La chiamata GET è la seguente:

Endpoint: https://platform.adobe.io/journey/imp/consent/decrypt

Parametri query:

* **emailParams**: stringa contenente i parametri **params** (payload crittografato) e **pid** (ID profilo crittografato).

I parametri **params** e **pid** verranno inclusi nell’evento di aggiornamento del consenso inviato agli endpoint personalizzati.

Requisiti dell’intestazione:

* x-api-key
* x-gw-ims-org-id
* autorizzazione (token utente dal tuo account tecnico)

+++
