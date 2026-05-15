---
solution: Journey Optimizer
product: journey optimizer
title: Creare il codice del contenuto e-mail
description: Scopri come creare il codice per il contenuto delle e-mail
feature: Email Design
topic: Content Management
role: User
level: Intermediate, Experienced
keywords: codice, HTML, editor
exl-id: 5fb79300-08c6-4c06-a77c-d0420aafca31
TQID: https://experienceleague.adobe.com/8CR92GEP0qQqj2h-JqzUdu9oq07Ahedcs1xh8rINvkY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: d595a60b-bcf5-4a63-a189-66a0be755cc7id: ee5bb250-0884-4d71-86eb-d8489e8bcaddid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 496
ht-degree: 22%

---

# Creare il codice del contenuto {#code-content}

**[!UICONTROL Crea il tuo codice]** ti consente di scrivere o incollare HTML non elaborato per creare contenuti e-mail direttamente nel Designer e-mail di [!DNL Journey Optimizer]. Utilizzare questa modalità quando è necessario il controllo completo del markup o quando si importa HTML esistente.

È necessario disporre delle competenze HTML e una volta scelta questa modalità, rimane nell’editor di codice, non è possibile passare all’editor visivo.

➡️ [Guarda un video su questa funzione](#video)

>[!NOTE]
>
>**[!UICONTROL Crea il tuo codice]** non è lo stesso dell&#39;editor avanzato di HTML in E-mail Designer. L’editor HTML avanzato consente di passare dalla visualizzazione HTML a quella visiva (desktop) in qualsiasi momento, non dall’editor di codice. [Ulteriori informazioni sull&#39;editor avanzato di HTML](email-expert-mode.md).

## Utilizzare l’editor di codice {#use-code-editor}

Per creare o modificare il contenuto delle e-mail tramite l’editor di codice, segui la procedura riportata di seguito.

1. Dalla home page di [E-mail Designer](get-started-email-design.md), seleziona **[!UICONTROL Crea un codice personale]**.

   ![](assets/code-your-own.png)

1. Immetti o incolla il codice HTML non elaborato.

1. Utilizza il riquadro a sinistra per sfruttare le funzionalità di personalizzazione di [!DNL Journey Optimizer]. [Ulteriori informazioni](../personalization/personalize.md)

   ![](assets/code-editor.png)

   >[!NOTE]
   >
   >L’editor di personalizzazione in E-mail Designer presenta alcune limitazioni funzionali rispetto alle espressioni di percorso. [Ulteriori informazioni sulle limitazioni della funzione data/ora](#date-time-limitations)

1. Se desideri cancellare il contenuto e-mail e avviare l’e-mail da un nuovo design, **[!UICONTROL Cambia il design]** nel menu delle opzioni.

   ![](assets/code-editor-change-design.png)

   >[!NOTE]
   >
   >Questa azione apre il modello selezionato in E-mail Designer. Da lì puoi completare il design dell’e-mail o tornare all’editor di codice utilizzando l’opzione **[!UICONTROL Passa all’editor di codice]**.

1. Fai clic sul pulsante **[!UICONTROL Anteprima]** per controllare la progettazione e la personalizzazione del messaggio utilizzando i profili di test. [Ulteriori informazioni](../content-management/preview-test.md)

   ![](assets/code-editor-preview.png)

1. Quando il codice è pronto, fai clic su **[!UICONTROL Salva]** quindi torna alla schermata di creazione del messaggio per finalizzarlo.

   ![](assets/code-editor-save.png)

>[!CAUTION]
>
>Impossibile fare riferimento alle immagini di [Adobe Experience Manager Assets](../integrations/assets.md) quando si utilizza il metodo Code your own. Archivia le immagini a cui si fa riferimento nel codice HTML in una posizione pubblica.

## Limitazioni della funzione data e ora {#date-time-limitations}

Quando si utilizza la personalizzazione nell&#39;editor di codice di E-mail Designer, la funzione `now()` non è disponibile per il calcolo dinamico delle date.

>[!IMPORTANT]
>
>La funzione `now()` è **non supportata** nel linguaggio di espressione di Email Builder. `now()` è disponibile in condizioni di percorso, ma non può essere utilizzato all&#39;interno del contenuto e-mail o nell&#39;editor di codice.

**Alternative disponibili:**

Utilizza le seguenti funzioni per lavorare con la data e l’ora correnti nella personalizzazione delle e-mail:

* **`getCurrentZonedDateTime()`** - Restituisce la data e l&#39;ora correnti con le informazioni sul fuso orario. Questa è l&#39;alternativa consigliata a `now()`.

  Esempio: `{%= getCurrentZonedDateTime() %}` restituisce `2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

* **`currentTimeInMillis()`** - Restituisce il tempo corrente in millisecondi epoca.

  Esempio: `{%= currentTimeInMillis() %}`

**Soluzioni consigliate:**

Se devi eseguire calcoli di date nel contenuto dell’e-mail:

* **Precalcola i campi data** - Calcola i valori data obbligatori nella pipeline dei dati o negli attributi del profilo prima di inviare l&#39;e-mail, quindi fai riferimento a tali valori precalcolati nella personalizzazione.

  Esempio: `{%= profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate %}`

* **Utilizza le funzioni di manipolazione data**. Utilizza [funzioni data/ora](../personalization/functions/dates.md) come `dayOfYear()` o `diffInDays()` con valori data dagli attributi del profilo.

  Esempio: `{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}`

* **Usa attributi calcolati** - Crea [attributi calcolati](../audience/computed-attributes.md) che eseguono calcoli di data complessi, rendendo i risultati disponibili come attributi di profilo.

Per l&#39;elenco completo delle funzioni supportate, vedere [Funzioni data e ora](../personalization/functions/dates.md).
