---
solution: Journey Optimizer
product: journey optimizer
title: Creare campagne di riscaldamento IP
description: Scopri come creare una campagna di riscaldamento IP
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pool, gruppo, sottodomini, recapito messaggi
hide: true
hidefromtoc: true
source-git-commit: ea86d44f7c9309ff69877e01cea6a13e7907a039
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 3%

---

# Creare campagne di riscaldamento IP {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="Attiva l&#39;opzione del piano di riscaldamento IP"
>abstract="Selezionare l&#39;opzione di attivazione del piano di riscaldamento IP. Una volta che la campagna è attiva, può essere associata a un piano di riscaldamento IP."

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione di guida:

* [Introduzione al riscaldamento dell’IP](ip-warmup-gs.md)
* **[Creare campagne di riscaldamento IP](ip-warmup-campaign.md)**
* [Creare un piano di riscaldamento IP](ip-warmup-plan.md)
* [Eseguire il piano di riscaldamento IP](ip-warmup-running.md)

>[!ENDSHADEBOX]

Devi creare una o più campagne con un’opzione specifica abilitata, in modo che possano essere utilizzate in un piano di riscaldamento IP.

Per creare una campagna di riscaldamento IP, segui i passaggi indicati di seguito.

1. Creare un messaggio e-mail [superficie](channel-surfaces.md) per il dominio e gli IP che hai identificato per il tuo piano di riscaldamento.<!--how do you identify these or who does it at the customer level?-->

   >[!NOTE]
   >
   >Scopri come selezionare il dominio e gli IP da utilizzare in un’area e-mail in [questa sezione](../email/email-settings.md#subdomains-and-ip-pools).

1. Creare un [campagna](../campaigns/create-campaign.md) e seleziona la [E-mail](../email/create-email.md#create-email-journey-campaign) azione.

1. Selezionate la superficie creata per il riscaldamento dell&#39;IP.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Fai clic su **[!UICONTROL Crea]**.

1. Dalla sezione **[!UICONTROL Pianificazione]** sezione, seleziona **[!UICONTROL Attivazione del piano di riscaldamento IP]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   La campagna [pianificazione](../campaigns/create-campaign.md#schedule) sarà guidato da [Piano di riscaldamento IP](ip-warmup-plan.md) sarà associato a, il che significa che la pianificazione non è più definita nella campagna stessa.

1. [Attiva](../campaigns/review-activate-campaign.md) la campagna. Una volta attivo, è pronto per l&#39;uso in un piano di riscaldamento IP.

>[!NOTE]
>
>Per una campagna live con il piano di riscaldamento IP attivato, il **[!UICONTROL Elimina]** finché non viene associato a un piano di riscaldamento IP.

Per ulteriori informazioni su come configurare una campagna, consulta [questa pagina](../campaigns/get-started-with-campaigns.md).

<!--Any recommendations when defining an audience? i.e do you have to include all your database or a limited number or according to your Excel file?-->

