---
solution: Journey Optimizer
product: journey optimizer
title: Best practice SMS per l’ottimizzazione dei costi
description: Scopri come ottimizzare i costi dei messaggi SMS gestendo i limiti dei caratteri, la codifica e la personalizzazione in Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Intermediate
source-git-commit: 7eaca4faf61431fa438afc7550ff4b89f95fa192
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Best practice per l’ottimizzazione dei costi degli SMS {#sms-cost-optimization}

I messaggi SMS vengono generalmente fatturati dai provider in base a un limite di 160 caratteri per messaggio. L’invio di messaggi SMS può comportare costi aggiuntivi se i messaggi sono suddivisi in più parti.

Segui queste linee guida per ottimizzare la tua strategia di messaggistica e ridurre le spese.

## Mantieni brevi i messaggi {#keep-messages-short}

Journey Optimizer consente fino a 1.500 caratteri nel corpo di un messaggio SMS. Quando superi questo limite, viene visualizzato un avviso e i messaggi che superano tale soglia attivano un errore.

La maggior parte dei provider SMS supporta la codifica GSM a 7 bit, dove un singolo SMS può contenere fino a 160 caratteri. I messaggi che superano questa lunghezza vengono automaticamente suddivisi in più parti SMS (concatenazione):

* **Meno di 160 caratteri**: 1 parte SMS
* **161-306 caratteri**: 2 parti SMS
* **307-459 caratteri**: 3 parti SMS

**Per ridurre al minimo i costi**, cerca di mantenere i messaggi sotto i 160 caratteri in modo che vengano fatturati come una singola parte SMS.

Ad esempio, un messaggio di 1.600 caratteri potrebbe utilizzare 10 crediti SMS, anche se viene visualizzato come un singolo messaggio in Journey Optimizer.

## Evita caratteri speciali che aumentano la lunghezza {#avoid-special-characters}

Alcuni caratteri, come `| ^ € { } [ ] ~ \`, vengono conteggiati come due caratteri nella codifica GSM. L&#39;inclusione di questi caratteri può accelerare il superamento del limite di **160 caratteri** da parte del messaggio.

## Impedisci codifica UCS-2 {#prevent-ucs2-encoding}

Se il messaggio include caratteri non GSM, come testo cinese o arabo, simboli di marchio o ritorni rigidi da strumenti di formattazione avanzati, il messaggio verrà codificato dal provider utilizzando UCS-2, che supporta solo 70 caratteri per SMS.

L’utilizzo della codifica UCS-2 può aumentare il numero di caratteri e, di conseguenza, influire sulla fatturazione dei messaggi con il provider di servizi.

Ad esempio, un messaggio Unicode di 200 caratteri verrà consegnato in 3 parti SMS.

## Best practice di authoring {#authoring-best-practices}

Componi il messaggio SMS finale direttamente in Journey Optimizer o incollalo da applicazioni di testo normale.

Evita l’utilizzo di applicazioni Rich Text, in quanto potrebbero introdurre caratteri nascosti o interruzioni di riga che attivano la codifica UCS-2, aumentando potenzialmente sia il numero di parti SMS che i costi associati.

## Controlla il conteggio dei caratteri prima dell’invio {#check-character-count}

Utilizza le applicazioni di testo normale o il menu **[!UICONTROL Simula contenuto]** di Journey Optimizer per verificare il numero di caratteri.

Mentre Journey Optimizer visualizza un conteggio di caratteri, spazi inclusi, durante la simulazione del contenuto, tieni presente che:

* **not** include caratteri generati tramite personalizzazione dinamica o alcuni caratteri speciali.

* Il conteggio **x/1500** funge da indicatore visivo del limite del payload tecnico, non del limite per messaggio, ad esempio il limite di 160 caratteri GSM a 7 bit.

* Adobe supporta la codifica UTF-8 nell’editor, che differisce dalla codifica GSM-7-bit.

## Informazioni sul reporting {#understanding-reporting}

**Il reporting di Journey Optimizer** conta il messaggio completo come un invio, indipendentemente dalle parti SMS. Questo consente di ridurre la quantità di profili coinvolgibili.

**Generazione rapporti sul provider** mostra le parti SMS effettive per la consegna e deve essere utilizzato per determinare la fatturazione e le interruzioni.

## Considerazioni su Personalization {#personalization-considerations}

La personalizzazione dinamica può aumentare la lunghezza di un messaggio. Ad esempio, la sostituzione di una variabile con un nome lungo può aggiungere caratteri aggiuntivi.

## Risorse aggiuntive {#additional-resources}

Rivedi i caratteri supportati e le regole di codifica nella [Guida al supporto dei caratteri Sinch](https://developers.sinch.com/docs/sms/resources/message-info/character-support/)

