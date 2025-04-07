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
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '1371'
ht-degree: 47%

---

# Annullamento iscrizione a mailing list{#list-unsubscribe}

<!--Do not modify - Legal Review Done -->

In [!DNL Adobe Journey Optimizer], durante la configurazione di una nuova configurazione del canale e-mail, quando [selezioni un sottodominio](email-settings.md#subdomains-and-ip-pools) dall&#39;elenco, viene visualizzata l&#39;opzione **[!UICONTROL Abilita annullamento sottoscrizione a elenco]**. Per impostazione predefinita, questa opzione è abilitata.

![](assets/preset-list-unsubscribe.png)

L’URL per l’annullamento dell’iscrizione all’elenco con un solo clic è un collegamento o un pulsante per l’annullamento dell’iscrizione visualizzato accanto alle informazioni sul mittente dell’e-mail e che consente ai destinatari di annullare immediatamente l’iscrizione alle mailing list con un solo clic.

Ad esempio, l’URL per l’annullamento dell’iscrizione con un solo clic mostra un collegamento come indicato di seguito in Gmail:

![](assets/preset-list-unsubscribe-header.png)

>[!IMPORTANT]
>
>Per visualizzare l’URL con un solo clic per l’annullamento dell’iscrizione nell’intestazione dell’e-mail, il client e-mail dei destinatari deve supportare questa funzione.

A seconda del client e-mail e delle impostazioni di annullamento dell’abbonamento alla configurazione e-mail, facendo clic sul collegamento di annullamento dell’abbonamento nell’intestazione e-mail si possono verificare i seguenti effetti:

* Quando la funzionalità **Invia a (annulla sottoscrizione)** è abilitata, la richiesta di annullamento dell&#39;iscrizione viene inviata all&#39;indirizzo predefinito dell&#39;annullamento dell&#39;iscrizione in base al sottodominio configurato.
* Quando la funzione **URL per l&#39;annullamento dell&#39;iscrizione con un solo clic** è abilitata o se hai inserito un URL per l&#39;annullamento dell&#39;iscrizione nel contenuto del corpo dell&#39;e-mail, il destinatario viene direttamente escluso, a livello di canale o a livello di ID (a seconda di come è configurato il consenso), quando fa clic sull&#39;URL per l&#39;annullamento dell&#39;iscrizione con un solo clic (in base al sottodominio configurato).

>[!NOTE]
>
>Scopri come gestire le impostazioni di annullamento dell&#39;abbonamento in [questa sezione](#enable-list-unsubscribe) di seguito.

In entrambi i casi, quando un destinatario fa clic sul collegamento di rinuncia, la richiesta di annullamento dell’abbonamento viene elaborata di conseguenza. Il profilo corrispondente viene immediatamente escluso e questa scelta viene aggiornata in [Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=it#getting-started){target="_blank"}.

>[!NOTE]
>
>A volte, gli eventi che causano l’annullamento dell’abbonamento potrebbero richiedere più tempo per essere riflessi a livello di profilo a causa dell’elaborazione dei dati a valle. Attendere qualche minuto per l&#39;aggiornamento del sistema.

## Abilitare l’annullamento di iscrizione a mailing list {#enable-list-unsubscribe}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="Aggiungi un URL per l’annullamento dell’iscrizione alle e-mail"
>abstract="Abilita questa opzione per aggiungere automaticamente un URL per l’annullamento dell’iscrizione all’intestazione dell’e-mail. Puoi anche impostare un URL per l’annullamento dell’iscrizione in un messaggio, inserendo un collegamento per la rinuncia con un clic nel contenuto dell’e-mail."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/channels/email/email-opt-out#one-click-opt-out" text="Impostare la rinuncia con un clic dal contenuto dell’e-mail"

Quando l&#39;opzione **[!UICONTROL Abilita annullamento iscrizione a mailing list]** è abilitata, se supportata dal client di posta elettronica dei destinatari, l&#39;intestazione dell&#39;e-mail include sia un mailto che un URL per impostazione predefinita che i destinatari possono utilizzare per annullare l&#39;iscrizione alla mailing list.

>[!NOTE]
>
>Se disabiliti questa opzione, nell’intestazione dell’e-mail non viene visualizzato alcun URL di annullamento iscrizione con un solo clic.

L’intestazione per l’annullamento dell’iscrizione a mailing list offre due opzioni che sono abilitate per impostazione predefinita, a meno che non vengano deselezionate:

![](assets/surface-list-unsubscribe.png){width="80%"}

* Un indirizzo **[!UICONTROL Invia a (annulla iscrizione)]**, che è l&#39;indirizzo di destinazione a cui vengono indirizzate le richieste di annullamento iscrizione per l&#39;elaborazione automatica. In [!DNL Journey Optimizer], l&#39;indirizzo e-mail per l&#39;annullamento dell&#39;iscrizione è l&#39;indirizzo predefinito **[!UICONTROL Invia a (annulla iscrizione)]** visualizzato nella configurazione del canale, in base al [sottodominio selezionato](email-settings.md#subdomains). <!--With this method, clicking the Unsubscribe link sends a pre-filled email to the unsubscribe address specified in the email header.-->

* **[!UICONTROL URL per l&#39;annullamento dell&#39;iscrizione con un solo clic]**, che per impostazione predefinita è l&#39;intestazione per l&#39;annullamento dell&#39;iscrizione di un elenco generato dall&#39;URL di rinuncia con un solo clic, in base al [sottodominio selezionato](email-settings.md#subdomains). <!--With this method, clicking the Unsubscribe link directly unsubscribes the user, requiring only a single action to unsubscribe.-->

Puoi selezionare il **[!UICONTROL Livello di consenso]** dall’elenco a discesa corrispondente. Può essere specifico per il canale o per l’identità del profilo. In base a questa impostazione, quando un utente annulla l’iscrizione utilizzando l’URL di annullamento iscrizione alla mailing list nell’intestazione di un’e-mail, il consenso viene aggiornato in [!DNL Adobe Journey Optimizer] a livello di canale o di ID.

## Guardrail e raccomandazioni {#list-unsubscribe-guardrails}

La funzione URL per l’annullamento dell’iscrizione all’elenco con un solo clic consente ai destinatari di rinunciare facilmente alle comunicazioni. Tuttavia, poiché non tutti i client e-mail supportano questo collegamento nell&#39;intestazione dell&#39;e-mail, Adobe consiglia di aggiungere anche un [collegamento di rinuncia con un solo clic](email-opt-out.md#one-click-opt-out) o un [collegamento per annullare l&#39;abbonamento](email-opt-out.md#add-unsubscribe-link) nel corpo dell&#39;e-mail.

Le funzioni **[!UICONTROL Indirizzo Mailto (annulla iscrizione)]** e **[!UICONTROL URL di annullamento iscrizione con un solo clic]** sono facoltative.

* Se hai attivato l&#39;opzione **[!UICONTROL Abilita annullamento sottoscrizione elenco]** nelle [impostazioni di configurazione e-mail](email-settings.md), ti consigliamo di abilitare entrambi i metodi: **Invia a (annulla iscrizione)** e **URL annullamento iscrizione con un solo clic**. Non tutti i client e-mail supportano il metodo HTTP. Grazie alla funzione di annullamento dell’iscrizione all’elenco Invia a, che consente di selezionare un’alternativa, la reputazione del mittente può essere protetta meglio e tutti i destinatari possono accedere a utilizzare la funzionalità di annullamento dell’iscrizione.

* Se non desideri utilizzare l’URL predefinito generato con un solo clic per annullare l’abbonamento, puoi deselezionare la funzione.

   * Nello scenario in cui l’opzione **[!UICONTROL Abilita annullamento di iscrizione a mailing list]** sia attivata e la funzione **[!UICONTROL URL di annullamento iscrizione con un solo clic]** sia deselezionata, se viene aggiunto un [collegamento di rinuncia con un solo clic](../email/email-opt-out.md#one-click-opt-out) a un messaggio creato utilizzando questa configurazione, l’intestazione Annullamento iscrizione alla mailing list rileva tale collegamento, inserito nel corpo dell’e-mail, e lo utilizza come valore dell’URL di annullamento iscrizione con un solo clic.

     ![](assets/preset-list-unsubscribe-opt-out-url.png)

   * Se non aggiungi un collegamento di rinuncia con un solo clic nel contenuto del messaggio e l’**[!UICONTROL URL di annullamento iscrizione con un solo clic]** predefinito è deselezionato nelle impostazioni di configurazione dei canali, nessun URL verrà trasferito nell’intestazione dell’e-mail come parte dell’intestazione per l’annullamento dell’iscrizione alla mailing list.

  >[!NOTE]
  >
  >Ulteriori informazioni sulla gestione delle funzionalità di annullamento dell&#39;iscrizione nei messaggi sono disponibili in [questa sezione](../email/email-opt-out.md#unsubscribe-header).

In [!DNL Journey Optimizer], il consenso è gestito dallo [Schema di consenso](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=it) di Experience Platform{target="_blank"}. Per impostazione predefinita, il valore del campo di consenso è vuoto e viene trattato come consenso alla ricezione delle comunicazioni. Puoi modificare questo valore predefinito durante l&#39;onboarding in uno dei possibili valori elencati [qui](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=it#choice-values){target="_blank"} oppure utilizzare [criteri di consenso](../action/consent.md) per ignorare la logica predefinita.

Attualmente, [!DNL Journey Optimizer] non aggiunge un tag specifico agli eventi di annullamento dell&#39;abbonamento attivati dalla funzione di annullamento dell&#39;abbonamento all&#39;elenco. Se devi distinguere i clic per annullare l’iscrizione all’elenco da altre azioni di annullamento dell’iscrizione, devi implementare un’assegnazione tag personalizzata esternamente o sfruttare una pagina di destinazione esterna per il tracciamento.

## Gestire esternamente i dati di annullamento iscrizione {#custom-managed}

>[!CONTEXTUALHELP]
>id="ajo_email_config_unsubscribe_custom"
>title="Definire la modalità di gestione dei dati di annullamento iscrizione"
>abstract="**Gestito da Adobe**: i dati sul consenso vengono gestiti da te all’interno del sistema Adobe.<br>**Gestito da cliente**: i dati sul consenso vengono gestiti da te in un sistema esterno e la sincronizzazione dei dati sul consenso non viene aggiornata nel sistema Adobe, a meno che questa non venga avviata da te."

>[!CONTEXTUALHELP]
>id="ajo_email_config_unsubscribe_custom_url"
>title="Inserisci il tuo URL per annullare l’iscrizione con un solo clic"
>abstract="L&#39;**URL per annullamento sottoscrizione con un solo clic** deve utilizzare il metodo di richiesta POST."

Se gestisci il consenso al di fuori di Adobe, seleziona l’opzione **[!UICONTROL Gestito da cliente]** per immettere un indirizzo e-mail personalizzato per l’annullamento dell’iscrizione e l’URL personalizzato per l’annullamento con un clic.

![](assets/surface-list-unsubscribe-custom.png){width="80%"}

L&#39;**[!UICONTROL URL per annullare l&#39;iscrizione con un solo clic]** deve essere un URL POST.

>[!WARNING]
>
>Se utilizzi l’opzione **[!UICONTROL Gestito da cliente]**, Adobe non archivia i dati sul consenso o di annullamento dell’iscrizione. Con l’opzione **[!UICONTROL Gestito da cliente]**, le organizzazioni scelgono di utilizzare un sistema esterno e saranno responsabili della gestione dei dati sul consenso in tale sistema esterno. Non esiste alcuna sincronizzazione automatica dei dati sul consenso tra il sistema esterno e [!DNL Journey Optimizer]. Qualsiasi sincronizzazione dei dati sul consenso, originata dal sistema esterno per aggiornare i dati sul consenso dell’utente in [!DNL Journey Optimizer], deve essere avviata dall’organizzazione come trasferimento di dati per inviare nuovamente i dati sul consenso in [!DNL Journey Optimizer].

### Configurare l’API di decrittografia {#configure-decrypt-api}

Con l&#39;opzione **[!UICONTROL Gestione clienti]** selezionata, se immetti endpoint personalizzati e li utilizzi in una campagna o in un percorso, [!DNL Journey Optimizer] aggiunge alcuni parametri predefiniti specifici del profilo all&#39;evento di aggiornamento del consenso <!--sent to the custom endpoint --> quando i destinatari fanno clic sul collegamento per annullare l&#39;abbonamento.

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

Di seguito sono riportati parametri di esempio e la risposta di consenso:

| Parametro query | Payload di esempio |
|---------|----------|
| pid | {<br>&quot;pid&quot;: &quot;5142733041546020095851529937068211571&quot;,<br>&quot;pns&quot;: &quot;CRMID&quot;,<br>&quot;e&quot;    : &quot;john@google.com&quot;,<br>&quot;ens&quot; : &quot;Email&quot;,<br>} |
| parametri | {<br>&quot;m&quot; : &quot;messageExecutionId&quot;,<br>&quot;ci&quot; : &quot;campaignId&quot;,<br>&quot;jv&quot; : &quot;journeyVersionId&quot;,<br>&quot;ja&quot; : &quot;journeyActionId&quot;,<br>&quot;s&quot; : &quot;sandboxId&quot;,<br>&quot;us&quot; : &quot;unsubscribeScope&quot;<br>} |

Risposta al consenso:

```
{
    "profileNameSpace": " CRMID ",
    "profileId": "5142733041546020095851529937068211571",
    "emailAddress": "john@google.com",
    "emailNameSpace": "Email",
    "sandboxId": "sandboxId",
    "optOutLevel": "channel",
    "channelType": "email",
    "timestamp": "2024-11-26T14:25:09.316930Z"
}
```

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

Di seguito sono riportati parametri di esempio e la risposta di consenso:

| Parametro query | Payload di esempio |
|---------|----------|
| emailParams | {<br>&quot;p&quot; : &quot;profileId&quot;,<br>&quot;pn&quot; : &quot;profileNamespace&quot;,<br>&quot;en&quot; : &quot;emailNamespace&quot;,<br>&quot;ci&quot; : &quot;campaignId&quot;,<br>&quot;jv&quot; : &quot;journeyVersionId&quot;,<br>&quot;ja&quot; : &quot;journeyActionId&quot;,<br>&quot;si&quot; : &quot;sandboxId&quot;,<br>&quot;us&quot;: &quot;unsubscribeScope&quot;<br>} |

Risposta al consenso:

```
{
    "profileNameSpace": " CRMID ",
    "profileId": "5142733041546020095851529937068211571",
    "emailAddress": "john@google.com",
    "emailNameSpace": "Email",
    "sandboxId": "sandboxId",
    "optOutLevel": "channel",
    "channelType": "email",
    "timestamp": "2024-11-26T14:25:09.316930Z"
}
```

+++
