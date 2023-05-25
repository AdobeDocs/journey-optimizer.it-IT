---
solution: Journey Optimizer
product: journey optimizer
title: Gestire la rinuncia
description: Scopri come gestire l’opt-out e la privacy
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: f5390bbb3bab435b21ace4d1842de0048132bc8c
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 1%

---

# Implementare il consenso per la rinuncia alla personalizzazione {#cpes-opt-out}


## Editor espressioni

Editor espressioni durante la personalizzazione di immagini, testo, riga dell’oggetto ( Segmento nelle campagne ) - Interfaccia utente e Headless

L’editor di personalizzazione non esegue alcun controllo del consenso o applicazione, in quanto non è coinvolto nella consegna delle azioni del messaggio. L’editor di personalizzazione aderisce alle etichette di controllo dell’accesso basate sui diritti fornite dal servizio di profilo unificato per consentire/non consentire l’utilizzo di campi diversi per la personalizzazione. Il servizio di anteprima e rendering dei messaggi nasconde i campi identificati con informazioni riservate.

Nelle campagne AJO, l’applicazione dei criteri di consenso può avvenire in due luoghi. I clienti possono includere le definizioni dei criteri di consenso nella creazione del pubblico o del segmento per garantire che il pubblico selezionato per la campagna abbia già filtrato i profili che non corrispondono ai criteri di consenso. In secondo luogo, il servizio runtime dei messaggi eseguirà un controllo generale del consenso a livello di canale per garantire che i profili abbiano acconsentito alla ricezione di comunicazioni di marketing sul canale specifico. Al momento, l’oggetto AJO Campaign non esegue ulteriori controlli di applicazione dei criteri di consenso.

Passaggi di Campagna AJO e Personalizzazione per applicare manualmente il consenso:

Lo stato di consenso e le preferenze di personalizzazione di un utente devono far parte delle regole e della definizione di pubblico prima dell’attivazione in una campagna di Journey Optimizer. Un utente marketing in Adobe Experience Platform può aggiungere un controllo del consenso al proprio pubblico creando una nuova composizione di pubblico o definendo un nuovo segmento tramite il generatore di regole.

Se utilizzi il compositore pubblico, puoi dividere il pubblico utilizzando gli attributi del profilo. Dopo aver effettuato le selezioni sugli attributi di consenso appropriati che desideri controllare, puoi salvare i tipi di pubblico risultanti per l’attivazione in una campagna. Tieni presente che se crei un pubblico che non ha dato il consenso per la personalizzazione e quindi selezioni questo pubblico per l’attivazione in una campagna, gli strumenti di personalizzazione rimarranno disponibili. Spetta all’utente marketing capire che, se lavora con un pubblico che non deve ricevere personalizzazioni, non deve utilizzare gli strumenti di personalizzazione.

Per creare un pubblico diviso nella composizione del pubblico, segui questi passaggi:

1. Seleziona il pubblico iniziale.

1. Fai clic sull’icona più per creare un pubblico diviso.

1. Nelle proprietà di [PROD143]e, scegliete &quot;attribute split&quot; come tipo.

1. Nel campo attributo, fai clic sull’icona della matita per visualizzare la finestra di selezione degli attributi.

1. Digita il valore Choice per cercare l’attributo di consenso della personalizzazione (tieni presente che si tratta dell’attributo path profile.consents.personalize.content.val)

1. Selezionare questo attributo.

1. In Percorso 1: scegli un’etichetta per definire il pubblico non personalizzato.

1. Scegli il valore appropriato da questo elenco: https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html?lang=en#choice-values

   In questo caso utilizzeremo una &quot;n&quot; per indicare NO come rinuncia alla personalizzazione

   Puoi creare un percorso separato per altri valori di scelta oppure scegliere di eliminare i percorsi rimanenti e attivare &quot;altri profili&quot;, che includerebbero tutti gli altri profili che non hanno un valore di scelta &quot;n&quot;.

1. Al termine, fai clic nella casella in cui è riportato &quot;Save Audience&quot; (Salva pubblico). Viene visualizzata una nuova finestra delle proprietà che consente di scegliere il nome da utilizzare per i tipi di pubblico derivati.

1. Al termine, pubblica la composizione del pubblico.

Se utilizzi il generatore di regole di segmento per creare il pubblico, puoi selezionare le scelte di personalizzazione e valore del consenso come parametri di esclusione nella definizione del pubblico. Aggiungendo i parametri di esclusione puoi creare un singolo segmento di pubblico di profili in cui gli individui che non hanno dato il consenso vengono esclusi.

