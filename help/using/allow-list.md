---
title: Elenco consentiti
description: Scopri come utilizzare l’elenco Consentiti.
feature: Consegna
topic: Gestione dei contenuti
role: User
level: Intermediate
source-git-commit: 288c27d4fc64a6d0a6f07b634ed044a6e858d0c1
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 2%

---

# Elenco Consentiti {#allow-list}

È ora possibile definire un elenco di sicurezza per l’invio specifico a livello di [sandbox](administration/sandboxes.md) per disporre di un ambiente sicuro a scopo di test. In un’istanza non di produzione, in cui possono verificarsi errori, l’elenco Consentiti ti assicura di non correre il rischio di inviare messaggi indesiderati ai clienti.

>[!CAUTION]
>
>Questa funzione non è disponibile nelle sandbox di produzione.

L’elenco Consentiti ti consente di specificare singoli indirizzi e-mail o domini che saranno gli unici destinatari o domini autorizzati a ricevere le e-mail che stai inviando da una sandbox specifica. Questo può impedire l’invio accidentale di e-mail a veri indirizzi dei clienti in un ambiente di test.

>[!NOTE]
>
>Questa funzione si applica solo al canale e-mail.

## Abilitare l’elenco Consentiti {#enable-allow-list}

Per abilitare l’elenco Consentiti su una sandbox non di produzione, devi effettuare un Adobe di chiamata API.

* Utilizzando questa API, puoi anche disabilitare la funzione in qualsiasi momento.

* È possibile aggiornare l’elenco Consentiti prima o dopo l’abilitazione della funzione.

* La logica di elenco Consentiti si applica quando la funzione è abilitata e se l’elenco Consentiti non è vuoto. [Ulteriori informazioni](#logic).

>[!NOTE]
>
>Quando abilitata, la funzione di elenco Consentiti viene rispettata durante l&#39;esecuzione dei percorsi, ma anche durante il test dei messaggi con [bozze](preview.md#send-proofs) e i percorsi di test utilizzando la modalità [test](building-journeys/testing-the-journey.md).

## Aggiungi entità all’elenco Consentiti {#add-entities}

>[!CAUTION]
>
>Questa funzione è **non** disponibile nelle sandbox di produzione. Si applica solo al canale e-mail.

Per aggiungere nuovi indirizzi e-mail o domini all’elenco Consentiti per una sandbox specifica, devi chiamare l’API di soppressione con il valore `ALLOWED` per l’attributo `listType` . Esempio:

![](assets/allow-list-api.png)

È possibile eseguire le operazioni **Add**, **Delete** e **Get**.

>[!NOTE]
>
>L&#39;elenco Consentiti può contenere fino a 1.000 voci.

Ulteriori informazioni sull&#39;esecuzione di chiamate API di Adobe nella [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).

## Logica Elenco Consentiti {#logic}

<!-- When the allowed list is \[enabled\]\(\add link here\) at the sandbox level using the API call above, the following applies.-->

1. Quando l&#39;elenco Consentiti è **vuoto**, la logica di elenco Consentiti non viene applicata. Ciò significa che puoi inviare e-mail a qualsiasi profilo, purché non siano presenti nell’ [elenco di soppressione](suppression-list.md).

1. Quando l&#39;elenco Consentiti è **non vuoto**, viene applicata la logica di elenco Consentiti:

   * Se un&#39;entità è **non nell&#39;elenco Consentiti** e non nell&#39;elenco di soppressione, il destinatario corrispondente non riceverà l&#39;e-mail, perché è **[!UICONTROL Not allowed]**.

   * Se un&#39;entità è **sull&#39;elenco Consentiti** e non sull&#39;elenco di eliminazione, l&#39;e-mail può essere inviata al destinatario corrispondente. Tuttavia, se l’entità si trova anche nell’ [elenco di soppressione](suppression-list.md), il destinatario corrispondente non riceverà l’e-mail, perché è **[!UICONTROL Suppressed]**.




