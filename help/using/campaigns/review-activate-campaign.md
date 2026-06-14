---
solution: Journey Optimizer
product: journey optimizer
title: Rivedere e attivare una campagna di azioni
description: Scopri come rivedere e attivare campagne d'azione in [!DNL Journey Optimizer].
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: campagna, revisione, convalida, attivazione, attivazione, ottimizzatore
exl-id: 7c4afc98-0d79-4e26-90f8-558bac037169
TQID: https://experienceleague.adobe.com/BKGXccq-kwZJA-cZ4SAyf3zJBIvyJnr5V01xmbQgwmo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: a653cc2e-bc85-4353-a306-399e5b247978
subfeature_v2:
  - id: f7479fa1-474b-479d-8c98-f6cee5865a38
  - id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: a5c0537a45acbc708ce62bd05a569630230201ac
workflow-type: tm+mt
source-wordcount: 340
ht-degree: 3%

---

# Rivedere e attivare la campagna Azione {#action-campaign-review}

>[!BEGINSHADEBOX]

**In questa pagina:** controlla la configurazione e il contenuto della tua campagna di azione per rilevare eventuali errori prima di attivarla, in modo da poter inviare il messaggio immediatamente o alla data pianificata.

>[!ENDSHADEBOX]

Una volta configurata la campagna Action, devi esaminarne il parametro e il contenuto prima di attivarla. Per farlo, segui la procedura indicata di seguito.

>[!IMPORTANT]
>
> Se la campagna è soggetta a un criterio di approvazione, è necessario richiedere l’approvazione per poter inviare la campagna. [Ulteriori informazioni](../test-approve/gs-approval.md)

1. Nella schermata di configurazione della campagna, fai clic su **[!UICONTROL Verifica per attivare]** per visualizzare un riepilogo della campagna.

   ![](assets/campaign-review.png)

1. Viene visualizzato un riepilogo della configurazione della campagna, che ti consente di verificare se un parametro è errato o mancante e di modificare la campagna se necessario.

   In caso di errori, non puoi attivare la campagna. Risolvi gli errori prima di procedere.

   ![](assets/create-campaign-alerts.png)

1. Quando una campagna utilizza [criteri di decisione](../experience-decisioning/create-decision.md) nel proprio contenuto, puoi rivedere la struttura di ogni criterio e copiare i dettagli tecnici direttamente dal riepilogo della campagna. [Scopri come](../experience-decisioning/use-decision-policy.md#decision-policy-summary)

1. Verifica che la tua campagna sia configurata correttamente, quindi fai clic su **[!UICONTROL Attiva]**.

1. La campagna è attivata. Il suo stato è **[!UICONTROL Live]** o **[!UICONTROL Pianificato]** se hai immesso una data di inizio. Il messaggio configurato nella campagna viene inviato immediatamente o alla data specificata.

   Lo stato **[!UICONTROL Completato]** viene assegnato automaticamente alla campagna 3 giorni dopo la sua attivazione o alla data di fine se ha un&#39;esecuzione ricorrente. [Ulteriori informazioni sugli stati delle campagne](manage-campaigns.md#statuses).

   Se non è stata specificata alcuna data di fine, la campagna mantiene lo stato **[!UICONTROL Live]**. Per modificarlo, devi interrompere la campagna manualmente. [Scopri come interrompere una campagna](manage-campaigns.md)

1. Dopo l’attivazione di una campagna, puoi controllarne le informazioni in qualsiasi momento aprendola. Il riepilogo consente di ottenere statistiche sul numero di profili target e di azioni consegnate e non riuscite.

   Puoi anche ottenere ulteriori statistiche nei report dedicati facendo clic sul pulsante **[!UICONTROL Report]**. [Ulteriori informazioni](../reports/campaign-global-report-cja.md)

   ![](assets/create-campaign-summary.png)