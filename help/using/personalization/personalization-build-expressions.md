---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni sull’editor di personalizzazione
description: Scopri come utilizzare l’editor di personalizzazione.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: espressione, editor, about, start
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: ff6619925a36d2687922d1b631d1cabbcb98167e
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 6%

---

# Introduzione all’editor di personalizzazione {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="Informazioni sull’editor di personalizzazione"
>abstract="L’editor di personalizzazione consente di selezionare, disporre, personalizzare e convalidare tutti i dati per creare una personalizzazione dei contenuti."

L&#39;editor di personalizzazione è il fulcro della personalizzazione in [!DNL Journey Optimizer]. È disponibile in ogni contesto in cui è necessario definire la personalizzazione, ad esempio e-mail, push e offerte.

Nell’interfaccia dell’editor di personalizzazione, seleziona, disponi, personalizza e convalida tutti i dati per creare una personalizzazione personalizzata per il contenuto.

![](assets/perso_ee1.png)

## Origini Personalization {#sources}

Nella parte sinistra della schermata viene visualizzato un selettore di dominio che consente di selezionare l’origine per la personalizzazione. Le origini disponibili sono:

* **[!UICONTROL Attributi profilo]** : elenca tutti i riferimenti associati allo schema profilo descritto nella [documentazione di Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.
* **[!UICONTROL Tipi di pubblico]**: elenca tutti i tipi di pubblico creati nel servizio di segmentazione di Adobe Experience Platform. Ulteriori informazioni sulla segmentazione sono disponibili [qui](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=it){target="_blank"}.
* **[!UICONTROL Decisioni di offerta]** : elenca tutte le offerte associate a un posizionamento specifico. Seleziona il posizionamento e inserisci le offerte nel contenuto. Per una documentazione completa su come gestire le offerte, consulta [questa sezione](../offers/get-started/starting-offer-decisioning.md).
* **[!UICONTROL Attributi contestuali]**: quando un&#39;attività di azione canale (e-mail, push, SMS) viene utilizzata in un percorso o in una campagna, gli attributi contestuali relativi a eventi e proprietà sono disponibili per la personalizzazione. Un esempio di personalizzazione che sfrutta gli attributi contestuali è presentato in [questa sezione](personalization-use-case.md).

>[!NOTE]
>
>Se esegui il targeting di un pubblico con attributi di arricchimento generati utilizzando un flusso di lavoro di composizione, puoi sfruttare questi attributi di arricchimento per personalizzare il messaggio. [Scopri come utilizzare gli attributi di arricchimento del pubblico](../audience/about-audiences.md#enrichment)

## Aggiungere personalizzazione {#add}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor_autocomplete"
>title="Completamento automatico"
>abstract="L&#39;attivazione di questa opzione consente al sistema di suggerire e completare automaticamente il codice durante la digitazione. Questa funzione è disponibile solo per i formati HTML e Testo e supporta gli attributi Profilo e Contesto. Se è disattivato tramite l’interruttore, l’editor fornisce il completamento automatico del codice nativo di HTML."

Nell’area di lavoro centrale puoi creare la sintassi di personalizzazione. Per utilizzare un attributo per personalizzare il messaggio, individuarlo nel riquadro di spostamento a sinistra e fare clic sul pulsante `+` per aggiungerlo all&#39;espressione.

Il menu con i puntini di sospensione accanto all&#39;icona `+` consente di ottenere ulteriori dettagli per ciascun attributo e di aggiungere gli attributi utilizzati più di frequente ai preferiti. Gli attributi aggiunti ai preferiti sono accessibili dal menu **[!UICONTROL Preferiti]** nel riquadro di navigazione a sinistra.

Inoltre, puoi definire il testo di fallback predefinito che verrà visualizzato se un attributo di profilo di tipo stringa è vuoto. A tale scopo, fare clic sul pulsante con i puntini di sospensione accanto all&#39;attributo e selezionare **[!UICONTROL Inserisci con testo di fallback]**. Scrivere il testo da visualizzare per impostazione predefinita se il valore dell&#39;attributo è vuoto per un profilo, quindi fare clic su **[!UICONTROL Aggiungi]**.

![](assets/attribute-details.png)

Nell’esempio seguente, l’editor di personalizzazione ti consente di selezionare i profili che hanno il compleanno oggi e quindi di completare la personalizzazione inserendo un’offerta specifica corrispondente a quel giorno.

![](assets/perso_ee2.png)

## Strumenti per la modifica delle espressioni

L’area di lavoro centrale fornisce vari strumenti per aiutarti a scrivere la tua espressione di personalizzazione.

![](assets/perso-workspace.png)

Le opzioni disponibili sono:

1. **[!UICONTROL Trova]** / **[!UICONTROL Trova e sostituisci]**: cerca nell&#39;espressione e sostituisci automaticamente parti di codice.
1. **[!UICONTROL Annulla]** / **[!UICONTROL Ripristina]**: annulla/ripristina l&#39;ultima operazione.
1. **[!UICONTROL Completamento automatico]**: suggerisce e completa automaticamente il codice durante la digitazione. Questa funzione è disponibile solo per i formati HTML e Testo e supporta gli attributi Profilo e Contesto. Se è disattivato tramite l’interruttore, l’editor fornisce il completamento automatico del codice nativo di HTML.

   ![](assets/perso-complete.png){width="70%" align="center" zoomable="yes"}

1. **[!UICONTROL HTML]** / **[!UICONTROL JSON]** / **[!UICONTROL Testo]**: identifica il formato del codice. Questo consente al sistema di adattare la convalida e la funzione di completamento automatico in base alla lingua selezionata.
1. **[!UICONTROL Convalida]**: verifica la sintassi dell&#39;espressione. Ulteriori informazioni in [questa sezione](personalization-validation.md).
1. **[!UICONTROL Salva come frammento]**: salva l&#39;espressione come frammento di espressione. [Ulteriori informazioni](../content-management/save-fragments.md#save-as-expression-fragment)
1. **[!UICONTROL Dimensione font]**: regola la dimensione font per i contenuti all&#39;interno dell&#39;editor per migliorarne la leggibilità.
1. **[!UICONTROL Parola a capo]**: attiva o disattiva il ritorno a capo automatico, consentendo la visualizzazione di espressioni lunghe su una singola riga o racchiuse nell&#39;editor. Le opzioni includono:
   * **Disattivato** (impostazione predefinita) - Nessun ritorno a capo automatico. Le linee lunghe si estendono oltre la vista dell’editor e richiedono uno scorrimento orizzontale.
   * **Il** - Dispone le righe alla larghezza dell&#39;editor.
   * **Colonna a capo automatico** - Dispone le righe quando i caratteri di una riga raggiungono gli 80 caratteri.
   * **Limitato** - Dispone le righe alla larghezza dell&#39;editor o a 80 caratteri, a seconda di quale dei due valori è più basso.

Nel riquadro di navigazione sono disponibili funzioni aggiuntive per aiutarti a creare la tua espressione di personalizzazione.

![](assets/perso-features.png)

* **[!UICONTROL Funzioni helper]** - Le funzioni helper consentono di eseguire operazioni sui dati, ad esempio calcoli, formattazione o conversioni di dati, condizioni e di manipolarli nel contesto della personalizzazione. [Ulteriori informazioni sulle funzioni helper disponibili](functions/functions.md)

* **[!UICONTROL Preferiti]** - Gli attributi aggiunti ai preferiti vengono visualizzati in questo elenco. Questo consente di accedere rapidamente agli elementi utilizzati con maggiore frequenza. Per aggiungere un attributo ai preferiti, fai clic sul menu con i puntini di sospensione e scegli **[!UICONTROL Aggiungi ai preferiti]**.

* **[!UICONTROL Condizioni]** - Sfrutta le regole condizionali create nella libreria per aggiungere contenuto dinamico ai messaggi. Questo consente di creare più varianti del messaggio in base alle condizioni. [Scopri come creare contenuti dinamici](../personalization/get-started-dynamic-content.md)

* **[!UICONTROL Frammenti]** - Sfrutta i frammenti di espressione creati o salvati nella sandbox corrente. Un frammento è un componente riutilizzabile a cui è possibile fare riferimento in [!DNL Journey Optimizer] campagne e percorsi. Questa funzionalità consente di precreare più blocchi di contenuto personalizzati che possono essere utilizzati dagli utenti di marketing per assemblare rapidamente i contenuti in un processo di progettazione migliorato. [Scopri come utilizzare i frammenti di espressione per la personalizzazione](../personalization/use-expression-fragments.md)

Una volta che l’espressione di personalizzazione è pronta, devi farla convalidare dall’editor di personalizzazione. Ulteriori informazioni in [questa sezione](personalization-validation.md).
