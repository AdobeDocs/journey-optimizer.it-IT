---
solution: Journey Optimizer
product: journey optimizer
title: Considerazioni e risoluzione dei problemi relativi ai frammenti di contenuto di Adobe Experience Manager
description: Considerazioni e problemi comuni relativi ai frammenti di contenuto di AEM in Journey Optimizer.
topic: Content Management
role: User
level: Beginner
exl-id: de4f441e-c3a3-4759-a634-bc9029328ebb
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: c7dc31c0-c4f7-42a7-8cf5-a8c5aeb0de74
source-git-commit: 6dbdae6edd95d97e039565ed5c6e3cab9f4a19d8
workflow-type: tm+mt
source-wordcount: 793
ht-degree: 1%

---

# Considerazioni e risoluzione dei problemi {#aem-fragments-limitations}

>[!BEGINSHADEBOX]

**In questa pagina:** rivedi le considerazioni chiave e i passaggi per la risoluzione dei problemi relativi ai frammenti di contenuto Adobe Experience Manager in Journey Optimizer, con informazioni sui tipi di frammenti, sul contenuto multilingue, sull&#39;accesso all&#39;archivio, sulla personalizzazione e sugli errori più comuni.

>[!ENDSHADEBOX]

## Considerazioni chiave {#considerations}

Quando si utilizzano frammenti di contenuto di [!DNL Adobe Experience Manager] in [!DNL Journey Optimizer], tenere presente quanto segue:

* **Tipi di frammenti di contenuto**
   * Sono supportati frammenti di contenuto semplici, frammenti di contenuto nidificati e **varianti di frammenti di contenuto**. Scegliere la variante quando si inserisce il frammento in [!DNL Journey Optimizer]. Se non selezioni una variante, viene utilizzata la variante **Main** (il contenuto principale del frammento in [!DNL Adobe Experience Manager]).

* **Contenuto multilingue**
   * Ogni variante deve essere creata, contrassegnata e pubblicata in [!DNL Adobe Experience Manager]. In [!DNL Journey Optimizer], selezionare la variante di frammento che corrisponde a ogni lingua o lingua del messaggio.
   * Non esiste alcuna risoluzione automatica della lingua o fallback tra varianti.

* **Accesso all&#39;archivio**
   * [!DNL Journey Optimizer] si integra solo con il livello [!DNL Adobe Experience Manager] **Pubblica** (Sites, Frammenti di contenuto). I frammenti di contenuto sono disponibili tramite un endpoint pubblico non autenticato.
   * Gli archivi dell&#39;autore possono essere visualizzati nel selettore dell&#39;archivio, ma solo i frammenti pubblicati in **Pubblica** possono essere utilizzati in [!DNL Journey Optimizer].

* **Stato frammento di contenuto**
   * I frammenti possono mostrare lo stato **[!UICONTROL Pubblicato]** o **[!UICONTROL Modificato]**; [!DNL Journey Optimizer] utilizza sempre la **versione pubblicata più recente**.
   * Le modifiche apportate dopo la pubblicazione non verranno applicate in [!DNL Journey Optimizer] finché il frammento non verrà ripubblicato in [!DNL Adobe Experience Manager]. Non è disponibile la riconciliazione automatica delle versioni tra i due prodotti.

* **Personalizzazione**
   * Supportato: attributi di profilo, attributi contestuali, stringhe statiche e variabili predichiarate.
   * Non supportato: attributi derivati o calcolati.

* **Aggiornamenti e controllo delle versioni**
   * Gli aggiornamenti richiedono la ripubblicazione manuale da [!DNL Adobe Experience Manager]. Non è disponibile la riconciliazione automatica delle versioni.
   * Quando un frammento di contenuto viene pubblicato o ripubblicato in [!DNL Adobe Experience Manager], [!DNL Journey Optimizer] lo aggiorna e aggiorna **tutte le varianti del frammento a cui si fa riferimento** nelle campagne o nei percorsi attivi.
   * L&#39;[!DNL Adobe Experience Manager] [azione di pubblicazione](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/manage-publication) può essere posticipata. Al termine, [!DNL Journey Optimizer] riceve un evento e aggiorna il contenuto.
   * Dopo un aggiornamento riuscito, le modifiche sono generalmente disponibili entro circa **5 minuti** per i percorsi unitari e nel **batch successivo** per i casi di utilizzo batch.

* **Memorizzazione in cache e verifica**
   * Quando un frammento viene aggiunto per la prima volta a una campagna o a un percorso, [!DNL Journey Optimizer] lo memorizza in cache. Se si seleziona un frammento già utilizzato altrove tramite **[!UICONTROL Apri AEM Content Advisor]**, verrà caricato dalla cache di [!DNL Journey Optimizer].
   * Dopo aver ripubblicato un frammento modificato in [!DNL Adobe Experience Manager], [!DNL Journey Optimizer] ascolta l&#39;evento e aggiorna la cache.
   * Le bozze riflettono sempre la **versione pubblicata più di recente**; non è possibile bloccare una versione cronologica per le bozze.

## Risoluzione dei problemi {#troubleshooting}

In caso di problemi durante l’utilizzo di Frammenti di contenuto Adobe Experience Manager in Journey Optimizer, consulta i problemi e le risoluzioni comuni seguenti:

| Problema | Causa | Risoluzione |
|-|-|-|
| **Tag non trovato** o **Frammento di contenuto non visibile nel selettore** | La sintassi del tag Adobe Experience Manager non corrisponde al formato richiesto `ajo-enabled:{OrgId}/{SandboxName}` | Verificare che l&#39;ID tag utilizzi l&#39;**ID organizzazione** e il **Nome sandbox** corretti. Verificare che non siano presenti spazi o separatori non corretti. Ripubblica il frammento di contenuto dopo aver corretto il tag. |
| **Frammento di contenuto non visualizzato nell&#39;elenco** | Il frammento di contenuto è in stato Bozza o non pubblicato | Nel selettore Journey Optimizer vengono visualizzati solo i frammenti di contenuto approvati e pubblicati. Pubblica il frammento di contenuto in Adobe Experience Manager e assicurati che abbia lo stato pubblicato. |
| **Errore variabile non definita** | Segnaposto Personalization non dichiarato nel tag helper per frammenti | Aggiungi tutti i parametri richiesti nel tag helper per frammenti. Ogni segnaposto utilizzato nel frammento di contenuto deve essere dichiarato in modo esplicito con il relativo mapping. |
| **La bozza visualizza contenuto imprevisto** | La bozza utilizza la versione pubblicata più recente da Adobe Experience Manager | Le bozze riflettono sempre la pubblicazione più recente del frammento di contenuto in Adobe Experience Manager. Se hai apportato modifiche recenti in Adobe Experience Manager, ripubblica il frammento e aggiorna la bozza. |
| **Errore di accesso negato (CPES)** | Ruolo utente non autorizzato ad accedere ad alcuni attributi | Contatta l’amministratore di sistema per verificare che il tuo ruolo disponga delle autorizzazioni appropriate per gli attributi di profilo o contestuali utilizzati nella personalizzazione. |
| **Il frammento visualizza contenuto vuoto o mancante** | Parametri di personalizzazione o valori di fallback richiesti mancanti | Assicurati che siano forniti tutti i parametri richiesti e prendi in considerazione l’aggiunta di valori di fallback per gli attributi facoltativi. |
| **L&#39;immagine non viene riprodotta o appare interrotta** | L’URL immagine nel frammento di contenuto è un percorso relativo o non è raggiungibile dal canale | Utilizza **URL assoluti** (`https://...`) per i campi immagine. I percorsi relativi da Adobe Experience Manager non sono supportati. Conferma l’URL in un browser o nell’anteprima di un messaggio. |
| **Il collegamento Experience League AEM restituisce 404** | Segnalibro non aggiornato, build di anteprima o pagina della guida di AEM non pubblicata | Apri l&#39;argomento [Frammenti di contenuto con Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} dalla documentazione live di Experience Manager e passa dal sommario nella pagina oppure cerca il nome della sezione (ad esempio **Configurazione Dispatcher**). |

Se il problema persiste, contatta il rappresentante Adobe con i dettagli relativi all’ID del frammento di contenuto, alla campagna o all’ID percorso ed eventuali messaggi di errore visualizzati.
