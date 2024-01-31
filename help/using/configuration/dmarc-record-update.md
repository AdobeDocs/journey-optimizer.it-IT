---
solution: Journey Optimizer
product: journey optimizer
title: Conformità ai nuovi requisiti DMARC
description: Scopri perché e quando impostare il record DMARC in Journey Optimizer
feature: Subdomains, Channel Configuration, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: sottodominio, dominio, posta, dmarc, record
source-git-commit: c5da9e9cfd5c03d7c6898e492582e5cc3e466447
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 6%

---

# Conformità ai nuovi requisiti DMARC {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Scopri di più sull’aggiornamento DMARC obbligatorio"
>abstract="Come parte delle procedure ottimali di settore, Google e Yahoo richiederanno che tu abbia un **Record DMARC** per qualsiasi dominio utilizzato per inviare loro e-mail, a partire dal **1 febbraio 2024**.<br>Di conseguenza, devi assicurarti di aver impostato il record DMARC per tutti i sottodomini che hai delegato ad Adobe in Journey Optimizer."

DMARC (Domain-based Message Authentication, Reporting, and Conformance) è un metodo di autenticazione e-mail che consente ai proprietari del dominio di proteggere il proprio dominio da utilizzi non autorizzati. Offrendo una politica chiara ai provider di posta elettronica/ISP, aiuta a evitare che attori dannosi inviino e-mail che affermano di essere dal tuo dominio. L’implementazione di DMARC riduce il rischio che le e-mail legittime vengano contrassegnate come spam o rifiutate e migliora il recapito dei messaggi e-mail.


Come parte delle procedure ottimali di settore, Google e Yahoo! richiedono entrambi che un **Record DMARC** per qualsiasi dominio utilizzato per inviare loro e-mail. Questo nuovo requisito si applica a partire dal **1 febbraio 2024**. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html#dmarc){target="_blank"}

>[!CAUTION]
>
>Non rispettare questo nuovo requisito da parte di Gmail e Yahoo! dovrebbe causare l’invio di e-mail nella cartella di posta indesiderata o il blocco.

Di conseguenza, Adobe consiglia vivamente di disporre di un record DMARC configurato per tutti i sottodomini a cui hai delegato l’Adobe in [!DNL Journey Optimizer]. Segui i passaggi seguenti che si applicano al tuo caso:

* Se è stato [completamente delegato](delegate-subdomain.md#full-subdomain-delegation) ad Adobe, per l’invio dei sottodomini, segui una delle opzioni seguenti:

   * Configurare DMARC nel dominio principale dei sottodomini delegati **nella soluzione di hosting**.
oppure
   * Configurare DMARC nei sottodomini delegati **nel[!DNL Journey Optimizer]** interfaccia utente di configurazione - senza alcun lavoro aggiuntivo sulla soluzione di hosting. [Scopri come](dmarc-record.md#implement-dmarc)

* Se hai impostato i sottodomini di invio con [CNAME](delegate-subdomain.md#cname-subdomain-delegation), esegui una delle opzioni seguenti:

   * Configurare DMARC nei sottodomini o nel dominio principale dei sottodomini **nella soluzione di hosting**.
oppure
   * Configurare DMARC nei sottodomini delegati **nel[!DNL Journey Optimizer]** interfaccia utente di configurazione. [Scopri come](dmarc-record.md#implement-dmarc)

  Tuttavia, con la delega CNAME sarà necessario inserire anche la voce nella soluzione di hosting. Di conseguenza, assicurati di coordinarti con il tuo reparto IT in modo che possa eseguire l’aggiornamento descritto in [questa sezione](dmarc-record.md#implement-dmarc).


Le timeline più recenti condivise da Google e Yahoo sono le seguenti:

* Google:

   * **Febbraio 2024** - Iniziano i mancati recapiti temporanei destinati a segnalare la mancata conformità. Le e-mail continueranno a essere consegnate come di consueto dopo un breve ritardo se non sei ancora in regola con le normative. Se sei pienamente conforme, non ci saranno mancati recapiti temporanei e non ne risentirai.

   * **Aprile 2024** - Inizieranno i blocchi per i mittenti che non sono conformi ai requisiti DMARC. Solo una parte dei messaggi e-mail non conformi verrà bloccata inizialmente, con la percentuale di messaggi bloccati che aumenterà nel tempo.

   * **1 giugno 2024** - Qualsiasi mittente non pienamente conforme subirà un blocco.

* Yahoo non ha fornito date esatte, ma ha detto che &quot;l&#39;implementazione dell&#39;applicazione inizierà a febbraio 2024. L&#39;applicazione sarà introdotta gradualmente&quot;.

>[!NOTE]
>
>In caso di domande o se hai bisogno di supporto, contatta il tuo consulente del team Deliverability di Adobe o il tuo rappresentante di Adobe.

**Collegamenti utili**

* Ulteriori informazioni su DMARC sono disponibili in [Guida alle best practice per la consegna](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html#about){target="_blank"}
* Ulteriori informazioni su queste modifiche sono disponibili in [Guida alle best practice per la consegna](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html){target="_blank"}
* Leggete [Annuncio Google Gmail](https://blog.google/products/gmail/gmail-security-authentication-spam-protection/){target="_blank"}
* Leggete [Yahoo! annuncio](https://blog.postmaster.yahooinc.com/post/730172167494483968/more-secure-less-spam){target="_blank"}
