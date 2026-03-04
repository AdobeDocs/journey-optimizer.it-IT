---
solution: Journey Optimizer
product: journey optimizer
title: CC (Carbon Copy) nella configurazione del canale e-mail
description: Configura i destinatari CC visibili nel canale e-mail di Journey Optimizer. Scopri come impostare il campo CC, come si differenzia da CCN e le limitazioni.
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
hide: true
hidefromtoc: true
keywords: CC, copia per conoscenza, e-mail, configurazione del canale, intestazioni e-mail, CCN
badge: label="Disponibilità limitata" type="Informative"
exl-id: 9649cc07-3183-4510-b5d9-b1e33eff43e9
source-git-commit: 780a9259ee081336d1efb3e38c2a8eee4e97b7e3
workflow-type: tm+mt
source-wordcount: '879'
ht-degree: 1%

---

# Aggiungi un campo CC alle e-mail {#cc-email-field}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_cc"
>title="Definisci un indirizzo e-mail CC"
>abstract="Puoi aggiungere un campo CC (copia per conoscenza) visibile alle e-mail inviate con questa configurazione di canale. Inserisci un indirizzo e-mail fisso o utilizza la personalizzazione (attributo di profilo o variabile di contesto). Tieni presente che l’utilizzo di CC viene conteggiato per il volume di messaggi consentito."

>[!AVAILABILITY]
>
>Questa funzione è disponibile per tutti i clienti con disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.

Puoi aggiungere un campo CC (copia per conoscenza) visibile alle e-mail inviate da [!DNL Journey Optimizer] tramite i tuoi percorsi e campagne. Questa funzionalità facoltativa è configurata a livello di [configurazione canale](channel-surfaces.md), insieme ai parametri di intestazione e-mail e all&#39;opzione e-mail Ccn.

>[!CAUTION]
>
>L’utilizzo della funzione CC viene conteggiato rispetto al numero di messaggi per i quali disponi della licenza. Abilitala solo se hai bisogno di destinatari CC visibili. Verifica la disponibilità di volumi con licenza nel contratto.

Come [Ccn](archiving-support.md#bcc-email), il campo Cc ha lo scopo di inviare una copia dell&#39;e-mail a un indirizzo aggiuntivo. Tuttavia, si distingue da Ccn nei seguenti modi:

* L’indirizzo e-mail CC è visibile al destinatario primario, quindi consente a quest’ultimo di vedere chi è stato copiato e a chi rivolgersi per il follow-up.
* A differenza di Ccn, il campo e-mail CC supporta la personalizzazione, che consente di utilizzare una configurazione di canale per molti scenari e di inviare la copia alla persona giusta per destinatario (ad esempio, il relativo gestione delle relazioni). Per le campagne attivate da API, questo consente di effettuare il CC dell’indirizzo relativo a un evento o a una transazione specifica.

>[!NOTE]
>
>Se devi conservare delle copie in cui l&#39;indirizzo non deve essere visibile al destinatario per scopi di archiviazione o conformità, utilizza [BCC](archiving-support.md#bcc-email) invece di CC.

## Abilita e-mail CC {#enable-cc}

Per abilitare l&#39;opzione **[!UICONTROL CC email]**, configura il campo CC nella [configurazione del canale e-mail](../email/email-settings.md).

![](assets/email-config-cc.png)

Puoi specificare qualsiasi indirizzo esterno nel formato corretto, ad eccezione di un indirizzo e-mail definito in un sottodominio delegato ad Adobe. Ad esempio, se hai delegato il sottodominio *marketing.luma.com* ad Adobe, qualsiasi indirizzo come *abc@marketing.luma.com* è vietato.

>[!CAUTION]
>
>Puoi definire un solo indirizzo e-mail. Assicurati che l’indirizzo CC disponga di una capacità di ricezione sufficiente per memorizzare tutte le e-mail inviate utilizzando la configurazione del canale corrente.
>
>Altri consigli sono elencati in [questa sezione](#cc-recommendations-limitations).

Il campo **[!UICONTROL CC email]** accetta tre tipi di valori:

* Un **valore hardcoded**, che può essere un indirizzo e-mail fisso.

* Attributo **profile**, ad esempio l&#39;indirizzo e-mail di gestione delle relazioni disponibile nel profilo.

* Attributo **contestuale** - questo valore può **essere utilizzato solo in campagne attivate da API**. Viene recuperato dal payload API che deve includere la variabile di contesto `context.channel.email.ccvalues` con il valore dell&#39;indirizzo CC.

  >[!WARNING]
  >
  >Quando CC è impostato utilizzando una **variabile di contesto**, è supportato solo in **campagne attivate da API**. Se utilizzi questa configurazione di canale in un percorso o in una campagna di azione, l’e-mail viene inviata solo al destinatario principale; non viene inviata alcuna copia all’indirizzo CC.

Qualsiasi [allegato](../email/pdf-attachments.md) incluso nel messaggio viene inviato sia al destinatario primario che all&#39;indirizzo CC.

Se il valore CC non è valido o è mancante al momento dell’invio (ad esempio, una variabile di contesto vuota), la copia CC viene ignorata; il destinatario primario riceve comunque l’e-mail.

Se sono presenti più valori per il campo CC (ad esempio, quando si utilizza un attributo o un’espressione di profilo che viene risolta in più indirizzi), per l’invio dell’e-mail viene utilizzato solo il primo valore.

## Modifica e-mail CC nelle configurazioni del canale esistenti {#cc-edit}

Se [modifichi una configurazione e-mail](channel-surfaces.md#edit-channel-surface) e aggiungi o modifichi il campo CC, puoi utilizzare solo:

* Un indirizzo e-mail CC **hardcoded** oppure
* Una **variabile di contesto** (per uso attivato da API).

>[!CAUTION]
>
>Quando modifichi una configurazione del canale e-mail esistente, non puoi aggiungere nuovi [attributi di profilo](../personalization/personalization-build-expressions.md#sources) al campo **[!UICONTROL E-mail CC]**. Devi creare una [nuova configurazione di canale](channel-surfaces.md#create-channel-surface).

## Raccomandazioni e limitazioni {#cc-recommendations-limitations}

* **Diritto:** l&#39;utilizzo di CC viene conteggiato per il volume di messaggi consentito. Utilizza CC solo se hai bisogno di destinatari CC visibili. Verifica la disponibilità di volumi con licenza nel contratto.

* **Privacy e conformità:** Per garantire la conformità in materia di privacy, le e-mail CC devono essere elaborate da un sistema in grado di memorizzare informazioni personali (PII) protette, se applicabile. Poiché i messaggi possono contenere dati sensibili o privati, ad esempio dati PII, accertati che l’indirizzo CC sia corretto e che l’accesso ai messaggi sia sicuro.

* **Gestione della casella in entrata:** La casella in entrata utilizzata per CC deve essere gestita correttamente per lo spazio e la consegna. Se la casella in entrata restituisce mancati recapiti, è possibile che alcune e-mail non vengano ricevute.

* **Intervallo di recapito:** è possibile recapitare i messaggi all&#39;indirizzo di posta elettronica CC prima dei destinatari di destinazione. I messaggi CC possono essere inviati anche se i messaggi originali potrebbero contenere [messaggi non recapitati](../reports/suppression-list.md#delivery-failures).

* **Generazione rapporti:** Le aperture, i clic e altri tipi di coinvolgimento dei destinatari CC sono inclusi nelle metriche di generazione rapporti e-mail. Pertanto, eventuali aperture o clic da destinatari CC causeranno errori di calcolo in [report](../reports/report-gs-cja.md).

* **Spam:** Non contrassegnare i messaggi come spam nella casella in entrata CC, in quanto influirà su tutte le altre e-mail inviate a questo indirizzo.

* **Recapito messaggi:** Utilizza CC in linea con le tue pratiche di invio e le aspettative dei destinatari. Un uso eccessivo di CC può influire sul recapito messaggi; segui le [best practice per il recapito messaggi](../reports/deliverability.md) e i termini del contratto.

>[!CAUTION]
>
>Non fare clic sul collegamento per annullare l&#39;abbonamento nelle e-mail inviate all&#39;indirizzo CC, in quanto l&#39;abbonamento del destinatario dell&#39;e-mail **To** verrà immediatamente annullato.
