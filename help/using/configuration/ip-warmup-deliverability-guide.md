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
source-git-commit: 07896931a7c06e1b712f3b65e1dcf939b521ba83
workflow-type: tm+mt
source-wordcount: '1088'
ht-degree: 6%

---

# Guida alla consegna del calore IP {#ip-warmup-deliverability-guide}

Quando si lanciano campagne e-mail con nuovi indirizzi IP o domini in Adobe Journey Optimizer, è fondamentale comprendere le nozioni di base sul recapito messaggi per creare una solida reputazione del mittente. Questa guida descrive i concetti chiave, i passaggi di preparazione e le best practice per aiutarti a passare da una reputazione pari a zero al posizionamento di successo nella casella in entrata.

➡️ [Guarda questo video per scoprire le nozioni di base sul recapito messaggi di riscaldamento IP](#video)

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
| Prenotare IP fissi e delegare sottodomini in AJO | Tutti gli elementi dell&#39;infrastruttura che avranno una reputazione futura sono legati a questi | Passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni e-mail]** > **[!UICONTROL Sottodomini]**. [Ulteriori informazioni](delegate-subdomain.md) |
| Configurare SPF e DKIM | Conferma che il server di invio è legittimo e autorizzato | Gestito automaticamente da Adobe dopo la delega del sottodominio e la creazione della configurazione del canale. [Ulteriori informazioni](delegate-subdomain.md) |
| Impostare il record DMARC | Abilita la generazione di rapporti di autenticazione e-mail e i criteri di applicazione futuri | Gestito automaticamente da Adobe dopo la delega del sottodominio e la creazione della configurazione del canale. [Ulteriori informazioni](dmarc-record.md) |
| Configurare il monitoraggio dell’elenco seed | Rileva i problemi di posizionamento della casella in entrata nelle prime fasi del processo di riscaldamento | Aggiungi indirizzi seed durante la creazione della configurazione del canale. [Ulteriori informazioni](seed-lists.md) |
| Crea un pubblico di alto coinvolgimento nella fase 1 | Aumenta le metriche di coinvolgimento anticipato con i destinatari più attivi | Crea un pubblico di meno di 5.000 contatti che hanno aperto o fatto clic negli ultimi 30 giorni |

>[!CAUTION]
>
>I problemi di autenticazione (SPF, DKIM, DMARC) non possono essere risolti tramite ramping del volume. Assicurati che siano configurate correttamente prima di iniziare l’invio.

## Esempio di calendario di riscaldamento di quattro settimane {#warmup-calendar}

Questo calendario di esempio fornisce un incremento progressivo del volume in base alla percentuale del volume giornaliero finale (UDV). Adatta questi numeri in base alle tue esigenze di invio specifiche e collabora con il tuo consulente di recapito messaggi per creare un piano personalizzato.

| Days | % di UDV | Pubblico target | Consigli sui contenuti |
|------|----------|-----------------|------------------------|
| 1-3 | 0,5% | I destinatari più coinvolti | Utilizza un formato breve in testo normale con un call-to-action chiaro sopra la piega |
| 4-7 | 1% | Utenti coinvolti e acquirenti recenti | Aggiungi un&#39;immagine protagonista leggera, limita i collegamenti a un massimo di 3 |
| 8-14 | 5% | Elenco di sottoscrittori attivi più ampio | Presenta il tuo modello di e-mail standard, ma evita di usare contenuti promozionali pesanti |
| 15-21 | 25% | Abbonati attivi e leggermente inattivi | Utilizza i normali contenuti di marketing monitorando attentamente le percentuali di reclami |
| 22-28 | 50-100% | Elenco completo (nel rispetto degli elenchi di soppressione) | Transizione alla cadenza di invio in stato stazionario |

>[!NOTE]
>
>Adobe Journey Optimizer fornisce una [funzionalità dedicata per i piani di riscaldamento IP](ip-warmup-gs.md) che automatizza la gestione dei volumi e semplifica il processo di riscaldamento senza richiedere configurazioni di percorso complesse.

## Utilizzo della funzione Piani di riscaldamento IP di AJO {#ajo-warmup-feature}

Adobe Journey Optimizer include una funzione di pianificazione dell&#39;IP ottimizzata che elimina la necessità di limitare manualmente il volume attraverso configurazioni di percorso complesse. Questa funzionalità garantisce un approccio standardizzato per la creazione della reputazione del mittente.

### Come funziona

1. **Crea campagne di riscaldamento IP**: crea una o più campagne con l&#39;opzione **[!UICONTROL Attivazione piano di riscaldamento IP]** abilitata. [Ulteriori informazioni](ip-warmup-campaign.md)

1. **Configura il piano**: accedi a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni e-mail]** > **[!UICONTROL Piani di riscaldamento IP]** e carica il modello di riscaldamento graduale preparato con il tuo consulente del recapito messaggi. [Ulteriori informazioni](ip-warmup-plan.md)

1. **Esegui fasi**: seleziona una campagna per ogni fase e attiva le esecuzioni corrispondenti. Il sistema esclude automaticamente i profili dalle esecuzioni precedenti per evitare il contatto eccessivo. [Ulteriori informazioni](ip-warmup-execution.md)

1. **Monitora e regola**: utilizza il dashboard di reporting consolidato per monitorare lo stato di avanzamento, monitorare lo stato di esecuzione e modificare il piano in caso di problemi. [Ulteriori informazioni](ip-warmup-execution.md#monitor-plan)

## Monitoraggio in tempo reale e metriche chiave {#monitoring}

Adobe Journey Optimizer fornisce funzionalità di reporting integrate per monitorare le prestazioni di riscaldamento dell’IP:

* **Rapporti live**: accedi alla misurazione e alla visualizzazione in tempo reale delle campagne dalla scheda **[!UICONTROL Ultime 24 ore]**. [Ulteriori informazioni](../reports/live-report.md)

* **Integrazione di Customer Journey Analytics**: per informazioni più approfondite, utilizza Customer Journey Analytics per analizzare i dati da Adobe Experience Platform e creare visualizzazioni personalizzate. [Ulteriori informazioni](../reports/report-gs-cja.md)

### Metriche di Target

Monitora questi indicatori di prestazioni chiave durante il riscaldamento:

| Metrica | Soglia target | Azione se superato |
|--------|-----------------|-------------------|
| Percentuale reclami | ≤ 0,1% | Controlla il segmento ed elimina i denuncianti cronici |
| Percentuale mancati recapiti permanenti | ≤ 2% | Verifica la qualità dell’elenco e le pratiche di igiene |
| Tasso di apertura | ≥ 10% | Verifica che il targeting dei tipi di pubblico interessati |

>[!TIP]
>
>Per un&#39;analisi completa delle campagne, utilizza le funzionalità [report live della campagna](../reports/campaign-live-report.md#email-live) e [report Customer Journey Analytics](../reports/campaign-global-report-cja-email.md).

## Risoluzione dei problemi del playbook {#troubleshooting}

Utilizza questa matrice di decisione per risolvere i problemi comuni durante il riscaldamento:

| Sintomo | Probabile causa | Azione consigliata |
|---------|--------------|-------------------|
| Errori temporanei di Yahoo (421 errori) | Volume aumentato troppo rapidamente | Sospendi l’invio per 24 ore, quindi riavvia al livello precedente |
| Tasso di apertura inferiore al 2% tra i conti seed | INSERIRE NELL&#39;ELENCO BLOCCATI IP | Controlla [Strumenti Google Postmaster](https://postmaster.google.com/) e [Microsoft SNDS](https://sendersupport.olc.protection.outlook.com/snds/); se necessario, apri un ticket di recapito messaggi |
| Il tasso di reclami supera lo 0,3% | Pubblico non mirato o non aggiornato | Controlla le definizioni dei segmenti ed escludi i denuncianti cronici dal tuo [elenco di soppressione](manage-suppression-list.md) |

>[!IMPORTANT]
>
>È meglio rallentare il riscaldamento che tentare di riparare la reputazione di un mittente danneggiato più tardi. Dare sempre priorità al mantenimento di metriche sane rispetto alla rampa di volume aggressiva.

## Best practice post-riscaldamento {#post-warmup}

Una volta completato il piano di riscaldamento e le metriche si sono stabilizzate:

* **Mantenere la coerenza**: gli aumenti dei volumi giornalieri devono essere inferiori al 30% su base settimanale per preservare la reputazione consolidata

* **Monitoraggio continuo**: pianifica controlli trimestrali di integrità della reputazione per identificare e risolvere proattivamente i problemi

* **Rispetta i segnali di coinvolgimento**: continua a dare priorità ai destinatari coinvolti e implementa campagne di ricoinvolgimento per gli abbonati inattivi

* **Mantieni autenticazione corrente**: verifica regolarmente che i record SPF, DKIM e DMARC rimangano configurati correttamente

## Punti chiave da eliminare {#key-takeaways}

* **Il riscaldamento dell&#39;IP è essenziale**: saltare il processo di riscaldamento costa più tempo e reputazione rispetto allo sforzo necessario per farlo correttamente

* **Decisioni basate sui dati**: tieni traccia delle percentuali di reclami, mancati recapiti e coinvolgimento ogni giorno e regola la tua strategia prima che gli ISP ti penalizzino

* **Prima l&#39;autenticazione, poi il volume**: risolvere tutti i problemi relativi a SPF, DKIM e DMARC prima di iniziare a incrementare il volume

* **Importanza della coerenza**: i provider di cassette postali preferiscono modelli di invio prevedibili; evitare picchi di volume improvvisi o pianificazioni di invio irregolari

## Video dimostrativo {#video}

Scopri le nozioni di base sul recapito messaggi, la creazione di reputazione e le best practice per il riscaldamento dell’IP in Adobe Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/3463790/?captions=ita&learn=on)

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

