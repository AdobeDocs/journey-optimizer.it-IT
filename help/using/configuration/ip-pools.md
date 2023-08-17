---
solution: Journey Optimizer
product: journey optimizer
title: Creare pool IP
description: Scopri come gestire i pool IP
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: IP, pool, gruppo, sottodomini, recapito messaggi
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 10%

---

# Creare pool IP {#create-ip-pools}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool_header"
>title="Configurare un pool IP"
>abstract="I pool IP raccolgono gli indirizzi IP dei sottodomini per migliorare il recapito dei messaggi e-mail."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool"
>title="Configurare un pool IP"
>abstract="Con Journey Optimizer puoi creare pool IP per raggruppare gli indirizzi IP dei sottodomini. Questo può migliorare in modo significativo il recapito delle e-mail, evitando che la reputazione di un sottodominio influisca sugli altri sottodomini."

## Informazioni sui pool IP {#about-ip-pools}

Con [!DNL Journey Optimizer], puoi creare pool IP per raggruppare gli indirizzi IP dei tuoi sottodomini.

La creazione di pool IP è vivamente consigliata per il recapito messaggi e-mail. In questo modo, puoi evitare che la reputazione di un sottodominio influisca sugli altri sottodomini.

Ad esempio, una best practice consiste nell’avere un pool IP per i messaggi di marketing e un altro per i messaggi transazionali. In questo modo, se uno dei messaggi di marketing non funziona correttamente e viene dichiarato come spam da un cliente, questo non influirà sui messaggi transazionali inviati allo stesso cliente, che riceverà comunque messaggi transazionali (conferme di acquisto, messaggi di recupero password, ecc.).

>[!CAUTION]
>
>La configurazione del pool IP è comune a tutti gli ambienti. Pertanto, qualsiasi creazione o modifica di pool IP influirà anche sulle sandbox di produzione.

## Creare un pool IP {#create-ip-pool}

Per creare un pool IP, eseguire la procedura seguente:

1. Accedere a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Pool IP]** , quindi fai clic su **[!UICONTROL Crea pool IP]**.

   ![](assets/ip-pool-create.png)

1. Specifica un nome e una descrizione (facoltativa) per il pool IP.

   >[!NOTE]
   >
   >Il nome deve iniziare con una lettera (A-Z) e includere solo caratteri alfanumerici o caratteri speciali ( _, ., - ).

1. Seleziona gli indirizzi IP da includere nel pool dall’elenco a discesa, quindi fai clic su **[!UICONTROL Invia]**.

   ![](assets/ip-pool-config.png)

   >[!NOTE]
   >
   >Tutti gli indirizzi IP forniti con la tua istanza sono disponibili nell’elenco.

Quando selezioni gli IP, puoi visualizzare dall’elenco i record PTR associati agli IP. Questo consente di verificare le informazioni di branding per ogni IP durante la creazione di un pool IP e di selezionare, ad esempio, gli IP con le stesse informazioni di branding. [Ulteriori informazioni sui record PTR](ptr-records.md)

![](assets/ip-pool-ptr-record.png)

>[!NOTE]
>
>Se per un IP non è configurato alcun record PTR, non è possibile selezionare tale IP. Rivolgiti al rappresentante del tuo Adobe per configurare il record PTR di tale IP.

Dopo la creazione di un pool IP, le informazioni PTR sono visibili quando si passa il mouse sugli indirizzi IP visualizzati sotto l&#39;elenco a discesa del pool IP.

![](assets/ip-pool-ptr-record-tooltip.png)

Il pool IP viene ora creato e visualizzato nell’elenco. Puoi selezionarla per accedere alle relative proprietà e visualizzare la superficie di canale associata (ossia il predefinito per messaggi). Per ulteriori informazioni su come associare una superficie di canale a un pool IP, consulta [questa sezione](channel-surfaces.md).

![](assets/ip-pool-created.png)

## Modificare un pool IP {#edit-ip-pool}

Per modificare un pool IP, effettua le seguenti operazioni.

1. Dall’elenco, fai clic sul nome del pool IP per aprirlo.

   ![](assets/ip-pool-list.png)

1. Modificane le proprietà come desiderato. Puoi modificare la descrizione e aggiungere o rimuovere indirizzi IP.

   >[!NOTE]
   >
   >Impossibile modificare il nome del pool IP. Se desideri modificarlo, elimina il pool IP e creane un altro con il nome desiderato.

   ![](assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >Procedi con ulteriore cautela quando consideri di eliminare un IP, in quanto questo comporterà un carico aggiuntivo sugli altri IP e potrebbe avere gravi ripercussioni sulla consegna dei messaggi. In caso di dubbi, contatta un esperto di consegna.

1. Salva le modifiche.

L’aggiornamento viene eseguito immediatamente o in modo asincrono, a seconda del pool IP associato a un [superficie di canale](channel-surfaces.md) oppure no:

* Se il pool IP è **non** associato a qualsiasi superficie di canale, l’aggiornamento è istantaneo (**[!UICONTROL Completato]** stato).
* Se il pool IP **è** associato a una superficie di canale, l’aggiornamento può richiedere fino a 3 ore (**[!UICONTROL Elaborazione]** stato).

>[!NOTE]
>
>Quando [creazione di una superficie di canale](channel-surfaces.md#create-channel-surface), se si seleziona un pool IP in corso di modifica (**[!UICONTROL Elaborazione]** stato) e non è mai stata associata al sottodominio selezionato per quella superficie, non puoi procedere con la creazione della superficie. [Ulteriori informazioni](channel-surfaces.md#subdomains-and-ip-pools)

Per verificare lo stato di aggiornamento del pool IP, fare clic su **[!UICONTROL Altre azioni]** e seleziona **[!UICONTROL Aggiornamenti recenti]**.

![](assets/ip-pool-recent-update.png)

>[!NOTE]
>
>Una volta aggiornato correttamente un pool IP, potrebbe essere necessario attendere:
>* pochi minuti prima di essere utilizzato dai messaggi unitari,
>* fino al successivo batch per rendere effettivo il pool IP nei messaggi batch.

È inoltre possibile utilizzare **[!UICONTROL Elimina]** per eliminare un pool IP. Non è possibile eliminare un pool IP associato a una superficie di canale.

