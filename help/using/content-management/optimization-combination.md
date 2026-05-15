---
solution: Journey Optimizer
product: journey optimizer
title: Combinare targeting e sperimentazione
description: Scopri come combinare il targeting e gli esperimenti in un singolo percorso o campagna per creare strategie di ottimizzazione sofisticate.
role: User
level: Intermediate
keywords: ottimizzazione, targeting, sperimentazione, combinazione, avanzato
exl-id: dafcb4d3-e33c-40c5-a5c6-972822a23cc0
TQID: https://experienceleague.adobe.com/klXmy7KQLcIHm-T6BMS1RaMKrwzdCfzvK3KK6fUs7KU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 306
ht-degree: 3%

---

# Combinare targeting e sperimentazione {#combination}

Journey Optimizer consente inoltre di combinare il targeting e gli esperimenti all’interno di un singolo percorso o campagna per creare strategie più sofisticate.

In effetti, puoi utilizzare il targeting per creare diverse varianti e, per ogni variante, utilizzare la sperimentazione per ottimizzare ulteriormente ogni contenuto. In questo modo gli esperimenti sono specifici per ogni regola di targeting e non si estendono su più varianti.

Ad esempio, puoi provare una promozione del 50% rispetto a una gift card da 50 dollari per i clienti negli Stati Uniti e testare in modo diverso i clienti in Europa, ad esempio la spedizione gratuita su ordini superiori a 50 euro rispetto al 20% di sconto sul prossimo acquisto.

Per combinare sia il targeting che gli esperimenti in un percorso o in una campagna, segui i passaggi riportati di seguito.

1. Crea un percorso o una campagna in cui puoi definire diverse regole di targeting. [Scopri come](optimization-targeting.md)

   ![](../campaigns/assets/msg-optimization-create-targeting.png){width=85%}

1. Crea un esperimento per la prima regola di targeting.

1. Progetta e configura l’esperimento sui contenuti come desideri. [Scopri come](../content-management/content-experiment.md)

   ![](../campaigns/assets/msg-optimization-targeting-with-experiment.png){width=85%}

   Una volta definita la sperimentazione, questa si applica solo alla prima regola di targeting.

1. Nella scheda **[!UICONTROL Azioni]**, seleziona **[!UICONTROL Modifica contenuto]**.

1. Per il gruppo definito dalla prima regola di targeting, puoi definire un contenuto specifico per ogni variante dell’esperimento.

   Se hai aggiunto più di un’azione in entrata al percorso o alla campagna, a ogni azione si applica la stessa combinazione di targeting ed esperimento. Tuttavia, devi definire un contenuto specifico per ogni variante di ciascuna azione.

   ![](../campaigns/assets/msg-optimization-targeting-experiment-design.png){width=85%}

1. Procedi in modo simile per le altre regole di targeting e progetta il contenuto corrispondente per ogni variante.

1. Salva le modifiche e [attiva](../campaigns/review-activate-campaign.md) il percorso o la campagna.

Una volta che il percorso/la campagna è attivo, agli utenti di ciascun gruppo target vengono assegnate in modo casuale le diverse varianti di contenuto definite per il gruppo a cui appartengono.

<!--
## Reporting on Message optimization

E.g. explaining how a marketer can look at the report to determine which treatment (e.g. which message content) is performing the best for the targeting audience
-->
