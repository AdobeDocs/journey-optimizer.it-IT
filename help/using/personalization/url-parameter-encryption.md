---
solution: Journey Optimizer
product: journey optimizer
title: Crittografare i parametri URL nel tracciamento
description: Scopri come crittografare i parametri di query URL sensibili in modo che i dati PII non siano esposti in testo normale sui collegamenti di tracciamento e sulle pagine di destinazione di Journey Optimizer.
feature: Personalization
topic: Personalization
role: Admin
level: Intermediate
badge: label="Disponibilità limitata" type="Informative"
keywords: crittografia, URL, tracciamento, pagina di destinazione, registro chiavi, personalizzazione, sicurezza, privacy, sandbox
source-git-commit: 4519c873e3391b63d0e879d797a99d9e67f83b87
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 3%

---


# Crittografare i parametri URL nel tracciamento {#url-parameter-encryption}

>[!AVAILABILITY]
>
>Questa funzione è disponibile in Disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.
>
>Questa funzionalità è attualmente disponibile solo per il canale e-mail.

## Perché utilizzare la crittografia dei parametri URL? {#why-url-parameter-encryption}

I collegamenti di tracciamento personalizzati e gli URL delle pagine di destinazione spesso includono attributi di profilo, identificatori, token o altri valori nella stringa di query. Tali parametri sono generalmente visibili come testo normale nell’e-mail o nell’SMS e rimangono leggibili se qualcuno copia, condivide o segnalibro il collegamento. Questo può essere un rischio per la sicurezza e la privacy quando i valori possono includere informazioni personali (PII, personally identifiable information) o altri dati sensibili che devono proteggere.

[!DNL Journey Optimizer] fornisce un helper di crittografia nell&#39;editor di personalizzazione per consentirti di crittografare qualsiasi valore di espressione al momento del rendering (ad esempio un attributo di profilo, un token o una stringa creata da diversi campi). La crittografia richiede sempre una chiave del Registro di sistema dell&#39;organizzazione.

È possibile crittografare solo i parametri di query scelti, utilizzando le chiavi gestite dagli amministratori in un registro a livello di sandbox, in modo che i valori riservati non vengano lasciati esposti in testo non crittografato quando il collegamento viene condiviso o ispezionato.

### Come funziona {#how-it-works}

* **Gli amministratori** utilizzano il Registro di sistema delle chiavi per [creare le chiavi](#create-keys) e [gestire le chiavi](#manage-keys) in conformità ai criteri di sicurezza della tua organizzazione.
* **Gli addetti al marketing** inseriscono l&#39;helper di crittografia nell&#39;editor di personalizzazione e trasmettono il valore da proteggere più un identificatore di chiave attiva dal Registro di sistema. Per informazioni sulla sintassi e sulle opzioni, vedere [Crittografia dei parametri URL](functions/helpers.md#url-parameter-encryption-helper).

>[!IMPORTANT]
>
>La decrittografia è responsabilità della tua organizzazione. [!DNL Journey Optimizer] crittografa i valori al rendering del messaggio. Il sito web, l’app o l’API devono decrittografare i parametri utilizzando lo stesso materiale e gli stessi processi di crittografia definiti, in modo coerente con il modello di sicurezza.

### Esempio

L&#39;URL di una pagina di destinazione può utilizzare un parametro di query come `token` il cui valore è un token di stringa (ad esempio un payload JSON con identificatori di offerta o profilo). Senza crittografia, il token di stringa è visibile come testo normale nel collegamento. Se racchiudi tale valore nell’helper di crittografia, il payload sensibile viene sostituito con un testo crittografato nell’URL, lasciando invariato il resto del collegamento.

## Creare le chiavi {#create-keys}

Prima di poter utilizzare l’helper per la crittografia dei parametri URL, devi creare una chiave. A questo scopo, segui i passaggi riportati qui sotto.

<!--
>[!IMPORTANT]
>
>To access and manage keys, you you must have the **View Key Registry** and **Manage Key Registry** permissions granted. [Learn more](../administration/high-low-permissions.md)-->

1. Vai a **[!UICONTROL Amministrazione]** > **[!UICONTROL Configurazioni]**.

1. Fai clic sul pulsante **[!UICONTROL Gestisci]** per aprire il **[!UICONTROL Registro di sistema delle chiavi]**.

   ![Sezione registro chiavi nel menu Amministrazione](assets/encryption-key-registry.png){width="80%"}

1. Utilizzando il pulsante dedicato, crea le chiavi necessarie per la tua organizzazione.

   ![Pulsante Crea chiave nella sezione Registro di sistema delle chiavi](assets/encryption-create-key.png){width="80%"}

1. Assegna loro un’etichetta chiara o un identificatore a cui i team possono fare riferimento nell’editor di personalizzazione.

   ![Dettagli chiave nella sezione Registro di sistema delle chiavi](assets/encryption-key-details.png){width="80%"}

1. Fai clic su **[!UICONTROL Invia]** per confermare le modifiche.

Una volta creata una chiave, gli addetti al marketing possono utilizzare l&#39;helper per la crittografia del parametro [URL](functions/helpers.md#url-parameter-encryption-helper) nell&#39;editor di personalizzazione per crittografare valori specifici inseriti nei parametri di query URL.

## Gestione chiavi {#manage-keys}

Per gestire le chiavi, segui la procedura riportata di seguito.

1. Accedere al **[!UICONTROL Registro chiavi]**. In una vista a elenco puoi visualizzare tutte le chiavi create per la sandbox corrente.

   ![Visualizzazione elenco chiavi del Registro di sistema](assets/encryption-key-registry-list.png){width="100%"}

1. Fai clic su una chiave con lo stato **[!UICONTROL Attivo]** per aprire i dettagli della chiave.

   ![Dettagli chiave attiva](assets/encryption-key-active-details.png){width="80%"}

1. Fai clic sul pulsante **[!UICONTROL Revoca]** per disabilitare definitivamente la chiave per la nuova crittografia.

   Una volta revocata una chiave, i tentativi di utilizzarla nell’helper non dovrebbero riuscire al momento del rendering. Le voci revocate rimangono visibili per il controllo di audit; i team potrebbero avere ancora bisogno del materiale corrispondente per decrittografare i payload precedenti sui propri sistemi.

1. Fai clic sul pulsante **[!UICONTROL Ruota]** per fornire nuovo materiale chiave mantenendo un identificatore di chiave stabile a cui i percorsi e le campagne fanno già riferimento.

   Il materiale precedente viene conservato nel Registro di sistema con uno stato revocato e un motivo appropriato (ad esempio un timestamp di rotazione) e una nuova riga o versione riflette la chiave attiva.

   >[!NOTE]
   >
   >Per crittografare i nuovi valori nell’editor di personalizzazione devono essere selezionate solo le chiavi attive. Non utilizzare le chiavi revocate per i nuovi contenuti.



