---
solution: Journey Optimizer
product: journey optimizer
title: Gestire la rinuncia
description: Scopri come gestire l’opt-out e la privacy
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: be372f8f80d304067748d539fb8e210df6280721
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 100%

---

# Implementare il consenso per la rinuncia alla personalizzazione {#cpes-opt-out}


## Editor espressioni

Editor espressioni durante la personalizzazione di immagini, testo, riga dell’oggetto (segmento nelle campagne) - Interfaccia utente e headless

L’Editor personalizzazione stesso non esegue alcun controllo o applicazione del consenso, in quanto non è coinvolto nelle azioni di consegna dei messaggi. L’Editor personalizzazione rispetta le etichette di controllo degli accessi basate sui diritti fornite dal servizio per profili unificati per consentire o meno l’utilizzo di campi diversi per la personalizzazione. Il servizio di anteprima e rendering dei messaggi nasconde i campi identificati con informazioni sensibili.

Nelle campagne AJO, l’applicazione dei criteri di consenso può avvenire in due punti. I clienti possono includere le definizioni dei criteri di consenso nella creazione del pubblico o del segmento affinché nel pubblico selezionato per la campagna siano già stati filtrati ed esclusi i profili che non corrispondono ai criteri di consenso. In secondo luogo, il servizio di runtime dei messaggi eseguirà un controllo generale del consenso a livello di canale per verificare che i profili abbiano acconsentito alla ricezione di comunicazioni di marketing tramite il canale specifico. Al momento, l’oggetto stesso della campagna AJO non esegue ulteriori controlli relativi all’applicazione dei criteri di consenso.

Campagna AJO e passaggi di personalizzazione per applicare manualmente il consenso:

Lo stato di consenso e le preferenze di personalizzazione di un utente devono far parte delle regole e della definizione del pubblico prima dell’attivazione in una campagna Journey Optimizer. Per aggiungere al proprio pubblico un controllo del consenso, l’utente marketing può creare in Adobe Experience Platform una nuova composizione di pubblico o definire un nuovo segmento tramite il generatore di regole.

Se utilizzi il compositore di pubblico, puoi suddividere il pubblico utilizzando gli attributi del profilo. Dopo aver selezionato gli attributi di consenso appropriati che desideri controllare, puoi salvare i tipi di pubblico risultanti per l’attivazione in una campagna. Tieni presente che se crei un pubblico che non ha dato il consenso alla personalizzazione e quindi selezioni tale pubblico per l’attivazione in una campagna, gli strumenti di personalizzazione rimarranno comunque disponibili. L’utente marketing dovrà quindi essere consapevole del fatto che, quando lavora con un pubblico che non deve ricevere personalizzazioni, non dovrà utilizzare gli strumenti di personalizzazione.

Per creare un pubblico suddiviso nella composizione del pubblico, segui questi passaggi:

1. Seleziona il pubblico iniziale.

1. Fai clic sull’icona più per creare un pubblico diviso.

1. Nelle proprietà di suddivisione, scegli il tipo “Suddivisione attributi”.

1. Nel campo Attributo, fai clic sull’icona della matita per visualizzare la finestra di selezione degli attributi.

1. In Valore scelta, digita l’attributo di consenso alla personalizzazione da cercare (tieni presente che si tratta del percorso di attributo profile.consents.personalize.content.val)

1. Seleziona questo attributo.

1. In Percorso 1: scegli un’etichetta per definire il pubblico non personalizzato.

1. Scegli il valore appropriato da questo elenco: https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=it#choice-values

   In questo esempio, per la rinuncia alla personalizzazione useremo una “n” per indicare NO.

   Puoi creare un percorso separato per altri valori di scelta; oppure puoi eliminare i percorsi rimanenti e attivare “Altri profili”, che includeranno tutti gli altri profili che non presentano il valore di scelta “n”.

1. Al termine, fai clic nella casella in cui è riportato “Salva pubblico”. Viene visualizzata una nuova finestra delle proprietà che consente di scegliere il nome da utilizzare per i tipi di pubblico derivati.

1. Al termine, pubblica la composizione del pubblico.

Se utilizzi il generatore di regole di segmento per creare il pubblico, nella definizione del pubblico puoi selezionare scelte di valore per personalizzazione e consenso come parametri di esclusione. Aggiungendo i parametri di esclusione puoi creare un singolo segmento di pubblico composto di profili da cui vengono esclusi i singoli utenti che non hanno dato il consenso.
