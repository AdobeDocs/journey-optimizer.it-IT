---
solution: Journey Optimizer
product: journey optimizer
title: Inviare dati ad AEP
description: Scopri come inviare dati ad AEP
feature: Journeys, Use Cases
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: percorso, caso d’uso
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 711
ht-degree: 3%

---

# Caso d&#39;uso: creare un&#39;azione personalizzata per inviare dati a [!DNL Adobe Experience Platform]{#send-data-to-aep}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come creare un percorso che aumenti gradualmente il volume delle e-mail utilizzando un&#39;attività Ottimizza con una condizione di limite del profilo per riscaldare l&#39;IP e proteggere la reputazione del mittente.

>[!ENDSHADEBOX]

Se di recente sei passato a un altro provider di servizi e-mail, indirizzo IP o dominio o sottodominio e-mail, stabilisci la tua reputazione di mittente. In caso contrario, le consegne potrebbero essere bloccate o spostate nelle cartelle di posta indesiderata dei destinatari. Per maggiori informazioni, consulta la [Guida alle best practice per il recapito messaggi](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=it){target="_blank"}.

Per riscaldare l’IP, puoi aumentare gradualmente il numero di consegne. Ulteriori informazioni sull&#39;ottimizzazione del recapito messaggi in Journey Optimizer](../reports/deliverability.md).[

Lo scopo di questo caso d’uso è la creazione di un percorso per incrementare le consegne di e-mail. Per configurare il percorso, eseguire la procedura seguente:

1. Creazione di un percorso. [Ulteriori informazioni](journey-gs.md).

1. Aggiungi un&#39;attività **[!UICONTROL Ottimizza]** al percorso. [Ulteriori informazioni](optimize.md).

1. Nelle impostazioni dell&#39;attività **[!UICONTROL Condition]**, imposta il numero massimo di destinatari per la consegna:

   1. Nelle impostazioni dell&#39;attività **[!UICONTROL Ottimizza]**, selezionare il metodo **[!UICONTROL Condizioni]** e impostare il campo **[!UICONTROL Tipo]** su **[!UICONTROL Limite del profilo]**. [Ulteriori informazioni](conditions.md#profile_cap).

   1. Imposta il campo **[!UICONTROL Limite]** sul numero massimo di destinatari per questa consegna.

   ![Condizione limite profilo per controllare il volume di esecuzione azioni personalizzato](assets/profile-cap-condition.png)

   Puoi aumentare gradualmente questo limite fino al numero totale dei tuoi abbonati.

1. Aggiungi un&#39;attività di azione **[!UICONTROL Email]** al percorso nominale dopo l&#39;attività **[!UICONTROL Condition]**.

   ![Percorso con azione personalizzata per l&#39;invio di dati al sistema esterno](assets/ramp-up-deliveries-message.png)

   Quando il percorso è in esecuzione, il messaggio viene inviato ai profili in entrata, fino al numero massimo di profili specificato. Quando questo limite viene raggiunto, i profili in ingresso seguono il percorso alternativo.

1. Completa il percorso con le attività che preferisci.

Dopo il riscaldamento dell’IP, puoi rimuovere questa condizione.

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** Questa pagina illustra un caso d&#39;uso di riscaldamento IP basato sul percorso che aumenta gradualmente il volume di consegna delle e-mail utilizzando una condizione di limite del profilo per proteggere la reputazione del mittente.

**Intenti:**

* Creare un percorso di riscaldamento IP per aumentare gradualmente il volume di invio delle e-mail
* Configurare una condizione di limite del profilo per limitare il numero di destinatari per consegna
* Aggiungere un’attività di azione E-mail al percorso di percorso nominale
* Rimuovi la condizione del limite del profilo una volta completato il riscaldamento dell’IP

**Glossario:**

* **Riscaldamento IP**: il processo di aumento graduale del volume di invio delle e-mail da un nuovo indirizzo IP per stabilire la reputazione del mittente *(specifico per prodotto)*
* **Limite di profili**: tipo di condizione in Journey Optimizer che limita il numero massimo di profili che possono accettare un percorso di percorso specifico *(specifico per prodotto)*
* **Percorso nominale**: il ramo principale di un percorso seguito dai profili quando vengono soddisfatte le condizioni *(specifico per prodotto)*

**Guardrail:**

* È necessario impostare una condizione Limite profilo nell’attività Condizione per controllare il volume di consegna durante il riscaldamento dell’IP.
* I profili che superano il limite massimo vengono instradati al percorso alternativo.
* Per rimuovere la condizione di chiusura, è necessario ricreare o modificare il percorso al termine del riscaldamento dell’IP.

**Terminologia:**

* Nome canonico: riscaldamento IP — Acronimo: n/d — varianti: riscaldamento IP, riscaldamento reputazione mittente
* Sinonimi: &quot;Limite del profilo&quot; = &quot;condizione del limite del destinatario&quot;
* Non confondere: &quot;riscaldamento IP&quot; ≠ &quot;autenticazione e-mail&quot; (la configurazione di SPF/DKIM/DMARC è separata)

**Domande frequenti:**

* **Q: perché devo riscaldare il mio IP?** — I nuovi indirizzi IP non dispongono di cronologia di invio, pertanto i provider di cassette postali possono bloccare o inviare messaggi di posta indesiderata fino a quando non viene stabilita la reputazione.
* **D: cosa succederà ai profili che superano il limite del profilo?** — Seguono il percorso alternativo definito nell&#39;attività Condizione.
* **D: Come si aumenta il limite nel tempo?** — Modificare il campo Limite nelle impostazioni dell&#39;attività Condizione e aumentarlo gradualmente fino al numero totale di abbonati.
* **Q: quando posso rimuovere la condizione del limite del profilo?** — Una volta che l’IP dispone di una cronologia di invio sufficiente e le metriche di recapito messaggi sono stabili, puoi rimuovere la condizione dal percorso.

+++
