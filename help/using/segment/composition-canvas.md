---
solution: Journey Optimizer
product: journey optimizer
title: Lavorare nell’area di lavoro per la composizione
description: Scopri come lavorare con l’area di lavoro della composizione
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '989'
ht-degree: 2%

---

# Lavorare nell’area di lavoro per la composizione {#composition-canvas}

L’area di lavoro della composizione è un’area di lavoro visiva che consente di creare composizioni sfruttando il pubblico e le attività (divise, escluse..).

I passaggi per configurare una composizione nell&#39;area di lavoro della composizione sono i seguenti:

1. [Definire i tipi di pubblico iniziali](#starting-audience)
1. [Aggiungi una o più attività](#action-activities)
1. [Salvare i risultati in un nuovo pubblico](#save)

## Selezionare il pubblico iniziale {#starting-audience}

>[!CONTEXTUALHELP]
>id="ajo_ao_merge_types"
>title="Tipi di unione"
>abstract="Specifica come devono essere uniti i profili dei tipi di pubblico selezionati."

Il primo passaggio per creare una composizione consiste nel selezionare uno o più tipi di pubblico esistenti come base della composizione.

Seleziona la **[!UICONTROL Pubblico]** quindi fai clic su **[!UICONTROL Aggiungi pubblico]** quindi seleziona uno o più tipi di pubblico.

In questo esempio, vogliamo eseguire il targeting di tutti i profili appartenenti al pubblico gold e silver.

![](assets/audiences-starting-audience.png)

Se selezioni più tipi di pubblico, specifica in che modo i profili di questi tipi di pubblico devono essere uniti:

* **[!UICONTROL Union]**: includere tutti i profili dal pubblico selezionato,
* **[!UICONTROL Intersection]**: includere profili comuni a tutti i tipi di pubblico selezionati,
* **[!UICONTROL Escludi sovrapposizione]**: includere profili che appartengono solo a uno dei tipi di pubblico. I profili appartenenti a più di un pubblico non verranno inclusi.

## Aggiungi attività {#action-activities}

Aggiungi le attività dopo aver selezionato il pubblico iniziale per perfezionare la selezione.

A questo scopo, fai clic sul pulsante + nel percorso della composizione, quindi seleziona l’attività desiderata. Viene visualizzato il riquadro a destra, che consente di configurare l’attività.

![](assets/audiences-select-activity.png)

>[!NOTE]
>
>Puoi aggiungere più **[!UICONTROL Pubblico]** e **[!UICONTROL Escludi]** attività necessarie nella composizione. Tuttavia, non è possibile aggiungere attività aggiuntive dopo **[!UICONTROL Classificazione]** e **[!UICONTROL Divisione]** attività .

Puoi rimuovere un’attività dall’area di lavoro in qualsiasi momento facendo clic sul pulsante Elimina nel riquadro a destra. Anche tutte le attività aggiunte dopo questa attività verranno rimosse dall’area di lavoro.

Le attività disponibili sono:

* [Pubblico](#audience): includere profili aggiuntivi appartenenti a uno o più tipi di pubblico esistenti,
* [Escludi](#exclude): escludere profili appartenenti a un pubblico esistente o escludere profili basati su attributi specifici,
* [Classificazione](#rank): classificare i profili in base a un attributo specifico, specificare il numero di profili da mantenere e includerli nella composizione,
* [Divisione](#split): dividi la composizione in più percorsi in base a percentuali casuali o su attributi.

### Attività pubblico {#audience}

>[!CONTEXTUALHELP]
>id="ajo_ao_audience"
>title="Attività pubblico"
>abstract="L’attività Pubblico ti consente di includere nella composizione profili aggiuntivi appartenenti a un pubblico esistente."

La **[!UICONTROL Pubblico]** l’attività ti consente di includere nella composizione profili aggiuntivi appartenenti a un pubblico esistente.

La configurazione di questa attività è identica a quella iniziale [Attività pubblico](#starting-audience).

### Escludi attività {#exclude}

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude_type"
>title="Tipo di esclusione"
>abstract="Utilizza il tipo di pubblico Escludi per escludere i profili appartenenti a un pubblico esistente. L’opzione Escludi utilizzando il tipo di attributo ti consente di escludere i profili basati su un attributo specifico."

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude"
>title="Escludi attività"
>abstract="L’attività Escludi ti consente di escludere i profili dalla composizione selezionando un pubblico esistente o utilizzando una regola."

La **[!UICONTROL Escludi]** l’attività ti consente di escludere i profili dalla composizione. Sono disponibili due tipi di esclusione:

* **[!UICONTROL Escludi pubblico]**: Escludi i profili appartenenti a un pubblico esistente.

   Fai clic sul pulsante **[!UICONTROL Aggiungi pubblico]** quindi seleziona il pubblico da escludere.

   ![](assets/audiences-exclude-audience.png)

* **[!UICONTROL Escludi utilizzando l’attributo]**: Escludere i profili in base a un attributo specifico.

   Seleziona l&#39;attributo da cercare e specifica il valore da escludere. In questo esempio, escludiamo dai profili di composizione il cui indirizzo di casa è in Giappone.

   ![](assets/audiences-exclude-attribute.png)

### Attività di classifica {#rank}

>[!CONTEXTUALHELP]
>id="ajo_ao_ranking"
>title="Attività di classificazione"
>abstract="L’attività Classifica ti consente di classificare i profili in base a un attributo specifico e di includerli nella composizione. Ad esempio, includi i 50 profili con la maggiore quantità di punti fedeltà."

>[!CONTEXTUALHELP]
>id="ajo_ao_rank_profilelimit_text"
>title="Aggiungi limite profilo"
>abstract="Attiva questa opzione per specificare un numero massimo di profili da includere nella composizione."

La **[!UICONTROL Classificazione]** l’attività ti consente di classificare i profili in base a un attributo specifico e di includerli nella composizione. Ad esempio, puoi includere i 50 profili con la maggiore quantità di punti fedeltà.

1. Seleziona l’attributo da cercare e specifica un ordine di classificazione (crescente o decrescente).

   >[!NOTE]
   >
   >Puoi selezionare gli attributi con i seguenti tipi di dati: numero intero, numeri, breve <!--(other?)-->

1. Attiva/disattiva la **[!UICONTROL Aggiungi limite profilo]** su e specifica un numero massimo di profili da includere nella composizione.

   ![](assets/audiences-rank.png)

### Dividi attività {#split}

>[!CONTEXTUALHELP]
>id="ajo_ao_control_group_text"
>title="Gruppo di controllo"
>abstract="Utilizza i gruppi di controllo per isolare una parte dei profili. Questo ti consente di misurare l’impatto di un’attività di marketing e di effettuare un confronto con il comportamento del resto della popolazione."

>[!CONTEXTUALHELP]
>id="ajo_ao_split"
>title="Dividi attività"
>abstract="L’attività Dividi ti consente di dividere la composizione in più percorsi. Quando si pubblica la composizione, un pubblico viene salvato in Adobe Experience Platform per ogni percorso."

>[!CONTEXTUALHELP]
>id="ajo_ao_split_type"
>title="Tipo di divisione"
>abstract="Utilizza il tipo di suddivisione percentuale per dividere in modo casuale i profili in più percorsi. Il tipo di suddivisione dell’attributo consente di suddividere i profili in base a un attributo specifico."

>[!CONTEXTUALHELP]
>id="ajo_ao_split_otherprofiles_text"
>title="Altri profili"
>abstract="Attiva questa opzione per creare un percorso aggiuntivo con i profili rimanenti che non corrispondono a nessuna delle condizioni specificate negli altri percorsi."

La **[!UICONTROL Divisione]** l’attività ti consente di dividere la composizione in più percorsi.

Questa operazione aggiunge automaticamente una **[!UICONTROL Salva]** attività alla fine di ogni percorso. Quando si pubblica la composizione, un pubblico viene salvato in Adobe Experience Platform per ogni percorso.

Sono disponibili due tipi di operazioni suddivise:

* **[!UICONTROL Divisione percentuale]**: dividi i profili in modo casuale in due o più percorsi. Ad esempio, puoi dividere i profili in 2 percorsi distinti del 45% ciascuno e aggiungere un percorso aggiuntivo per il gruppo di controllo.

   ![](assets/audiences-split-percentage.png)

* **[!UICONTROL Divisione attributo]**: dividere i profili in base a un attributo specifico. In questo esempio, suddividiamo i profili in base alle loro preferenze per il tipo di stanza.

   ![](assets/audiences-split.png)

   >[!NOTE]
   >
   >La **[!UICONTROL Altri profili]** consente di creare un percorso aggiuntivo con i profili rimanenti che non corrispondono a nessuna delle condizioni specificate negli altri percorsi.

## Salvare i tipi di pubblico {#save}

Configura i tipi di pubblico risultanti che verranno salvati in Adobe Experience Platform.

A questo scopo, seleziona la **[!UICONTROL Save audience]** alla fine di ogni percorso, specifica il nome del nuovo pubblico da creare.

![](assets/audiences-publish.png)

Una volta pronta la composizione, puoi pubblicarla. [Scopri come creare le composizioni](create-compositions.md)

Per saperne di più:

* [Introduzione alla composizione dei tipi di pubblico](get-started-audience-orchestration.md)
* [Creare flussi di lavoro di composizione](create-compositions.md)
* [Accesso e gestione dei tipi di pubblico](access-audiences.md)
