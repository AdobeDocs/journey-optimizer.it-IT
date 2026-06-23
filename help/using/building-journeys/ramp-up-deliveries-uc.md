---
solution: Journey Optimizer
product: journey optimizer
title: Aumentare le consegne
description: Scopri come incrementare gradualmente le consegne
feature: Journeys, Use Cases, IP Warmup Plans
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
hide: true
keywords: recapito messaggi, percorso, caso d’uso, e-mail, reputazione
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/en0jMw69ddHSQrIH05-9FfGuDwNKb36f5Lp3fLp2oAk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2:
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 807
ht-degree: 2%

---

# Caso d’uso: aumentare gradualmente le consegne{#use-case-ramp-up-your-deliveries}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come creare un percorso che incrementa gradualmente le consegne di e-mail utilizzando l&#39;attività Ottimizza e un limite di profili, per riscaldare un nuovo indirizzo IP e stabilire la reputazione del mittente.

>[!ENDSHADEBOX]

Se recentemente sei passato a un altro provider di servizi e-mail, indirizzo IP o dominio o sottodominio e-mail, devi stabilire la tua reputazione di mittente. In caso contrario, le consegne potrebbero essere bloccate o spostate nella cartella di posta indesiderata della cassetta postale dei destinatari. Scopri come aumentare la reputazione delle e-mail con la preparazione degli indirizzi IP nella [Guida alle best practice per il recapito messaggi](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=it){target="_blank"}.

Per riscaldare l’IP, puoi aumentare gradualmente il numero di consegne. Ulteriori informazioni sull&#39;ottimizzazione del recapito messaggi in Journey Optimizer[&#128279;](../reports/deliverability.md).

Lo scopo di questo caso d’uso è la creazione di un percorso per incrementare le consegne di e-mail. Per configurare il percorso, eseguire la procedura seguente:

1. Creazione di un percorso. [Ulteriori informazioni](journey-gs.md).

1. Aggiungi un&#39;attività **[!UICONTROL Ottimizza]** al percorso. [Ulteriori informazioni](optimize.md).

1. Nelle impostazioni dell&#39;attività **[!UICONTROL Condition]**, imposta il numero massimo di destinatari per la consegna:

   1. Nelle impostazioni dell&#39;attività **[!UICONTROL Ottimizza]**, selezionare il metodo **[!UICONTROL Condizioni]** e impostare il campo **[!UICONTROL Tipo]** su **[!UICONTROL Limite del profilo]**. [Ulteriori informazioni](conditions.md#profile_cap).

   1. Imposta il campo **[!UICONTROL Limite]** sul numero massimo di destinatari per questa consegna.

   ![Configurazione della condizione del limite del profilo per il controllo del volume di consegna](assets/profile-cap-condition.png)

   Puoi aumentare gradualmente questo limite fino al numero totale dei tuoi abbonati.

1. Aggiungi un&#39;attività di azione **[!UICONTROL Email]** al percorso nominale dopo l&#39;attività **[!UICONTROL Condition]**.

   ![Configurazione dei messaggi e-mail nel percorso di consegna con rampe di transizione](assets/ramp-up-deliveries-message.png)

   Quando il percorso è in esecuzione, il messaggio viene inviato ai profili in entrata, fino al numero massimo di profili specificato. Quando questo limite viene raggiunto, i profili in ingresso seguono il percorso alternativo.

1. Completa il percorso con le attività che preferisci.

Dopo il riscaldamento dell’IP, puoi rimuovere questa condizione.

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

- **TL;DR:** Questo caso d&#39;uso descrive come creare un percorso Adobe Journey Optimizer che incrementa gradualmente il volume di consegna delle e-mail utilizzando una condizione di limite del profilo per proteggere la reputazione del mittente durante la preparazione dell&#39;IP.

**Intenti:**
- Creare un percorso per aumentare gradualmente il volume di consegna e-mail per la preparazione degli indirizzi IP
- Configurare una condizione di limite del profilo per limitare il numero di destinatari per esecuzione della consegna
- Proteggere la reputazione del mittente quando si passa a un nuovo provider di servizi e-mail, indirizzo IP o dominio
- Rimuovi la condizione di limite del volume dopo che l&#39;IP è completamente riscaldato

**Glossario:**
- **Riscaldamento IP**: il processo di aumento graduale del volume di invio delle e-mail da un nuovo indirizzo IP o dominio per creare la reputazione del mittente con i provider di cassette postali *(specifici per prodotto)*
- **Limite di profili**: tipo di condizione nell&#39;attività Ottimizza che limita il numero massimo di profili che ricevono un messaggio in un&#39;esecuzione di percorso specifica *(specifico per prodotto)*
- **Ottimizza attività**: attività di area di lavoro del percorso utilizzata per applicare condizioni, regole di targeting o sperimentazione per controllare il modo in cui i profili scorrono in un percorso *(specifico per prodotto)*

**Guardrail:**
- Per controllare il volume di consegna, nel metodo Condizioni dell’attività Ottimizza deve essere impostata una condizione di limite del profilo.
- I profili che superano il limite assumono il percorso alternativo definito nel percorso.
- Il limite massimo per il profilo dovrebbe essere aumentato gradualmente nel tempo fino al numero totale di abbonati.

**Terminologia:**
- Nome canonico: consegne di rampa — Acronimo: none — varianti: riscaldamento IP, riscaldamento IP, rampa di consegna
- Sinonimi: &quot;riscaldamento IP&quot; = &quot;riscaldamento IP&quot; = &quot;costruzione della reputazione del mittente&quot;
- Non confondere: &quot;Limite del profilo&quot; ≠ &quot;Limite delle dimensioni del pubblico&quot; (Il limite del profilo è un limite di consegna per esecuzione; la dimensione del pubblico è il numero totale di profili qualificati)

**Domande frequenti:**
- **D: perché devo incrementare gradualmente le consegne quando si passa a un nuovo IP o dominio?** — Un nuovo IP o dominio non dispone di cronologia di invio, pertanto i provider di caselle di posta possono bloccare o inviare messaggi di posta indesiderata fino a quando non viene stabilita una reputazione positiva attraverso un volume graduale e crescente.
- **D: in che modo la condizione Limite del profilo controlla il volume di consegna?** — Imposta un numero massimo di profili che possono ricevere il messaggio in una singola esecuzione di percorso; i profili oltre tale limite utilizzano invece un percorso alternativo.
- **Q: quando posso rimuovere la condizione Limite del profilo?** — Una volta che l&#39;IP è completamente riscaldato e la reputazione del mittente è stabilita, è possibile rimuovere la condizione dal percorso.
- **Q: posso aumentare gradualmente il limite nel tempo?** — Sì; è possibile aggiornare il campo Limite nella condizione Limite profilo per aumentare progressivamente il numero di destinatari per esecuzione fino al numero completo di abbonati.

+++
