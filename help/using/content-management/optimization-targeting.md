---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare il targeting nell’ottimizzazione dei messaggi
description: Scopri come sfruttare le regole di targeting per fornire contenuti personalizzati a segmenti di pubblico specifici.
role: User
level: Intermediate
keywords: targeting, ottimizzazione, pubblico, personalizzazione, regole
source-git-commit: 27de3d2171e6f6575eb66ada20f951f6cb3abc98
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 0%

---

# Usa targeting {#targeting}

>[!CONTEXTUALHELP]
>id="ajo_content_targeting_fallback"
>title="Cos’è il contenuto di fallback?"
>abstract="Il contenuto di fallback consente al pubblico di ricevere un contenuto predefinito quando non è stata qualificata alcuna regola di targeting.</br>Se non selezioni questa opzione, i tipi di pubblico non idonei per una regola di targeting definita sopra non riceveranno contenuto."

Il targeting offre contenuti personalizzati a segmenti di pubblico specifici in base agli attributi del profilo utente o agli attributi contestuali.

A differenza della sperimentazione, che è un’assegnazione casuale del contenuto di un messaggio, il targeting è deterministico in termini di distribuzione del contenuto al pubblico giusto.

Con il targeting è possibile definire regole specifiche in base a:

* **Attributi del profilo utente** come la posizione (esempio: geotargeting), età o preferenze. Ad esempio, negli Stati Uniti gli utenti possono vedere una promozione &quot;Golden Gate&quot;, mentre in Francia gli utenti possono vedere una promozione &quot;Eiffel Tower&quot;.

* **Dati contestuali** come tipo di dispositivo (esempio: device-targeting), l’ora del giorno o i dettagli della sessione. Ad esempio, gli utenti desktop ricevono contenuti ottimizzati per il desktop, mentre gli utenti mobili ricevono contenuti ottimizzati per il mobile.

* **Tipi di pubblico** che possono essere utilizzati per includere o escludere profili con una particolare appartenenza al pubblico.

Per impostare il targeting, segui i passaggi indicati di seguito.

1. Crea un [percorso](../building-journeys/journey-gs.md#jo-build) o una [campagna](../campaigns/create-campaign.md).

   >[!NOTE]
   >
   >Se fai parte di un percorso, aggiungi un&#39;attività **[!UICONTROL Azione]**, scegli un&#39;attività canale e seleziona **[!UICONTROL Configura azione]**. [Ulteriori informazioni](../building-journeys/journey-action.md#add-action)

1. Dalla scheda **[!UICONTROL Azioni]**, seleziona almeno un&#39;azione.

1. Nella sezione **[!UICONTROL Ottimizzazione]**, seleziona **[!UICONTROL Crea regola di targeting]**.

   ![](../campaigns/assets/msg-optimization-select-targeting.png){width=85%}

1. Fai clic su **[!UICONTROL Crea regola]** > **[!UICONTROL Crea nuovo]** e utilizza il generatore di regole per definire i criteri in movimento.

   ![](../campaigns/assets/msg-optimization-create-rule.png){width=100%}

   Ad esempio, definisci una regola per i residenti negli Stati Uniti, una regola per i residenti in Francia e una regola per i residenti in India.

   ![](../campaigns/assets/msg-optimization-create-targeting.png){width=85%}

1. Puoi anche fare clic su **[!UICONTROL Crea regola]** > **[!UICONTROL Seleziona regola]** per selezionare una regola di targeting esistente creata dal menu **[!UICONTROL Regole]**. [Ulteriori informazioni](../experience-decisioning/rules.md)

   ![](../campaigns/assets/msg-optimization-select-rule.png){width=70%}

   In questo caso, la formula che costituisce la regola viene semplicemente copiata nel percorso o nella campagna. Eventuali modifiche successive apportate alla regola dal menu **[!UICONTROL Regole]** non influiranno sulla copia del percorso o della campagna.

   >[!AVAILABILITY]
   >
   >[La creazione di regole di targeting](../experience-decisioning/rules.md#create) dal menu dedicato [!DNL Journey Optimizer] è attualmente disponibile per le organizzazioni che hanno acquistato l&#39;offerta del componente aggiuntivo Decisioning e per le altre organizzazioni (disponibilità limitata).
   >
   >Questa capacità verrà gradualmente estesa a tutti i clienti. Nel frattempo, contatta il tuo rappresentante Adobe per ottenere l’accesso.

1. Dopo aver aggiunto una regola, puoi comunque modificarla. Scegli **[!UICONTROL Modifica in linea]** per aggiornarlo in movimento utilizzando il generatore di regole, oppure **[!UICONTROL Seleziona regola]** per raccogliere un&#39;altra regola esistente.

   ![](../campaigns/assets/msg-optimization-modify-rule.png){width=100%}

   >[!NOTE]
   >
   >La modifica in linea di una regola non influisce sulla regola esistente da cui ha origine.

1. Selezionare l&#39;opzione **[!UICONTROL Abilita contenuto di fallback]** in base alle esigenze. Il contenuto di fallback consente al pubblico di ricevere un contenuto predefinito quando non sono qualificate regole di targeting.

   >[!NOTE]
   >
   >Se non selezioni questa opzione, i tipi di pubblico non idonei per una regola di targeting definita sopra non riceveranno contenuto.

1. Salva le impostazioni della regola di targeting.

1. Nella scheda **[!UICONTROL Azioni]**, seleziona **[!UICONTROL Modifica contenuto]**.

1. Progetta il contenuto appropriato per ogni gruppo definito dalle impostazioni delle regole di targeting.

   ![](../campaigns/assets/msg-optimization-targeting-design.png){width=85%}

   In questo esempio, progetta un contenuto specifico per i residenti negli Stati Uniti, un contenuto diverso per i residenti francesi e un altro contenuto per i residenti in India.

1. [Attiva](review-activate-campaign.md) il percorso o la campagna.

Una volta che il percorso/la campagna è attivo, vengono inviati contenuti personalizzati per ciascun target in modo che i residenti degli Stati Uniti ricevano un messaggio specifico, i residenti della Francia un messaggio diverso e così via.

<!--Default content:

* If no targeting rules match, default content can be delivered.

* If default content is not enabled, passthrough behavior ensures lower-priority campaigns are evaluated.-->

