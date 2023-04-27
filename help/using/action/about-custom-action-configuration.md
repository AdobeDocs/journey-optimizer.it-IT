---
solution: Journey Optimizer
product: journey optimizer
title: Configurare un’azione personalizzata
description: Scopri come configurare un’azione personalizzata
feature: Actions
topic: Administration
role: Admin
level: Experienced
keywords: azione, terze parti, personalizzato, percorsi, API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 15%

---

# Configurare un’azione personalizzata {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="Azioni personalizzate"
>abstract="Se utilizzi un sistema di terze parti per l’invio di messaggi o desideri che i percorsi inviino chiamate API a un sistema di terze parti, utilizza azioni personalizzate per configurarne la connessione al tuo percorso. Ad esempio, mediante azioni personalizzate è possibile connettersi ai seguenti sistemi: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com), Firebase, ecc."

Se utilizzi un sistema di terze parti per l’invio di messaggi o desideri che i percorsi inviino chiamate API a un sistema di terze parti, utilizza azioni personalizzate per configurarne la connessione al tuo percorso. Ad esempio, è possibile connettersi ai seguenti sistemi con azioni personalizzate: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase, ecc.

Le azioni personalizzate sono azioni aggiuntive definite dagli utenti tecnici e rese disponibili agli esperti di marketing. Una volta configurati, vengono visualizzati nella palette a sinistra del percorso, nella **[!UICONTROL Azione]** categoria. Per ulteriori informazioni, consulta [questa pagina](../building-journeys/about-journey-activities.md#action-activities).

## Limitazioni {#custom-actions-limitations}

Le azioni personalizzate presentano alcune limitazioni elencate in [questa pagina](../start/guardrails.md).

Nei parametri di azione personalizzati è possibile passare una raccolta semplice e una raccolta di oggetti. Ulteriori informazioni sulle limitazioni della raccolta in [questa pagina](../building-journeys/collections.md#limitations).

Tieni presente che i parametri delle azioni personalizzate hanno un formato previsto (ad esempio: (stringa, decimale, ecc.). Devi fare attenzione a rispettare questi formati previsti. Ulteriori informazioni [caso d&#39;uso](../building-journeys/collections.md).

## Consenso e governance dei dati {#privacy}

In Journey Optimizer, puoi applicare i criteri di governance dei dati e di consenso alle azioni personalizzate per impedire l’esportazione di campi specifici in sistemi di terze parti o escludere i clienti che non hanno acconsentito a ricevere comunicazioni e-mail, push o SMS. Per ulteriori informazioni, consulta le pagine seguenti:

* [Governance dei dati](../action/action.md).
* [Consenso](../action/action.md).


## Passaggi di configurazione {#configuration-steps}

Di seguito sono riportati i passaggi principali necessari per configurare un’azione personalizzata:

1. Nella sezione del menu AMMINISTRAZIONE, seleziona **[!UICONTROL Configurazioni]**. In  **[!UICONTROL Azioni]** sezione, fai clic su **[!UICONTROL Gestisci]**. Fai clic su **[!UICONTROL Crea azione]** per creare una nuova azione. Il riquadro di configurazione delle azioni si apre sul lato destro dello schermo.

   ![](assets/custom2.png)

1. Immetti un nome per l’azione.

   >[!NOTE]
   >
   >Non utilizzare spazi o caratteri speciali. Non usare più di 30 caratteri.

1. Aggiungi una descrizione all’azione. Questo passaggio è facoltativo.
1. Il numero di percorsi che utilizzano questa azione viene visualizzato nella **[!UICONTROL Utilizzato in]** campo . Puoi fare clic su **[!UICONTROL Visualizza percorsi]** per visualizzare l’elenco dei percorsi che utilizzano questa azione.
1. Definire i diversi **[!UICONTROL Configurazione URL]** Parametri. Consulta [questa pagina](../action/about-custom-action-configuration.md#url-configuration).
1. Configura le **[!UICONTROL Autenticazione]** sezione . Questa configurazione è la stessa delle origini dati.  Vedi [questa sezione](../datasource/external-data-sources.md#custom-authentication-mode).
1. Definisci la **[!UICONTROL Parametri azione]**. Consulta [questa pagina](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Fai clic su **[!UICONTROL Salva]**.

   L’azione personalizzata è ora configurata ed è pronta per essere utilizzata nei percorsi. Consulta [questa pagina](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Quando un&#39;azione personalizzata viene utilizzata in un percorso, la maggior parte dei parametri è di sola lettura. È possibile modificare solo il **[!UICONTROL Nome]**, **[!UICONTROL Descrizione]**, **[!UICONTROL URL]** e **[!UICONTROL Autenticazione]** sezione .

## Configurazione URL {#url-configuration}

Quando configuri un’azione personalizzata, devi definire quanto segue **[!UICONTROL Configurazione URL]** parametri:

![](assets/journeyurlconfiguration.png)

1. In **[!UICONTROL URL]** specifica l’URL del servizio esterno:

   * Se l’URL è statico, immetti l’URL in questo campo.

   * Se l’URL include un percorso dinamico, immetti solo la parte statica dell’URL, ovvero lo schema, l’host, la porta e, facoltativamente, una parte statica del percorso.

      Esempio: `https://xxx.yyy.com/somethingstatic/`

      Quando aggiungi l’azione personalizzata a un percorso, specificerai il percorso dinamico dell’URL. [Maggiori informazioni](../building-journeys/using-custom-actions.md).
   >[!NOTE]
   >
   >Per motivi di sicurezza, si consiglia vivamente di utilizzare lo schema HTTPS per l’URL. Non consentiamo l’uso di indirizzi di Adobe che non sono pubblici e l’uso di indirizzi IP.
   >
   >Quando definisci un’azione personalizzata sono consentite solo le porte predefinite: 80 per http e 443 per https.

1. Seleziona la chiamata **[!UICONTROL Metodo]**: può essere **[!UICONTROL POST]** o **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > La **DELETE** metodo non supportato. Se devi aggiornare una risorsa esistente, seleziona la **PUT** metodo .

1. Definisci le intestazioni e i parametri di query:

   * In **[!UICONTROL Intestazioni]** sezione, fai clic su **[!UICONTROL Aggiungi un campo intestazione]** definire le intestazioni HTTP del messaggio di richiesta da inviare al servizio esterno. La **[!UICONTROL Content-Type]** e **[!UICONTROL Charset]** i campi di intestazione sono impostati per impostazione predefinita. Non è possibile modificare o eliminare questi campi.

   * In **[!UICONTROL Parametri query]** sezione, fai clic su **[!UICONTROL Aggiungi un campo del parametro Query]** per definire i parametri da aggiungere nell’URL.

   ![](assets/journeyurlconfiguration2bis.png)

1. Immettere l&#39;etichetta o il nome del campo.

1. Seleziona il tipo: **[!UICONTROL Costante]** o **[!UICONTROL Variabile]**. Se hai selezionato **[!UICONTROL Costante]**, quindi inserisci il valore costante nel **[!UICONTROL Valore]** campo . Se hai selezionato **[!UICONTROL Variabile]**, quindi specificherai questa variabile quando aggiungi l’azione personalizzata a un percorso. [Maggiori informazioni](../building-journeys/using-custom-actions.md).

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >Dopo aver aggiunto l’azione personalizzata a un percorso, puoi comunque aggiungere campi di intestazione o parametri di query se il percorso è in stato di bozza. Se non desideri che le modifiche alla configurazione interessino il percorso, duplica l’azione personalizzata e aggiungi i campi alla nuova azione personalizzata.
   >
   >Le intestazioni vengono convalidate in base alle regole di analisi dei campi. Ulteriori informazioni in [questa documentazione](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## Definire i parametri dell’azione {#define-the-message-parameters}

In **[!UICONTROL Parametri azione]** incolla un esempio del payload JSON da inviare al servizio esterno.

![](assets/messageparameterssection.png)

>[!NOTE]
>
>L&#39;esempio di payload non può contenere valori null. I nomi di campo nel payload non possono contenere un &quot;.&quot; aggiuntivo. Non possono iniziare con un carattere &quot;$&quot;.

Puoi definire il tipo di parametro (ad esempio: (stringa, numero intero, ecc.).

Puoi anche scegliere se specificare se un parametro è una costante o una variabile:

* **Costante** significa che il valore del parametro è definito nel riquadro di configurazione delle azioni da un utente tecnico. Il valore sarà sempre lo stesso in tutti i percorsi. Non varia e l’addetto al marketing non lo vedrà quando utilizza l’azione personalizzata nel percorso. Potrebbe trattarsi, ad esempio, di un ID previsto dal sistema di terze parti. In tal caso, il valore passato è rappresentato dal campo a destra della costante/variabile di attivazione/disattivazione.
* **Variabile** indica che il valore del parametro varia. Gli addetti al marketing che utilizzano questa azione personalizzata in un percorso possono passare liberamente il valore desiderato o specificare dove recuperare il valore per questo parametro (ad esempio dall’evento, da Adobe Experience Platform, ecc.). In tal caso, il campo a destra della costante/variabile di attivazione è l’etichetta che gli addetti al marketing vedranno nel percorso per denominare questo parametro.

![](assets/customactionpayloadmessage2.png)
