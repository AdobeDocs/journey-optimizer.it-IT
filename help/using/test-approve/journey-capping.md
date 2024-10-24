---
title: Limitazione percorso e arbitrato
description: Scopri come creare regole di limite per i percorsi e come arbitrare l’immissione del percorso
role: User
level: Beginner
badge: label="Disponibilità limitata"
hide: true
hidefromtoc: true
source-git-commit: 0eedadee1e8c1d4642d8602d48bcc9a49a0a2e53
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 3%

---


# Limitazione percorso e arbitrato {#journey-capping}

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione:

* [Guida introduttiva alla gestione dei conflitti e alla definizione delle priorità](gs-conflict-prioritization.md)
* [Rilevare potenziali conflitti in percorsi e campagne](conflicts.md)
* [Assegnare punteggi di priorità a percorsi e campagne](priority-scores.md)
* **[Limitazione Percorsi e arbitrato](journey-capping.md)**

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Gli strumenti per la gestione dei conflitti e la definizione delle priorità sono attualmente disponibili solo come Disponibilità limitata per determinati utenti.

La limitazione dei percorsi consente di limitare il numero di percorsi in cui un profilo può essere iscritto, evitando il sovraccarico di comunicazione. In Journey Optimizer, puoi impostare due tipi di regole per i limiti:

* **Limite di voci** limita il numero di voci di percorso in un determinato periodo per un profilo.
* **Il limite di concorrenza** limita il numero di percorsi in cui un profilo può essere iscritto contemporaneamente.

Entrambi i tipi di limite di percorso sfruttano i punteggi di priorità per arbitrare le voci.

➡️ [Scopri questa funzione nel video](#video)

## Creazione di una regola di limite di percorso {#create-rule}

Per creare una regola di limite di percorso, effettuare le seguenti operazioni:

1. Passa al menu **[!UICONTROL Regole aziendali (Beta)]** per accedere all&#39;inventario dei set di regole.

1. Selezionare il set di regole in cui si desidera aggiungere la regola di limite o creare un nuovo set di regole:

   * Per utilizzare un set di regole esistente, selezionarlo dall&#39;elenco. Le regole di limite di percorso possono essere aggiunte solo ai set di regole con il dominio &quot;percorso&quot;. Puoi controllare queste informazioni negli elenchi dei set di regole, nella colonna **[!UICONTROL Dominio]**.

     ![](assets/journey-capping-list.png)

   * Per creare la regola di limitazione all&#39;interno di un nuovo set di regole, fai clic su **[!UICONTROL Crea set di regole]**, specifica un nome univoco per il set di regole e seleziona &quot;Percorso&quot; dal menu a discesa **[!UICONTROL Dominio set di regole]**, quindi fai clic su **[!UICONTROL Salva]**.

     ![](assets/journey-capping-rule-set.png)

1. Nella schermata del set di regole, fai clic sul pulsante **[!UICONTROL Aggiungi regola]**, quindi configura la regola in base alle tue esigenze:

   ![](assets/journey-capping-concurrency.png)

   * Specifica un nome univoco per la regola.

   * Nell&#39;elenco a discesa **[!UICONTROL Tipo di regola]**, specificare il tipo di limite per la regola.

      * **[!UICONTROL Limite Percorso di ingresso]**: limita il numero di ingressi nel percorso in un determinato periodo per un profilo.
      * **[!UICONTROL Limite di concorrenza Percorso]**: limita il numero di percorsi in cui è possibile iscrivere contemporaneamente un profilo.

   * Espandi le sezioni seguenti per scoprire come configurare ogni tipo di limite:

     +++Configurare una regola di limitazione delle voci di percorso

      1. Nel campo **[!UICONTROL Limitazione]**, imposta il numero massimo di percorsi che un profilo può immettere.
      1. Nel campo **[!UICONTROL Durata]**, definisci il periodo di tempo da considerare. La durata si basa sul fuso orario UTC. Ad esempio, il limite giornaliero verrà reimpostato alla mezzanotte UTC.

     In questo esempio, vogliamo impedire ai profili di immettere più di &quot;5&quot; percorsi in un mese.

     ![](assets/journey-capping-entry-example.png)

     >[!NOTE]
     >
     >Il sistema prenderà in considerazione la priorità dei prossimi percorsi pianificati a cui verrà applicata la stessa regola.
     >
     >In questo esempio, se l’addetto marketing ha già inserito 4 percorsi ed è previsto un altro percorso pianificato questo mese con priorità maggiore, ai clienti verrà impedito di accedere al percorso con priorità inferiore.

+++

     +++Configurare una regola di limitazione della concorrenza di percorso

      1. Nel campo **[!UICONTROL Limitazione]**, imposta il numero massimo di percorsi in cui un profilo può essere iscritto contemporaneamente.

      1. Utilizza il campo **[!UICONTROL Prioritization look ahead]** per determinare le voci di percorso in base ai punteggi di priorità in un periodo scelto (ad esempio, 1 giorno, 7 giorni, 30 giorni). Questo consente di dare priorità all’ingresso in percorsi di valore superiore se un profilo è idoneo a più percorsi.

     In questo esempio, vogliamo impedire ai profili di entrare nel percorso se sono già iscritti a un altro percorso contenente lo stesso set di regole. Se un altro percorso entro i prossimi 7 giorni ha un punteggio di priorità più alto, il profilo non entrerà in questo percorso.

     ![](assets/journey-capping-concurrency-example.png){width="50%" zommable="yes"}

+++

1. Quando la regola di limite è pronta per essere applicata ai percorsi, attivala facendo clic sul pulsante con i puntini di sospensione accanto al nome.

   ![](assets/journey-capping-activate-rule.png)

1. Attiva l’intero set di regole facendo clic sul pulsante con i puntini di sospensione accanto al pulsante Aggiungi regola nell’angolo superiore destro dello schermo.

   ![](assets/journey-capping-activate-rule-set.png)

## Applicare le regole di limitazione ai percorsi {#apply-capping}

Per applicare una regola di limite a un percorso, accedere al percorso e aprirne le proprietà. Nel menu a discesa **[!UICONTROL Regole di limitazione]**, seleziona il set di regole pertinente.

Dopo l’attivazione del percorso, diventano effettive le regole di limitazione definite nel set di regole.

![](../test-approve/assets/journey-capping-apply.png)

>[!IMPORTANT]
>
>Se un percorso viene attivato immediatamente, potrebbero essere necessari fino a 15 minuti per iniziare a eliminare i clienti. È possibile pianificare l&#39;inizio del percorso per almeno 15 minuti per evitare che ciò si verifichi.

## Video introduttivo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435530?quality=12)
