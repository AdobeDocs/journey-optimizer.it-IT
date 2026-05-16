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
keywords: recapito messaggi, percorso, caso d’uso, e-mail, reputazione
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/en0jMw69ddHSQrIH05-9FfGuDwNKb36f5Lp3fLp2oAk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 300
ht-degree: 8%

---

# Caso d’uso: aumentare gradualmente le consegne{#use-case-ramp-up-your-deliveries}

Se recentemente sei passato a un altro provider di servizi e-mail, indirizzo IP o dominio o sottodominio e-mail, devi stabilire la tua reputazione di mittente. In caso contrario, le consegne potrebbero essere bloccate o spostate nella cartella di posta indesiderata della cassetta postale dei destinatari. Scopri come aumentare la reputazione delle e-mail con la preparazione degli indirizzi IP nella [Guida alle best practice per il recapito messaggi](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=it){target="_blank"}.

Per riscaldare l’IP, puoi aumentare gradualmente il numero di consegne. Ulteriori informazioni sull&#39;ottimizzazione del recapito messaggi in Journey Optimizer[&#128279;](../reports/deliverability.md).

Lo scopo di questo caso d’uso è la creazione di un percorso per incrementare le consegne di e-mail. Per configurare il percorso, eseguire la procedura seguente:

1. Creazione di un percorso. [Ulteriori informazioni](journey-gs.md).

1. Aggiungi un&#39;attività **[!UICONTROL Ottimizza]** al percorso. [Ulteriori informazioni](optimize.md).

1. Nelle impostazioni dell&#39;attività **[!UICONTROL Condition]**, imposta il numero massimo di destinatari per la consegna:

   1. Nelle impostazioni dell&#39;attività **[!UICONTROL Ottimizza]**, selezionare il metodo **[!UICONTROL Condizioni]** e impostare il campo **[!UICONTROL Tipo]** su **[!UICONTROL Limite del profilo]**. [Ulteriori informazioni](conditions.md#profile_cap).

   1. Imposta il campo **[!UICONTROL Limite]** sul numero massimo di destinatari per questa consegna.

   ![Configurazione della condizione del limite del profilo per il controllo del volume di consegna](assets/profile-cap-condition.png)

   Puoi aumentare gradualmente questo limite fino al numero totale dei tuoi abbonati.

1. Aggiungi un&#39;attività di azione **[!UICONTROL Email]** al percorso nominale dopo l&#39;attività **[!UICONTROL Condition]**.

   ![Configurazione dei messaggi e-mail nel percorso di consegna con rampe di transizione](assets/ramp-up-deliveries-message.png)

   Quando il percorso è in esecuzione, il messaggio viene inviato ai profili in entrata, fino al numero massimo di profili specificato. Quando questo limite viene raggiunto, i profili in ingresso seguono il percorso alternativo.

1. Completa il percorso con le attività che preferisci.

Dopo il riscaldamento dell’IP, puoi rimuovere questa condizione.
