---
solution: Journey Optimizer
product: journey optimizer
title: Funzioni di accessibilità in Journey Optimizer
description: Ulteriori informazioni sull’accessibilità nell'interfaccia utente di Journey Optimizer
feature: Accessibility
role: User
level: Beginner
exl-id: d971c04c-9b37-4cd7-8a2d-b915e394079b
source-git-commit: 95e50386d4190d0b967d133a327c25ab1681b5c1
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 100%

---

# Accessibilità in Journey Optimizer{#accessibility}

Per accessibilità si intende una serie di funzioni che rendono un prodotto software utilizzabile, con il minor sforzo possibile, per gli utenti con disabilità visive, uditive, cognitive, motorie o di altro tipo. Adobe è leader del settore nell’accessibilità e supporta la creazione di esperienze web eccellenti incoraggiando gli sviluppatori a produrre contenuti avanzati e coinvolgenti accessibili a tutti gli utenti. Per ulteriori informazioni sull’impegno di Adobe per l’accessibilità, visita la [pagina sull‘Accessibilità di Adobe](https://www.adobe.com/accessibility.html){target="_blank"}.

Per raggiungere l’obiettivo di conformità all’accessibilità, [!DNL Journey Optimizer] segue le best practice riconosciute a livello internazionale nelle linee guida per l’accessibilità dei contenuti web (WCAG) 2.1 Livello A e livello AA. Per ulteriori informazioni, consulta l’ultimo [Rapporto sulla conformità all’accessibilità di Adobe Journey Optimizer](https://www.adobe.com/accessibility/compliance/adobe-journey-optimizer.html){target="_blank"}.

>[!NOTE]
>
>Le linee guida per la progettazione di contenuto accessibile per e-mail e pagine di destinazione sono descritte in [questa sezione](../email/accessible-content.md).

Le funzioni di accessibilità in [!DNL Adobe Journey Optimizer] sono ereditate da Adobe Experience Platform:

* Accessibilità da tastiera
* Contrasto colore
* Convalida dei campi obbligatori

Le funzioni di accessibilità di Adobe Experience Platform sono descritte in dettaglio [in questa documentazione](https://experienceleague.adobe.com/docs/experience-platform/accessibility/features.html?lang=it){target="_blank"}.

In [!DNL Journey Optimizer] sono disponibili le scelte rapide da tastiera comuni seguenti:

| Azione | Scelta rapida |
| --- | --- |
| Spostarsi tra elementi, sezioni e gruppi di menu dell’interfaccia utente | Tab |
| Consente di spostarsi all’indietro tra gli elementi, le sezioni e i gruppi di menu dell’interfaccia utente. | Maiusc+Tab |
| Spostati all’interno delle sezioni per impostare lo stato attivo su singoli elementi | Freccia |
| Seleziona o cancella un elemento attivo | Invio o barra spaziatrice |
| Annulla una selezione, comprimi un pannello o chiudi una finestra di dialogo | Esc |

È possibile utilizzare queste scelte rapide in aree specifiche dell‘interfaccia utente di [!DNL Journey Optimizer]:

<table>
  <thead>
    <tr>
      <th>Elemento di interfaccia</th>
      <th>Azione</th>
      <th>Scelta rapida</th>
    </tr>
  </thead>
  <tr>
    <td rowspan="8">Area di lavoro del percorso in stato bozza</td>
    <td>Aggiungi un’attività dalla palette a sinistra nella prima posizione disponibile, dall’alto verso il basso</td>
    <td>Fai doppio clic sull’attività</td>
  </tr>
  <tr>
    <td>Seleziona tutte le attività</td>
    <td>Ctrl + A (Windows)<br/>Comando + A (Mac)</td>
  </tr>
  <tr>
    <td>Elimina le attività selezionate</td>
    <td>Elimina o backspace, quindi premi Invio per confermare l’eliminazione</td>
  </tr>
  <tr>
    <td>Zoom avanti e indietro (quando è attiva l’area di lavoro o uno dei suoi elementi secondari)</td>
    <td>Ctrl +/- (Windows) o Comando +/- (Mac)</td>
  </tr>  
  <tr>
    <td>Passa da un’attività e un percorso all’altro (quando è attiva l‘area di lavoro) o da un pulsante all’altro nella barra degli strumenti (quando è attiva la barra degli strumenti)</td>
    <td>Tasti freccia</td>
  </tr>   
  <tr>
    <td>Rendi attivo l’elemento azionabile successivo sull’area di lavoro; la barra degli strumenti è il primo elemento</td>
    <td>Tab</td>
  </tr>  
  <tr>
    <td>Apri il riquadro di configurazione a destra (quando è attiva un’attività)</td>
    <td>INVIO</td>
  </tr>   
  <tr>
    <td>Sposta un’attività nell’area di lavoro (quando è attiva un’attività)</td>
    <td>Maiusc + tasti freccia</td>
  </tr>  
  <tr>
  <td rowspan="3">
  Riquadro di configurazione dei seguenti elementi:
<ul>
  <li>Attività in un percorso</li>
  <li>Evento</li>
  <li>Origine dati</li>
  <li>Azione</li>
</ul>
  </td>
    <td>Passa al campo successivo da configurare</td>
    <td>Tab</td>
  </tr>
  <tr>
    <td>Salva le modifiche e chiudi il riquadro di configurazione</td>
    <td>Invio</td>
  </tr>
  <tr>
    <td>Ignora le modifiche e chiudi il riquadro di configurazione</td>
    <td>Esc</td>
  </tr>
<!-- //Ajouter ce raccourci quand il marchera (actuellement, le raccourci Ctrl/Cmd+F du navigateur a priorité sur celui de AJO).//
  <tr>
    <td>Page with a search bar</td>
    <td>Select the search bar</td>
    <td>Ctrl/Command + F</td>
  </tr>
-->
  <tr>
    <td>Campo di testo</td>
    <td>Seleziona tutto il testo nel campo selezionato</td>
    <td>Ctrl + A (Windows)<br/>Comando + A (Mac)</td>
  </tr>
  <tr>
    <td rowspan="2">Finestra a comparsa</td>
    <td>Salva le modifiche o conferma l’azione</td>
    <td>Invio</td>
  </tr>
  <tr>
    <td>Chiudi la finestra</td>
    <td>Esc</td>
  </tr>
  <tr>
    <td>Editor di espressioni semplici</td>
    <td>Selezionare e aggiungere un campo</td>
    <td>Fai doppio clic su un campo</td>
  </tr>
  <tr>
    <td>Navigazione nei campi XDM</td>
    <td>Seleziona tutti i campi di un nodo</td>
    <td>Seleziona il nodo principale</td>
  </tr>
  <tr>
    <td>Anteprima payload</td>
    <td>Seleziona il payload</td>
    <td>Ctrl + A (Windows)<br/>Comando + A (Mac)</td>
  </tr>
</table>
