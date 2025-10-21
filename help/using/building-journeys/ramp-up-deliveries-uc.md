---
solution: Journey Optimizer
product: journey optimizer
title: Aumentare le consegne
description: Scopri come incrementare gradualmente le consegne
feature: Journeys, Use Cases, IP Warmup Plans
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
hide: true
hidefromtoc: true
keywords: recapito messaggi, percorso, caso d’uso, e-mail, reputazione
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 2%

---

# Caso d’uso: aumentare gradualmente le consegne{#use-case-ramp-up-your-deliveries}

Se recentemente sei passato a un altro provider di servizi e-mail, indirizzo IP o dominio o sottodominio e-mail, devi stabilire la tua reputazione di mittente. In caso contrario, le consegne potrebbero essere bloccate o spostate nella cartella di posta indesiderata della cassetta postale dei destinatari. Scopri come aumentare la reputazione delle e-mail con la preparazione degli indirizzi IP nella [Guida alle best practice per il recapito messaggi](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=it){target="_blank"}.

Per riscaldare l’IP, puoi aumentare gradualmente il numero di consegne. Ulteriori informazioni sull&#39;ottimizzazione del recapito messaggi in Journey Optimizer[.](../reports/deliverability.md)

Lo scopo di questo caso d’uso è la creazione di un percorso per incrementare le consegne di e-mail. Per configurare il percorso, eseguire la procedura seguente:

1. Creazione di un percorso. [Ulteriori informazioni](journey-gs.md).

1. Aggiungi un&#39;attività **[!UICONTROL Condition]** al percorso. [Ulteriori informazioni](condition-activity.md).

1. Nelle impostazioni dell&#39;attività **[!UICONTROL Condition]**, imposta il numero massimo di destinatari per la consegna:

   1. Nelle impostazioni dell&#39;attività **[!UICONTROL Condition]**, impostare il campo **[!UICONTROL Type]** su **[!UICONTROL Limite del profilo]**. [Ulteriori informazioni](condition-activity.md#profile_cap).

   1. Imposta il campo **[!UICONTROL Limite]** sul numero massimo di destinatari per questa consegna.

   ![](assets/profile-cap-condition.png)

   Puoi aumentare gradualmente questo limite fino al numero totale dei tuoi abbonati.

1. Aggiungi un&#39;attività di azione **[!UICONTROL Email]** al percorso nominale dopo l&#39;attività **[!UICONTROL Condition]**.

   ![](assets/ramp-up-deliveries-message.png)

   Quando il percorso è in esecuzione, il messaggio viene inviato ai profili in entrata, fino al numero massimo di profili specificato. Quando questo limite viene raggiunto, i profili in ingresso seguono il percorso alternativo.

1. Completa il percorso con le attività che preferisci.

Dopo il riscaldamento dell’IP, puoi rimuovere questa condizione.
