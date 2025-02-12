---
solution: Journey Optimizer
product: journey optimizer
title: Configurare le impostazioni e-mail
description: Scopri come configurare l’annullamento dell’iscrizione a un elenco a livello di configurazione del canale
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: impostazioni, e-mail, configurazione
source-git-commit: d782c668b412cebeacd1289c79bbf86ec710786b
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 32%

---

# Annullamento iscrizione elenco{#list-unsubscribe}

<!--Do not modify - Legal Review Done -->

Durante la configurazione di una nuova configurazione del canale e-mail, dopo aver [selezionato un sottodominio](email-settings.md#subdomains-and-ip-pools) dall&#39;elenco, viene visualizzata l&#39;opzione **[!UICONTROL Abilita annullamento sottoscrizione a elenco]**.

![](assets/preset-list-unsubscribe.png)

## Abilita annullamento iscrizione elenco {#enable-list-unsubscribe}

Questa opzione è abilitata per impostazione predefinita per includere un URL di annullamento iscrizione con un solo clic nell’intestazione dell’e-mail, ad esempio:

![](assets/preset-list-unsubscribe-header.png)

>[!NOTE]
>
>Se disabiliti questa opzione, nell’intestazione dell’e-mail non viene visualizzato alcun URL di annullamento iscrizione con un solo clic.

L’intestazione Annulla iscrizione elenco offre due opzioni, che sono abilitate per impostazione predefinita a meno che non si deselezioni una o entrambe:

![](assets/surface-list-unsubscribe.png){width="80%"}

* Un indirizzo **[!UICONTROL Invia a (annulla iscrizione)]**, che è l’indirizzo di destinazione a cui vengono indirizzate le richieste di annullamento iscrizione per l’elaborazione automatica.

  In [!DNL Journey Optimizer], l&#39;indirizzo e-mail per l&#39;annullamento dell&#39;iscrizione è l&#39;indirizzo predefinito **[!UICONTROL Invia a (annulla iscrizione)]** visualizzato nella configurazione del canale, in base al [sottodominio selezionato](#subdomains-and-ip-pools). <!--With this method, clicking the Unsubscribe link sends a pre-filled email to the unsubscribe address specified in the email header.-->

* L&#39;**[!UICONTROL URL per l&#39;annullamento dell&#39;iscrizione con un solo clic]**, che per impostazione predefinita è l&#39;intestazione per l&#39;annullamento dell&#39;iscrizione dell&#39;elenco generato con un solo clic, in base al sottodominio impostato e configurato nelle impostazioni di configurazione del canale. <!--With this method, clicking the Unsubscribe link directly unsubscribes the user, requiring only a single action to unsubscribe.-->

Puoi selezionare il **[!UICONTROL Livello di consenso]** dall&#39;elenco a discesa corrispondente. Può essere specifico per il canale o per l’identità del profilo. In base a questa impostazione, quando un utente annulla l&#39;iscrizione utilizzando l&#39;URL per l&#39;annullamento dell&#39;iscrizione all&#39;elenco nell&#39;intestazione di un&#39;e-mail, il consenso viene aggiornato in [!DNL Adobe Journey Optimizer], a livello di canale o di ID.

Le funzioni **[!UICONTROL Invia a (annulla iscrizione)]** e **[!UICONTROL URL di annullamento iscrizione con un solo clic]** sono facoltative.

Se non desideri utilizzare l’URL predefinito di annullamento iscrizione con un solo clic generato, puoi deselezionare la funzione. Nello scenario in cui l’opzione **[!UICONTROL Abilita annullamento di iscrizione a mailing list]** sia attivata e la funzione **[!UICONTROL URL di annullamento iscrizione con un solo clic]** sia deselezionata, se viene aggiunto un [collegamento di rinuncia con un solo clic](../email/email-opt-out.md#one-click-opt-out) a un messaggio creato utilizzando questa configurazione, l’intestazione Annullamento iscrizione alla mailing list rileva tale collegamento, inserito nel corpo dell’e-mail, e lo utilizza come valore dell’URL di annullamento iscrizione con un solo clic.

![](assets/preset-list-unsubscribe-opt-out-url.png)

>[!NOTE]
>
>Se non aggiungi un collegamento di rinuncia con un solo clic nel contenuto del messaggio e l’**[!UICONTROL URL di annullamento iscrizione con un solo clic]** predefinito è deselezionato nelle impostazioni di configurazione dei canali, nessun URL verrà trasferito nell’intestazione dell’e-mail come parte dell’intestazione per l’annullamento dell’iscrizione alla mailing list.

Ulteriori informazioni sulla gestione delle funzionalità di annullamento dell&#39;iscrizione nei messaggi sono disponibili in [questa sezione](../email/email-opt-out.md#unsubscribe-header).

## Gestire esternamente i dati di annullamento dell’abbonamento {#custom-managed}

>[!CONTEXTUALHELP]
>id="ajo_email_config_unsubscribe_custom"
>title="Definire la modalità di gestione dei dati di annullamento dell’abbonamento"
>abstract="**Adobe managed**: i dati di consenso sono gestiti dall&#39;utente all&#39;interno del sistema Adobe.<br>**Gestione clienti**: i dati di consenso vengono gestiti dall&#39;utente in un sistema esterno e la sincronizzazione dei dati di consenso non viene aggiornata nel sistema Adobe a meno che non sia stata avviata dall&#39;utente."

>[!AVAILABILITY]
>
>Questa funzionalità viene rilasciata in Disponibilità limitata (LA) per un set limitato di clienti.

Se gestisci il consenso all&#39;esterno di Adobe, seleziona l&#39;opzione **[!UICONTROL Gestione clienti]** per immettere un indirizzo e-mail personalizzato per l&#39;annullamento dell&#39;iscrizione e il tuo URL personalizzato con un solo clic.

![](assets/surface-list-unsubscribe-custom.png){width="80%"}

>[!WARNING]
>
>Se utilizzi l&#39;opzione **[!UICONTROL Gestione clienti]**, Adobe non archivia i dati relativi agli annullamenti dell&#39;abbonamento o al consenso. Con l&#39;opzione **[!UICONTROL Gestione clienti]**, le organizzazioni scelgono di utilizzare un sistema esterno e saranno responsabili della gestione dei propri dati di consenso in tale sistema esterno. Non esiste alcuna sincronizzazione automatica dei dati sul consenso tra il sistema esterno e [!DNL Journey Optimizer]. Qualsiasi sincronizzazione dei dati sul consenso, originata dal sistema esterno per aggiornare i dati sul consenso dell&#39;utente in [!DNL Journey Optimizer], deve essere avviata dall&#39;organizzazione come trasferimento di dati per inviare nuovamente i dati sul consenso in [!DNL Journey Optimizer].

## Configurare l’API di decrittografia {#configure-decrypt-api}

Con l&#39;opzione **[!UICONTROL Gestione clienti]** selezionata, se immetti endpoint personalizzati e li utilizzi in una campagna o in un percorso, [!DNL Journey Optimizer] aggiunge alcuni parametri predefiniti specifici del profilo all&#39;evento di aggiornamento del consenso <!--sent to the custom endpoint --> quando i destinatari fanno clic sul collegamento Annulla iscrizione.

Questi parametri vengono inviati all’endpoint in modo crittografato. Pertanto, il sistema di consenso esterno deve implementare un&#39;API specifica tramite [Adobe Developer](https://developer.adobe.com){target="_blank"} per decrittografare i parametri inviati da Adobe.

La chiamata di GET per recuperare questi parametri dipende dall&#39;opzione Elenco annullamenti sottoscrizione in uso: **[!UICONTROL URL annullamento sottoscrizione con un solo clic]** o **[!UICONTROL Invia a (annullamento sottoscrizione)]**.

<!--To configure the API to send back the information to [!DNL Adobe Journey Optimizer] when a recipient has unsubscribed using the List unsubscribe option with custom endpoints, follow the steps below.-->

+++ URL per annullamento iscrizione con un clic

Con l&#39;opzione **[!UICONTROL URL per l&#39;annullamento dell&#39;iscrizione]** con un solo clic, facendo clic sul collegamento per annullare l&#39;iscrizione l&#39;utente verrà annullato direttamente.

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

+++ Invia a (annulla iscrizione)

Con l&#39;opzione **[!UICONTROL Invia a (annulla iscrizione)]**, facendo clic sul collegamento Annulla iscrizione, viene inviata un&#39;e-mail precompilata all&#39;indirizzo di annullamento dell&#39;iscrizione specificato.

La chiamata GET è la seguente.

Endpoint: https://platform.adobe.io/journey/imp/consent/decrypt

Parametri query:

* **emailParams**: stringa contenente i parametri **params** (payload crittografato) e **pid** (ID profilo crittografato).

I parametri **params** e **pid** verranno inclusi nell&#39;evento di aggiornamento del consenso inviato agli endpoint personalizzati.

Requisiti dell’intestazione:

* x-api-key
* x-gw-ims-org-id
* autorizzazione (token utente dal tuo account tecnico)

+++
