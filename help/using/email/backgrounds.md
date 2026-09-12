---
solution: Journey Optimizer
product: journey optimizer
title: Personalizzare lo sfondo delle e-mail
description: Scopri come personalizzare lo sfondo delle e-mail
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: sfondo, e-mail, colore, editor
exl-id: 09a2e892-8c6f-460d-8b12-5026582c6ed0
TQID: https://experienceleague.adobe.com/8kFppIm3Q-zHDqalE0Vt0CK5Z1ts9fGspVu476TapSk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
  - id: c41e8697-e629-4c38-96b3-564faaa17acf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 7047a27a870c50f7a093ec7d98d8398948b78edb
workflow-type: tm+mt
source-wordcount: 887
ht-degree: 12%

---

# Personalizzare lo sfondo delle e-mail {#backgrounds}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come impostare i colori e le immagini di sfondo a livello di corpo, riquadro di visualizzazione, struttura e colonna dell’e-mail all’interno dell’E-mail designer.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ac_edition_backgroundimage"
>title="Impostazioni dello sfondo"
>abstract="Puoi personalizzare il colore o l’immagine di sfondo del contenuto. Ricorda che l’immagine di sfondo non è supportata da tutti i client e-mail."

Gli sfondi ti aiutano a rafforzare la tua identità del brand e a richiamare l’attenzione sulle aree chiave della tua e-mail. In E-mail Designer, puoi impostare un colore o un’immagine di sfondo a diversi livelli del contenuto, dal corpo generale alle singole strutture e colonne, per un controllo preciso del rendering degli sfondi in tutta l’e-mail.

Quando imposti gli sfondi nel Designer e-mail, tieni presenti le seguenti best practice:

* Applicare un colore di sfondo al corpo solo se il progetto lo richiede.
* Se possibile, è preferibile impostare i colori di sfondo a livello di colonna.
* Evita di utilizzare i colori di sfondo nei componenti immagine o testo, in quanto sono più difficili da gestire.
* Verifica le immagini di sfondo tra i client e-mail effettivi prima dell’invio, poiché il rendering può essere diverso dall’anteprima di E-mail Designer.

Le seguenti impostazioni consentono di applicare un colore o un’immagine di sfondo a qualsiasi livello del contenuto dell’e-mail, dal corpo verso il basso alle singole strutture e colonne.

>[!TIP]
>
>Se un tema viene applicato all’e-mail, non puoi ignorare direttamente il colore di sfondo impostato dal tema per un determinato componente. Per sbloccare lo stile, utilizza l&#39;icona dedicata nella scheda **[!UICONTROL Stili]**. [Scopri come](apply-email-themes.md#unlocking-styles)

## Impostare un colore di sfondo {#background-color}

1. **Colore sfondo corpo** - Imposta un **[!UICONTROL Colore sfondo]** per l&#39;intera e-mail. Assicurati di selezionare **[!UICONTROL Body]** nella **[!UICONTROL Struttura di navigazione]** accessibile dalla palette a sinistra e di utilizzare l&#39;opzione dedicata dalla scheda **[!UICONTROL Stili]** a destra.

   ![Invia un&#39;e-mail a Designer con il corpo selezionato nella struttura di navigazione e l&#39;opzione Colore di sfondo evidenziata nel pannello Stili](assets/background_1.png)

1. **Colore di sfondo del riquadro di visualizzazione** - Imposta un **[!UICONTROL Colore riquadro di visualizzazione]** per applicare lo stesso colore di sfondo in tutti i componenti della struttura, indipendentemente dal colore di sfondo del corpo.

   ![Invia un&#39;e-mail al pannello Stili di Designer evidenziando l&#39;opzione di colore del riquadro di visualizzazione e aprendo un selettore di colori per scegliere il colore di sfondo applicato a tutte le strutture](assets/background_2.png)

1. **Colore di sfondo struttura** - Per applicare un colore di sfondo a un singolo componente struttura, selezionarlo direttamente nell&#39;area di lavoro o nella tavolozza a sinistra e impostare un colore specifico per tale struttura.

   ![Pannello Stili Designer e-mail per una struttura selezionata, con l&#39;opzione Colore sfondo evidenziata](assets/background_3.png)

   >[!TIP]
   >
   >In tal caso, assicurarsi di non impostare un colore di sfondo del riquadro di visualizzazione, in quanto potrebbe nascondere i colori di sfondo della struttura.

1. **Colore di sfondo colonna** - Imposta un colore di sfondo a livello di colonna. Di nuovo, assicurati di selezionare la colonna desiderata dalla palette a sinistra e di impostare un colore specifico per tale colonna.

   ![Pannello Stili Designer e-mail per una colonna selezionata, con l&#39;opzione Colore sfondo evidenziata](assets/background_5.png)

   >[!TIP]
   >
   >Si tratta del caso d’uso più comune e della best practice, in quanto offre maggiore flessibilità durante la modifica del resto del contenuto delle e-mail.

## Impostare un&#39;immagine di sfondo {#background-image}

È inoltre possibile impostare una **[!UICONTROL immagine di sfondo]** per il contenuto di un componente struttura o colonna. Questo è più comunemente utilizzato a livello di struttura; impostarne uno a livello di colonna è possibile, ma raramente viene utilizzato.

>[!NOTE]
>
>Alcuni programmi e-mail non supportano le immagini di sfondo. Se non è supportato, viene utilizzato il colore di sfondo della riga. Assicurati di selezionare un colore di sfondo di fallback appropriato nel caso in cui l’immagine non possa essere visualizzata.

![Pannello Stili Designer e-mail con immagine di sfondo attivata e posizionamento immagine impostato su Altezza massima a destra, con l&#39;immagine che riempie una colonna](assets/background_4.png)

>[!TIP]
>
>Visualizza l’anteprima dell’immagine di sfondo tra i client e-mail effettivi prima dell’invio, non solo nell’anteprima di E-mail Designer. La stessa immagine e lo stesso posizionamento possono essere riprodotti correttamente nell’editor, ma vengono estesi o ritagliati in modo diverso in alcuni client, ad esempio Outlook su iOS.

Una volta impostata un&#39;immagine di sfondo, utilizza il menu a discesa **[!UICONTROL Posizionamento immagine]** per controllare il modo in cui l&#39;immagine riempie la struttura o la colonna. È possibile selezionare le opzioni seguenti:

![Il pannello Stili Designer e-mail mostra il menu a discesa Posizionamento immagine con varie opzioni](assets/background_6.png){width=80%}

**Ridimensiona per riempire, centrato:**

* **[!UICONTROL Adatta]** - Allunga l&#39;immagine per riempire il contenitore su entrambi gli assi, senza mantenerne le proporzioni.
* **[!UICONTROL Larghezza intera]** - Ridimensiona l&#39;immagine proporzionalmente alla larghezza del contenitore e la centra verticalmente.
* **[!UICONTROL Altezza massima]**: ridimensiona l&#39;immagine in modo proporzionale all&#39;altezza del contenitore e la centra in orizzontale.

**Scala per riempimento, ancorata a un bordo:**

* **[!UICONTROL Larghezza intera - Superiore]** - Uguale a **[!UICONTROL Larghezza intera]**, ancorata alla parte superiore del contenitore. L&#39;overflow viene ritagliato nella parte inferiore.
* **[!UICONTROL Larghezza intera - Inferiore]** - Uguale a **[!UICONTROL Larghezza intera]**, ancorata alla parte inferiore del contenitore. L&#39;overflow viene ritagliato nella parte superiore.
* **[!UICONTROL Altezza massima - Sinistra]** - Uguale a **[!UICONTROL Altezza massima]**, ancorata alla sinistra del contenitore. L&#39;overflow viene ritagliato a destra.
* **[!UICONTROL Altezza massima - Destra]** - Uguale a **[!UICONTROL Altezza massima]**, ancorata alla destra del contenitore. L&#39;overflow viene ritagliato a sinistra.

**Sezione:**

* **[!UICONTROL Ripeti]** - Affianca l&#39;immagine alle dimensioni originali per riempire il contenitore.

**Posizione senza ridimensionamento:**

* **[!UICONTROL Sinistra]**, **[!UICONTROL Destra]**, **[!UICONTROL Centro]**, **[!UICONTROL Superiore]**, **[!UICONTROL Inferiore]** - Posiziona l&#39;immagine alle dimensioni originali, ancorata al bordo o al centro corrispondente del contenitore.

>[!NOTE]
>
>Le opzioni ancorate al bordo consentono un maggiore controllo su quale parte dell&#39;immagine rimane visualizzata quando non corrisponde alle proporzioni della struttura, rispetto alle opzioni centrate sopra riportate.

{{$include /help/_includes/do-not-localize/email/ai-augmented-backgrounds.md}}
