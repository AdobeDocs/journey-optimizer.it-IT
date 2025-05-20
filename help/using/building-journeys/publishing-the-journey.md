---
solution: Journey Optimizer
product: journey optimizer
title: Pubblica il percorso
description: Scopri come pubblicare un percorso
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: pubblicazione, percorso, live, validità, verifica
exl-id: e0ca8aef-4f1d-4631-8c34-1692d96e8b51
source-git-commit: 5bdacef2196592776c6b37708b0df0986460ca1f
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 41%

---

# Pubblicare il percorso {#publishing-the-journey}

Per attivare un percorso e consentirne l’accesso da parte di nuovi profili, è necessario pubblicarlo. La pubblicazione rende il percorso attivo e funzionale. Prima di pubblicare, è necessario assicurarsi che il percorso sia completo e valido e correggere eventuali errori, in quanto un percorso non può essere pubblicato se contiene errori.

➡️ [Guarda il video su questa funzione](#video)

## Processo di pubblicazione {#journey-publication}

I passaggi per pubblicare un percorso sono descritti di seguito:

1. Prima di pubblicare il percorso, assicurati che sia valido e privo di errori. I percorsi non possono essere pubblicati se contengono errori.

   * Scopri come verificare il percorso in [questa pagina](testing-the-journey.md).
   * Scopri come risolvere gli errori di percorso in [questa sezione](../building-journeys/troubleshooting.md#checking-for-errors-before-testing).

1. Per pubblicare il percorso, fai clic sull&#39;opzione **[!UICONTROL Pubblica]**, che si trova nel menu a discesa in alto a destra.

   >[!NOTE]
   >
   > Se il percorso è soggetto a una policy di approvazione, è necessario richiedere l’approvazione prima di poterla pubblicare. [Ulteriori informazioni](../test-approve/gs-approval.md)


   ![](assets/journeyuc1_18.png)

Il percorso pubblicato è in modalità **sola lettura**. Quando un percorso è di sola lettura, è possibile modificare solo le etichette e le descrizioni delle attività, il nome del percorso e la descrizione del percorso. Se hai bisogno di apportare ulteriori modifiche a un percorso pubblicato, crea [una nuova versione](journey-ui.md#journey-versions) del percorso.

Quando si arresta un percorso, questo viene arrestato in modo permanente: tutte le persone che scorrono nel percorso vengono fermate in modo permanente e il percorso smette di consentire nuovi ingressi. Per eseguire nuovamente il percorso, è necessario duplicarlo e pubblicare il nuovo percorso.


>[!IMPORTANT]
>
>Se vengono apportate modifiche a una decisione di offerta utilizzata in un messaggio di un percorso, devi annullare la pubblicazione del percorso e ripubblicarlo.  In questo modo le modifiche verranno incorporate nel messaggio del percorso e il messaggio sarà coerente con gli ultimi aggiornamenti.


## Versioni del percorso {#journey-versions}

Nell’elenco dei percorsi vengono visualizzate tutte le versioni dei percorsi e i relativi numeri di versione. Quando cerchi un percorso, la prima volta che apri l’applicazione le versioni più recenti vengono visualizzate nella parte superiore dell’elenco. Successivamente, puoi definire l’ordinamento desiderato, che verrà mantenuto dall’applicazione come preferenza utente. La versione del percorso viene visualizzata anche nella parte superiore dell’interfaccia di modifica del percorso, sopra l’area di lavoro.

![](assets/journeyversions1.png)

>[!NOTE]
>
>In genere, un profilo non può essere presente più volte nello stesso percorso e contemporaneamente per tutte le versioni attive del percorso. Se è stato abilitato il reingresso, un profilo può entrare di nuovo in un percorso, ma solo dopo che sarà completamente uscito dall’istanza precedente del percorso. [Ulteriori informazioni](entry-management.md).

### Creazione di una nuova versione di un percorso {#journey-create-new-version}

Se devi apportare delle modifiche a un percorso live, crea una nuova versione del percorso. Per creare una nuova versione di un percorso esistente, effettuare le seguenti operazioni:

1. Apri la versione più recente del percorso live, fai clic su **[!UICONTROL Crea una nuova versione]** e conferma.

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >È possibile creare una nuova versione solo a partire dalla versione più recente di un percorso.

1. Apporta le modifiche necessarie, quindi fai clic su **[!UICONTROL Pubblica]** e conferma.

Dal momento in cui il percorso viene pubblicato, i singoli utenti inizieranno a confluire nell’ultima versione del percorso. Le persone che erano già entrate in una versione precedente vi rimangono fino al completamento del percorso. Se in un secondo momento entrano di nuovo nello stesso percorso, passeranno alla versione più recente.

È possibile interrompere le versioni di percorso singolarmente. Tutte le versioni di un percorso hanno lo stesso nome.

Quando pubblichi una nuova versione di un percorso, la versione precedente termina automaticamente e il suo stato diventa **Chiuso**. Un percorso chiuso non accetta alcun ingresso. Anche se si interrompe la versione più recente, la versione precedente rimane chiusa.


>[!NOTE]
>
>Al controllo delle versioni dei percorsi si applicano specifiche protezioni e limitazioni. Ulteriori informazioni sono disponibili in [questa pagina](../start/guardrails.md#journey-versions-journey-versions-g).


## Video dimostrativo {#video}

Scopri come pubblicare un percorso in questo video:

>[!VIDEO](https://video.tv.adobe.com/v/3424998?quality=12)