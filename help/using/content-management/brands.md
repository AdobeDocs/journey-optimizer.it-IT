---
solution: Journey Optimizer
product: journey optimizer
title: Gestisci marchio
description: Scopri come creare e gestire le linee guida per il brand
badge: label="Beta" type="Informative"
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: b1b7abbe-8600-4a8d-b0b5-0dbd49abc275
source-git-commit: d80f9309cfff4307b1b37ce44b037730a374d4a2
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 16%

---

# Creare e gestire i brand {#brands}

>[!CONTEXTUALHELP]
>id="ajo_brand_overview"
>title="Introduzione ai brand"
>abstract="Crea e personalizza i tuoi brand per definire la tua identità visiva e verbale unica e allo stesso tempo semplificare la generazione di contenuti che corrispondono allo stile e alla voce del tuo marchio."

>[!CONTEXTUALHELP]
>id="ajo_brand_ai_menu"
>title="Seleziona il tuo marchio"
>abstract="Scegli il tuo marchio per assicurarti che tutti i contenuti generati dall’intelligenza artificiale siano personalizzati in base alle specifiche e alle linee guida del tuo marchio."

>[!CONTEXTUALHELP]
>id="ajo_brand_score_overview"
>title="Selezione del brand"
>abstract="Seleziona il tuo marchio per assicurarti che i contenuti siano realizzati in conformità con le linee guida, gli standard e l’identità specifici, mantenendo la coerenza e l’integrità del marchio."

>[!CONTEXTUALHELP]
>id="ajo_brand_score"
>title="Punteggio di allineamento del brand"
>abstract="Il punteggio di allineamento del brand misura il rispetto dei contenuti rispetto alle linee guida del brand, garantendo coerenza in termini di colori, font, logo, immagini e stile di scrittura."

>[!CONTEXTUALHELP]
>id="ajo_brand_colors"
>title="Punteggio colori"
>abstract="Punteggio colori"

>[!CONTEXTUALHELP]
>id="ajo_brand_fonts"
>title="Punteggio font"
>abstract="Punteggio font"

>[!CONTEXTUALHELP]
>id="ajo_brand_logos"
>title="Punteggio logo"
>abstract="Punteggio logo"

>[!CONTEXTUALHELP]
>id="ajo_brand_imagery"
>title="Punteggio immagine"
>abstract="Punteggio immagine"

>[!CONTEXTUALHELP]
>id="ajo_brand_writing_style"
>title="Scrittura punteggio stile"
>abstract="Scrittura punteggio stile"

>[!AVAILABILITY]
>
>Questa funzionalità viene rilasciata come versione beta privata. Sarà disponibile progressivamente per tutta la clientela nelle prossime versioni.

Le linee guida per il marchio sono un set dettagliato di regole e standard che stabiliscono l’identità visiva e verbale di un marchio. Essi fungono da riferimento per mantenere una rappresentazione coerente del marchio su tutte le piattaforme di marketing e comunicazione.

In [!DNL Journey Optimizer], ora puoi inserire e organizzare manualmente i dettagli del tuo marchio o caricare documenti di linee guida per l&#39;estrazione automatica delle informazioni.

## Accedere ai brand {#generative-access}

Per accedere al menu **[!UICONTROL Brands]** in [!DNL Adobe Journey Optimizer], è necessario concedere agli utenti le autorizzazioni **[!UICONTROL Managed Brand Kit]** o **[!UICONTROL Enable AI Assistant]**. [Ulteriori informazioni](../administration/permissions.md)

+++  Scopri come assegnare le autorizzazioni relative al brand

1. Nel prodotto **Autorizzazioni**, passa alla scheda **Ruoli** e seleziona il **Ruolo** desiderato.

1. Fai clic su **Modifica** per modificare le autorizzazioni.

1. Aggiungi la risorsa **Assistente AI**, quindi seleziona **Kit marchio gestito** o **[!UICONTROL Abilita assistente AI]** dal menu a discesa.

   Si noti che l&#39;autorizzazione **[!UICONTROL Abilita Assistente Ia]** fornisce accesso in sola lettura al menu **[!UICONTROL Marchi]**.

   ![](assets/brands-permission.png){zoomable="yes"}

1. Fai clic su **Salva** per applicare le modifiche.

   Le autorizzazioni degli utenti già assegnati a questo ruolo verranno aggiornate automaticamente.

1. Per assegnare questo ruolo a nuovi utenti, passa alla scheda **Utenti** nella dashboard **Ruoli** e fai clic su **Aggiungi utente**.

1. Immetti il nome o l’indirizzo e-mail dell’utente o sceglilo dall’elenco e fai clic su **Salva**.

1. Se l’utente non è già stato creato in precedenza, consulta [questa documentazione](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/abac/permissions-ui/users).

+++

## Crea il tuo marchio {#create-brand-kit}

>[!CONTEXTUALHELP]
>id="ajo_brands_create"
>title="Crea il tuo marchio"
>abstract="Inserisci il nome del brand e carica il file delle linee guida per il brand. Lo strumento estrae automaticamente i dettagli chiave, semplificando il mantenimento dell’identità del brand."

Per creare e gestire la linea guida del brand, puoi inserire i dettagli personalmente o caricare il documento di linee guida del brand per estrarre automaticamente le informazioni:

1. Nel menu **[!UICONTROL Marchi]**, fai clic su **[!UICONTROL Crea marchio]**.

   ![](assets/brands-1.png)

1. Immetti un **[!UICONTROL Nome]** per il tuo marchio.

1. Trascina e rilascia o seleziona il file per caricare le linee guida per il brand ed estrarre automaticamente le informazioni rilevanti per il brand. Fai clic su **[!UICONTROL Crea marchio]**.

   Il processo di estrazione delle informazioni ora inizia. Il completamento potrebbe richiedere alcuni minuti.

   ![](assets/brands-2.png)

1. I contenuti e gli standard di creazione visiva vengono ora compilati automaticamente. Sfoglia le diverse schede per adattare le informazioni in base alle esigenze.

1. Dalla scheda **[!UICONTROL Stile scrittura]**, fai clic su ![](assets/do-not-localize/Smock_Add_18_N.svg) per aggiungere una linea guida o un&#39;esclusione, inclusi esempi.

   ![](assets/brands-3.png)

1. Dalla scheda **[!UICONTROL Contenuto visivo]**, fai clic su ![](assets/do-not-localize/Smock_Add_18_N.svg) per aggiungere un&#39;altra linea guida o esclusione.

1. Per aggiungere un&#39;immagine che mostra l&#39;utilizzo corretto, selezionare **[!UICONTROL Esempio]** e fare clic su **[!UICONTROL Seleziona immagine]**. È inoltre possibile aggiungere un’immagine che mostra un utilizzo errato come esempio di esclusione.

   ![](assets/brands-4.png)

1. Una volta configurata, fai clic su **[!UICONTROL Salva]**, quindi su **[!UICONTROL Pubblica]** per rendere disponibili le linee guida del brand nell&#39;assistente AI.

1. Per apportare modifiche al tuo marchio pubblicato, fai clic su **[!UICONTROL Modifica marchio]**.

   >[!NOTE]
   >
   >In questo modo viene creata una copia temporanea in modalità di modifica, che sostituisce la versione live pubblicata.

   ![](assets/brands-8.png)

1. Dal dashboard **[!UICONTROL Brands]**, apri il menu avanzato facendo clic sull&#39;icona ![](assets/do-not-localize/Smock_More_18_N.svg) per:

   * Visualizza brand
   * Modifica
   * Duplica
   * Pubblica
   * Annulla pubblicazione
   * Elimina

   ![](assets/brands-6.png)

Le linee guida del brand sono ora accessibili dal menu a discesa **[!UICONTROL Brand]** nell&#39;assistente AI, consentendo di generare contenuti e risorse in linea con le specifiche dell&#39;utente. [Ulteriori informazioni sull&#39;assistente di IA](gs-generative.md)

![](assets/brands-7.png)
