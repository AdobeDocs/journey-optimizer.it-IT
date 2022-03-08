---
title: Utilizzare azioni personalizzate
description: Scopri come utilizzare le azioni personalizzate
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: 68407db81224e9c2b6930c800e57b65e081781fe
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 6%

---

# Utilizzare azioni personalizzate {#use-custom-actions}

Il riquadro di configurazione dell’attività mostra i parametri di configurazione dell’URL e i parametri di autenticazione configurati per l’azione personalizzata. [Ulteriori informazioni](../action/about-custom-action-configuration.md).

>[!NOTE]
>
>Non puoi passare una raccolta semplice nei parametri delle azioni personalizzate. Campi di raccolta più complessi (array di oggetti) non supportati.  Tieni presente che i parametri hanno un formato previsto (ad esempio: (stringa, decimale, ecc.). Devi fare attenzione a rispettare questi formati previsti.

## Configurazione URL

### Percorso dinamico

Se l’URL include un percorso dinamico, specifica il percorso nel **[!UICONTROL Path]** campo .

>[!NOTE]
>
>Non puoi impostare la parte statica dell’URL nel percorso, ma nella configurazione globale dell’azione personalizzata. [Ulteriori informazioni](../action/about-custom-action-configuration.md).

Per concatenare campi e stringhe di testo normale, utilizza le funzioni Stringa o il segno Più (+) nell’editor di espressioni avanzate. Racchiudere le stringhe di testo normale tra virgolette singole (&#39;) o tra virgolette doppie (&quot;). [Ulteriori informazioni](expression/expressionadvanced.md).

Questa tabella mostra un esempio di configurazione:

| Campo | Valore |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| Path | `The id of marketingCampaign + '/messages'` |

L’URL concatenato ha questo modulo:

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;campaign id=&quot;&quot;>`/messages`

![](../assets/journey-custom-action-url.png)

### Intestazioni

La **[!UICONTROL URL Configuration]** La sezione mostra i campi di intestazione dinamici, ma non i campi di intestazione costanti. I campi di intestazione dinamica sono campi di intestazione HTTP il cui valore è configurato come variabile. [Ulteriori informazioni](../action/about-custom-action-configuration.md).

Se necessario, specifica il valore dei campi di intestazione dinamici:

1. Seleziona l’azione personalizzata nel percorso.
1. Nel riquadro di configurazione, fai clic sull’icona a forma di matita accanto al campo di intestazione nel **[!UICONTROL URL Configuration]** sezione .

   ![](../assets/journey-dynamicheaderfield.png)

1. Seleziona un campo e fai clic su **[!UICONTROL OK]**.

## Parametri azione

In **[!UICONTROL Action parameters]** vedrai i parametri del messaggio definiti come _&quot;Variabile&quot;_. Per questi parametri, puoi definire dove ottenere queste informazioni (ad esempio: eventi, origini dati), passa i valori manualmente o utilizza l’editor di espressioni avanzate per casi d’uso avanzati. I casi di utilizzo avanzati possono essere di manipolazione dati e di altro utilizzo di funzioni. Vedi [Documentazione di Adobe Journey Orchestration](expression/expressionadvanced.md).

**Argomenti correlati**

[Configurare un’azione](../action/about-custom-action-configuration.md)
