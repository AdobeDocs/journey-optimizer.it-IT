---
title: Elenco consentiti
description: Scopri come utilizzare l’elenco Consentiti.
feature: Consegna
topic: Gestione dei contenuti
role: User
level: Intermediate
source-git-commit: e2743c8fa624a7a95b12c3adb5dc17a1b632c25d
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 1%

---

# Elenco Consentiti {#allow-list}

È ora possibile definire un elenco di sicurezza per l’invio specifico a livello di [sandbox](administration/sandboxes.md) per disporre di un ambiente sicuro a scopo di test. In un’istanza non di produzione, in cui possono verificarsi errori, l’elenco Consentiti ti assicura di non correre il rischio di inviare messaggi indesiderati ai clienti.

L’elenco Consentiti ti consente di specificare singoli indirizzi e-mail o domini che saranno gli unici destinatari o domini autorizzati a ricevere le e-mail che stai inviando da una sandbox specifica. Questo può impedire l’invio accidentale di e-mail a veri indirizzi dei clienti in un ambiente di test.

>[!CAUTION]
>
>Questa funzione è **non** disponibile nelle sandbox di produzione. Si applica solo al canale e-mail.

## Abilitare l’elenco Consentiti {#enable-allow-list}

Per abilitare questa funzione in una sandbox non di produzione, aggiorna l’elenco Consentiti in modo che non sia più vuoto. Per disattivarlo, svuotare l&#39;elenco Consentiti in modo che sia nuovamente vuoto.

Ulteriori informazioni sulla logica di elenco Consentiti in [questa sezione](#logic).

<!--
To enable the allowed list on a non-production sandbox, you need to make an Adobe API call.

* Using this API, you can also disable the feature at any time.

* You can update the allowed list before or after enabling the feature.

* The allowed list logic applies when the feature is enabled and if the allowed list is not empty. Learn more in this section (logic).
-->

>[!NOTE]
>
>Quando abilitata, la funzione di elenco Consentiti viene rispettata durante l&#39;esecuzione dei percorsi, ma anche durante il test dei messaggi con [bozze](preview.md#send-proofs) e i percorsi di test utilizzando la modalità [test](building-journeys/testing-the-journey.md).

## Aggiungi entità all’elenco Consentiti {#add-entities}

Per aggiungere nuovi indirizzi e-mail o domini all’elenco Consentiti per una sandbox specifica, devi chiamare l’API di soppressione con il valore `ALLOWED` per l’attributo `listType` . Esempio:

![](assets/allow-list-api.png)

È possibile eseguire le operazioni **Add**, **Delete** e **Get**.

>[!NOTE]
>
>L&#39;elenco Consentiti può contenere fino a 1.000 voci.

<!--Learn more on making Adobe API calls in the [Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).-->

## Logica Elenco Consentiti {#logic}

<!-- When the allowed list is enabled (enable-allow-list) at the sandbox level using the API call above, the following applies.-->

Quando l&#39;elenco Consentiti è **vuoto**, la logica di elenco Consentiti non viene applicata. Ciò significa che puoi inviare e-mail a qualsiasi profilo, purché non siano presenti nell’ [elenco di soppressione](suppression-list.md).

Quando l&#39;elenco Consentiti è **non vuoto**, viene applicata la logica di elenco Consentiti:

* Se un&#39;entità è **non nell&#39;elenco Consentiti** e non nell&#39;elenco di soppressione, il destinatario corrispondente non riceverà l&#39;e-mail, perché è **[!UICONTROL Not allowed]**.

* Se un&#39;entità è **sull&#39;elenco Consentiti** e non sull&#39;elenco di eliminazione, l&#39;e-mail può essere inviata al destinatario corrispondente. Tuttavia, se l’entità si trova anche nell’ [elenco di soppressione](suppression-list.md), il destinatario corrispondente non riceverà l’e-mail, perché è **[!UICONTROL Suppressed]**.




