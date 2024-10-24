---
solution: Journey Optimizer
product: journey optimizer
title: Bloccare il contenuto nei modelli e-mail
description: Scopri come bloccare il contenuto nei modelli e-mail.
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: 2a666364144cf320a9ed20741da7d6f5d22b0d96
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 3%

---


# Bloccare il contenuto nei modelli e-mail {#lock-content-email-templates}

Journey Optimizer consente di bloccare il contenuto nei modelli e-mail, bloccando l’intero modello o strutture e componenti specifici. Questo consente di evitare modifiche o eliminazioni non intenzionali, garantendo un maggiore controllo sulla personalizzazione dei modelli e migliorando l’efficienza e l’affidabilità delle campagne e-mail.

>[!AVAILABILITY]
>
>Gli utenti autorizzati a creare modelli di contenuto possono abilitare il blocco.

Il blocco del contenuto può essere applicato al livello **struttura** o al livello **componente**. Di seguito sono elencati i principali principi applicabili a livello di struttura e componente quando si blocca il contenuto nel modello.

* Quando una struttura è bloccata:

   * Anche tutto il contenuto all’interno di tale struttura è bloccato per impostazione predefinita.
   * Nessun contenuto può essere aggiunto alla struttura.
   * Per impostazione predefinita, non è possibile eliminare la struttura. È possibile ignorare questa restrizione abilitando l’opzione &quot;Consenti eliminazione&quot;.
   * I singoli componenti di contenuto all’interno della struttura bloccata possono essere impostati come modificabili.

* Quando una struttura è modificabile (struttura non bloccata):

   * I singoli componenti di contenuto possono essere bloccati all’interno di tale struttura.
   * Per impostazione predefinita, non è possibile eliminare un componente se è bloccato o se è selezionato &quot;Solo blocco di contenuto modificabile&quot;. È possibile ignorare questa restrizione abilitando l’opzione &quot;Consenti eliminazione&quot;.

## Bloccare un modello e-mail {#define}

### Abilita blocco del contenuto {#enable}

Puoi abilitare il blocco del contenuto per un modello e-mail direttamente in E-mail Designer, sia che tu stia creando un nuovo modello che ne stia modificando uno esistente. Segui questi passaggi:

1. Apri o crea un modello e-mail e accedi alla schermata di modifica del contenuto nel Designer e-mail.

1. Nel riquadro **[!UICONTROL Corpo]** a destra, attiva l&#39;opzione **[!UICONTROL Governance]**.

1. Dall&#39;elenco a discesa **[!UICONTROL Modalità]**, selezionare la modalità di blocco desiderata per il modello:

   * **[!UICONTROL Blocco del contenuto]**: blocca sezioni specifiche del contenuto all&#39;interno del modello. Per impostazione predefinita, tutte le strutture e i componenti diventano modificabili. Puoi quindi bloccare selettivamente singoli elementi.
   * **[!UICONTROL Sola lettura]**: blocca l&#39;intero contenuto del modello, impedendo eventuali modifiche.

   ![](assets/template-lock-enable.png)

1. Se hai selezionato la modalità **[!UICONTROL Blocco contenuto]**, puoi definire ulteriormente il modo in cui gli utenti possono interagire con il modello. Attiva l&#39;opzione **[!UICONTROL Abilita edizione contenuto]** e scegli una delle opzioni seguenti:

   * **[!UICONTROL Consenti aggiunta struttura e contenuto]**: gli utenti possono aggiungere strutture tra quelle esistenti e aggiungere componenti di contenuto o frammenti all&#39;interno di strutture modificabili.

   * **[!UICONTROL Consenti solo l&#39;aggiunta di contenuto]**: gli utenti possono aggiungere componenti di contenuto o frammenti all&#39;interno di strutture modificabili, ma non possono aggiungere o duplicare strutture.

1. Dopo aver selezionato la modalità di blocco, puoi definire quali strutture e/o componenti bloccare se hai selezionato la modalità **[!UICONTROL Blocco contenuto]**:

   * [Scopri come bloccare le strutture](#lock-structures)
   * [Scopri come bloccare i componenti](#lock-components)

   Se hai scelto la modalità **[!UICONTROL Sola lettura]**, puoi procedere con la finalizzazione e il salvataggio del modello come di consueto.

Puoi modificare le impostazioni di **[!UICONTROL Governance]** in qualsiasi momento durante la progettazione del modello selezionando il corpo del modello. A questo scopo, fai clic sul collegamento **[!UICONTROL Corpo]** nella barra di navigazione in alto nel riquadro a destra.

![](assets/template-lock-body.png)

### Blocca strutture {#lock-structures}

Per bloccare una struttura all’interno del modello:

1. Seleziona la struttura da bloccare.

1. Nell&#39;elenco a discesa **[!UICONTROL Blocca tipo]** scegliere **[!UICONTROL Bloccato]**.

   ![](assets/template-lock-structure.png)

   >[!NOTE]
   >
   >Per impostazione predefinita, gli utenti non possono eliminare le strutture bloccate. È possibile ignorare questa restrizione abilitando l&#39;opzione **[!UICONTROL Consenti eliminazione]**.

Dopo aver bloccato una struttura, non è più possibile duplicare o aggiungere altri componenti o frammenti di contenuto al suo interno. Anche tutti i componenti all’interno di una struttura bloccata vengono bloccati per impostazione predefinita. Per rendere modificabile un componente all’interno di una struttura bloccata:

1. Seleziona il componente da sbloccare.

1. Attiva l&#39;opzione **[!UICONTROL Usa blocco specifico]**.

1. Nell&#39;elenco a discesa **[!UICONTROL Blocca tipo]** scegliere **[!UICONTROL Modificabile]**. Per consentire la modifica del contenuto durante il blocco degli stili, selezionare **[!UICONTROL Solo contenuto modificabile]**. [Scopri come bloccare i componenti](#lock-components)

   ![](assets/template-lock-editable-component.png)

### Blocca componenti {#lock-components}

Per bloccare un componente specifico all’interno di una struttura:

1. Selezionare il componente e abilitare l&#39;opzione **[!UICONTROL Usa blocco specifico]** nel riquadro di destra.

1. Dall&#39;elenco a discesa **[!UICONTROL Blocca tipo]**, selezionare l&#39;opzione di blocco preferita:

   ![](assets/template-lock-component.png)

   * **[!UICONTROL Solo blocco contenuto modificabile]**: blocca gli stili del componente ma consente la modifica del contenuto.
   * **[!UICONTROL Bloccato]**: blocco completo del contenuto e degli stili del componente.

   >[!NOTE]
   >
   >Il tipo di blocco **[!UICONTROL Modificabile]** consente agli utenti di modificare un componente, anche all&#39;interno di una struttura bloccata. [Scopri come bloccare le strutture](#lock-structures)

1. Per impostazione predefinita, gli utenti non possono eliminare i componenti bloccati. È possibile abilitare l&#39;eliminazione attivando l&#39;opzione **[!UICONTROL Consenti eliminazione]**.

### Identificare il contenuto bloccato {#identify}

Per identificare facilmente le strutture e i componenti bloccati all&#39;interno del modello, utilizzare la **[!UICONTROL struttura di spostamento]** disponibile nel menu a sinistra. Questo menu fornisce una panoramica visiva di tutti gli elementi del modello, evidenziando gli elementi bloccati con un’icona a forma di lucchetto e gli elementi modificabili con un’icona a forma di matita.

Nell’esempio seguente, la governance è abilitata per il corpo del modello. *La struttura 2* è bloccata con *Il componente 1* è modificabile, mentre *La struttura 3* è completamente bloccata.

![](assets/template-lock-navigation.png)

## Utilizzare i modelli con contenuti bloccati {#use}

Quando si utilizza un modello con contenuto bloccato, nel riquadro di destra viene visualizzato il messaggio **[!UICONTROL Governance abilitata]**.

A seconda del tipo di blocco applicato al modello, è possibile eseguire azioni diverse sulle strutture e sui componenti del modello. Per identificare rapidamente tutte le aree modificabili nel modello, attiva le opzioni **[!UICONTROL Evidenzia aree modificabili]**.

Ad esempio, nel modello seguente, tutte le aree sono modificabili, ad eccezione dell’immagine superiore che è stata bloccata, il che significa che non è possibile modificarla o rimuoverla.

![](assets/template-lock-highlight.png)

Per informazioni dettagliate sui diversi tipi di blocco che è possibile applicare, vedere le sezioni seguenti:

* [Blocca strutture](#lock-structures)
* [Blocca componenti](#lock-components)

Di seguito sono riportati alcuni esempi di modifica delle e-mail e della configurazione associata di blocco del contenuto che è stata configurata:


| Tipo di blocco del contenuto | Configurazione del modello | Edizione e-mail |
| ------- | ------- | ------- |
| Modello di contenuto di sola lettura | ![](assets/locking-sample-read-only-conf.png){zoomable="yes"} | ![](assets/locking-sample-read-only.png){zoomable="yes"} |
| Il contenuto completo è modificabile, ma gli utenti non possono aggiungere alcuna struttura o componente | ![](assets/locking-sample-no-addition-conf.png){zoomable="yes"} | ![](assets/locking-sample-no-addition.png){zoomable="yes"} |
| Struttura bloccata che non può essere eliminata | ![](assets/locking-sample-structure-locked-conf.png){zoomable="yes"} | ![](assets/locking-sample-structure-locked.png){zoomable="yes"} |
| Componente con stili bloccati che non può essere eliminato. Gli utenti possono solo modificare il contenuto. | ![](assets/locking-sample-content-only-conf.png){zoomable="yes"} | ![](assets/locking-sample-content-only.png){zoomable="yes"} |
| Componente modificabile in una struttura bloccata. | ![](assets/locking-sample-editable-component-conf.png){zoomable="yes"} | ![](assets/locking-sample-editable-component.png){zoomable="yes"} |
