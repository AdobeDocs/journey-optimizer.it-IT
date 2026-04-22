---
solution: Journey Optimizer
product: journey optimizer
title: Crittografa parametri URL
description: Scopri come crittografare i parametri di query URL sensibili in modo che i dati PII non siano esposti in testo normale sui collegamenti di tracciamento e sulle pagine di destinazione di Journey Optimizer.
feature: Personalization
topic: Personalization
role: Admin
level: Intermediate
badge: label="Disponibilità limitata" type="Informative"
keywords: crittografia, URL, tracciamento, pagina di destinazione, registro chiavi, personalizzazione, sicurezza, privacy, sandbox
exl-id: 82e2b6e4-769f-4bdc-b2e2-19352fbaec8e
source-git-commit: 1039daee3b328828361976513cc4d1ba5ce1169a
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 2%

---

# Crittografa parametri URL {#url-parameter-encryption}

>[!AVAILABILITY]
>
>Questa funzione è disponibile in Disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.
>
>Questa funzionalità è attualmente disponibile solo per il canale e-mail.

## Perché utilizzare la crittografia dei parametri URL? {#why-url-parameter-encryption}

I collegamenti di tracciamento personalizzati e gli URL delle pagine di destinazione spesso includono attributi di profilo, identificatori, token o altri valori nella stringa di query. Tali parametri sono generalmente visibili come testo normale nell’e-mail o nell’SMS e rimangono leggibili se qualcuno copia, condivide o segnalibro il collegamento. Questo può essere un rischio per la sicurezza e la privacy quando i valori possono includere informazioni personali (PII, personally identifiable information) o altri dati sensibili che devono proteggere.

[!DNL Journey Optimizer] fornisce un helper di crittografia nell&#39;editor di personalizzazione per consentirti di crittografare qualsiasi valore di espressione al momento del rendering (ad esempio un attributo di profilo, un token o una stringa creata da diversi campi). La crittografia richiede sempre una chiave del Registro di sistema dell&#39;organizzazione.

You encrypt only the query parameters you choose, using keys that administrators manage in a sandbox-level registry, so confidential values are not left exposed in clear text when the link is shared or inspected.

### Come funziona {#how-it-works}

* **Administrators** use the key registry to [create keys](#create-keys) and [manage keys](#manage-keys) in accordance with your organization&#39;s security policies.
* **Marketers** insert the `Encrypt` helper in the personalization editor and pass the value to protect plus an active key identifier from the registry. Per informazioni sulla sintassi e sulle opzioni, vedere [questa sezione](functions/helpers.md#url-parameter-encryption-helper).

>[!IMPORTANT]
>
>La decrittografia è responsabilità della tua organizzazione. [!DNL Journey Optimizer] crittografa i valori al rendering del messaggio. Your website, app, or API must decrypt parameters using the same cryptographic material and processes you define—consistent with your security model.

### Esempio

A landing page URL might use a query parameter such as `token` whose value is a string token (for example a JSON payload with offer or profile identifiers). Senza crittografia, il token di stringa è visibile come testo normale nel collegamento. Se racchiudi tale valore nell’helper di crittografia, il payload sensibile viene sostituito con un testo crittografato nell’URL, lasciando invariato il resto del collegamento.

## Creare le chiavi {#create-keys}

Prima di poter utilizzare l’helper per la crittografia dei parametri URL, devi creare una chiave. A questo scopo, segui i passaggi riportati qui sotto.

>[!NOTE]
>
>Attualmente non sono disponibili autorizzazioni specifiche per accedere e gestire le chiavi. Anche i ruoli che concedono l&#39;accesso alla sezione **[!UICONTROL Configurations]** in **[!UICONTROL Administration]** concedono l&#39;accesso al Registro di sistema delle chiavi. Tuttavia, per una versione futura sono pianificate autorizzazioni specifiche.

<!--
>[!IMPORTANT]
>
>To access and manage keys, you you must have the **View Key Registry** and **Manage Key Registry** permissions granted. [Learn more](../administration/high-low-permissions.md)
-->

1. Vai a **[!UICONTROL Amministrazione]** > **[!UICONTROL Configurazioni]**.

1. Fai clic sul pulsante **[!UICONTROL Gestisci]** per aprire il **[!UICONTROL Registro di sistema delle chiavi]**.

   ![Sezione registro chiavi nel menu Amministrazione](assets/encryption-key-registry.png){width="80%"}

1. Utilizzando il pulsante dedicato, crea le chiavi necessarie per la tua organizzazione.

   ![Pulsante Crea chiave nella sezione Registro di sistema delle chiavi](assets/encryption-create-key.png){width="80%"}

1. Assegna loro un’etichetta chiara o un identificatore a cui i team possono fare riferimento nell’editor di personalizzazione.

   ![Key details in Key registry section](assets/encryption-key-details.png){width="80%"}

1. Click **[!UICONTROL Submit]** to confirm your changes.

Once a key is created, marketers can use the [URL parameter encryption](functions/helpers.md#url-parameter-encryption-helper) helper in the personalization editor to encrypt specific values that they place in URL query parameters.

## Gestione chiavi {#manage-keys}

To manage keys, follow the steps below.

1. Access the **[!UICONTROL Key registry]**. In una vista a elenco puoi visualizzare tutte le chiavi create per la sandbox corrente.

   ![Key registry list view](assets/encryption-key-registry-list.png){width="100%"}

1. Click a key with the **[!UICONTROL Active]** status to open the key details.

   ![Active key details](assets/encryption-key-active-details.png){width="80%"}

1. Click the **[!UICONTROL Revoke]** button to permanently disable the key for new encryption.

   Once a key is revoked, attempts to use it in the helper should fail at render time. Le voci revocate rimangono visibili per il controllo di audit; i team potrebbero avere ancora bisogno del materiale corrispondente per decrittografare i payload precedenti sui propri sistemi.

1. Fai clic sul pulsante **[!UICONTROL Ruota]** per fornire nuovo materiale chiave mantenendo un identificatore di chiave stabile a cui i percorsi e le campagne fanno già riferimento.

   Il materiale precedente viene conservato nel Registro di sistema con uno stato revocato e un motivo appropriato (ad esempio un timestamp di rotazione) e una nuova riga o versione riflette la chiave attiva.

   >[!NOTE]
   >
   >Per crittografare i nuovi valori nell’editor di personalizzazione devono essere selezionate solo le chiavi attive. Non utilizzare le chiavi revocate per i nuovi contenuti.

