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
exl-id: a274656e-2570-4a9c-b72b-4e8e920b7462
TQID: https://experienceleague.adobe.com/yweu8QtcWU42ZI2z93vIf5-LUGP7pQ16bJUQnmDKNGY
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: c6e980f5-2d4f-494f-beef-186b9ecf1513
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 363
ht-degree: 8%

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
>Procedi solo se [comprendi completamente gli impatti](#limitations) sui percorsi e sulle campagne che fanno riferimento al frammento.

1. Passa a **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Frammenti]**.

1. Seleziona il frammento pubblicato e fai clic su **[!UICONTROL Modifica]** per creare una versione bozza.

   ![](assets/fragment-live-modify.png){width="70%" align="left"}

1. Fai clic su **[!UICONTROL Modifica]** per aprire l&#39;editor del contenuto del frammento.

1. Passa a **[!UICONTROL editor di codice]** o **[!UICONTROL modalità avanzata]** nell&#39;editor di personalizzazione.

1. Digita o copia-incolla manualmente l&#39;attributo contestuale utilizzando la sintassi `{{context.attribute_name}}`:

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
* [Modificare un frammento](manage-fragments.md#edit-fragments)
* [Campagne attivate da API](../campaigns/api-triggered-campaigns.md)
* [Sintassi di personalizzazione](../personalization/personalization-syntax.md)
