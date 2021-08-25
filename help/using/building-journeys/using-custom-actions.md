---
title: Utilizzare azioni personalizzate
description: Scopri come utilizzare le azioni personalizzate
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: 6b18f009a3c907649fd1e0261ffc7cfcc5acaef4
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 10%

---

# Utilizzare azioni personalizzate {#section_f2c_hbg_nhb}

Il riquadro di configurazione dell’attività mostra i parametri di configurazione dell’URL e i parametri di autenticazione configurati per l’azione personalizzata. [Ulteriori informazioni](../action/about-custom-action-configuration.md).

>[!NOTE]
>
>Non puoi passare una raccolta semplice nei parametri delle azioni personalizzate. Campi di raccolta più complessi (array di oggetti) non supportati.  Tieni presente che i parametri hanno un formato previsto (ad esempio: (stringa, decimale, ecc.). Devi fare attenzione a rispettare questi formati previsti.

## Configurazione URL

### Percorso dinamico

Se l’URL include un percorso dinamico, specifica il percorso nel campo **[!UICONTROL Path]** .

>[!NOTE]
>
>Non puoi impostare la parte statica dell’URL nel percorso, ma nella configurazione globale dell’azione personalizzata. [Ulteriori informazioni](../action/about-custom-action-configuration.md).

Per concatenare campi e stringhe di testo normale, utilizza le funzioni Stringa o il segno Più (+) nell’editor di espressioni avanzate. Racchiudere le stringhe di testo normale tra virgolette singole (&#39;) o tra virgolette doppie (&quot;). [Ulteriori informazioni](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html?lang=it){target=&quot;_blank&quot;}.

Questa tabella mostra un esempio di configurazione:

| Campo | Valore |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| Path | `The id of marketingCampaign + '/messages'` |

L’URL concatenato ha questo modulo:

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;campaign ID=&quot;&quot;>`/messages`

![](../assets/journey-custom-action-url.png)

### Intestazioni

La sezione **[!UICONTROL URL Configuration]** mostra i campi di intestazione dinamici, ma non i campi di intestazione costanti. I campi di intestazione dinamica sono campi di intestazione HTTP il cui valore è configurato come variabile. [Ulteriori informazioni](../action/about-custom-action-configuration.md).

Se necessario, specifica il valore dei campi di intestazione dinamici:

1. Seleziona l’azione personalizzata nel percorso.
1. Nel riquadro di configurazione, fai clic sull’icona a forma di matita accanto al campo intestazione nella sezione **[!UICONTROL URL Configuration]** .

   ![](../assets/journey-dynamicheaderfield.png)

1. Seleziona un campo e fai clic su **[!UICONTROL OK]**.

## Parametri azione

Nella sezione **[!UICONTROL Action parameters]** vedrai i parametri del messaggio definiti come _&quot;Variable&quot;_. Per questi parametri, puoi definire dove ottenere queste informazioni (ad esempio: eventi, origini dati), passa i valori manualmente o utilizza l’editor di espressioni avanzate per casi d’uso avanzati. I casi di utilizzo avanzati possono essere di manipolazione dati e di altro utilizzo di funzioni. Consulta la [documentazione del Journey Orchestration di Adobe](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html){target=&quot;_blank&quot;}.

**Argomenti correlati**

[Configurare un’azione](../action/about-custom-action-configuration.md)
