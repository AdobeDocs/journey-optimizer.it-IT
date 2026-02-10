---
solution: Journey Optimizer
product: journey optimizer
title: Inviare dati ad AEP
description: Scopri come inviare dati ad AEP
feature: Journeys, Use Cases
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: percorso, caso d’uso
version: Journey Orchestration
source-git-commit: 70653bafbbe8f1ece409e3005256d9dff035b518
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 2%

---

# Caso d&#39;uso: creare un&#39;azione personalizzata per inviare dati a [!DNL Adobe Experience Platform]{#send-data-to-aep}

Se di recente sei passato a un altro provider di servizi e-mail, indirizzo IP o dominio o sottodominio e-mail, stabilisci la tua reputazione di mittente. In caso contrario, le consegne potrebbero essere bloccate o spostate nelle cartelle di posta indesiderata dei destinatari. Per maggiori informazioni, consulta la [Guida alle best practice per il recapito messaggi](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=it){target="_blank"}.

Per riscaldare l’IP, puoi aumentare gradualmente il numero di consegne. Ulteriori informazioni sull&#39;ottimizzazione del recapito messaggi in Journey Optimizer[.](../reports/deliverability.md)

Lo scopo di questo caso d’uso è la creazione di un percorso per incrementare le consegne di e-mail. Per configurare il percorso, eseguire la procedura seguente:

1. Creazione di un percorso. [Ulteriori informazioni](journey-gs.md).

1. Aggiungi un&#39;attività **[!UICONTROL Condition]** al percorso. [Ulteriori informazioni](condition-activity.md).

1. Nelle impostazioni dell&#39;attività **[!UICONTROL Condition]**, imposta il numero massimo di destinatari per la consegna:

   1. Nelle impostazioni dell&#39;attività **[!UICONTROL Condition]**, impostare il campo **[!UICONTROL Type]** su **[!UICONTROL Limite del profilo]**. [Ulteriori informazioni](condition-activity.md#profile_cap).

   1. Imposta il campo **[!UICONTROL Limite]** sul numero massimo di destinatari per questa consegna.

   ![Condizione limite profilo per controllare il volume di esecuzione azioni personalizzato](assets/profile-cap-condition.png)

   Puoi aumentare gradualmente questo limite fino al numero totale dei tuoi abbonati.

1. Aggiungi un&#39;attività di azione **[!UICONTROL Email]** al percorso nominale dopo l&#39;attività **[!UICONTROL Condition]**.

   ![Percorso con azione personalizzata per l&#39;invio di dati al sistema esterno](assets/ramp-up-deliveries-message.png)

   Quando il percorso è in esecuzione, il messaggio viene inviato ai profili in entrata, fino al numero massimo di profili specificato. Quando questo limite viene raggiunto, i profili in ingresso seguono il percorso alternativo.

1. Completa il percorso con le attività che preferisci.

Dopo il riscaldamento dell’IP, puoi rimuovere questa condizione.
