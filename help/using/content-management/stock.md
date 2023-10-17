---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare le immagini di Adobe Stock
description: Introduzione ad Adobe Stock
feature: Assets, Integrations
topic: Content Management
role: User
level: Beginner
keywords: archivio, immagini, integrazione, foto
exl-id: 0715f65f-04bd-4dc2-a152-98111f4c42e6
source-git-commit: c2f2dde40385f56ea86be15a5857fa9e5e2e2fed
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 13%

---

# Utilizzare [!DNL Adobe Stock] immagini {#stock}

## Introduzione a [!DNL Adobe Stock] {#get-started-stock}

Il plug-in per l’integrazione di E-mail designer di [!DNL Adobe Stock] e [!DNL Adobe Journey Optimizer] offre ai clienti un modo semplice per cercare le immagini da utilizzare nella creazione dei messaggi, acquistarne la licenza e salvarle.

[Adobe Stock](https://helpx.adobe.com/stock/get-started.html){target="_blank"} consente di accedere a milioni di foto, video, illustrazioni e grafica vettoriale di alta qualità, curate e gratuite. È possibile scegliere di acquistare un pacchetto di credito per concedere in licenza le risorse oppure acquistare una sola licenza Standard o Estesa per il cespite necessario. Adobe Stock fornisce anche una raccolta gratuita di risorse.

Con [!DNL Adobe Journey Optimizer], puoi caricare le immagini nelle e-mail direttamente da [!DNL Adobe Stock] e aggiungerle alla cartella **[!UICONTROL Risorse]** utilizzando l’opzione **[!UICONTROL Trova le foto di Adobe Stock]**. Inoltre, l’opzione **[!UICONTROL Trova foto Stock simili]** consente di trovare immagini che corrispondono al contenuto, al colore e alla composizione della risorsa utilizzata nella consegna.

## Autorizzazioni{#stock-permissions}

Il **[!UICONTROL Trova foto Adobe Stock]** e **[!UICONTROL Trova immagine simile]** Sono disponibili opzioni per gli utenti con accesso a un profilo di prodotto AEM Assets Essentials.

Per ulteriori informazioni, consulta [Documentazione essenziale di Assets](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/get-started-admins/deploy-administer.html#add-users-to-essentials){target="_blank"}.

## Inserisci un&#39;immagine da [!DNL Adobe Stock] {#add-stock-image}

Per aggiungere immagini da [!DNL Adobe Stock] al contenuto, segui la procedura indicata di seguito:

1. Dalla sezione **[!UICONTROL Componenti contenuto]** in E-mail Designer, trascina e rilascia una **Immagine**.

1. Fai clic su **[!UICONTROL Trova foto Adobe Stock]** sul lato sinistro di E-mail Designer.

   ![](assets/stock-find-photos.png)

1. Sfoglia la libreria o immetti un termine nel campo di ricerca.

   ![](assets/stock-select-from-lib.png)

1. Seleziona l’immagine scelta e fai clic su **[!UICONTROL Salva]**.

   Se l&#39;immagine selezionata non dispone della licenza, è necessario [ottenere la licenza](#license-stock-image).

## Trova foto simili {#similar-stock-image}

Puoi sostituire qualsiasi immagine esistente nel contenuto dell’e-mail con una foto di [!DNL Adobe Stock]. Questa opzione è disponibile per tutte le immagini: immagini Stock con o senza licenza e immagini dalla cartella Assets.

Per sfogliare foto simili, procedere come segue:

1. Selezionare l&#39;immagine da sostituire.
1. Fai clic su **[!UICONTROL Trova foto Stock simili]** per visualizzare le risorse in [!DNL Adobe Stock] che corrispondono al contenuto, al colore e alla composizione dell’immagine.

   ![](assets/stock-similar.png)

1. Seleziona l’immagine scelta e fai clic su **[!UICONTROL Salva]**.

   ![](assets/stock-similar-results.png)

   Se l&#39;immagine selezionata non dispone della licenza, è necessario [ottenere la licenza](#license-stock-image).

1. Se necessario, personalizza l&#39;immagine con **[!UICONTROL Impostazioni]** e **[!UICONTROL Stili]** schede. [Ulteriori informazioni sulle impostazioni dei componenti](../email/content-components.md).

## Ottieni la licenza da [!DNL Adobe Stock] {#license-stock-image}

Se l&#39;immagine è già concessa in licenza, viene rappresentata da ![](assets/stock_10.png) icona. In caso contrario, è necessario concedere la licenza.

Per ottenere la licenza e scaricare l&#39;immagine, effettuare le seguenti operazioni:

1. Selezionala e fai clic su **[!UICONTROL Ottieni licenza per immagine Adobe Stock]** icona.

   ![](assets/stock-license-icon.png)

   Viene quindi reindirizzato al [!DNL Adobe Stock] per acquistare la licenza.

   ![](assets/stock-license-photo.png)

1. Dalla sezione [!DNL Adobe Stock] per scaricare l&#39;immagine e rimuovere la filigrana, è necessario acquistare la risorsa.

   Questo acquisto dipende dal piano o dall’abbonamento Adobe Stock. Se disponi di più account Adobe Stock, verrai reindirizzato all’ultimo ID Stock utilizzato. In questo caso, assicurati di aver effettuato l’accesso all’account corretto prima di concedere la licenza alla risorsa.

   Per ulteriori informazioni sui piani e i prezzi di Adobe Stock in [Documentazione di Adobe Stock](https://stock.adobe.com/plans){target="_blank"}.

   >[!WARNING]
   > Se viene inviata un’e-mail contenente un’immagine senza licenza, l’immagine mantiene la forma senza licenza con la filigrana.

1. Una volta completato l’acquisto, puoi tornare all’e-mail in [!DNL Adobe Journey Optimizer] e seleziona **[!UICONTROL Importa immagine stock]** per importare l’immagine con licenza nelle risorse.

   ![](assets/stock_6.png)

1. Seleziona la cartella in cui memorizzare la risorsa. Per ulteriori informazioni su [!DNL Assets Essentials], fai riferimento a questo [pagina](assets-essentials.md#get-started-assets-essentials).

## Argomenti correlati{#stock-related-topics}

* [Progettazione di e-mail in Journey Optimizer](../email/get-started-email-design.md)
* [Impostazioni dei componenti per la progettazione delle e-mail](../email/content-components.md)
* [Guida introduttiva di Adobe Stock](https://helpx.adobe.com/stock/get-started.html){target="_blank"}.

