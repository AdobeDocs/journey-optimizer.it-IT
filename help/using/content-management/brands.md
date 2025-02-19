---
solution: Journey Optimizer
product: journey optimizer
title: Gestisci marchio
description: Scopri come creare e gestire le linee guida per il brand
badge: label="Beta" type="Informative"
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: b1ccacd30acb886e06a3305f0c7046d85f558357
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 22%

---

# Creare e gestire i brand {#brands}

>[!AVAILABILITY]
>
>Questa funzionalità viene rilasciata come versione beta privata. Sarà disponibile progressivamente per tutti i clienti nelle prossime versioni.

Le linee guida per il marchio sono un set dettagliato di regole e standard che stabiliscono l’identità visiva e verbale di un marchio. Essi fungono da riferimento per mantenere una rappresentazione coerente del marchio su tutte le piattaforme di marketing e comunicazione.

In [!DNL Journey Optimizer], ora puoi inserire e organizzare manualmente i dettagli del tuo marchio o caricare documenti di linee guida per l&#39;estrazione automatica delle informazioni.

## Marchi di accesso {#generative-access}

Per accedere al menu **[!UICONTROL Brands]** in [!DNL Adobe Journey Optimizer], è necessario concedere agli utenti le autorizzazioni **[!UICONTROL Managed Brand Kit]** o **[!UICONTROL Enable AI Assistant]**. [Ulteriori informazioni](../administration/permissions.md)

+++  Scopri come assegnare le autorizzazioni relative al marchio

1. Nel prodotto **Autorizzazioni**, passa alla scheda **Ruoli** e seleziona il **Ruolo** desiderato.

1. Fai clic su **Modifica** per modificare le autorizzazioni.

1. Aggiungi la risorsa **Assistente AI**, quindi seleziona **Kit marchio gestito** o **[!UICONTROL Abilita assistente AI]** dal menu a discesa.

   Si noti che l&#39;autorizzazione **[!UICONTROL Abilita Assistente Ia]** fornisce accesso in sola lettura al menu Marchi.

   ![](assets/brands-permission.png){zoomable="yes"}

1. Fai clic su **Salva** per applicare le modifiche.

   Le autorizzazioni degli utenti già assegnati a questo ruolo verranno aggiornate automaticamente.

1. Per assegnare questo ruolo a nuovi utenti, passa alla scheda **Utenti** nella dashboard **Ruoli** e fai clic su **Aggiungi utente**.

1. Immetti il nome o l’indirizzo e-mail dell’utente o sceglilo dall’elenco e fai clic su **Salva**.

1. Se l’utente non è già stato creato in precedenza, consulta [questa documentazione](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/abac/permissions-ui/users).

+++

## Crea il tuo marchio {#create-brand-kit}

Per creare e gestire le linee guida per i marchi, puoi immettere autonomamente i dettagli oppure caricare il documento sulle linee guida per i marchi in modo che le informazioni vengano estratte automaticamente:

1. Nel menu **[!UICONTROL Marchi]**, fai clic su **[!UICONTROL Crea marchio]**.

   ![](assets/brands-1.png)

1. Immetti un **[!UICONTROL Nome]** per il tuo marchio<!--and a **[!UICONTROL Description]** to your brand guideline-->.

   ![](assets/brands-2-temp.png)

<!--

[Upload feature currently behind feature flag so hidden from doc - should be available again by EOM (Feb)]

1. Drag and drop or select your file to upload your brand guidelines and extract automatically relevant brand information. Click **[!UICONTROL Create brand]**.

    The information extraction process now begins. Note that it may take several minutes to complete.

    ![](assets/brands-2.png)

1. Your Content and visual creation standards are now automatically populated. Browse through the different tabs to adapt the information as needed.

-->

1. Dalla scheda **[!UICONTROL Stile scrittura]**, fare clic su ![](assets/do-not-localize/Smock_Add_18_N.svg) per aggiungere una linea guida o un&#39;esclusione. Puoi anche aggiungere esempi.

   ![](assets/brands-3.png)

1. Dalla scheda **[!UICONTROL Contenuto visivo]**, fai clic su ![](assets/do-not-localize/Smock_Add_18_N.svg) per aggiungere un&#39;altra linea guida o esclusione.

1. Per aggiungere un esempio di immagine, fare clic su **[!UICONTROL Seleziona immagine]**. È inoltre possibile aggiungere un’immagine che mostra un utilizzo errato come esempio di esclusione.

   ![](assets/brands-4.png)

1. Una volta configurata, fai clic su **[!UICONTROL Salva]** e quindi su **[!UICONTROL Pubblica]** per rendere disponibili le linee guida dei brand nell&#39;assistente AI.

1. Per apportare modifiche al tuo marchio pubblicato, fai clic su **[!UICONTROL Modifica marchio]**. In questo modo viene creata una copia temporanea in modalità di modifica, che sostituisce la versione live pubblicata.

   ![](assets/brands-8.png)

1. Dal dashboard **[!UICONTROL Brands]**, apri il menu avanzato facendo clic sull&#39;icona ![](assets/do-not-localize/Smock_More_18_N.svg) per:

   * Visualizza brand
   * Modifica
   * Duplica
   * Pubblica
   * Annulla pubblicazione
   * Elimina

   ![](assets/brands-6.png)

Le linee guida del brand sono ora accessibili dal menu a discesa Brands nel menu dell’assistente AI, consentendo di generare contenuti e risorse in linea con le specifiche. [Ulteriori informazioni sull&#39;assistente di IA](gs-generative.md)

![](assets/brands-7.png)
