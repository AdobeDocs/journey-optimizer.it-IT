---
solution: Journey Optimizer
product: journey optimizer
title: Aggiungere attributi contestuali ai frammenti pubblicati
description: Scopri come aggiungere attributi contestuali ai frammenti pubblicati (disponibilità limitata)
feature: Fragments
topic: Content Management
role: User
level: Intermediate, Experienced
hide: true
hidefromtoc: true
source-git-commit: 4162403bedc1632ed28db122e2ec16e3c00a2630
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 3%

---

# Aggiungere attributi contestuali ai frammenti pubblicati {#adding-contextual-attributes}

>[!AVAILABILITY]
>
>Questa funzionalità è disponibile solo per determinati clienti e comporta rischi significativi. Verifica con il tuo rappresentante Adobe che questa funzionalità sia abilitata per la tua organizzazione.

Per impostazione predefinita, l&#39;aggiunta di nuovi [attributi di personalizzazione](../personalization/personalization-build-expressions.md) a un frammento pubblicato non è supportata. Dopo la pubblicazione di un frammento, il set di attributi di profilo o contestuali viene bloccato per tutte le campagne e i percorsi.

Tuttavia, per alcuni clienti, è possibile aggiungere **attributi contestuali** solo ai frammenti pubblicati.

>[!WARNING]
>
>Quando si aggiungono attributi di personalizzazione a un frammento pubblicato, il processo di convalida è meno rigoroso e potrebbero non essere rilevati errori. Questo potrebbe causare interruzioni non intenzionali tra percorsi e campagne che utilizzano tale frammento su larga scala.

## Guardrail e limitazioni {#limitations}

* Assicurati che tutti i percorsi e le campagne che attualmente utilizzano il frammento siano in grado di gestire i nuovi attributi contestuali.
* Non è possibile aggiungere attributi di profilo ai frammenti pubblicati. Sono supportati solo gli attributi contestuali.
* Gli attributi contestuali devono essere immessi manualmente nell’editor di codice e non possono essere selezionati dall’interfaccia utente dell’editor di personalizzazione.
* Quando si aggiungono attributi personalizzati a frammenti live, le convalide sono meno complesse, il che significa che gli errori potrebbero non essere rilevati e causare interruzioni non intenzionali su larga scala.
* Dopo la pubblicazione, eventuali errori influiranno immediatamente su tutte le comunicazioni che utilizzano quel frammento.

## Aggiungere attributi contestuali {#add-contextual-attributes}

Per aggiungere attributi contestuali a un frammento pubblicato, effettua le seguenti operazioni.

>[!IMPORTANT]
>
>Procedi solo se comprendi appieno l’impatto su percorsi e campagne che fanno riferimento al frammento. [Ulteriori informazioni](#limitations)

1. Passa a **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Frammenti]**.

1. Seleziona il frammento pubblicato e fai clic su **[!UICONTROL Modifica]** per creare una versione bozza.

   ![](assets/fragment-live-modify.png){width="70%" align="left"}

1. Fai clic su **[!UICONTROL Modifica]** per aprire l&#39;editor del contenuto del frammento.

1. Passa a **[!UICONTROL editor di codice]** o **[!UICONTROL modalità avanzata]** nell&#39;editor di personalizzazione.

1. Digita o copia-incolla manualmente l’attributo contestuale utilizzando la sintassi:

   ```
   {{context.attribute_name}}
   ```

   Esempio per un attributo `promotionCode`:

   ```
   {{context.promotionCode}}
   ```

   >[!CAUTION]
   >
   >Verificare la precisione del percorso attributo. Gli errori potrebbero non essere rilevati e compromettere le comunicazioni del percorso o della campagna su larga scala.

1. Salva le modifiche.

1. Una volta confermate, fai clic su **[!UICONTROL Pubblica]** per rendere attive le modifiche.

>[!NOTE]
>Per evitare interruzioni non intenzionali tra percorsi e campagne, puoi testare i percorsi degli attributi contestuali in un ambiente non di produzione.

## Argomenti correlati {#related-topics}

* [Gestire i frammenti](manage-fragments.md)
* [Utilizzare frammenti visivi nelle e-mail](../email/use-visual-fragments.md)
* [Utilizzare frammenti di espressione](../personalization/use-expression-fragments.md)
* [Campagne attivate da API](../campaigns/api-triggered-campaigns.md)
* [Sintassi di personalizzazione](../personalization/personalization-syntax.md)

