---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione ai messaggi mobile
description: Scopri come creare e inviare messaggi mobili in Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: c1027268-0bbe-4e35-a5a6-2aef78083dd3
TQID: https://experienceleague.adobe.com/Ev0xJ86fpweQxgf-VjGUEl4ebk6BdzhVof2BgiMR9EM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: c13ff12d-60f1-49cd-833a-d43359628223
source-git-commit: 75ebd043971ce40e2da0f627622441a46a8e667c
workflow-type: tm+mt
source-wordcount: 1314
ht-degree: 19%

---

# Introduzione ai messaggi mobile {#get-started-sms}

>[!BEGINSHADEBOX]

**In questa pagina:** Introduzione alla messaggistica mobile in Adobe Journey Optimizer per creare, personalizzare e inviare SMS, MMS e messaggi RCS in percorsi e campagne, inclusi il supporto del provider, i requisiti di configurazione e i prerequisiti RCS.

>[!ENDSHADEBOX]

Utilizza [!DNL Journey Optimizer] per inviare messaggi mobili ai clienti attraverso tre canali: **SMS**, **MMS** e **RCS** da un unico editor SMS/MMS/RCS dove puoi creare, personalizzare e visualizzare in anteprima i contenuti.

* **SMS (Short Message Service)**: invia messaggi di solo testo composti da un massimo di 160 caratteri, supportati in tutti i dispositivi mobili.
* **MMS (Multimedia Message Service)**: arricchisci i tuoi messaggi con immagini, video, clip audio e GIF, oltre a un massimo di 1.600 caratteri di testo. [Ulteriori informazioni sulle limitazioni di MMS](../start/guardrails.md#sms-guardrails)
* Contenuti interattivi con marchio **RCS (Rich Communication Services)**:Deliver direttamente nell&#39;app di messaggistica nativa dei clienti, senza la necessità di scaricare ulteriori app.

>[!IMPORTANT]
>
>Se è la prima volta che crei messaggi mobili, assicurati che il canale dei messaggi mobile sia stato configurato. [Ulteriori informazioni](mobile-configuration.md)

I messaggi mobili possono essere creati e inviati in un percorso o in una campagna utilizzando l’azione Messaggio mobile:

* In un **Percorso**: aggiungi un&#39;azione Messaggio mobile al tuo percorso, definisci le impostazioni di base, quindi componi il contenuto nel riquadro Azioni messaggio mobile a destra. [Scopri come creare un percorso](../building-journeys/journey-gs.md)

* In una **campagna**:Create una campagna, seleziona Messaggio mobile come azione, definisci le impostazioni di base, quindi modifica il contenuto del messaggio. Scopri come creare [una campagna di azione](../campaigns/campaign-action.md#action-campaign-action) | [una campagna attivata da API](../campaigns/api-triggered-campaigns.md) | [una campagna orchestrata](../orchestrated/create-orchestrated-campaign.md#create)

## Casi d’uso {#use-cases}

SMS, MMS e RCS funzionano al meglio quando devi raggiungere gli utenti in modo affidabile, indipendentemente dal fatto che abbiano installato la tua app o una connessione Internet disponibile.

| Beneficio | Perché | Casi d’uso di esempio |
| --- | --- | --- |
| Massima portata e immediatezza | Nessuna app o connessione Internet necessaria per ricevere il messaggio | Raggiungere gli utenti senza un’app per smartphone installata |
| Visibilità garantita | Gli SMS hanno tassi di apertura superiori al 90% | Codici OTP, promemoria di appuntamenti, notifiche di consegna |
| Contenuti avanzati tramite MMS/RCS | Aggiunge immagini, video ed elementi interattivi oltre al testo normale | Promozioni con marchio, cataloghi di prodotti |
| Raggiungi gli utenti senza accesso all’app | Funziona per i destinatari che non hanno installato o aperto l’app | Coinvolgere nuovamente gli utenti di app non più in esecuzione, onboarding di clienti non-app |
| CTA ad alta urgenza | Consegnato direttamente a un dispositivo gli utenti controllano frequentemente | Vendite flash, avvisi di frode, avvisi di interruzione del servizio |
| Livellamento con altri canali | Completa i messaggi push, e-mail e in-app per una copertura più ampia | Percorsi multicanale con SMS come canale di fallback |

## Quando non utilizzare {#when-not-to-use}

SMS, MMS e RCS non sono sempre la scelta più efficiente o appropriata. Considera un altro canale nelle seguenti situazioni:

* I costi rappresentano un problema per gli elevati volumi di invio, poiché SMS e MMS vengono fatturati per messaggio e i costi per messaggio si sommano rapidamente e su larga scala
* Il contenuto è lungo o complesso e più adatto alle e-mail, che supportano una formattazione più ricca e testo più lungo
* I destinatari non hanno esplicitamente acconsentito, il che comporta rischi legali e di conformità nella maggior parte delle aree geografiche e delle normative sulla messaggistica

## Funzioni chiave {#key-features}

| Funzione | Descrizione |
|---|---|
| **Personalizzazione** | Personalizza i messaggi con attributi di profilo, contenuto condizionale e dati dinamici utilizzando l’editor di personalizzazione. [Ulteriori informazioni](../personalization/personalize.md) |
| **Supporto provider** | Connetti con [Sinch](mobile-configuration-sinch.md), [Twilio](mobile-configuration-twilio.md), [Infobip](mobile-configuration-infobip.md) o qualsiasi [provider personalizzato](mobile-configuration-custom.md) tramite l&#39;integrazione API. |
| **abbreviazione URL** | Aggiungi URL abbreviati e tracciabili per monitorare il coinvolgimento. Richiede la configurazione del sottodominio. [Ulteriori informazioni](mobile-subdomains.md) |
| **Gestione rinuncia** | Gestione incorporata delle parole chiave di rinuncia standard (STOP, QUIT, CANCEL, ecc.) per Sinch e Infobip. [Ulteriori informazioni](mobile-opt-out.md) |
| **Anteprima e test** | Convalida il contenuto con profili di test e dati di esempio prima dell’invio. [Ulteriori informazioni](send-mobile-message.md) |
| **Generazione rapporti** | Tieni traccia delle prestazioni della campagna e del percorso con [report campagne](../reports/campaign-global-report-cja-sms.md) e [report percorso](../reports/journey-global-report-cja-sms.md) dedicati. |

## Requisiti di configurazione {#configuration-requirements}

Prima di inviare messaggi da dispositivi mobili, devi:

1. **Scegli un provider SMS**: seleziona tra Sinch, Twilio, Infobip o configura un provider personalizzato
2. **Configura credenziali API**: integra i token API e gli ID servizio del provider con Journey Optimizer
3. **Crea configurazioni canale**: configura configurazioni SMS per messaggi di marketing e messaggi transazionali
4. **Configura sottodomini (facoltativo)**: obbligatorio solo se si prevede di utilizzare la riduzione degli URL nei messaggi

Questi passaggi di configurazione vengono in genere eseguiti da un amministratore di sistema. [Introduzione alla configurazione di SMS](mobile-configuration.md)

### Requisiti per RCS {#requirement-rcs}

Per utilizzare RCS in Journey Optimizer sono necessari i seguenti prerequisiti:

* **Credenziali API Sinch RCS**: un amministratore deve configurare le credenziali API per il fornitore di Sinch RCS (ID progetto, ID app e token API). [Ulteriori informazioni](mobile-configuration-sinch.md)
* **Configurazione del canale per messaggi mobili**: un amministratore deve creare una configurazione di canale con una credenziale abilitata per RCS selezionata, in modo che i messaggi vengano recapitati come RCS anziché come SMS. [Ulteriori informazioni](mobile-configuration.md)
* **SMS di fallback**: fortemente consigliato. I destinatari i cui dispositivi non supportano RCS non riceveranno il messaggio a meno che non sia disponibile il fallback SMS. I clienti che non dispongono di un volume di SMS esistente devono acquistare un SMS e un codice breve. [Ulteriori informazioni](design-mobile.md#rcs-content)
* **Fornitore supportato**: l&#39;authoring RCS nativo richiede Sinch RCS (Adobe rivende o direct). Twilio, Infobip e altri provider devono utilizzare un’integrazione provider personalizzata.
* **Supporto dispositivo**: la consegna RCS è supportata sui dispositivi Android e iOS. La disponibilità del vettore e quella regionale variano, RCS non è disponibile a livello globale.

## Risorse aggiuntive {#additional-resources}

Per ulteriori informazioni sulla messaggistica mobile in Journey Optimizer, consulta gli argomenti riportati di seguito. Per ulteriori casi d&#39;uso e best practice, consulta anche la [panoramica di SMS/MMS/RCS](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/mobile-learning-hub/mobile-channels-overview/sms-mms-rcs-overview){target="_blank"} nel Mobile Learning Hub.

+++Guide alla configurazione

Scopri come impostare e configurare l’ambiente SMS:

* [Panoramica sulla configurazione dei canali SMS](mobile-configuration.md)
* [Creare configurazioni dei canali SMS](mobile-configuration-surface.md)
* [Configurare i sottodomini SMS per la riduzione URL](mobile-subdomains.md)

+++

+++Guide alla configurazione del provider

Configurazione dettagliata per ogni fornitore di servizi SMS:

* [Configurare il provider Sinch](mobile-configuration-sinch.md)
* [Configurare il provider Twilio](mobile-configuration-twilio.md)
* [Configurare il provider Infobip](mobile-configuration-infobip.md)
* [Configurare un provider SMS personalizzato](mobile-configuration-custom.md)

+++

+++Creazione di contenuti e gestione

Crea, personalizza e gestisci il contenuto dei messaggi mobili:

* [Creare messaggi SMS/RCS/MMS](create-mobile-message.md)
* [Anteprima, test e invio dei messaggi](send-mobile-message.md)
* [Personalization nei messaggi mobili](../personalization/personalize.md)
* [Contenuto dinamico](../personalization/get-started-dynamic-content.md)
* [Generare contenuti SMS con l’Assistente IA](../content-management/generative-text.md)

+++

+++Conformità e privacy

Assicurati che i messaggi mobili siano conformi alle normative e agli standard sulla privacy:

* [Gestione delle rinunce](mobile-opt-out.md)
* [Privacy e consenso](../privacy/opt-out.md#opt-out-decision-management)

+++

+++Tracciamento delle prestazioni

Monitora e analizza le campagne SMS e le prestazioni del percorso:

* [Rapporti sulla campagna SMS](../reports/campaign-global-report-cja-sms.md)
* [Rapporti sul percorso SMS](../reports/journey-global-report-cja-sms.md)

+++

+++Integrazione di campagna e percorso

Scopri come incorporare gli SMS nei percorsi e nelle campagne del cliente:

* [Aggiungere messaggi SMS ai percorsi](../building-journeys/journey-action.md)
* [Creare campagne SMS](../campaigns/create-campaign.md)

+++

+++Domande frequenti per RCS

**La messaggistica RCS nativa è disponibile con Twilio o Infobip?**

No. La finestra di progettazione RCS nativa in Journey Optimizer non è disponibile quando si utilizzano provider SMS di terze parti come Twilio o Infobip. I messaggi RCS possono tuttavia essere inviati tramite una [integrazione provider personalizzata](mobile-configuration-custom.md).

**Perché acquistare SMS insieme a RCS?**

Per abilitare il fallback SMS, che è il percorso consigliato, è necessario acquistare un volume di SMS e un codice breve. Se SMS non è configurato, i profili il cui dispositivo o gestore non supporta RCS non riceveranno il messaggio.

**La messaggistica RCS nativa è disponibile per i clienti diretti di Sinch?**

Sì. I clienti che utilizzano l’API conversazionale di Sinch hanno accesso all’authoring RCS nativo, inclusi i clienti Adobe di rivendita e Sinch direct.

**RCS è disponibile ovunque?**

No. L&#39;adozione di un vettore continua a crescere a livello globale, ma RCS non è universalmente supportato in tutti i vettori e le aree geografiche. Durante la pianificazione delle campagne RCS è necessario ricercare la disponibilità regionale e il supporto dei vettori.

**Dove vengono visualizzati i messaggi RCS nel dispositivo?**

I messaggi RCS vengono visualizzati nella stessa posizione dei messaggi SMS standard, nell’applicazione di messaggistica nativa del dispositivo. Arrivano da un mittente di marca e verificato, dando ai destinatari i segnali di affidabilità per sapere che il messaggio è legittimo.

**Quali sono i limiti dei caratteri per un messaggio RCS?**

I tipi di messaggi Rich Media (Single) supportano fino a 3.072 caratteri, un numero notevolmente superiore al limite di 160 caratteri per gli SMS standard. I tipi di messaggio RCS di base sono limitati a 160 caratteri, in linea con il limite SMS standard.

+++

## Video dimostrativi {#videos}

**Configurare e inviare messaggi SMS**

Scopri come configurare, creare e includere la messaggistica SMS nei tuoi percorsi cliente.

+++Guarda il video

>[!VIDEO](https://video.tv.adobe.com/v/3420509?learn=on)

+++

**Esplorare le funzionalità di messaggistica per dispositivi mobili**

Scopri le funzionalità complete di messaggistica per dispositivi mobili offerte da Adobe Journey Optimizer agli esperti di marketing.

+++Guarda il video

>[!VIDEO](https://video.tv.adobe.com/v/3426021?quality=12&learn=on)

+++

**Inviare messaggi RCS brandizzati**

Scopri come configurare e inviare messaggi RCS interattivi e in linea con il brand in Adobe Journey Optimizer utilizzando un provider SMS personalizzato.

+++Guarda il video

>[!VIDEO](https://video.tv.adobe.com/v/3464755)

+++
