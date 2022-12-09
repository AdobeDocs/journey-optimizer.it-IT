---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni sull’editor di espressioni avanzate
description: Scopri come creare espressioni avanzate
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 9ea6cc3a-6a1b-4e8f-82ff-f8b1812617d7
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---

# Informazioni sull’editor di espressioni avanzate {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="Informazioni sull’editor di espressioni avanzate"
>abstract="Utilizza l’editor di espressioni avanzate per creare espressioni avanzate in varie schermate dell’interfaccia. Ad esempio, puoi creare espressioni durante la configurazione e l’utilizzo dei percorsi e durante la definizione di una condizione di origine dati."

Utilizza l’editor di espressioni avanzate per creare espressioni avanzate in varie schermate dell’interfaccia. Ad esempio, puoi creare espressioni durante la configurazione e l’utilizzo dei percorsi e durante la definizione di una condizione di origine dati.
È inoltre disponibile ogni volta che devi definire parametri di azione che richiedono specifiche manipolazioni dei dati. Puoi sfruttare i dati provenienti dagli eventi o le informazioni aggiuntive recuperate dall’origine dati. In un percorso, l’elenco visualizzato dei campi dell’evento è contestuale e varia a seconda degli eventi aggiunti nel percorso.

L’editor di espressioni avanzate offre un set di funzioni e operatori incorporati che ti consentono di manipolare i valori e definire un’espressione adatta alle tue esigenze. L’editor di espressioni avanzate ti consente inoltre di definire i valori del parametro dell’origine dati esterna, di manipolare i campi e le raccolte delle mappe, ad esempio gli eventi di esperienza.

![](../assets/journey65.png)

_Interfaccia dell’editor di espressioni avanzate_

L’editor di espressioni avanzate può essere utilizzato per:

* creare [condizioni avanzate](../condition-activity.md#about_condition) sulle origini dati e le informazioni sugli eventi
* definire personalizzato [attendere attività](../wait-activity.md#custom)
* definire la mappatura dei parametri delle azioni

Quando possibile, puoi passare tra le due modalità utilizzando **[!UICONTROL Advanced mode]** / **[!UICONTROL Simple mode]** pulsante . Viene descritta la modalità semplice [qui](../condition-activity.md#about_condition).

>[!NOTE]
>
>Le condizioni possono essere definite nell’editor di espressioni semplice o avanzato. Restituiscono sempre un tipo booleano.
>
>I parametri delle azioni possono essere definiti selezionando i campi o tramite l’editor di espressioni avanzate. Restituiscono un tipo di dati specifico in base alla relativa espressione.

## Accesso all’editor di espressioni avanzate {#accessing-the-advanced-expression-editor}

Puoi accedere all’editor di espressioni avanzate in diversi modi:

* Quando crei una condizione di origine dati, puoi accedere all’editor avanzato facendo clic su **[!UICONTROL Advanced mode]**.

   ![](../assets/journeyuc2_33.png)

* Quando crei un timer personalizzato, l’editor avanzato viene visualizzato direttamente.
* Quando mappi il parametro dell&#39;azione, fai clic su **[!UICONTROL Advanced mode]**.

## Esplorazione dell’interfaccia{#discovering-the-interface}

Questa schermata ti consente di scrivere manualmente l’espressione.

![](../assets/journey70.png)

Nella parte sinistra dello schermo sono visualizzati i campi e le funzioni disponibili:

* **[!UICONTROL Events]**: scegli uno dei campi ricevuti dall’evento in entrata. L’elenco visualizzato dei campi dell’evento è contestuale e varia a seconda degli eventi aggiunti nel percorso. [Leggi tutto](../../event/about-events.md)
* **[!UICONTROL Segments]**: se hai abbandonato un **[!UICONTROL Segment qualification]** , scegli il segmento da utilizzare nell&#39;espressione. [Leggi tutto](../condition-activity.md#using-a-segment)
* **[!UICONTROL Data Sources]**: scegli dall’elenco dei campi disponibili nei gruppi di campi delle origini dati. [Leggi tutto](../../datasource/about-data-sources.md)
* **[!UICONTROL Journey properties]**: questa sezione raggruppa i campi tecnici relativi al percorso per un determinato profilo. [Leggi tutto](journey-properties.md)
* **[!UICONTROL Functions]**: scegli dall’elenco a di funzioni integrate che consentono di eseguire filtri complessi. Le funzioni sono organizzate per categorie. [Leggi tutto](functions.md)

![](../assets/journey65.png)

Un meccanismo di completamento automatico visualizza suggerimenti contestuali.

![](../assets/journey68.png)

Un meccanismo di convalida della sintassi verifica l&#39;integrità del codice. Gli errori vengono visualizzati sopra l’editor.

![](../assets/journey69.png)

**Necessità di parametri per la creazione di condizioni con l’editor di espressioni avanzate**

Se selezioni un campo da un’origine dati esterna che richiede la chiamata di un parametro (vedi [questa pagina](../../datasource/external-data-sources.md). Ad esempio, in un’origine dati correlata al meteo, un parametro utilizzato di frequente sarà &quot;city&quot;. Di conseguenza, è necessario selezionare il punto in cui si desidera ottenere questo parametro della città. È inoltre possibile applicare funzioni ai parametri per eseguire modifiche di formato o concatenazioni.

![](../assets/journeyuc2_19.png)

Per casi d’uso più complessi, se desideri includere i parametri dell’origine dati nell’espressione principale, puoi definirne i valori utilizzando la parola chiave &quot;params&quot;. Vedi [questa pagina](../expression/field-references.md).
