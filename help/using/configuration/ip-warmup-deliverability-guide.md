---
solution: Journey Optimizer
product: journey optimizer
title: Guida alla consegna del calore IP
description: Scopri le nozioni di base sul recapito messaggi e le best practice per il riscaldamento dell’IP
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, recapito messaggi, reputazione, ISP, coinvolgimento
source-git-commit: 5dd6ebadd7b8c7490cb10496282697ce32ff3693
workflow-type: tm+mt
source-wordcount: '1064'
ht-degree: 5%

---

# Guida alla consegna del calore IP {#ip-warmup-deliverability-guide}

Quando si lanciano campagne e-mail con nuovi indirizzi IP o domini in Adobe Journey Optimizer, è fondamentale comprendere le nozioni di base sul recapito messaggi per creare una solida reputazione del mittente. Questa guida descrive i concetti chiave, i passaggi di preparazione e le best practice per aiutarti a passare da una reputazione pari a zero al posizionamento di successo nella casella in entrata.

➡️ Scopri le nozioni di base sul recapito messaggi, la creazione di reputazione e le best practice per il riscaldamento dell&#39;IP nel video [Post sul blog di Adobe](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950){target="_blank"}.

>[!NOTE]
>
>Per istruzioni dettagliate sull&#39;implementazione di piani di riscaldamento IP in Adobe Journey Optimizer, consultare [Introduzione ai piani di riscaldamento IP](ip-warmup-gs.md).

## Perché la reputazione di IP e domini è importante {#reputation-matters}

I provider di cassette postali (Gmail, Yahoo, Microsoft, Apple Mail e altri) valutano ogni mittente in base a quattro pilastri chiave:

* **Reclami**: i destinatari hanno contrassegnato i messaggi come spam?
* **Coinvolgimento**: i destinatari aprono, fanno clic o rispondono alle e-mail?
* **Infrastruttura**: l&#39;infrastruttura di invio è autenticata, stabile e affidabile?
* **Contenuto**: il contenuto del messaggio è legittimo e utile?

Il riscaldamento IP riguarda principalmente i primi tre pilastri dimostrando gradualmente ai provider di caselle postali che la nuova infrastruttura è legittima e desiderata prima di raggiungere il volume di invio completo.

## Lista di controllo pre-volo {#pre-flight-checklist}

Prima di iniziare a scaldare gli indirizzi IP, assicurati che siano presenti tutti gli elementi fondamentali. La tabella seguente illustra i compiti essenziali da completare prima di avviare il piano di riscaldamento dell’IP.

| Attività | Perché è importante | Come eseguire |
|------|----------------|-------------------|
| Prenotare IP fissi e delegare sottodomini in AJO | Tutti gli elementi che rivestono una reputazione futura riguardano queste infrastrutture. | Passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni e-mail]** > **[!UICONTROL Sottodomini]**. [Ulteriori informazioni](delegate-subdomain.md) |
| Configurare SPF e DKIM | Conferma che il server di invio è legittimo e autorizzato. | Gestito automaticamente da Adobe dopo [delega del sottodominio](delegate-subdomain.md) e [creazione della configurazione del canale](channel-surfaces.md). |
| Verifica che il record DMARC sia configurato (p=none) | Abilita il reporting dell’autenticazione e-mail e i criteri di applicazione futuri. | Verifica che il record DMARC sia impostato per tutti i sottodomini delegati. Quando deleghi un nuovo sottodominio, puoi impostare DMARC direttamente nell’interfaccia. [Ulteriori informazioni](dmarc-record.md) |
| Configurare il monitoraggio dell’elenco seed | Rileva i problemi di posizionamento della casella in entrata nelle prime fasi del processo di riscaldamento. | Aggiungi indirizzi seed durante la creazione della configurazione del canale. [Ulteriori informazioni](seed-lists.md) |
| Crea un pubblico di alto coinvolgimento nella fase 1 | Incrementa le metriche di coinvolgimento anticipato con i destinatari più attivi. | Crea un pubblico di meno di 5.000 contatti che hanno aperto o fatto clic negli ultimi 30 giorni. [Ulteriori informazioni](../audience/creating-a-segment-definition.md) |

>[!CAUTION]
>
>I problemi di autenticazione (SPF, DKIM, DMARC) non possono essere risolti tramite ramping del volume. Assicurati che siano configurate correttamente prima di iniziare l’invio.

## Esempio di calendario di riscaldamento di quattro settimane {#warmup-calendar}

Questo calendario di esempio fornisce un incremento progressivo del volume in base alla percentuale del volume giornaliero finale (UDV). Adatta questi numeri in base alle tue esigenze di invio specifiche e collabora con il tuo consulente di recapito messaggi per creare un piano personalizzato.

| Days | % di UDV | Pubblico target | Consigli sui contenuti |
|------|----------|-----------------|------------------------|
| 1-3 | 0,5% | I destinatari più coinvolti | Utilizza un formato breve e in testo normale con un call-to-action chiaro sopra la piega. |
| 4-7 | 1% | Utenti coinvolti e acquirenti recenti | Aggiungi un’immagine protagonista leggera, limita i collegamenti a un massimo di 3. |
| 8-14 | 5% | Elenco di sottoscrittori attivi più ampio | Presenta il modello di e-mail standard, ma evita pesanti contenuti promozionali. |
| 15-21 | 25% | Abbonati attivi e leggermente inattivi | Utilizza i normali contenuti di marketing monitorando attentamente le percentuali di reclami. |
| 22-28 | 50-100% | Elenco completo (nel rispetto degli elenchi di soppressione) | Transizione alla cadenza di invio allo stato stazionario. |

## Utilizzo della funzione Piani di riscaldamento IP {#ajo-warmup-feature}

Adobe Journey Optimizer include una funzionalità semplificata di [piani di riscaldamento IP](ip-warmup-gs.md) che elimina la necessità di limitare manualmente il volume attraverso complesse impostazioni di percorso. Questa funzionalità garantisce un approccio standardizzato per la creazione della reputazione del mittente.

### Come funziona

1. **Crea campagne di riscaldamento IP**: crea una o più campagne con l&#39;opzione **[!UICONTROL Attivazione piano di riscaldamento IP]** abilitata. [Ulteriori informazioni](ip-warmup-campaign.md)

1. **Configura il piano**: accedi a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni e-mail]** > **[!UICONTROL Piani di riscaldamento IP]** e carica il modello di riscaldamento graduale preparato con il tuo consulente del recapito messaggi. [Ulteriori informazioni](ip-warmup-plan.md)

1. **Esegui fasi**: seleziona una campagna per ogni fase e attiva le esecuzioni corrispondenti. Il sistema esclude automaticamente i profili dalle esecuzioni precedenti per evitare il contatto eccessivo. [Ulteriori informazioni](ip-warmup-execution.md)

1. **Monitora e regola**: utilizza il dashboard di reporting consolidato per monitorare lo stato di avanzamento, monitorare lo stato di esecuzione e modificare il piano in caso di problemi. [Ulteriori informazioni](ip-warmup-execution.md#monitor-plan)

## Monitoraggio in tempo reale e metriche chiave {#monitoring}

Adobe Journey Optimizer fornisce funzionalità di reporting integrate per monitorare le prestazioni di riscaldamento dell’IP:

* **Rapporti live**: accedi alla misurazione e alla visualizzazione in tempo reale delle campagne dalla scheda **[!UICONTROL Ultime 24 ore]**. [Ulteriori informazioni](../reports/campaign-live-report.md#email-live)

* **Rapporti cronologici**: per informazioni più approfondite, utilizza Customer Journey Analytics per analizzare i dati da Adobe Experience Platform e creare visualizzazioni personalizzate. [Ulteriori informazioni](../reports/report-gs-cja.md)

### Metriche di Target

Monitora questi indicatori di prestazioni chiave durante il riscaldamento:

| Metrica | Soglia target | Azione correttiva |
|--------|-----------------|-------------------|
| Percentuale reclami | ≤ 0,1% | Se viene superato, controlla i segmenti ed elimina i reclamanti cronici. |
| Percentuale mancati recapiti permanenti | ≤ 2% | Se viene superato, rivedi l’elenco delle pratiche di qualità e igiene. |
| Tasso di apertura | ≥ 10% | Se il valore è troppo basso, verifica che il targeting dei tipi di pubblico interessati sia corretto. |

## Risoluzione dei problemi del playbook {#troubleshooting}

Utilizza questa matrice di decisione per risolvere i problemi comuni durante il riscaldamento:

| Sintomo | Probabile causa | Azione consigliata |
|---------|--------------|-------------------|
| Errori temporanei di Yahoo (421 errori) | Volume aumentato troppo rapidamente | Sospendi l’invio per 24 ore, quindi riavvia al livello precedente. |
| Tasso di apertura inferiore al 2% tra i conti seed | INSERIRE NELL&#39;ELENCO BLOCCATI IP | Controlla [Strumenti Google Postmaster](https://postmaster.google.com/) e [Microsoft SNDS](https://sendersupport.olc.protection.outlook.com/snds/); se necessario, apri un ticket di recapito messaggi. |
| Il tasso di reclami supera lo 0,3% | Pubblico non mirato o non aggiornato | Controlla le definizioni dei segmenti ed escludi i denuncianti cronici dal tuo [elenco di soppressione](manage-suppression-list.md). |

>[!IMPORTANT]
>
>È meglio rallentare il riscaldamento che tentare di riparare la reputazione di un mittente danneggiato più tardi. Dare sempre priorità al mantenimento di metriche sane rispetto alla rampa di volume aggressiva.

## Best practice post-riscaldamento {#post-warmup}

Una volta completato il piano di riscaldamento e le metriche si sono stabilizzate:

* **Mantenere la coerenza**: gli aumenti di volume giornalieri non superano il 30% su base settimanale per preservare la reputazione consolidata.

* **Monitoraggio continuo**: pianifica controlli di integrità trimestrali della reputazione per identificare e risolvere i problemi in modo proattivo.

* **Rispetta i segnali di coinvolgimento**: continua a dare la priorità ai destinatari coinvolti e implementa campagne di ricoinvolgimento per gli abbonati inattivi.

* **Mantieni autenticazione corrente**: verifica regolarmente che i record SPF, DKIM e DMARC rimangano configurati correttamente.

## Punti chiave da eliminare {#key-takeaways}

* **Il riscaldamento dell&#39;IP è essenziale**: saltare il processo di riscaldamento costa più tempo e reputazione rispetto allo sforzo necessario per farlo correttamente.

* **Decisioni basate sui dati**: tieni traccia delle percentuali di reclamo, mancato recapito e coinvolgimento ogni giorno e regola la tua strategia prima che gli ISP ti penalizzino.

* **Prima l&#39;autenticazione, poi il volume**: risolvere tutti i problemi relativi a SPF, DKIM e DMARC prima di iniziare a incrementare il volume.

* **La coerenza è importante**: i provider di cassette postali sono a favore di modelli di invio prevedibili ed evitano picchi di volume improvvisi o pianificazioni di invio irregolari.

<!--
>[!NOTE]
>
>For more guidance, explore the [Adobe Journey Optimizer Deliverability Guide blog post](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950).-->

## Argomenti correlati {#related-topics}

* [Introduzione ai piani di preparazione IP](ip-warmup-gs.md)
* [Creare campagne di preparazione IP](ip-warmup-campaign.md)
* [Creare un piano di preparazione IP](ip-warmup-plan.md)
* [Eseguire il piano di preparazione IP](ip-warmup-execution.md)
* [Impostare le configurazioni dei canali](channel-surfaces.md)
* [Delega sottodomini](delegate-subdomain.md)
* [Gestire elenco di soppressione](manage-suppression-list.md)
* [Guida alle procedure consigliate per la consegna](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=it)

