---
solution: Journey Optimizer
product: journey optimizer
title: Inviare utilizzando gli scaglioni
description: Pianifica la consegna dei messaggi delle campagne in uscita in batch controllati nel tempo. L’invio tramite ondata supporta il recapito messaggi e consente di mantenere la reputazione del mittente.
feature: Campaigns
topic: Campaign scheduling
role: User
level: Intermediate
keywords: ondate, batch, pianificazione, campagna, percorso, recapito messaggi
source-git-commit: 6c509ef134c4240b243d255fd1ab7ec6bb062bf0
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 1%

---

# Inviare con scaglioni nelle campagne {#send-using-waves}

Puoi suddividere la consegna dei messaggi in uscita della campagna in più batch (ondate) e pianificarli nel tempo. L’invio ondata consente di bilanciare il carico, evitare l’eccessiva sovraccarico dei sistemi a valle (come i call center o le pagine di destinazione) e supportare il recapito dei messaggi e la reputazione del mittente, in particolare per gli invii di volumi elevati.

<!--
>[!CAUTION]
>
>Wave sending applies to **outbound** actions only (Email, SMS, Push, Direct mail).-->

Journey Optimizer consente di definire il numero di scaglioni, la loro dimensione (come percentuale del pubblico o come numeri assoluti) e quando viene eseguito ogni scaglione.

## Limitazioni e protezioni {#limitations-guardrails}

* L&#39;invio ondata si applica solo alle **azioni in uscita** (e-mail, SMS, push, direct mail).
* È necessario definire almeno **2 scaglioni** e aggiungere fino a **10 scaglioni**.
* L&#39;intervallo minimo tra l&#39;inizio di due scaglioni è **30 minuti**.
* L’inizio di un’ondata non può precedere l’inizio della campagna o essere nel passato.

## Configurare l’invio ondata {#configure-wave-sending}

Per configurare come e quando inviare scaglioni in una campagna, segui i passaggi indicati di seguito.

1. Crea o apri una [campagna Azione](create-campaign.md) contenente un&#39;azione in uscita (ad esempio E-mail, SMS, Push).

1. Nella scheda **[!UICONTROL Pianifica]** della campagna, seleziona **[!UICONTROL Consegna azioni campagna in modo graduale]**.

   ![](assets/campaign-wave-option.png){width="100%"}

   >[!NOTE]
   >
   >L&#39;opzione **[!UICONTROL Consegna campagne in ondate]** viene visualizzata solo quando nella scheda **[!UICONTROL Azioni]** della campagna è selezionata un&#39;azione in uscita. [Ulteriori informazioni](campaign-action.md)

1. Imposta il numero di scaglioni che desideri inviare (ad esempio, 4).

   >[!NOTE]
   >
   >È necessario definire almeno 2 scaglioni e aggiungere fino a 10 scaglioni.

1. Scegliete come definire la dimensione e la tempistica dell&#39;onda come descritto di seguito.

### Onde uguali {#equal-waves}

Per impostazione predefinita, il pubblico è suddiviso in ondate di uguali dimensioni. Pianifica il tempo per la prima ondata e imposta un intervallo fisso tra l&#39;inizio di ogni ondata (ad esempio, 2 ore).

![](assets/campaign-equal-waves.png){width="80%"}

>[!NOTE]
>
>L&#39;intervallo minimo tra l&#39;inizio di due scaglioni è **30 minuti**.

Il sistema pianifica quindi automaticamente le ondate successive (ad esempio, la prima ondata alle ore 9:00, la seconda alle ore 11:00, la terza alle ore 1:00, la quarta alle ore 15:00).

### Distribuzione personalizzata {#custom-distribution}

Seleziona l&#39;opzione **[!UICONTROL Distribuzione personalizzata]** per definire la dimensione di ogni ondata come percentuale del pubblico totale (ad esempio, 15%, 20%, 25%, 40%).

![](assets/campaign-wave-percentage.png){width="80%"}

>[!NOTE]
>
>Il totale su tutte le ondate deve essere uguale al 100%. In caso contrario, verrà visualizzato un messaggio di avviso.<!--are the waves actually sent or does the system prevent user from saving the campaign?-->

Seleziona **[!UICONTROL Numeri]** per definire la dimensione di ogni ondata come numero assoluto di profili (ad esempio, 10.000; 50.000).

![](assets/campaign-wave-numbers.png){width="80%"}

>[!NOTE]
>
>Quando si utilizzano i numeri, il sistema non verifica che la somma copra l&#39;intero pubblico. È necessario assicurarsi che le dimensioni delle onde coprano il pubblico al quale si intende inviare il messaggio. Ulteriori informazioni sono disponibili nelle [Domande frequenti](#faq).

### Pianificazione personalizzata {#custom-schedule}

Seleziona **[!UICONTROL Pianifica ogni scaglione]** per definire una data e un&#39;ora di inizio specifiche per ogni scaglione. Non è necessario che le onde siano equidistanti (ad esempio, 9:00 AM, 11:00 AM, 5:00 PM, 8:30 PM).

![](assets/campaign-wave-custom-schedule.png){width="80%"}

>[!NOTE]
>
>L&#39;intervallo minimo tra l&#39;inizio di due scaglioni è **30 minuti**.

## Casi d’uso {#use-cases}

L’invio ondata consente di controllare quando e quanti messaggi vengono inviati, migliorando il recapito messaggi, proteggendo la reputazione del mittente e allineando gli invii con la capacità operativa. Considera l’utilizzo delle onde in questi scenari:

* **Gestione call center o risposta:** limitare il numero di messaggi inviati al giorno o all&#39;ora in modo che i team a valle (ad esempio, l&#39;assistenza clienti) possano gestire le risposte. Ad esempio, invia 20 messaggi al giorno per far corrispondere la capacità del call center.

  ![](assets/campaign-waves-ex-call-center.png){width="75%"}

* **Volume elevato e recapito messaggi:** Evita di inviare una campagna di grandi dimensioni in un&#39;unica ripresa. Distribuisci la consegna nel tempo per contribuire a mantenere la reputazione del mittente e ridurre il rischio di essere segnalato come spam.

  ![](assets/campaign-waves-ex-high-volume.png){width="75%"}

* **Incremento:** Quando si utilizza una nuova piattaforma o un nuovo indirizzo IP, aumentare progressivamente il volume (ad esempio, 10% nella prima ondata, quindi 15%, 20% e così via) per creare la reputazione gradualmente.

  ![](assets/campaign-waves-ex-ramp-up.png){width="75%"}

## Domande frequenti {#faq}

+++ Cosa succede se la somma delle dimensioni delle onde non è uguale al pubblico totale?

* Se la somma delle dimensioni dell&#39;ondata **supera** il pubblico (ad esempio, pianifichi 100.000 nella prima ondata per un pubblico di 100.000), la prima ondata verrà inviata al pubblico completo e le ondate rimanenti non avranno più nessuno a cui inviare, non verranno eseguite.
* Se la somma **è inferiore** rispetto al pubblico (ad esempio, si definiscono quattro ondate per un totale di 40.000 profili per un pubblico di 100.000), solo i profili inclusi in tali ondate riceveranno il messaggio. Il resto del pubblico non riceverà la comunicazione e non verrà ritentato nelle ondate successive.

+++

+++ Posso assegnare segmenti o criteri diversi a singole ondate?

È possibile definire solo la dimensione e la tempistica delle onde. La selezione dei destinatari è la stessa per tutta la campagna; non è possibile assegnare segmenti o criteri diversi a singole ondate.

+++

## Passaggi successivi {#next}

* [Pianifica la campagna Azione](campaign-schedule.md)—imposta la data di inizio, la data di fine, la frequenza e il controllo della tariffa.
* [Rivedi e attiva la campagna](review-activate-campaign.md). Controlla la campagna e attiva.
