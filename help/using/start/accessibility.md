---
solution: Journey Optimizer
product: journey optimizer
title: Funzioni di accessibilità in Journey Optimizer
description: Ulteriori informazioni sull’accessibilità nell’interfaccia utente di Journey Optimizer
feature: Overview
role: User
level: Beginner
source-git-commit: 78675ca22d8ee9a93d9af128d5708c305523da78
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 54%

---

# Accessibilità in Journey Optimizer{#accessibility}

Per accessibilità si intende una serie di funzioni che rendono un prodotto software utilizzabile, con il minor sforzo possibile, per gli utenti con disabilità visive, uditive, cognitive, motorie o di altro tipo. Adobe è leader di settore nell’accessibilità e supporta la creazione di esperienze web eccezionali incoraggiando gli sviluppatori a produrre contenuti avanzati e coinvolgenti accessibili a tutti gli utenti. Ulteriori informazioni sull’impegno di Adobe per l’accessibilità nel [Pagina Accessibilità di Adobe](https://www.adobe.com/accessibility.html){target="_blank"}.

Per raggiungere l’obiettivo di conformità all’accessibilità, [!DNL Journey Optimizer] segue le best practice riconosciute a livello internazionale nelle linee guida per l’accessibilità dei contenuti web (WCAG) 2.1 Livello A e livello AA. Per saperne di più [Rapporto sulla conformità per l’accessibilità di Adobe Journey Optimizer](https://www.adobe.com/accessibility/compliance/adobe-journey-optimizer-2022.html){target="_blank"}.


Le funzioni di accessibilità in [!DNL Adobe Journey Optimizer] sono ereditate da Adobe Experience Platform:

* Accessibilità da tastiera
* Contrasto colore
* Convalida dei campi obbligatori

Le funzioni di accessibilità di Adobe Experience Platform sono descritte in dettaglio [in questa documentazione](https://experienceleague.adobe.com/docs/experience-platform/accessibility/features.html?lang=it){target="_blank"}.

Sono disponibili le seguenti scelte rapide da tastiera comuni in [!DNL Journey Optimizer]:

| Azione | Tasti di scelta rapida |
| --- | --- |
| Spostarsi tra elementi, sezioni e gruppi di menu dell’interfaccia utente | Scheda |
| Consente di spostarsi all’indietro tra gli elementi, le sezioni e i gruppi di menu dell’interfaccia utente. | Maiusc+Tab |
| Spostati all’interno delle sezioni per impostare lo stato attivo su singoli elementi | Freccia |
| Seleziona o cancella un elemento attivo | Invio o barra spaziatrice |
| Annulla una selezione, comprimi un pannello o chiudi una finestra di dialogo | Esc |

Puoi utilizzare queste scelte rapide in aree specifiche di [!DNL Journey Optimizer] interfaccia utente:

<table>
  <thead>
    <tr>
      <th>Elemento di interfaccia</th>
      <th>Azione</th>
      <th>Tasti di scelta rapida</th>
    </tr>
  </thead>
  <tr>
    <td>Elenco percorsi, azioni, origini dati o eventi</td>
    <td>Creare un percorso, un’azione, un’origine dati o un evento</td>
    <td>C</td>
  </tr>
  <tr>
    <td rowspan="3">Area di lavoro del percorso in stato bozza</td>
    <td>Aggiungi un’attività dalla palette a sinistra nella prima posizione disponibile, dall’alto verso il basso</td>
    <td>Fai doppio clic sull’attività</td>
  </tr>
  <tr>
    <td>Seleziona tutte le attività</td>
    <td>CTRL + A (Windows)<br/>CMD + A (Mac)</td>
  </tr>
  <tr>
    <td>Elimina le attività selezionate</td>
    <td>Elimina o backspace, quindi premi Invio per confermare l’eliminazione</td>
  </tr>
  <tr>
    <td>Zoom avanti e indietro (messa a fuoco su tela o su uno dei suoi elementi figlio)</td>
    <td>CTRL +/- (Windows) o CMD +/- (Mac)</td>
  </tr>  
  <tr>
    <td>Navigare tra ogni attività e percorso (area di lavoro) o tra i pulsanti della barra degli strumenti (area di lavoro dedicata alla barra degli strumenti)</td>
    <td>Tasti freccia</td>
  </tr>   
  <tr>
    <td>Sposta lo stato attivo sull’elemento actionable successivo nell’area di lavoro, poiché la barra degli strumenti è la prima</td>
    <td>Scheda</td>
  </tr>  
  <tr>
    <td>Apri il riquadro di configurazione a destra (attivazione su un’attività)</td>
    <td>INVIO</td>
  </tr>   
  <tr>
    <td>Sposta un’attività nell’area di lavoro (attiva un’attività)</td>
    <td>Tasti MAIUSC + freccia</td>
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
    <td>Scheda</td>
  </tr>
  <tr>
    <td>Salva le modifiche e chiudi il riquadro di configurazione</td>
    <td>Invio</td>
  </tr>
  <tr>
    <td>Ignora le modifiche e chiudi il riquadro di configurazione</td>
    <td>Esc</td>
  </tr>
  <tr>
    <td rowspan="4">Percorso in modalità di test</td>
    <td>Attivare o disattivare la modalità di test</td>
    <td>T</td>
  </tr>
  <tr>
    <td>Attivare un evento in un percorso basato su eventi</td>
    <td>E</td>
  </tr>
  <tr>
    <td>

Attiva un evento in un percorso basato su segmenti per il quale è attivata l’opzione **[!UICONTROL Singolo profilo alla volta]**

</td>
    <td>P</td>
  </tr>
  <tr>
    <td>Visualizzare i registri di test</td>
    <td>L</td>
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
