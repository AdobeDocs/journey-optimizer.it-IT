---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare frammenti visivi
description: Scopri come utilizzare i frammenti visivi durante la creazione di e-mail nelle campagne e nei percorsi Journey Optimizer
feature: Email Design, Fragments
topic: Content Management
role: User
level: Beginner
exl-id: 25a00f74-ed08-479c-9a5d-4185b5f3c684
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 2%

---

# Aggiungere frammenti visivi alle e-mail {#use-visual-fragments}

Un frammento è un componente riutilizzabile a cui è possibile fare riferimento in una o più e-mail tra campagne Journey Optimizer, percorsi o modelli di contenuto. Questa funzionalità consente di precreare più blocchi di contenuto personalizzati che possono essere utilizzati dagli utenti di marketing per assemblare rapidamente i contenuti delle e-mail in un processo di progettazione migliorato. [Scopri come creare e gestire i frammenti](../content-management/fragments.md).

➡️ [Scopri come gestire, creare e utilizzare i frammenti in questo video](../content-management/fragments.md#video-fragments)

## Utilizzare un frammento {#use-fragment}

Per utilizzare un frammento in un’e-mail, segui i passaggi seguenti.

>[!NOTE]
>
>Puoi aggiungere fino a 30 frammenti in una determinata consegna. I frammenti possono essere nidificati solo fino a un livello.


1. Apri qualsiasi contenuto e-mail o modello utilizzando [E-mail Designer](get-started-email-design.md).

1. Seleziona l&#39;icona **[!UICONTROL Frammenti]** dalla barra a sinistra.

   ![](assets/fragments-in-designer.png)

1. Viene visualizzato l’elenco di tutti i frammenti visivi creati nella sandbox corrente. Sono ordinati per data di creazione: i frammenti visivi aggiunti di recente vengono visualizzati per primi nell’elenco. Puoi eseguire le seguenti operazioni:

   * Cerca un frammento specifico iniziando a digitarne l’etichetta.
   * Ordina i frammenti in ordine crescente o decrescente.
   * Modifica la modalità di visualizzazione dei frammenti (scheda o elenco).
   * Aggiorna l’elenco.

   >[!NOTE]
   >
   >Se alcuni frammenti sono stati modificati o aggiunti durante la modifica del contenuto, l’elenco verrà aggiornato con le modifiche più recenti.

1. Trascina un frammento dall’elenco nell’area in cui desideri inserirlo.

   ![](assets/fragment-insert.png)

   >[!CAUTION]
   >
   >Puoi aggiungere al contenuto qualsiasi frammento **Bozza** o **Live**. Tuttavia, non potrai attivare il percorso o la campagna se al suo interno viene utilizzato un frammento con lo stato Bozza. Durante la pubblicazione di un percorso o di una campagna, i frammenti bozza mostreranno un errore e dovrai approvarli per poterli pubblicare.

1. Come qualsiasi altro componente, puoi spostare il frammento all’interno del contenuto.

1. Seleziona il frammento per visualizzare il riquadro corrispondente a destra. Da lì puoi eliminare il frammento dal contenuto o duplicarlo. Puoi anche eseguire queste azioni direttamente dal menu contestuale visualizzato sopra il frammento.

   ![](assets/fragment-right-pane.png)

1. Dalla scheda **[!UICONTROL Impostazioni]** puoi effettuare le seguenti operazioni:

   * Scegli i dispositivi su cui vuoi visualizzare il frammento.
   * Apri il frammento in una nuova scheda per modificarlo, se necessario. [Ulteriori informazioni](../content-management/fragments.md#fragments)
   * Esplora i riferimenti. [Ulteriori informazioni](../content-management/fragments.md#visual-expression)

1. Puoi personalizzare ulteriormente il frammento utilizzando la scheda **[!UICONTROL Stili]**.

1. Se necessario, puoi interrompere l’ereditarietà con il frammento originale. [Ulteriori informazioni](#break-inheritance)

1. Aggiungi tutti i frammenti desiderati e **[!UICONTROL Salva]** le modifiche.

## Usa variabili implicite {#implicit-variables-in-fragments}

Le variabili implicite migliorano la funzionalità dei frammenti esistenti per migliorare l’efficienza in termini di riutilizzabilità dei contenuti e casi di utilizzo di script. I frammenti possono utilizzare variabili di input e creare variabili di output utilizzabili nel contenuto di campagne e percorsi.

Scopri come utilizzare le variabili implicite in [questa sezione](../personalization/use-expression-fragments.md#implicit-variables).

## Personalizza campi modificabili {#customize-fields}

Se alcune parti del frammento selezionato sono state rese modificabili, è possibile ignorarne il valore predefinito dopo aver aggiunto il frammento nel contenuto. [Scopri come rendere personalizzabili i tuoi frammenti](../content-management/customizable-fragments.md)

Per personalizzare i campi modificabili in un frammento, effettua le seguenti operazioni:

1. Aggiungi il frammento al contenuto.

1. Selezionala per aprire il riquadro delle proprietà sul lato destro.

   Tutti i campi modificabili nel frammento vengono visualizzati nella scheda **Impostazioni**, nella sezione **Frammento**.

1. Quando selezioni un campo modificabile nel riquadro di destra, questo viene evidenziato in verde nel riquadro di anteprima centrale, facilitando l’identificazione della sua posizione nel contenuto.

   Nell&#39;esempio seguente è possibile modificare l&#39;immagine **source** e **alt text**, nonché il pulsante &quot;Fai clic qui&quot; **URL**.

   ![](assets/fragment-editable.png)

## Interrompi ereditarietà {#break-inheritance}

Quando modifichi un frammento visivo, le modifiche vengono sincronizzate. Vengono propagati automaticamente a tutti i percorsi/campagne in bozza o live e ai modelli di contenuto contenenti tale frammento.

I frammenti aggiunti a un messaggio e-mail o a un modello di contenuto vengono sincronizzati per impostazione predefinita. Tuttavia, puoi interrompere l’ereditarietà dal frammento originale. In tal caso, il contenuto del frammento viene copiato nella progettazione corrente e le modifiche non vengono più sincronizzate.

Per interrompere l’ereditarietà, effettua le seguenti operazioni:

1. Seleziona il frammento.

1. Fai clic sull’icona Sblocca nella barra degli strumenti contestuale.

   ![](assets/fragment-break-inheritance.png)

1. Il frammento diventa un elemento autonomo non più collegato al frammento originale. Modificalo come qualsiasi altro componente del contenuto. [Ulteriori informazioni](content-components.md)
