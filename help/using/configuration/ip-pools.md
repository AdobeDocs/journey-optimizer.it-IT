---
solution: Journey Optimizer
product: journey optimizer
title: Creare pool IP
description: Scopri come gestire i pool IP
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 1%

---

# Creare pool IP {#create-ip-pools}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool_header"
>title="Configurare un pool IP"
>abstract="Puoi creare pool IP per raggruppare gli indirizzi IP dei tuoi sottodomini per migliorare il recapito dei messaggi e-mail."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool"
>title="Configurare un pool IP"
>abstract="Con Journey Optimizer puoi creare pool IP per raggruppare gli indirizzi IP dei sottodomini. Questo può migliorare in modo significativo il recapito messaggi e-mail, perché in questo modo puoi impedire che la reputazione di un sottodominio influisca sugli altri sottodomini."

## Informazioni sui pool IP {#about-ip-pools}

Con [!DNL Journey Optimizer], puoi creare pool IP per raggruppare gli indirizzi IP dei sottodomini.

La creazione di pool IP è vivamente consigliata per il recapito messaggi e-mail. In questo modo puoi evitare che la reputazione di un sottodominio influisca sugli altri sottodomini.

Ad esempio, una best practice consiste nell’avere un pool IP per i messaggi di marketing e un altro per i messaggi transazionali. In questo modo, se uno dei tuoi messaggi di marketing funziona correttamente e viene dichiarato come spam da un cliente, questo non influenzerà i messaggi transazionali inviati allo stesso cliente, che riceverà comunque messaggi transazionali (conferme di acquisto, messaggi di recupero password, ecc.).

## Creare un pool IP {#create-ip-pool}

Per creare un pool IP, effettua le seguenti operazioni:

1. Accedere al **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Pool IP]** menu, quindi fai clic su **[!UICONTROL Crea pool IP]**.

   ![](assets/ip-pool-create.png)

1. Immetti un nome e una descrizione (facoltativi) per il pool IP.

   >[!NOTE]
   >
   >Il nome deve iniziare con una lettera (A-Z) e includere solo caratteri alfanumerici o caratteri speciali ( _, ., - ).

1. Seleziona gli indirizzi IP da includere nel pool dall’elenco a discesa, quindi fai clic su **[!UICONTROL Invia]**.

   ![](assets/ip-pool-config.png)

   >[!NOTE]
   >
   >Nell’elenco sono disponibili tutti gli indirizzi IP forniti con la tua istanza.

Il pool IP viene ora creato e visualizzato nell’elenco. Puoi selezionarlo per accedere alle relative proprietà e visualizzare la superficie del canale associata (ad esempio, un messaggio preimpostato). Per ulteriori informazioni su come associare una superficie di canale a un pool IP, consulta [questa sezione](channel-surfaces.md).

![](assets/ip-pool-created.png)

## Modificare un pool IP {#edit-ip-pool}

Per modificare un pool IP:

1. Dall’elenco, fai clic sul nome del pool IP per aprirlo.

   ![](assets/ip-pool-list.png)

1. Modifica le proprietà desiderate. Puoi modificare la descrizione e aggiungere o rimuovere indirizzi IP.

   >[!NOTE]
   >
   >Il nome del pool IP non è modificabile. Se desideri modificarlo, devi eliminare il pool IP e crearne un altro con il nome desiderato.

   ![](assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >Procedi con maggiore attenzione quando consideri l’eliminazione di un IP, in quanto questo causerà un ulteriore carico sugli altri IP e potrebbe avere gravi ripercussioni sul recapito messaggi. In caso di dubbio, contatta un esperto di recapito.

1. Salva le modifiche.

L’aggiornamento ha effetto immediato o asincrono, a seconda che il pool IP sia associato a un [superficie del canale](channel-surfaces.md) o no:

* Se il pool IP è **not** associato a qualsiasi superficie del canale, l&#39;aggiornamento è istantaneo (**[!UICONTROL Completato]** status).
* Se il pool IP **è** associato a una superficie del canale, l’aggiornamento può richiedere fino a 3 ore (**[!UICONTROL Elaborazione]** status).

>[!NOTE]
>
>Quando [creazione di una superficie del canale](channel-surfaces.md#create-channel-surface), se selezioni un pool IP in edizione (**[!UICONTROL Elaborazione]** status) e non è mai stato associato al sottodominio selezionato per quella superficie, non è possibile procedere con la creazione della superficie. [Ulteriori informazioni](channel-surfaces.md#subdomains-and-ip-pools)

Per controllare lo stato dell’aggiornamento del pool IP, fai clic sul pulsante **[!UICONTROL Altre azioni]** e seleziona **[!UICONTROL Ultimi aggiornamenti]**.

![](assets/ip-pool-recent-update.png)

>[!NOTE]
>
>Una volta aggiornato correttamente un pool IP, potresti dover attendere:
>* alcuni minuti prima che sia consumata dai messaggi unitari,
>* fino al batch successivo per l&#39;efficacia del pool IP nei messaggi batch.


È inoltre possibile utilizzare **[!UICONTROL Elimina]** per eliminare un pool IP. Non è possibile eliminare un pool IP associato a una superficie del canale.

