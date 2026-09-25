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
    internal-label: Journey Optimizer
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
    internal-label: Content management
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
    internal-label: Email
subfeature_v2:
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
    internal-label: Email design
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
    internal-label: Publish
  - id: c41e8697-e629-4c38-96b3-564faaa17acf
    internal-label: Dynamic content
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: 7047a27a870c50f7a093ec7d98d8398948b78edb
workflow-type: ht
source-wordcount: '887'
ht-degree: 100%
---
# Personalizzare lo sfondo delle e-mail {#backgrounds}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come impostare i colori e le immagini di sfondo a livello di corpo, riquadro di visualizzazione, struttura e colonna dell’e-mail all’interno dell’E-mail designer.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ac_edition_backgroundimage"
>title="Impostazioni dello sfondo"
>abstract="Puoi personalizzare il colore o l’immagine di sfondo del contenuto. Ricorda che l’immagine di sfondo non è supportata da tutti i client e-mail."

Gli sfondi ti consentono di rafforzare la tua identità del brand e di richiamare l’attenzione sulle aree chiave della tua e-mail. In E-mail designer, puoi impostare un’immagine o un colore di sfondo a diversi livelli del contenuto, dal corpo generale alle singole strutture e colonne, per un controllo preciso del rendering degli sfondi in tutta l’e-mail.

Quando imposti gli sfondi in E-mail designer, tieni presenti le seguenti best practice:

* Applica un colore di sfondo al corpo solo se il progetto lo richiede.
* Se possibile, preferisci l’impostazione dei colori di sfondo a livello di colonna.
* Evita di utilizzare i colori di sfondo nei componenti immagine o testo, in quanto sono più difficili da gestire.
* Testa le immagini di sfondo tra i client e-mail effettivi prima dell’invio, poiché il rendering può essere diverso dall’anteprima di E-mail designer.

Le seguenti impostazioni ti consentono di applicare un’immagine o un colore di sfondo a qualsiasi livello del contenuto dell’e-mail, dal corpo verso il basso alle singole strutture e colonne.

>[!TIP]
>
>Se un tema viene applicato all’e-mail, non puoi sostituire direttamente il colore di sfondo impostato dal tema per un determinato componente. Devi per prima cosa sbloccare tale stile utilizzando l’icona dedicata nella scheda **[!UICONTROL Stili]**. [Scopri come](apply-email-themes.md#unlocking-styles)

## Impostare un colore di sfondo {#background-color}

1. **Colore di sfondo del corpo**: imposta un **[!UICONTROL colore di sfondo]** per l’intera e-mail. Assicurati di selezionare il **[!UICONTROL corpo]** nella **[!UICONTROL struttura di navigazione]** accessibile dalla palette a sinistra e utilizza l’opzione dedicata dalla scheda **[!UICONTROL Stili]** a destra.

   ![E-mail designer con il corpo selezionato nella struttura di navigazione e l’opzione Colore di sfondo evidenziata nel pannello Stili](assets/background_1.png)

1. **Colore di sfondo del riquadro di visualizzazione**: imposta un **[!UICONTROL colore per il riquadro di visualizzazione]** per applicare lo stesso colore di sfondo a tutti i componenti della struttura, indipendentemente dal colore di sfondo dell’e-mail.

   ![Pannello Stili di E-mail designer con l’opzione colore del riquadro di visualizzazione evidenziata e un selettore di colori aperto per scegliere il colore di sfondo applicato a tutte le strutture](assets/background_2.png)

1. **Colore di sfondo della struttura**: per applicare un colore di sfondo a un singolo componente della struttura, selezionalo direttamente nell’area di lavoro o nella palette a sinistra e imposta un colore specifico per tale struttura.

   ![Pannello Stili di E-mail designer per una struttura selezionata, con l’opzione Colore di sfondo evidenziata](assets/background_3.png)

   >[!TIP]
   >
   >In questo caso, assicurati di non impostare un colore di sfondo del riquadro di visualizzazione, in quanto questo potrebbe nascondere i colori di sfondo della struttura.

1. **Colore di sfondo della colonna**: imposta un colore di sfondo a livello della colonna. Di nuovo, assicurati di selezionare la colonna desiderata dalla palette a sinistra e di impostare un colore specifico per tale colonna.

   ![Pannello Stili di E-mail designer e-mail per una colonna selezionata, con l’opzione Colore di sfondo evidenziata](assets/background_5.png)

   >[!TIP]
   >
   >Si tratta del caso d’uso e della best practice più comuni, in quanto offre maggiore flessibilità durante la modifica del resto del contenuto delle e-mail.

## Impostare un’immagine di sfondo {#background-image}

Puoi anche impostare un’**[!UICONTROL Immagine di sfondo]** per il contenuto di un componente della struttura o della colonna. Questo è più comunemente utilizzato a livello della struttura; impostarne uno a livello di colonna è possibile, ma raramente viene utilizzato.

>[!NOTE]
>
>Alcuni programmi e-mail non supportano le immagini di sfondo. Se non è supportato, viene utilizzato il colore di sfondo della riga. Assicurati di selezionare un colore di sfondo di fallback appropriato nel caso in cui l’immagine non possa essere visualizzata.

![Pannello Stili di E-mail designer con immagine di sfondo attivata e posizionamento dell’immagine impostato su Altezza intera - A destra, con l’immagine che riempie una colonna](assets/background_4.png)

>[!TIP]
>
>Visualizza l’anteprima dell’immagine di sfondo tra i client e-mail effettivi prima dell’invio, non solo nell’anteprima di E-mail designer. La stessa immagine e lo stesso posizionamento possono essere sottoposte a rendering correttamente nell’editor, ma vengono estesi o ritagliati in modo diverso in alcuni client, ad esempio Outlook su iOS.

Una volta impostata un’immagine di sfondo, utilizza il menu a discesa **[!UICONTROL Posizionamento immagine]** per controllare il modo in cui l’immagine riempie la struttura o la colonna. Sono disponibili le opzioni seguenti da selezionare:

![Il pannello Stili di E-mail designer che mostra il menu a discesa Posizionamento immagine con varie opzioni](assets/background_6.png){width=80%}

**Ridimensiona per riempire, centrato:**

* **[!UICONTROL Adatta]**: allunga l’immagine per riempire il contenitore su entrambi gli assi, senza mantenerne le proporzioni.
* **[!UICONTROL Larghezza intera]**: ridimensiona l’immagine proporzionalmente alla larghezza del contenitore e la centra verticalmente.
* **[!UICONTROL Altezza massima]**: ridimensiona l’immagine in modo proporzionale all’altezza del contenitore e la centra in orizzontalmente.

**Ridimensiona per riempire, ancorata a un bordo:**

* **[!UICONTROL Larghezza intera - In alto]**: uguale a **[!UICONTROL Larghezza intera]**, ancorata alla parte superiore del contenitore. L’overflow viene ritagliato nella parte inferiore.
* **[!UICONTROL Larghezza intera - In basso]**: uguale a **[!UICONTROL Larghezza intera]**, ancorata alla parte inferiore del contenitore. L’overflow viene ritagliato nella parte superiore.
* **[!UICONTROL Altezza Intera - A sinistra]**: uguale a **[!UICONTROL Altezza massima]**, ancorata alla sinistra del contenitore. L’overflow viene ritagliato a destra.
* **[!UICONTROL Altezza intera - A destra]**: uguale a **[!UICONTROL Altezza massima]**, ancorata alla destra del contenitore. L’overflow viene ritagliato a sinistra.

**Sezione:**

* **[!UICONTROL Ripeti]**: seziona l’immagine alle dimensioni originali per riempire il contenitore.

**Posizione senza ridimensionamento:**

* **[!UICONTROL Sinistra]**, **[!UICONTROL Destra]**, **[!UICONTROL Centro]**, **[!UICONTROL Alto]**, **[!UICONTROL Basso]**: posiziona l’immagine alle dimensioni originali, ancorata al bordo corrispondente o al centro del contenitore.

>[!NOTE]
>
>Le opzioni ancorate al bordo consentono un maggiore controllo su quale parte dell’immagine rimane visualizzata quando non corrisponde alle proporzioni della struttura, rispetto alle opzioni centrate sopra riportate.

{{$include /help/_includes/do-not-localize/email/ai-augmented-backgrounds.md}}
