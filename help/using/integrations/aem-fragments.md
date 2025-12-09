---
solution: Journey Optimizer
product: journey optimizer
title: Frammenti di contenuto di AEM
description: Scopri come accedere e gestire i frammenti di contenuto di AEM
topic: Content Management
role: User
level: Beginner
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
source-git-commit: e292d584e3c3d1997c2c3e6bb3675758ff530bf9
workflow-type: tm+mt
source-wordcount: '1121'
ht-degree: 5%

---

# Frammenti di contenuto di Adobe Experience Manager {#aem-fragments}

Integrando Adobe Experience Manager as a Cloud Service con Adobe Journey Optimizer, ora puoi incorporare facilmente i frammenti di contenuto AEM nei contenuti Journey Optimizer. Questa connessione diretta facilita il processo di accesso e utilizzo dei contenuti AEM, consentendo la creazione di campagne e percorsi personalizzati e dinamici.

Per ulteriori informazioni sui frammenti di contenuto di AEM, consulta [Utilizzo dei frammenti di contenuto](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} nella documentazione di Experience Manager.

## Prima di iniziare {#start}

>[!AVAILABILITY]
>
>Per i clienti del settore sanitario, l&#39;integrazione è abilitata solo dopo aver concesso in licenza le offerte aggiuntive Journey Optimizer Healthcare Shield e Adobe Experience Manager Enhanced Security.

### Limitazioni {#limitations}

Quando si lavora con frammenti di contenuto Adobe Experience Manager in Journey Optimizer, tieni presente le seguenti limitazioni:

* **Tipi di frammenti di contenuto**: sono supportati solo frammenti di contenuto semplici. Le varianti e i frammenti nidificati non sono attualmente supportati.

* **Contenuto multilingue**: è supportato solo il flusso manuale.

* **Personalization**: sono supportati solo gli attributi di profilo, gli attributi contestuali, le stringhe statiche e le variabili predichiarate. Gli attributi derivati o calcolati non sono supportati.

* **Aggiornamenti e controllo delle versioni**: gli aggiornamenti dei frammenti di contenuto richiedono la ripubblicazione manuale da Adobe Experience Manager. Non esiste riconciliazione automatica delle versioni tra Adobe Experience Manager e Journey Optimizer.

* **Memorizzazione in cache**: Journey Optimizer recupera i frammenti di contenuto in tempo reale da Adobe Experience Manager Publish. Non esiste alcun caching pre-rendering.

* **Strumenti di correzione**: la bozza per campagne e percorsi pubblicati riflette i dati della pubblicazione più recente dei frammenti di contenuto di Experience Manager. Nessun blocco di versione cronologico.

* **Accesso utente**: si consiglia di limitare il numero di utenti con accesso alla pubblicazione di frammenti di contenuto per ridurre il rischio di errori accidentali.

### Flusso di sincronizzazione dei contenuti {#content-sync-flow}

L’integrazione tra Adobe Experience Manager e Journey Optimizer segue questo flusso di dati:

1. **[Crea e crea](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#creating-a-content-fragment)**: il contenuto viene creato e configurato in Adobe Experience Manager come frammenti di contenuto.

1. **[Assegnazione tag](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#manage-tags)**: i frammenti di contenuto devono essere contrassegnati con il tag specifico di Journey Optimizer (`ajo-enabled:{OrgId}/{SandboxName}`).

1. **[Pubblicazione](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#publishing-and-previewing-a-fragment)**: i frammenti di contenuto vengono pubblicati in Adobe Experience Manager, rendendoli disponibili in Journey Optimizer.

1. **[Accesso](#aem-add)**: Journey Optimizer recupera e visualizza in tempo reale i frammenti di contenuto disponibili dall&#39;istanza Adobe Experience Manager Publish.

1. **[Integrazione](#aem-add)**: i frammenti di contenuto sono selezionati e integrati in campagne o percorsi.

## Creare e assegnare un tag in Experience Manager

Prima di utilizzare il frammento di contenuto in Journey Optimizer, è necessario creare un tag specifico per Journey Optimizer:

1. Accedi al tuo ambiente **Experience Manager**.

1. Dal menu **Strumenti**, seleziona **Assegnazione tag**.

   ![](assets/do-not-localize/aem_tag_1.png)

1. Fare clic su **Crea tag**.

1. Verificare che l&#39;ID sia conforme alla sintassi seguente: `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}`.

1. Fai clic su **Crea**.

1. Definisci il modello per frammenti di contenuto come descritto nella [documentazione di Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragment-models){target="_blank"} e assegna il nuovo tag Journey Optimizer creato.

Questa connessione in tempo reale garantisce che il contenuto sia sempre aggiornato, ma significa anche che eventuali modifiche ai frammenti pubblicati influiranno immediatamente sulle campagne e sui percorsi attivi.

Ora puoi iniziare a creare e configurare il frammento di contenuto per un utilizzo successivo in Journey Optimizer. Ulteriori informazioni sono disponibili nella [documentazione di Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing){target="_blank"}.

## Aggiungere frammenti di contenuto Experience Manager {#aem-add}

Dopo aver creato e personalizzato i frammenti di contenuto di AEM, puoi importarli nella campagna o nel percorso di ottimizzazione del Percorso.

1. Crea la tua [campagna](../campaigns/create-campaign.md) o [Percorso](../building-journeys/journey-gs.md).

1. Per accedere al frammento di contenuto AEM, fai clic sull&#39;![icona Personalization](assets/do-not-localize/Smock_PersonalizationField_18_N.svg) in un campo di testo qualsiasi oppure apri il codice sorgente tramite un componente di contenuto HTML.

   ![](assets/aem_campaign_2.png)

1. Dal menu **[!UICONTROL Frammento di contenuto di AEM]** nel riquadro a sinistra, fare clic su **[!UICONTROL Apri selettore CF di AEM]**.

   ![](assets/aem_campaign_3.png)

1. Seleziona un **[!UICONTROL frammento di contenuto]** dall&#39;elenco disponibile per l&#39;importazione nel contenuto di Journey Optimizer.

1. Fai clic su **[!UICONTROL Mostra filtri]** per ottimizzare l&#39;elenco dei frammenti di contenuto.

   Per impostazione predefinita, il filtro Frammento di contenuto è predefinito per visualizzare solo il contenuto approvato.

   ![](assets/aem_campaign_4.png)

1. Dopo aver selezionato il **[!UICONTROL frammento di contenuto]**, fai clic su **[!UICONTROL Seleziona]** per aprirlo.

   ![](assets/aem_campaign_5.png)

1. Fai clic su **[!UICONTROL Visualizza frammento]** per visualizzare le informazioni sul frammento. L&#39;apertura del menu **[!UICONTROL Informazioni frammento]** comporta l&#39;attivazione della modalità di sola lettura per l&#39;editor.

   Seleziona **[!UICONTROL Anteprima]** dal menu di destra per visualizzare il frammento in Adobe Experience Manager.

   ![](assets/aem_campaign_7.png)

1. Fai clic sull&#39;![icona Altre azioni](assets/do-not-localize/Smock_MoreSmallList_18_N.svg) per accedere al menu avanzato del frammento:

   * **[!UICONTROL Scambia frammento]**
   * **[!UICONTROL Esplora riferimenti]**
   * **[!UICONTROL Apri in AEM]**

   ![](assets/aem_campaign_8.png)

1. Scegli i campi desiderati dal **[!UICONTROL frammento]** da aggiungere al contenuto.
   <!--
    Note that if you choose to copy the value, any future updates to the Content Fragment will not be reflected in your campaign or journey. However, using dynamic placeholders ensures real-time updates.-->

   ![](assets/aem_campaign_6.png)

1. Per abilitare la personalizzazione in tempo reale, tutti i segnaposto utilizzati all&#39;interno di un **[!UICONTROL frammento di contenuto]** devono essere dichiarati esplicitamente dall&#39;utente come parametri nel tag helper del frammento. Puoi mappare questi segnaposto ad attributi di profilo, attributi contestuali, stringhe statiche o variabili predefinite utilizzando i metodi seguenti:

   1. **Mappatura attributi contestuali o di profilo**: assegnare il segnaposto a un attributo contestuale o di profilo, ad esempio nome = profile.person.name.firstName.

   1. **Mappatura stringa statica**: assegna un valore stringa fisso inserendolo tra virgolette doppie, ad esempio nome = &quot;John&quot;.

   1. **Mappatura variabile**: fare riferimento a una variabile dichiarata in precedenza all&#39;interno dello stesso HTML, ad esempio name = &#39;variableName&#39;.
In questo caso, assicurati che **_variableName_** sia dichiarato prima di aggiungere l&#39;ID frammento, utilizzando la seguente sintassi:

      ```html
      {% let variableName = attribute name %} 
      ```

   Nell&#39;esempio seguente, il segnaposto **_name_** è mappato all&#39;attributo **_profile.person.name.firstName_** all&#39;interno del frammento.

   ![](assets/aem_campaign_9.png){zoomable="yes"}

1. Fai clic su **[!UICONTROL Salva]**. Ora puoi testare e controllare il contenuto del messaggio come descritto in [questa sezione](../content-management/preview.md).
Dopo aver eseguito i test e convalidato il contenuto, puoi [inviare la tua campagna](../campaigns/review-activate-campaign.md) o [pubblicare il percorso](../building-journeys/publish-journey.md) al tuo pubblico.

Adobe Experience Manager consente di identificare le campagne o i percorsi Journey Optimizer in cui viene utilizzato un frammento di contenuto. Ulteriori informazioni sono disponibili nella [documentazione di Adobe Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/extension-content-fragment-ajo-external-references).

## Risoluzione dei problemi {#troubleshooting}

In caso di problemi durante l’utilizzo di Frammenti di contenuto Adobe Experience Manager in Journey Optimizer, consulta i problemi e le risoluzioni comuni seguenti:

| Problema | Causa | Risoluzione |
|-|-|-|
| **Tag non trovato** o **Frammento di contenuto non visibile nel selettore** | La sintassi del tag Adobe Experience Manager non corrisponde al formato richiesto `ajo-enabled:{OrgId}/{SandboxName}` | Verificare che l&#39;ID tag utilizzi l&#39;**ID organizzazione** e il **Nome sandbox** corretti. Verificare che non siano presenti spazi o separatori non corretti. Ripubblica il frammento di contenuto dopo aver corretto il tag. |
| **Frammento di contenuto non visualizzato nell&#39;elenco** | Il frammento di contenuto è in stato Bozza o non approvato | Nel selettore Journey Optimizer vengono visualizzati solo i frammenti di contenuto approvati e pubblicati. Pubblica il frammento di contenuto in Adobe Experience Manager e assicurati che abbia lo stato approvato. |
| **Errore variabile non definita** | Segnaposto Personalization non dichiarato nel tag helper per frammenti | Aggiungi tutti i parametri richiesti nel tag helper per frammenti. Ogni segnaposto utilizzato nel frammento di contenuto deve essere dichiarato in modo esplicito con il relativo mapping. |
| **La bozza visualizza contenuto imprevisto** | La bozza utilizza la versione pubblicata più recente da Adobe Experience Manager | Le bozze riflettono sempre la pubblicazione più recente del frammento di contenuto in Adobe Experience Manager. Se hai apportato modifiche recenti in Adobe Experience Manager, ripubblica il frammento e aggiorna la bozza. |
| **Errore di accesso negato (CPES)** | Ruolo utente non autorizzato ad accedere ad alcuni attributi | Contatta l’amministratore di sistema per verificare che il tuo ruolo disponga delle autorizzazioni appropriate per gli attributi di profilo o contestuali utilizzati nella personalizzazione. |
| **Il frammento visualizza contenuto vuoto o mancante** | Parametri di personalizzazione o valori di fallback richiesti mancanti | Assicurati che siano forniti tutti i parametri richiesti e prendi in considerazione l’aggiunta di valori di fallback per gli attributi facoltativi. |

Se il problema persiste, contatta il rappresentante Adobe con i dettagli relativi all’ID del frammento di contenuto, alla campagna o all’ID percorso ed eventuali messaggi di errore visualizzati.
