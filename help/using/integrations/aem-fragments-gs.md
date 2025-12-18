---
solution: Journey Optimizer
product: journey optimizer
title: Frammenti di contenuto di AEM
description: Scopri come accedere e gestire i frammenti di contenuto di AEM
topic: Content Management
role: User
level: Beginner
source-git-commit: b06229e7a2fc64fbe28154c798b152cca8203a86
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 6%

---

# Introduzione ai frammenti di contenuto di Adobe Experience Manager {#aem-fragments}

Integrando Adobe Experience Manager as a Cloud Service con Adobe Journey Optimizer, ora puoi incorporare facilmente i frammenti di contenuto AEM nei contenuti Journey Optimizer. Questa connessione diretta facilita il processo di accesso e utilizzo dei contenuti AEM, consentendo la creazione di campagne e percorsi personalizzati e dinamici.

Per ulteriori informazioni sui frammenti di contenuto di AEM, consulta [Utilizzo dei frammenti di contenuto](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} nella documentazione di Experience Manager.

## Prima di iniziare {#start}

>[!AVAILABILITY]
>
>Per i clienti del settore sanitario, l&#39;integrazione è abilitata solo dopo aver concesso in licenza le offerte aggiuntive Journey Optimizer Healthcare Shield e Adobe Experience Manager Enhanced Security.

### Limitazioni {#limitations}

Quando si lavora con frammenti di contenuto Adobe Experience Manager in Journey Optimizer, tieni presente le seguenti limitazioni:

* **Tipi di frammenti di contenuto**: sono supportati frammenti di contenuto semplici e frammenti di contenuto nidificati. Le varianti di frammento di contenuto non sono attualmente supportate.

* **Contenuto multilingue**: è supportato solo il flusso manuale. Ogni variante di lingua deve essere creata in modo indipendente in Adobe Experience Manager, taggata, pubblicata e selezionata manualmente in Journey Optimizer. Non esiste una risoluzione automatica della lingua o un meccanismo di fallback.

* **Accesso all&#39;archivio**: Journey Optimizer si integra esclusivamente con il livello di pubblicazione Adobe Experience Manager, in cui i frammenti di contenuto sono disponibili tramite un endpoint pubblico non autenticato. Anche se gli archivi dell’Autore possono essere visualizzati nel selettore dell’archivio, in Journey Optimizer è possibile utilizzare solo i frammenti di contenuto pubblicati nel livello di pubblicazione.

* **Stato frammento di contenuto**: in Journey Optimizer vengono visualizzati frammenti di contenuto con stato **Pubblicato** e **Modificato**. In ogni caso, viene utilizzata solo l’ultima versione pubblicata. Se un frammento viene modificato dopo la pubblicazione, tali modifiche non verranno applicate in Journey Optimizer fino a quando il frammento di contenuto non viene ripubblicato in Adobe Experience Manager. Non esiste riconciliazione automatica delle versioni tra Adobe Experience Manager e Journey Optimizer.

* **Personalization**: sono supportati solo gli attributi di profilo, gli attributi contestuali, le stringhe statiche e le variabili predichiarate. Gli attributi derivati o calcolati non sono supportati.

* **Aggiornamenti e controllo delle versioni**: gli aggiornamenti dei frammenti di contenuto richiedono la ripubblicazione manuale da Adobe Experience Manager. Non esiste riconciliazione automatica delle versioni tra Adobe Experience Manager e Journey Optimizer. Quando un frammento di contenuto viene pubblicato in Adobe Experience Manager, Journey Optimizer riceve un evento e gli aggiornamenti dal lato Journey Optimizer. In caso di esito positivo, l’aggiornamento sarà disponibile dopo 5 minuti per i Percorsi unitari e nel batch successivo per i casi di utilizzo in batch.

* **Memorizzazione in cache e verifica**: i frammenti di contenuto vengono recuperati in tempo reale dal livello di pubblicazione di Adobe Experience Manager. Non esiste alcun pre-rendering o caching di snapshot. Le bozze per campagne e percorsi riflettono sempre la versione pubblicata più di recente del frammento di contenuto e non è possibile bloccare le versioni storiche per la bozza.

* **Accesso utente**: si consiglia di limitare il numero di utenti con accesso alla pubblicazione di frammenti di contenuto per ridurre il rischio di errori accidentali.


### Ciclo di vita dei frammenti di contenuto

![](assets/do-not-localize/AEM_CF.png)

I frammenti di contenuto seguono diverse fasi del ciclo di vita a seconda del livello Adobe Experience Manager in cui esistono. [Ulteriori informazioni nella documentazione di Adobe Experience Manager](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

Il contenuto viene creato e gestito nel **livello di authoring**, dove i frammenti possono avere stati come Nuovo, Bozza, Pubblicato, Modificato o Non pubblicato. Questi stati sono validi solo per il **livello di authoring** e supportano la creazione e la revisione dei contenuti.

Quando viene pubblicato un frammento di contenuto, viene creata una copia nel **livello di pubblicazione** ed esposta tramite un endpoint pubblico non autenticato. Journey Optimizer si integra esclusivamente con questo **livello di pubblicazione**.

Di conseguenza, Journey Optimizer fa emergere solo frammenti di contenuto pubblicati o modificati e utilizza sempre l’ultima versione pubblicata. Eventuali modifiche apportate dopo la pubblicazione non vengono applicate in Journey Optimizer fino a quando il frammento di contenuto non viene ripubblicato.


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
