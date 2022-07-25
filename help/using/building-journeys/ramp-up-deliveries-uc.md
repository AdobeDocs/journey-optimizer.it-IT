---
title: Incremento delle consegne
description: Scopri come incrementare le consegne
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 3%

---

# Caso di utilizzo: incrementare le consegne{#use-case-ramp-up-your-deliveries}

Se ti sei recentemente trasferito in un altro provider di servizi e-mail, indirizzo IP o dominio e-mail o sottodominio, devi stabilire la tua reputazione come mittente. In caso contrario, le consegne potrebbero essere bloccate o spostate nella cartella spam della cassetta postale dei destinatari. Scopri come aumentare la reputazione delle e-mail con il riscaldamento dell’IP nel [Guida alle best practice per il recapito messaggi](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html){target=&quot;_blank&quot;}.

Per scaldare l’IP, puoi gradualmente aumentare il numero delle consegne. Ulteriori informazioni [ottimizzazione del recapito messaggi in Journey Optimizer](../reports/deliverability.md).

Lo scopo di questo caso d’uso è quello di creare un percorso per incrementare le consegne delle e-mail. Per configurare questo percorso, effettua le seguenti operazioni:

1. Creare un percorso. [Ulteriori informazioni](journey-gs.md).

1. Aggiungi un **[!UICONTROL Condition]** attività al percorso. [Ulteriori informazioni](condition-activity.md).

1. In **[!UICONTROL Condition]** impostazioni dell’attività, imposta il numero massimo di destinatari per la consegna:

   1. In **[!UICONTROL Condition]** impostazioni attività, imposta **[!UICONTROL Type]** campo a **[!UICONTROL Profile cap]**. [Ulteriori informazioni](condition-activity.md#profile_cap).

   1. Imposta la **[!UICONTROL Limit]** al numero massimo di destinatari per la consegna.

   ![](assets/profile-cap-condition.png)

   Puoi aumentare gradualmente questo limite fino al numero totale di abbonati.

1. Aggiungi un **[!UICONTROL Email]** attività di azione sul percorso nominale dopo il **[!UICONTROL Condition]** attività.

   ![](assets/ramp-up-deliveries-message.png)

   Quando il percorso viene eseguito, al messaggio vengono inviati i profili in entrata, fino al numero massimo di profili specificati. Una volta raggiunto questo limite, i profili che entrano prendono il percorso alternativo.

1. Completa il percorso con le attività che preferisci.

Una volta che l’IP si è riscaldato, puoi rimuovere questa condizione.
