---
solution: Journey Optimizer
product: journey optimizer
title: Aumentare le consegne
description: Scopri come incrementare gradualmente le consegne
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: recapito messaggi, percorso, caso d’uso, e-mail, reputazione
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 6%

---

# Caso d’uso: aumentare gradualmente le consegne{#use-case-ramp-up-your-deliveries}

Se recentemente sei passato a un altro provider di servizi e-mail, indirizzo IP o dominio o sottodominio e-mail, devi stabilire la tua reputazione di mittente. In caso contrario, le consegne potrebbero essere bloccate o spostate nella cartella di posta indesiderata della cassetta postale dei destinatari. Scopri come aumentare la reputazione e-mail con la preparazione degli indirizzi IP nel [Guida alle best practice per la consegna](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=it){target="_blank"}.

Per riscaldare l’IP, puoi aumentare gradualmente il numero di consegne. Ulteriori informazioni su [ottimizzazione del recapito messaggi in Journey Optimizer](../reports/deliverability.md).

Lo scopo di questo caso d’uso è la creazione di un percorso per incrementare le consegne di e-mail. Per configurare il percorso, eseguire la procedura seguente:

1. Creare un percorso. [Ulteriori informazioni](journey-gs.md).

1. Aggiungi un **[!UICONTROL Condizione]** al percorso. [Ulteriori informazioni](condition-activity.md).

1. In **[!UICONTROL Condizione]** impostazioni delle attività, imposta il numero massimo di destinatari per la consegna:

   1. In **[!UICONTROL Condizione]** impostazioni delle attività, impostare **[!UICONTROL Tipo]** campo a **[!UICONTROL Limite del profilo]**. [Ulteriori informazioni](condition-activity.md#profile_cap).

   1. Imposta il **[!UICONTROL Limite]** al numero massimo di destinatari per questa consegna.

   ![](assets/profile-cap-condition.png)

   Puoi aumentare gradualmente questo limite fino al numero totale dei tuoi abbonati.

1. Aggiungi un **[!UICONTROL E-mail]** attività di azione al percorso nominale dopo il **[!UICONTROL Condizione]** attività.

   ![](assets/ramp-up-deliveries-message.png)

   Quando il percorso è in esecuzione, il messaggio viene inviato ai profili in entrata, fino al numero massimo di profili specificato. Quando questo limite viene raggiunto, i profili in ingresso seguono il percorso alternativo.

1. Completa il percorso con le attività che preferisci.

Dopo il riscaldamento dell’IP, puoi rimuovere questa condizione.
