---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# Note sulla versione {#release-notes}

In questa pagina sono elencate tutte le nuove funzioni e i miglioramenti per [!DNL Journey Optimizer]. È inoltre possibile consultare [ultimi aggiornamenti della documentazione](documentation-updates.md) per ulteriori modifiche.

[!DNL Adobe Journey Optimizer] è stato generato in modo nativo su [!DNL Adobe Experience Platform] e eredita dalle ultime innovazioni e miglioramenti. Ulteriori informazioni su queste modifiche in [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti a [Newsletter trimestrale di Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} e ricevere gli ultimi aggiornamenti dei prodotti, storie entusiasmanti, casi d&#39;uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.


## Versione di ottobre 2022 {#oct-2022-release}

<!--

### New capability{#oct-2022-features}

<table>
<thead>
<tr>
<th><strong>Direct Mail Channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add direct mail messages in your campaigns and journeys. Direct mail is an offline channel that allows you to personalize and generate the files required by direct mail providers to send mail to your customers.</p>
<p>When you prepare a direct mail delivery, Journey Optimizer generates a file including all the targeted profiles and the chosen contact information (postal address for example). You will then be able to send this file to your direct mail provider who will take care of the actual sending.</p>
</td>
</tr>
</tbody>
</table>

-->

### Miglioramenti {#oct-2022-improvements}

**Percorsi**

* La **Forza il rientro sulla ricorrenza** è stata aggiunta un’opzione nei parametri ricorrenti di pianificazione dei segmenti di lettura. Questa opzione ti consente di uscire automaticamente da tutti i profili ancora presenti nel percorso all’esecuzione successiva. Quando l’opzione è disattivata, i profili devono terminare il percorso prima di poter reimmettere in un’altra occorrenza. [Ulteriori informazioni](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Amministrazione**

* È stato aggiunto un messaggio all’interfaccia utente per informare che le configurazioni di sottodominio, sottodominio della pagina di destinazione, record PTR e pool IP sono comuni a tutte le sandbox e quindi qualsiasi modifica a una di queste configurazioni avrà un impatto anche sulle sandbox di produzione.
* I passaggi per caricare l’elenco di soppressione come file CSV dall’interfaccia utente sono stati modificati. [Ulteriori informazioni](../configuration/manage-suppression-list.md#download-suppression-list)

**Campagne**

* Ora puoi archiviare le campagne completate e interrotte. [Ulteriori informazioni](../campaigns/modify-stop-campaign.md#archive)
