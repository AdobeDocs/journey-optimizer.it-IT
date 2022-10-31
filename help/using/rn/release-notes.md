---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
description: Note sulla versione di Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 48%

---

# Note sulla versione {#release-notes}

Questa pagina elenca tutte le nuove funzionalità e i miglioramenti introdotti in [!DNL Journey Optimizer]. Per ulteriori modifiche, puoi consultare anche la pagina dedicata agli [ultimi aggiornamenti della documentazione](documentation-updates.md).

[!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Scopri di più su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target=&quot;_blank&quot;}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Iscriviti alla [newsletter trimestrale di Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target=&quot;_blank&quot;} e ricevi gli ultimi aggiornamenti dei prodotti, storie interessanti, casi d’uso, suggerimenti e altro ancora direttamente nella tua casella in entrata ogni trimestre.


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

* La **Forza il rientro sulla ricorrenza** è stata aggiunta un’opzione nei parametri ricorrenti di pianificazione dei segmenti di lettura. Questa opzione ti consente di far uscire automaticamente tutti i profili ancora presenti nel percorso all’esecuzione successiva. Quando l’opzione è disattivata, i profili devono terminare il percorso prima di poter reimmettere in un’altra occorrenza. [Ulteriori informazioni](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Amministrazione**

* È stato aggiunto un messaggio all’interfaccia utente per informare che le configurazioni di sottodominio, sottodominio della pagina di destinazione, record PTR e pool IP sono comuni a tutte le sandbox e quindi qualsiasi modifica a una di queste configurazioni avrà un impatto anche sulle sandbox di produzione.
* I passaggi per caricare l’elenco di soppressione come file CSV dall’interfaccia utente sono stati modificati. [Ulteriori informazioni](../configuration/manage-suppression-list.md#download-suppression-list)

**Campagne**

* Ora puoi archiviare le campagne completate e interrotte. [Ulteriori informazioni](../campaigns/modify-stop-campaign.md#archive)
