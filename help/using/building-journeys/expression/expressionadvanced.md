---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’editor espressioni avanzato
description: Scopri come creare espressioni avanzate
feature: Journeys
role: Developer
level: Experienced
keywords: editor espressioni, dati, percorso
exl-id: 9ea6cc3a-6a1b-4e8f-82ff-f8b1812617d7
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 55%

---

# Utilizzare l’editor espressioni avanzato {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="Editor di espressioni avanzate"
>abstract="Utilizza l’editor di espressioni avanzate per creare espressioni avanzate in varie schermate dell’interfaccia. Ad esempio, puoi creare espressioni durante la configurazione e l’utilizzo di percorsi e durante la definizione di una condizione di origine dati."

Utilizza l’editor di espressioni avanzate di Percorso per creare espressioni avanzate in varie schermate dell’interfaccia. Ad esempio, puoi creare espressioni durante la configurazione e l’utilizzo di percorsi e durante la definizione di una condizione di origine dati.

È inoltre disponibile ogni volta che hai bisogno di definire parametri di azione che richiedono specifiche manipolazioni dei dati. Puoi sfruttare i dati provenienti dagli eventi o le informazioni aggiuntive recuperate dall’origine dati. In un percorso, l’elenco visualizzato dei campi dell’evento è contestuale e varia in base agli eventi aggiunti nel percorso.

![](../assets/journey65.png)


L’editor di espressioni avanzate offre un set di funzioni e operatori incorporati che consente di manipolare i valori e definire un’espressione adatta alle tue esigenze. L’editor di espressioni avanzate ti consente inoltre di definire i valori del parametro dell’origine dati esterna, di manipolare i campi e le raccolte delle mappe.

>[!NOTE]
>
>Le funzioni e le funzionalità disponibili nell&#39;editor di espressioni avanzate del Percorso sono diverse da quelle disponibili nell&#39;[editor di personalizzazione](../../personalization/functions/functions.md).

## Accedere all’editor di espressioni avanzate {#accessing-the-advanced-expression-editor}

L’editor di espressioni avanzate può essere utilizzato per:

* creare [condizioni avanzate](../condition-activity.md#about_condition) sulle origini dati e sulle informazioni sull’evento
* definire le [attività di attesa](../wait-activity.md#custom) personalizzate
* definire la mappatura dei parametri di azione

Se possibile, puoi passare tra le due modalità utilizzando il pulsante **[!UICONTROL Modalità avanzata]** / **[!UICONTROL Modalità semplice]**. La modalità semplice è descritta [qui](../condition-activity.md#about_condition).

>[!NOTE]
>
>* Le condizioni possono essere definite nell’editor di espressioni semplice o avanzato. Restituiscono sempre un tipo booleano.
>
>* I parametri delle azioni possono essere definiti selezionando i campi o tramite l’editor di espressioni avanzate. I parametri restituiscono un tipo di dati specifico in base alla relativa espressione.

Puoi accedere all’editor di espressioni avanzate con diverse modalità:

* Quando crei una condizione di origine dati, puoi accedere all&#39;editor avanzato facendo clic su **[!UICONTROL Modalità avanzata]**.

  ![](../assets/journeyuc2_33.png)

* Quando crei un timer personalizzato, l’editor avanzato viene visualizzato direttamente.
* Quando mappi il parametro dell&#39;azione, fai clic su **[!UICONTROL Modalità avanzata]**.

## Scopri l’interfaccia {#discovering-the-interface}

Questa schermata ti consente di scrivere manualmente l’espressione.

![](../assets/journey70.png)

Nella parte sinistra dello schermo sono visualizzati i campi e le funzioni disponibili:

* **[!UICONTROL Eventi]**: scegli uno dei campi ricevuti dall&#39;evento in entrata. L’elenco visualizzato dei campi dell’evento è contestuale e varia in base agli eventi aggiunti nel percorso. [Ulteriori informazioni](../../event/about-events.md)

  >[!CAUTION]
  >
  >La creazione di espressioni utilizzando eventi di esperienza non è supportata. Si fa riferimento ad approcci alternativi e best practice per la creazione di espressioni/logiche con eventi di esperienza [qui](../../building-journeys/exp-event-lookup.md)

* **[!UICONTROL Tipi di pubblico]**: se hai rimosso un evento **[!UICONTROL Qualificazione del pubblico]**, scegli il pubblico che desideri utilizzare nell&#39;espressione. [Ulteriori informazioni](../condition-activity.md#using-a-segment)
* **[!UICONTROL Origini dati]**: scegli dall&#39;elenco di campi disponibili nei gruppi di campi delle origini dati. [Ulteriori informazioni](../../datasource/about-data-sources.md)
* **[!UICONTROL proprietà Percorso]**: questa sezione raggruppa i campi tecnici relativi al percorso per un determinato profilo. [Ulteriori informazioni](journey-properties.md)
* **[!UICONTROL Funzioni]**: scegli dall&#39;elenco di funzioni incorporate che consentono di eseguire filtri complessi. Le funzioni sono organizzate per categorie. [Ulteriori informazioni](functions.md)

![](../assets/journey65.png)

Un meccanismo di completamento automatico visualizza i suggerimenti contestuali.

![](../assets/journey68.png)

Un meccanismo di convalida della sintassi verifica l’integrità del tuo codice. Gli errori vengono visualizzati sopra l’editor.

![](../assets/journey69.png)


>[!TIP]
>
>Quando crei condizioni nell’editor di espressioni avanzate, assicurati che le espressioni non contengano caratteri nascosti o non stampabili. Utilizza inoltre espressioni a riga singola per evitare errori di analisi.


**Necessità di parametri per la creazione di condizioni con l’editor di espressioni avanzate**

Se selezioni un campo da un&#39;origine dati esterna che richiede la chiamata di un parametro (vedi [questa pagina](../../datasource/external-data-sources.md)), a destra viene visualizzata una nuova scheda che consente di specificare questo parametro. Il valore del parametro può provenire dagli eventi posizionati nel percorso o nell’origine dati di Experience Platform (e non da altre origini dati esterne). Ad esempio, in un’origine dati correlata al meteo, un parametro utilizzato di frequente sarà “city”. Di conseguenza, devi selezionare il punto in cui vuoi ottenere questo parametro della città. Ai parametri è possibile applicare anche le funzioni, al fine di eseguire modifiche di formato o concatenazioni.

![](../assets/journeyuc2_19.png)

Per casi di utilizzo più complessi, se desideri includere i parametri dell’origine dati nell’espressione principale, puoi definirne i valori utilizzando la parola chiave “params”. Consulta [questa pagina](../expression/field-references.md).
