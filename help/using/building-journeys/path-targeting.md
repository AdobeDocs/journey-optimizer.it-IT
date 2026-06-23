---
solution: Journey Optimizer
product: journey optimizer
title: Targeting del percorso
description: Scopri come utilizzare il targeting dei percorsi nei percorsi
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: targeting, regole, percorso, percorso, ottimizzazione, personalizzazione
exl-id: b30ce5c9-a0e2-4601-97a3-5bec648368e4
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1327
ht-degree: 2%

---

# Sfruttare il targeting del percorso {#targeting}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come utilizzare le regole di targeting nell&#39;attività Ottimizza per indirizzare in modo deterministico tipi di pubblico specifici lungo i percorsi di percorso corretti, con un percorso di fallback facoltativo.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_path_targeting_fallback"
>title="Cos’è un percorso di fallback?"
>abstract="I percorsi di fallback consentono al pubblico di entrare in un percorso alternativo qualora non si qualifichi alcuna regola di targeting. </br>Se questa opzione non è selezionata, qualsiasi pubblico non idoneo per una regola di targeting non entrerà nel percorso di fallback ed uscirà dal percorso."

Le regole di targeting consentono di determinare regole o qualifiche specifiche che devono essere soddisfatte affinché un cliente possa accedere a uno dei percorsi di percorso, in base a segmenti di pubblico specifici<!-- depending on profile attributes or contextual attributes-->.

A differenza della sperimentazione, che è un’assegnazione casuale di un determinato percorso, il targeting è deterministico in termini di garantire che il pubblico o il profilo giusto entri nel percorso specificato.

<!--
With targeting, specific rules can be defined based on:

* **User profile attributes** such as location (eg. geo-targeting), age, or preferences. For example, users in the US receive a "Golden Gate" promotion, while users in France receive an "Eiffel Tower" promotion.

* **Contextual data** such as device type (eg. device-targeting), time of day, or session details. For example, desktop users receive desktop-optimized content, while mobile users receive mobile-optimized content.

* **Audiences** which can be used to include or exclude profiles that have a particular audience membership.
-->

Per impostare il targeting in un percorso, segui i passaggi indicati di seguito.

1. Dalla sezione **[!UICONTROL Orchestrazione]**, trascina l&#39;attività **[!UICONTROL Ottimizza]** nell&#39;area di lavoro del percorso.

1. Aggiungi un’etichetta facoltativa che può essere utile per identificare l’attività nei rapporti e nei registri della modalità di test.

1. Selezionare **[!UICONTROL Regola di targeting]** dall&#39;elenco a discesa **[!UICONTROL Metodo]**.

   ![Selezione di regole di targeting nell&#39;attività Ottimizza](assets/journey-optimize-targeting.png){width=60%}

1. Fai clic su **[!UICONTROL Crea regola di targeting]**.

1. Fai clic su **[!UICONTROL Crea regola]** > **[!UICONTROL Crea nuovo]** e utilizza il generatore di regole per definire i criteri.

   ![Interfaccia del generatore di regole per la creazione di criteri di targeting](assets/journey-targeting-create-rule.png){width=100%}

   Definire ad esempio una regola per i membri Gold del programma fedeltà (`loyalty.status.equals("Gold", false)`) e una regola per gli altri membri (`loyalty.status.notEqualTo("Gold", false)`).

   ![Regola di targeting dello stato di fedeltà per i membri Gold e non Gold](assets/journey-targeting-rule.png)

1. Puoi anche fare clic su **[!UICONTROL Crea regola]** > **[!UICONTROL Seleziona regola]** per selezionare una regola di targeting esistente creata dal menu **[!UICONTROL Regole]**. [Ulteriori informazioni](../experience-decisioning/rules.md)

   ![Seleziona regola di targeting esistente dal menu Regole](assets/journey-targeting-select-rule.png){width=70%}

   In questo caso, la formula che costituisce la regola viene semplicemente copiata nell’attività di percorso. Eventuali modifiche successive apportate alla regola dal menu **[!UICONTROL Regole]** non influiranno sulla copia del percorso.

   >[!AVAILABILITY]
   >
   >[La creazione di regole di targeting](../experience-decisioning/rules.md#create) dal menu dedicato [!DNL Journey Optimizer] è attualmente disponibile per le organizzazioni che hanno acquistato l&#39;offerta del componente aggiuntivo Decisioning e per le altre organizzazioni (disponibilità limitata).
   >
   >Questa capacità verrà gradualmente estesa a tutti i clienti. Nel frattempo, contatta il tuo rappresentante Adobe per ottenere l’accesso.

1. Dopo aver aggiunto una regola, puoi comunque modificarla. Scegli **[!UICONTROL Modifica in linea]** per aggiornarlo in movimento utilizzando il generatore di regole, oppure **[!UICONTROL Seleziona regola]** per raccogliere un&#39;altra regola esistente.

   ![Modifica le opzioni in linea o Seleziona regola per modificare le regole di targeting](assets/journey-targeting-modify-rule.png){width=100%}

   >[!NOTE]
   >
   >La modifica in linea di una regola non influisce sulla regola esistente da cui ha origine.

1. Selezionare l&#39;opzione **[!UICONTROL Abilita percorso di fallback]** in base alle esigenze. Questa azione crea un percorso di fallback per il pubblico che non soddisfa nessuna delle regole di targeting definite in precedenza.

   >[!NOTE]
   >
   >Se non selezioni questa opzione, qualsiasi pubblico non idoneo per una regola di targeting non entra nel percorso di fallback ed esce dal percorso.

1. Fai clic su **[!UICONTROL Crea]** per salvare le impostazioni delle regole di targeting.

1. Sempre nel percorso, rilascia azioni specifiche per personalizzare ogni percorso. Ad esempio, crea un’e-mail con offerte personalizzate per i membri Gold Loyalty e un promemoria SMS per tutti gli altri membri.

   ![Percorsi Percorsi con e-mail per iscritti Gold e SMS per altri](assets/journey-targeting-paths.png)

1. Se hai selezionato l&#39;opzione **[!UICONTROL Abilita contenuto di fallback]** durante la definizione delle impostazioni della regola, definisci una o più azioni per il percorso di fallback aggiunto automaticamente.

   ![Configurazione del percorso di fallback per profili non qualificati](assets/journey-targeting-fallback.png){width=70%}

1. Facoltativamente, utilizzare **[!UICONTROL Aggiungi un percorso alternativo in caso di timeout o errore]** per definire un&#39;azione alternativa in caso di problemi. [Ulteriori informazioni](using-the-journey-designer.md#paths)

1. Progetta il contenuto appropriato per ogni azione corrispondente a ciascun gruppo definito dalle impostazioni della regola di targeting.

   In questo esempio, progettare un&#39;e-mail con offerte speciali per gli iscritti Gold e un promemoria SMS per gli altri membri.<!--You can seamlessly navigate between the different contents for each action. ![Content design panel for targeting rule actions](assets/journey-targeting-design.png)-->

1. [Pubblica](publish-journey.md) il tuo percorso.

Una volta che il percorso è attivo, il percorso specificato per ciascun segmento viene elaborato in modo che i membri Gold entrino nel percorso con le offerte e-mail, mentre gli altri membri entrino nel percorso con il promemoria SMS.

Segui il successo del tuo percorso con il rapporto sul Percorso. [Ulteriori informazioni](../reports/journey-global-report-cja.md#targeting)

## Casi di utilizzo delle regole di targeting {#uc-targeting}

Gli esempi seguenti mostrano come utilizzare l&#39;attività **[!UICONTROL Ottimizza]** con il metodo **[!UICONTROL Regola di targeting]** per personalizzare i percorsi per diversi tipi di pubblico secondario.

+++Canali specifici del segmento

I membri fedeltà con stato Gold possono ricevere offerte personalizzate tramite e-mail, mentre tutti gli altri membri sono indirizzati a promemoria SMS.

<!--➡️ Use the revenue per profile or conversion rate as the optimization metric.-->

![Canali specifici del segmento destinati a iscritti Gold con e-mail e altri con SMS](assets/journey-optimize-targeting-uc-segment.png)

+++

+++Targeting basato sul comportamento

Ai clienti che hanno aperto un’e-mail ma non hanno fatto clic su viene inviata una notifica push, mentre a quelli che non hanno aperto viene inviato un SMS.

<!--➡️ Use the click-through rate or downstream conversions as the optimization metric.-->

![Destinazione basata sul comportamento per il coinvolgimento e-mail con fallback push o SMS](assets/journey-optimize-targeting-uc-behavior.png)

+++

+++Targeting cronologia acquisti

I clienti che hanno acquistato di recente possono entrare in un breve percorso di &quot;Grazie + Cross-selling&quot;, mentre quelli senza cronologia di acquisto entrano in un percorso di sviluppo più lungo.

<!--➡️ Use the repeat purchase rate or engagement rate as the optimization metric.-->

![Destinazione cronologia acquisti con percorso di cross-selling per acquirenti e percorso di sviluppo per non acquirenti](assets/journey-optimize-targeting-uc-purchase.png)

+++

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

- **TL;DR:** In questa pagina viene illustrato come utilizzare il targeting dei percorsi nei percorsi Adobe Journey Optimizer per indirizzare in modo deterministico segmenti di pubblico specifici in percorsi di percorso designati in base a regole definite.

**Intenti:**
- Configurare il targeting deterministico dei percorsi utilizzando l’attività Ottimizza con un metodo di regola di targeting
- Crea nuove regole di targeting o riutilizza regole esistenti dal menu Regole
- Definisci un percorso di fallback per i profili non idonei per alcuna regola di targeting
- Personalizzare i percorsi del percorso per segmenti di pubblico distinti (ad esempio, livelli di fedeltà, comportamento, cronologia degli acquisti)
- Modificare le regole di targeting in linea senza influire sulla definizione della regola originale

**Glossario:**
- **Ottimizza attività**: attività di area di lavoro del percorso utilizzata per suddividere i profili in percorsi diversi tramite sperimentazione (casuale) o targeting (deterministico) *(specifico per prodotto)*
- **Regola di targeting**: una condizione di qualifica deterministica che determina il percorso di percorso immesso da un profilo, in base agli attributi di profilo o pubblico *(specifico per prodotto)*
- **Percorso di fallback**: un percorso di percorso alternativo per i profili che non soddisfano nessuna delle regole di targeting definite *(specifico per prodotto)*

**Guardrail:**
- Il targeting dei percorsi è attualmente a disponibilità limitata; contatta il rappresentante Adobe per richiedere l’accesso.
- La creazione di regole di targeting dal menu dedicato delle regole di Journey Optimizer richiede il componente aggiuntivo Decisioning o è disponibile su richiesta (disponibilità limitata).
- Quando una regola viene selezionata dal menu Regole e copiata nel percorso, le modifiche successive alla regola originale non influiscono sulla copia del percorso.
- La modifica in linea di una regola non modifica la regola originale da cui proviene.
- Se l’opzione del percorso di fallback non è abilitata, i profili non idonei per alcuna regola di targeting escono completamente dal percorso.

**Terminologia:**
- Nome canonico: Path Targeting — Acronimo: none — varianti: deterministic path routing, rule-based path split
- Sinonimi: &quot;regola di targeting&quot; = &quot;regola di qualificazione&quot; = &quot;condizione percorso&quot;
- Non confondere: &quot;Targeting&quot; ≠ &quot;Sperimentazione&quot; (il targeting è deterministico; la sperimentazione è assegnazione casuale)

**Domande frequenti:**
- **D: Qual è la differenza tra targeting percorso e sperimentazione percorso?** — Il targeting è deterministico: i profili immettono un percorso basato su regole definite. La sperimentazione è casuale: i profili vengono assegnati ai percorsi in base al caso per confrontare le prestazioni.
- **D: cosa succede ai profili non idonei per alcuna regola di targeting?** — Se l&#39;opzione del percorso di fallback è abilitata, viene immesso il percorso di fallback. Se non è abilitata, esce completamente dal percorso.
- **D: è possibile riutilizzare una regola esistente dal menu Regole?** — Sì, ma la formula della regola viene copiata nell&#39;attività di percorso; le modifiche successive alla regola originale nel menu Regole non influiranno sulla copia del percorso.
- **Q: la modifica in linea di una regola di targeting cambia la regola originale?** — No, la modifica in linea aggiorna solo la regola all&#39;interno dell&#39;attività di percorso e non influisce sulla regola di origine.
- **Q: chi può accedere al targeting del percorso?** — Al momento la disponibilità è limitata; contatta il rappresentante Adobe per richiedere l’accesso.

+++
