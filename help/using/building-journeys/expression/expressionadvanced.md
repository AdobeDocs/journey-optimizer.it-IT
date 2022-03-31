---
solution: Journey Optimizer
title: Informazioni sull’editor di espressioni avanzate
description: Scopri come creare espressioni avanzate
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 9ea6cc3a-6a1b-4e8f-82ff-f8b1812617d7
source-git-commit: 8a859af9ad09ca3f240ff6f355d4e5f34d2e4eac
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 80%

---

# Informazioni sull’editor di espressioni avanzate {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="Informazioni sull’editor di espressioni avanzate"
>abstract="Use the advanced expression editor to build advanced expressions in various screens of the interface. For example, you can build expressions when configuring and using journeys, and when defining a data source condition."

Utilizza l’editor di espressioni avanzate per creare espressioni avanzate in varie schermate dell’interfaccia. For example, you can build expressions when configuring and using journeys, and when defining a data source condition.
È inoltre disponibile ogni volta che hai bisogno di definire parametri di azione che richiedono specifiche manipolazioni dei dati. Puoi sfruttare i dati provenienti dagli eventi o le informazioni aggiuntive recuperate dall’origine dati. In un percorso, l’elenco visualizzato dei campi dell’evento è contestuale e varia in base agli eventi aggiunti nel percorso.

L’editor di espressioni avanzate offre un set di funzioni e operatori incorporati che ti consente di manipolare i valori e definire un’espressione adatta alle tue esigenze. L’editor di espressioni avanzate ti consente inoltre di definire i valori del parametro dell’origine dati esterna, di manipolare i campi e le raccolte delle mappe, ad esempio gli eventi di esperienza.

![](../assets/journey65.png)

_Interfaccia dell’editor di espressioni avanzate_

L’editor di espressioni avanzate può essere utilizzato per:

* creare [condizioni avanzate](../condition-activity.md#about_condition) sulle origini dati e sulle informazioni sull’evento
* definire le [attività di attesa](../wait-activity.md#custom) personalizzate
* definire la mappatura dei parametri di azione

Ove possibile, puoi passare tra le due modalità utilizzando il pulsante **[!UICONTROL Advanced mode]**/**[!UICONTROL Simple mode]**. La modalità semplice è descritta [qui](../condition-activity.md#about_condition).

>[!NOTE]
>
>Le condizioni possono essere definite nell’editor di espressioni semplice o avanzato. Restituiscono sempre un tipo booleano.
>
>I parametri delle azioni possono essere definiti selezionando i campi o tramite l’editor di espressioni avanzate. I parametri restituiscono un tipo di dati specifico in base alla relativa espressione.

## Accesso all’editor di espressioni avanzate {#accessing-the-advanced-expression-editor}

Puoi accedere all’editor di espressioni avanzate con diverse modalità:

* Quando crei una condizione di origine dati, puoi accedere all’editor avanzato facendo clic su **[!UICONTROL Advanced mode]**.

   ![](../assets/journeyuc2_33.png)

* Quando crei un timer personalizzato, l’editor avanzato viene visualizzato direttamente.
* Quando mappi il parametro dell’azione, fai clic su **[!UICONTROL Advanced mode]**.

## Descrizione dell’interfaccia{#discovering-the-interface}

Questa schermata ti consente di scrivere manualmente l’espressione.

![](../assets/journey70.png)

Nella parte sinistra dello schermo sono visualizzati i campi e le funzioni disponibili:

* **[!UICONTROL Events]**: scegli uno dei campi ricevuti dall’evento in entrata. L’elenco visualizzato dei campi dell’evento è contestuale e varia in base agli eventi aggiunti nel percorso. [Ulteriori informazioni](../../event/about-events.md)
* **[!UICONTROL Segments]**: se hai abbandonato un **[!UICONTROL Segment qualification]** , scegli il segmento da utilizzare nell&#39;espressione. [Ulteriori informazioni](../condition-activity.md#using-a-segment)
* **[!UICONTROL Data Sources]**: scegli dall’elenco di campi disponibili nei gruppi di campi delle origini dati. [Ulteriori informazioni](../../datasource/about-data-sources.md)
* **[!UICONTROL Journey properties]**: questa sezione raggruppa i campi tecnici relativi al percorso per un determinato profilo. [Ulteriori informazioni](journey-properties.md)
* **[!UICONTROL Functions]**: scegli dall’elenco di funzioni integrate che consentono di eseguire filtri complessi. Le funzioni sono organizzate per categorie. [Ulteriori informazioni](functions.md)

![](../assets/journey65.png)

Un meccanismo di completamento automatico visualizza i suggerimenti contestuali.

![](../assets/journey68.png)

Un meccanismo di convalida della sintassi verifica l’integrità del tuo codice. Gli errori vengono visualizzati sopra l’editor.

![](../assets/journey69.png)

**Necessità di parametri per la creazione di condizioni con l’editor di espressioni avanzate**

Se selezioni un campo da un’origine dati esterna che richiede la chiamata di un parametro (vedi [questa pagina](../../datasource/external-data-sources.md). Ad esempio, in un’origine dati correlata al meteo, un parametro utilizzato di frequente sarà “city”. Di conseguenza, devi selezionare il punto in cui vuoi ottenere questo parametro della città. Ai parametri è possibile applicare anche le funzioni, al fine di eseguire modifiche di formato o concatenazioni.

![](../assets/journeyuc2_19.png)

Per casi di utilizzo più complessi, se desideri includere i parametri dell’origine dati nell’espressione principale, puoi definirne i valori utilizzando la parola chiave “params”. Consulta [questa pagina](../expression/field-references.md).
