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
source-git-commit: 1ec2c406e777e08de97c3ad53cee5986afeb3c44
workflow-type: tm+mt
source-wordcount: '344'
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

Prima di creare il piano di riscaldamento IP in [!DNL Journey Optimizer], devi innanzitutto creare una o più campagne con l’opzione dedicata abilitata, in modo che possano essere utilizzate in un piano di riscaldamento IP.

Per creare una campagna di riscaldamento IP, segui i passaggi indicati di seguito.

1. Creare un [email](../email/email-settings.md) channel [superficie](channel-surfaces.md) per il dominio e gli IP che hai identificato per il tuo piano di riscaldamento.

   >[!NOTE]
   >
   >Scopri come selezionare il dominio e gli IP da utilizzare in un’area e-mail in [questa sezione](../email/email-settings.md#subdomains-and-ip-pools).
   >
   >Se necessario, rivolgiti al tuo consulente del team Deliverability per identificare il dominio e gli IP da utilizzare per il piano di riscaldamento dell’IP.<!--TBC-->

1. Creare un [campagna](../campaigns/create-campaign.md) e seleziona la [E-mail](../email/create-email.md#create-email-journey-campaign) azione.

1. Selezionate la superficie creata per il riscaldamento dell&#39;IP.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Fai clic su **[!UICONTROL Crea]**.

1. Dalla sezione **[!UICONTROL Pianificazione]** sezione, seleziona **[!UICONTROL Attivazione del piano di riscaldamento IP]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   La campagna [pianificazione](../campaigns/create-campaign.md#schedule) sarà guidata dal piano di riscaldamento IP a cui sarà associata, il che significa che la pianificazione non è più definita nella campagna stessa.

1. Completa i passaggi per creare una campagna e-mail, ad esempio la definizione delle proprietà della campagna, [pubblico](../audience/about-audiences.md)<!--best practices for IP warmup in terms of audience?-->, e [contenuto](../email/get-started-email-design.md#key-steps).

   >[!NOTE]
   >
   >Per ulteriori informazioni su come configurare una campagna, consulta [questa pagina](../campaigns/get-started-with-campaigns.md).

1. [Attiva](../campaigns/review-activate-campaign.md) la campagna.

   >[!NOTE]
   >
   >Per una campagna live con il piano di riscaldamento IP attivato, il **[!UICONTROL Elimina]** finché non viene associato a un piano di riscaldamento IP. Una volta utilizzata in un piano di riscaldamento IP, la campagna non può più essere eliminata.

1. La campagna viene visualizzata in **[!UICONTROL Campagne]** elenco. Per recuperare facilmente tutte le campagne di riscaldamento IP create nella sandbox corrente, puoi filtrare per opzione la campagna **[!UICONTROL Riscaldamento IP]**.

   ![](assets/ip-warmup-campaign-filter.png)

Una volta pubblicata, la campagna è pronta per essere utilizzata in un piano di riscaldamento IP. [Ulteriori informazioni](ip-warmup-plan.md)

<!--Any recommendations when defining an audience? i.e do you have to include all your database or a limited number or according to your Excel file?-->

