---
solution: Journey Optimizer
product: journey optimizer
title: Aggiornamento DMARC obbligatorio
description: Scopri perché e quando impostare il record DMARC in Journey Optimizer
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: sottodominio, dominio, posta, dmarc, record
source-git-commit: 7d5a2a9b80110505688b5bfda2e286c7a6432441
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Aggiornamento DMARC obbligatorio {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Ulteriori informazioni sull&#39;aggiornamento DMARC obbligatorio"
>abstract="Come parte delle procedure ottimali di settore, Google e Yahoo richiederanno che tu abbia un **Record DMARC** per qualsiasi dominio utilizzato per inviare loro e-mail, a partire dal **1 febbraio 2024**. <br>Di conseguenza, devi assicurarti di aver impostato il record DMARC per tutti i sottodomini che hai delegato ad Adobe in Journey Optimizer."

Come parte delle procedure ottimali di settore, Google e Yahoo richiederanno che tu abbia un **Record DMARC** per qualsiasi dominio utilizzato per inviare loro e-mail. Questo nuovo requisito inizia il **1 febbraio 2024**.

Ulteriori informazioni sui requisiti di Google e Yahoo in [questa sezione](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>Il mancato rispetto di questo nuovo requisito da parte di Gmail e Yahoo dovrebbe comportare l’invio di e-mail nella cartella di posta indesiderata o il blocco.

Di conseguenza, Adobe consiglia vivamente di disporre di un record DMARC configurato per tutti i sottodomini a cui hai delegato l’Adobe in [!DNL Journey Optimizer]. Segui i passaggi seguenti che si applicano al tuo caso:

* Se è stato [completamente delegato](delegate-subdomain.md#full-subdomain-delegation) ad Adobe, per l’invio dei sottodomini, segui una delle due opzioni seguenti:

   * Configurare DMARC nel dominio principale dei sottodomini delegati **nella soluzione di hosting**.

   * Configurare DMARC nei sottodomini delegati **utilizzo della funzionalità in arrivo in [!DNL Journey Optimizer] interfaccia utente di amministrazione** - senza alcun lavoro aggiuntivo sulla soluzione di hosting.

* Se hai impostato [Delega CNAME](delegate-subdomain.md#cname-subdomain-delegation) per i sottodomini di invio, segui una delle due opzioni seguenti:
   * Configurare DMARC nei sottodomini o nel dominio principale dei sottodomini **nella soluzione di hosting**.
   * Configurare DMARC nei sottodomini delegati **utilizzo della funzionalità in arrivo in [!DNL Journey Optimizer] interfaccia utente di amministrazione**. Tuttavia, richiederà anche l’ingresso nella soluzione di hosting. Di conseguenza, assicurati di coordinarti con il tuo reparto IT in modo che possa eseguire l’aggiornamento non appena [!DNL Journey Optimizer] (il 30 gennaio). <!--and be ready on February 1st, 2024-->

**Maggiori dettagli sulla [!DNL Journey Optimizer] La prossima funzionalità di DMARC sarà presto disponibile.**

>[!NOTE]
>
>In caso di domande o se hai bisogno di supporto, contatta il tuo consulente del team Deliverability di Adobe o il tuo rappresentante di Adobe.

Le timeline più recenti condivise da Google e Yahoo sono le seguenti:

* Google:

   * **Febbraio 2024** - Iniziano i mancati recapiti temporanei destinati a segnalare la mancata conformità. Le e-mail continueranno a essere consegnate come di consueto dopo un breve ritardo se non sei ancora in regola con le normative. Se sei pienamente conforme, non ci saranno mancati recapiti temporanei e non ne risentirai.

   * **Aprile 2024** - Inizieranno i blocchi per i mittenti che non sono conformi ai requisiti DMARC. Solo una parte dei messaggi e-mail non conformi verrà bloccata inizialmente, con la percentuale di messaggi bloccati che aumenterà nel tempo.

   * **1 giugno 2024** - Qualsiasi mittente non pienamente conforme subirà un blocco.

* Yahoo non ha fornito date esatte, ma ha detto che &quot;l&#39;implementazione dell&#39;applicazione inizierà a febbraio 2024. L&#39;applicazione sarà introdotta gradualmente&quot;.

>[!NOTE]
>
>Ulteriori informazioni sull&#39;implementazione di DMARC in [Guida alle best practice per la consegna](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"} per comprendere meglio l’impatto sul recapito messaggi e-mail.
