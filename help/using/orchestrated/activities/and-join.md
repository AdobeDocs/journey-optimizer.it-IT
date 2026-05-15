---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività AND-join
description: Scopri come utilizzare l’attività AND-join in una campagna orchestrata
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/6mTYgjWPoUUos8rWCE5qWwPWBl4387c9SRq1U4QgreQ
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d556b755-390a-43f0-be32-a08cf6236126id: fe338112-e2ce-4876-8989-fc4d497613f1
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 276
ht-degree: 84%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="Attività AND-join"
>abstract="L’attività **And-join** consente di sincronizzare più rami di esecuzione di una campagna orchestrata. Viene attivata al termine di tutte le attività precedenti. Questo consente di assicurarti che determinate attività siano state completate prima di continuare a eseguire la campagna orchestrata."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_join"
>title="Attività di unione"
>abstract="Segnaposto per l’attività di unione."

L’attività **[!UICONTROL AND-join]** è un’attività di **[!UICONTROL Controllo del flusso]**. Consente di sincronizzare più rami di esecuzione di una campagna orchestrata.

Questa attività attiva la relativa transizione in uscita solo dopo che tutte le transizioni in entrata sono state attivate; in altre parole, dopo che tutte le attività precedenti sono state completate. Questo ti consente di verificare che alcune attività siano state completate prima di continuare a eseguire la campagna orchestrata.

## Configurare l’attività And-join{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="Opzioni di unione"
>abstract="Seleziona le attività che vuoi unire. Nel menu a discesa **Set primario**, scegli la popolazione di transizione in entrata da mantenere."

Per configurare l’attività **[!UICONTROL AND-join]**, segui questi passaggi:

![](../assets/workflow-andjoin.png)

1. Aggiungi più attività, come le attività del canale, per creare almeno due rami di esecuzione diversi.

1. Inserisci un’attività **[!UICONTROL AND-join]** in uno qualsiasi dei rami.

1. Nella sezione **[!UICONTROL Opzioni di unione]**, seleziona tutte le attività precedenti che desideri unire.

1. Nel menu a discesa **[!UICONTROL Set primario]**, scegli la popolazione di transizione in entrata da mantenere.

## Esempio{#and-join-example}

Questo esempio illustra due rami coordinati della campagna, ciascuno con una consegna e-mail, il cui targeting sono rispettivamente i membri di livello Gold e quelli di livello Silver. **[!UICONTROL AND-join]** si attiva quando vengono attivate entrambe le transizioni in ingresso e l’SMS verrà inviato solo dopo il completamento di entrambe le consegne e-mail, dopo un ritardo di 7 giorni.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
