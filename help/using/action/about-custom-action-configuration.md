---
solution: Journey Optimizer
product: journey optimizer
title: Configurare un’azione personalizzata
description: Scopri come configurare un’azione personalizzata
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: azione, terze parti, personalizzato, percorsi, API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: e0f7eca8b3313cb5eb8e201c567622ded20a82d2
workflow-type: tm+mt
source-wordcount: '1342'
ht-degree: 18%

---

# Configurare un’azione personalizzata {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="Azioni personalizzate"
>abstract="Se utilizzi un sistema di terze parti per l’invio di messaggi o desideri che i percorsi inviino chiamate API a un sistema di terze parti, utilizza azioni personalizzate per configurarne la connessione al tuo percorso. Ad esempio, mediante azioni personalizzate è possibile connettersi ai seguenti sistemi: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com), Firebase, ecc."

Se utilizzi un sistema di terze parti per l’invio di messaggi o desideri che i percorsi inviino chiamate API a un sistema di terze parti, utilizza azioni personalizzate per configurarne la connessione al tuo percorso. Ad esempio, è possibile connettersi ai seguenti sistemi con azioni personalizzate: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase, ecc.

Le azioni personalizzate sono azioni aggiuntive definite dagli utenti tecnici e rese disponibili agli esperti di marketing. Una volta configurate, vengono visualizzate nella palette a sinistra del percorso, nel **[!UICONTROL Azione]** categoria. Per ulteriori informazioni, consulta [questa pagina](../building-journeys/about-journey-activities.md#action-activities).

## Limitazioni{#custom-actions-limitations}

Le azioni personalizzate presentano alcune limitazioni elencate in [questa pagina](../start/guardrails.md).

Nei parametri delle azioni personalizzati, puoi trasmettere una semplice raccolta e un insieme di oggetti. Ulteriori informazioni sulle limitazioni della raccolta in [questa pagina](../building-journeys/collections.md#limitations).

Inoltre, i parametri delle azioni personalizzate hanno un formato previsto (ad esempio, stringa, decimale, ecc.). Devi fare attenzione a rispettare questi formati previsti. Ulteriori informazioni [caso d’uso](../building-journeys/collections.md).

## Best practice{#custom-action-enhancements-best-practices}

Per tutte le azioni personalizzate viene definito un limite massimo di 300.000 chiamate in un minuto. Inoltre, il limite predefinito viene eseguito per host e per sandbox. Ad esempio, se in una sandbox hai due endpoint con lo stesso host (ad esempio: `https://www.adobe.com/endpoint1` e `https://www.adobe.com/endpoint2`), il limite verrà applicato a tutti gli endpoint nell’host adobe.com. &quot;endpoint1&quot; ed &quot;endpoint2&quot; condivideranno la stessa configurazione di limitazione e il fatto che un endpoint raggiunga il limite avrà un impatto sull’altro endpoint.

Questo limite è stato impostato in base all’utilizzo da parte della clientela, per proteggere gli endpoint esterni interessati dalle azioni personalizzate. Devi tenerne conto nei percorsi basati sul pubblico definendo una velocità di lettura appropriata (5000 profili al secondo quando vengono utilizzate le azioni personalizzate). Se necessario, puoi ignorare questa impostazione definendo un limite di limitazione di utilizzo o di limitazione maggiore tramite le rispettive API. Consulta [questa pagina](../configuration/external-systems.md).

Non eseguire il targeting degli endpoint pubblici con azioni personalizzate per vari motivi:

* Senza limiti o limitazioni corretti, esiste il rischio di inviare troppe chiamate a un endpoint pubblico che potrebbe non supportare tale volume.
* I dati del profilo possono essere inviati tramite azioni personalizzate, pertanto il targeting di un endpoint pubblico potrebbe causare la condivisione involontaria di informazioni personali esternamente.
* Non hai alcun controllo sui dati restituiti dagli endpoint pubblici. Se un endpoint modifica la propria API o inizia a inviare informazioni errate, queste saranno rese disponibili nelle comunicazioni inviate, con potenziali effetti negativi.

## Consenso e governance dei dati {#privacy}

In Journey Optimizer, puoi applicare la governance dei dati e i criteri di consenso alle azioni personalizzate per impedire l’esportazione di campi specifici in sistemi di terze parti o escludere clienti che non hanno acconsentito a ricevere comunicazioni e-mail, push o SMS. Per ulteriori informazioni, consulta le pagine seguenti:

* [Governance dei dati](../action/action-privacy.md).
* [Consenso](../action/action-privacy.md).


## Passaggi di configurazione {#configuration-steps}

Di seguito sono riportati i passaggi principali necessari per configurare un’azione personalizzata:

1. Nella sezione del menu ADMINISTRATION, selezionare **[!UICONTROL Configurazioni]**. In  **[!UICONTROL Azioni]** , fare clic su **[!UICONTROL Gestisci]**. Clic **[!UICONTROL Crea azione]** per creare una nuova azione. Il riquadro di configurazione delle azioni si apre sul lato destro dello schermo.

   ![](assets/custom2.png)

1. Immetti un nome per l&#39;azione.

   >[!NOTE]
   >
   >Non utilizzare spazi o caratteri speciali. Non usare più di 30 caratteri.

1. Aggiungi una descrizione all’azione. Questo passaggio è facoltativo.
1. Il numero di percorsi che utilizzano questa azione viene visualizzato nel **[!UICONTROL Utilizzato in]** campo. Puoi fare clic su **[!UICONTROL Visualizza percorsi]** per visualizzare l&#39;elenco dei percorsi che utilizzano questa azione.
1. Definisci i diversi **[!UICONTROL Configurazione URL]** parametri. Consulta [questa pagina](../action/about-custom-action-configuration.md#url-configuration).
1. Configurare **[!UICONTROL Autenticazione]** sezione. Questa configurazione è la stessa delle origini dati.  Consulta [questa sezione](../datasource/external-data-sources.md#custom-authentication-mode).
1. Definisci il **[!UICONTROL Parametri azione]**. Consulta [questa pagina](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Fai clic su **[!UICONTROL Salva]**.

   L’azione personalizzata è ora configurata ed è pronta per essere utilizzata nei percorsi. Consulta [questa pagina](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Quando un’azione personalizzata viene utilizzata in un percorso, la maggior parte dei parametri è di sola lettura. È possibile modificare solo **[!UICONTROL Nome]**, **[!UICONTROL Descrizione]**, **[!UICONTROL URL]** campi e **[!UICONTROL Autenticazione]** sezione.

## Configurazione endpoint {#url-configuration}

Durante la configurazione di un’azione personalizzata, devi definire quanto segue **[!UICONTROL Configurazione endpoint]** parametri:

![](assets/action-response1bis.png){width="70%" align="left"}

1. In **[!UICONTROL URL]** , specifica l’URL del servizio esterno:

   * Se l’URL è statico, inseriscilo in questo campo.

   * Se l&#39;URL include un percorso dinamico, immettere solo la parte statica dell&#39;URL, ovvero lo schema, l&#39;host, la porta e, facoltativamente, una parte statica del percorso.

     Esempio: `https://xxx.yyy.com/somethingstatic/`

     Specificherai il percorso dinamico dell’URL quando aggiungi l’azione personalizzata a un percorso. [Ulteriori informazioni](../building-journeys/using-custom-actions.md).

   >[!NOTE]
   >
   >Per motivi di sicurezza, si consiglia vivamente di utilizzare lo schema HTTPS per l’URL. Non consentiamo l’uso di indirizzi Adobe non pubblici e l’uso di indirizzi IP.
   >
   >Durante la definizione di un’azione personalizzata sono consentite solo le porte predefinite: 80 per http e 443 per https.

1. Seleziona la chiamata **[!UICONTROL Metodo]**: può essere **[!UICONTROL POST]**, **[!UICONTROL GET]** o **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > Il **DELETE** metodo non supportato. Se devi aggiornare una risorsa esistente, seleziona la **PUT** metodo.

1. Definisci le intestazioni e i parametri di query:

   * In **[!UICONTROL Intestazioni]** , fare clic su **[!UICONTROL Aggiungere un campo intestazione]** per definire le intestazioni HTTP del messaggio di richiesta da inviare al servizio esterno. Il **[!UICONTROL Content-Type]** e **[!UICONTROL Charset]** i campi dell’intestazione sono impostati per impostazione predefinita. Non è possibile modificare o eliminare questi campi.

   * In **[!UICONTROL Parametri di query]** , fare clic su **[!UICONTROL Aggiungere un campo Parametro query]** per definire i parametri che desideri aggiungere all’URL.

   ![](assets/journeyurlconfiguration2bis.png)

1. Immettere l&#39;etichetta o il nome del campo.

1. Selezionare il tipo: **[!UICONTROL Costante]** o **[!UICONTROL Variabile]**. Se hai selezionato **[!UICONTROL Costante]**, quindi inserisci il valore costante nel **[!UICONTROL Valore]** campo. Se hai selezionato **[!UICONTROL Variabile]**, quindi specificherai questa variabile quando aggiungi l’azione personalizzata a un percorso. [Ulteriori informazioni](../building-journeys/using-custom-actions.md).

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >Dopo aver aggiunto l’azione personalizzata a un percorso, puoi comunque aggiungere campi di intestazione o parametri di query se il percorso si trova nello stato Bozza. Se non desideri che le modifiche alla configurazione influiscano sul percorso, duplica l’azione personalizzata e aggiungi i campi alla nuova azione personalizzata.
   >
   >Le intestazioni vengono convalidate in base alle regole di analisi dei campi. Ulteriori informazioni in [questa documentazione](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## Definire i parametri di payload {#define-the-message-parameters}

1. In **[!UICONTROL Richiesta]** incolla un esempio del payload JSON da inviare al servizio esterno. Questo campo è facoltativo e disponibile solo per i metodi di chiamata POST e PUT.

1. In **[!UICONTROL Risposta]** incolla un esempio del payload restituito dalla chiamata. Questo campo è facoltativo e disponibile per tutti i metodi di chiamata. Per informazioni dettagliate su come sfruttare le risposte alle chiamate API nelle azioni personalizzate, consulta [questa pagina](../action/action-response.md).

>[!NOTE]
>
>La funzionalità di risposta è attualmente disponibile in versione beta.

![](assets/action-response2bis.png){width="70%" align="left"}

>[!NOTE]
>
>L’esempio di payload non può contenere valori Null. I nomi dei campi nel payload non possono contenere un &quot;.&quot; aggiuntivo. Non possono iniziare con il carattere &quot;$&quot;.

Potrai definire il tipo di parametro (ad esempio stringa, numero intero e così via).

Puoi anche scegliere se specificare se un parametro è una costante o una variabile:

* **Costante** significa che il valore del parametro è definito nel riquadro di configurazione dell’azione da un utente tecnico. Il valore sarà sempre lo stesso tra i percorsi. Non varia e l’addetto marketing non la vede quando utilizza l’azione personalizzata nel percorso. Potrebbe essere ad esempio un ID previsto dal sistema di terze parti. In tal caso, il campo a destra della costante/variabile di attivazione è il valore passato.
* **Variabile** indica che il valore del parametro varia. Gli addetti al marketing che utilizzano questa azione personalizzata in un percorso saranno liberi di trasmettere il valore desiderato o di specificare dove recuperare il valore per questo parametro (ad esempio dall’evento, da Adobe Experience Platform, ecc.). In tal caso, il campo a destra della costante/variabile di attivazione è l’etichetta che gli addetti al marketing vedranno nel percorso per denominare questo parametro.

![](assets/customactionpayloadmessage2.png)