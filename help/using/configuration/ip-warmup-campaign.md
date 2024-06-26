---
solution: Journey Optimizer
product: journey optimizer
title: Creare campagne di preparazione IP
description: Scopri come creare una campagna di riscaldamento IP
feature: Campaigns, IP Warmup Plans
topic: Administration
role: Admin
level: Intermediate
keywords: IP, pool, recapito messaggi
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: a9995ca1-d7eb-4f8d-a9d9-fe56198ac325
source-git-commit: c400104c86e1a9a2de819db7743b3f77153ad90b
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 17%

---

# Creare campagne di preparazione IP {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="Attivare l’opzione piano di riscaldamento IP"
>abstract="Quando selezioni questa opzione, la campagna può essere utilizzata in un piano di preparazione IP. La pianificazione della campagna sarà quindi guidata dal piano di preparazione IP a cui è associata."

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione:

* [Introduzione ai piani di preparazione IP](ip-warmup-gs.md)
* **[Creare campagne di riscaldamento IP](ip-warmup-campaign.md)**
* [Creare un piano di preparazione IP](ip-warmup-plan.md)
* [Eseguire il piano di preparazione IP](ip-warmup-execution.md)

>[!ENDSHADEBOX]

Prima di creare il piano di riscaldamento IP in [!DNL Journey Optimizer], devi innanzitutto creare una o più campagne progettate specificamente per l’utilizzo in un piano di riscaldamento IP<!--through a dedicated option-->.

Per creare una campagna di riscaldamento IP, segui i passaggi indicati di seguito.

1. Creare un [email](../email/email-settings.md) channel [superficie](channel-surfaces.md) per il dominio e gli IP che hai identificato per il tuo piano di riscaldamento.

   >[!NOTE]
   >
   >Scopri come selezionare il dominio e gli IP da utilizzare in un’area e-mail in [questa sezione](../email/email-settings.md#subdomains-and-ip-pools).
   >
   >Collabora con il tuo consulente di recapito messaggi per identificare il dominio e gli IP da utilizzare per il piano di riscaldamento dell’IP.<!--TBC-->

1. Creare un marketing pianificato [campagna](../campaigns/create-campaign.md) e seleziona la [E-mail](../email/create-email.md#create-email-journey-campaign) azione.

   <!--Select the Marketing category. The IP warmup plan activation option is only available for  marketing-type campaigns.-->

1. Selezionate la superficie creata per il riscaldamento dell&#39;IP.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Fai clic su **[!UICONTROL Crea]**.

1. Dalla sezione **[!UICONTROL Pianificazione]** sezione, seleziona **[!UICONTROL Attivazione del piano di riscaldamento IP]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   La campagna [pianificazione](../campaigns/create-campaign.md#schedule) sarà guidata dal piano di riscaldamento IP a cui sarà associata, il che significa che la pianificazione non è più definita nella campagna stessa.

1. Completa i passaggi per creare una campagna e-mail, ad esempio la definizione delle proprietà della campagna, [pubblico](../audience/about-audiences.md)<!--best practices for IP warmup in terms of audience?-->, e [contenuto](../email/get-started-email-design.md#key-steps).

   Tieni presente che devi selezionare un pubblico basato su regole per la tua campagna di riscaldamento IP. [Ulteriori informazioni](../audience/creating-a-segment-definition.md)

   >[!NOTE]
   >
   >Per ulteriori informazioni su come configurare una campagna, consulta [questa pagina](../campaigns/get-started-with-campaigns.md).

1. [Attiva](../campaigns/review-activate-campaign.md) la campagna. Lo stato cambia in **[!UICONTROL Live]**.

   Le regole business non devono essere utilizzate in un piano di riscaldamento IP. L’applicazione di queste regole potrebbe ostacolare il raggiungimento del numero desiderato di profili mirati per le campagne.

   >[!NOTE]
   >
   >Per una campagna live con il piano di riscaldamento IP attivato, il **[!UICONTROL Elimina]** finché non viene associato a un piano di riscaldamento IP. Una volta utilizzata in un piano, la campagna non può più essere eliminata.

1. La campagna viene visualizzata in **[!UICONTROL Campagne]** elenco. Per recuperare facilmente tutte le campagne di riscaldamento IP create nella sandbox corrente, puoi filtrare in base al **[!UICONTROL Riscaldamento IP]** opzione della campagna.

   ![](assets/ip-warmup-campaign-filter.png)

Una volta pubblicata, la campagna è pronta per essere utilizzata in un piano di riscaldamento IP. [Ulteriori informazioni](ip-warmup-plan.md)

Una campagna di riscaldamento IP può essere utilizzata solo in un piano di riscaldamento IP. Tuttavia, la stessa campagna può essere utilizzata in una o più fasi dello stesso piano di riscaldamento IP. [Ulteriori informazioni](ip-warmup-plan.md#define-phases)

>[!NOTE]
>
>Quando una campagna live viene utilizzata in un piano di riscaldamento IP, dopo che il piano è [contrassegnato come completato](ip-warmup-execution.md#mark-as-completed), lo stato di tale campagna diventa **[!UICONTROL Interrotto]**.

