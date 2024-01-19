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
source-git-commit: 7cbd6a9e80a8d6b87b3c3011db80549a3b5f6e73
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Aggiornamento DMARC obbligatorio {#dmarc-record-update}

>[!CONTEXTUALHELP]
>id="ajo_admin_dmarc_banner_link"
>title="Ulteriori informazioni sull&#39;aggiornamento DMARC obbligatorio"
>abstract="Come parte delle procedure ottimali di settore, Google e Yahoo richiederanno che tu abbia un **Record DMARC** per qualsiasi dominio utilizzato per inviare loro e-mail. Questo nuovo requisito inizia il **1 febbraio 2024**. <br>Di conseguenza, Adobe consiglia vivamente di disporre di un record DMARC configurato per tutti i sottodomini a cui hai delegato Adobe in Journey Optimizer."

Come parte delle procedure ottimali di settore, Google e Yahoo richiederanno che tu abbia un **Record DMARC** per qualsiasi dominio utilizzato per inviare loro e-mail. Questo nuovo requisito inizia il **1 febbraio 2024**.

Ulteriori informazioni sui requisiti di Google e Yahoo in [questa sezione](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

>[!CAUTION]
>
>Il mancato rispetto di questo nuovo requisito da parte di Gmail e Yahoo dovrebbe comportare l’invio di e-mail nella cartella di posta indesiderata o il blocco.

Di conseguenza, Adobe consiglia vivamente di disporre di un record DMARC configurato per tutti i sottodomini a cui hai delegato l’Adobe in [!DNL Journey Optimizer]. Segui una delle due opzioni seguenti:

* Configurare DMARC nei sottodomini o nel dominio principale dei sottodomini; **nella soluzione di hosting**.

* Configurare DMARC nei sottodomini delegati **utilizzo della funzionalità in arrivo in [!DNL Journey Optimizer] interfaccia utente di amministrazione** - senza alcun lavoro aggiuntivo sulla soluzione di hosting.

  >[!CAUTION]
  >
  >Se hai impostato [Delega CNAME](delegate-subdomain.md#cname-subdomain-delegation) per i sottodomini di invio, sarà necessario anche un certo numero di ingressi nella soluzione di hosting. Assicurati di coordinarti con il tuo reparto IT in modo che possa eseguire l&#39;aggiornamento non appena [!DNL Journey Optimizer] (il 30 gennaio 2024). <!--and be ready on February 1st, 2024-->

  Maggiori dettagli sulla [!DNL Journey Optimizer] La prossima funzionalità di DMARC sarà presto disponibile.

<!--
* If you have [fully delegated](delegate-subdomain.md#full-subdomain-delegation) your sending subdomains to Adobe, follow either one of the two options below:

    * Set up DMARC on your subdomains or on the parent domain of your subdomains **in your hosting solution**.

    * Set up DMARC on your delegated subdomains **using the upcoming feature in the [!DNL Journey Optimizer] administration UI** - with no extra work on your hosting solution.

* If you have set up [CNAME delegation](delegate-subdomain.md#cname-subdomain-delegation) for your sending subdomains, follow either one of the two options below:
    * Set up DMARC on your subdomains or on the parent domain of your subdomains **in your hosting solution**.
    * Set up DMARC on your delegated subdomains **using the upcoming feature in the [!DNL Journey Optimizer] administration UI**. However, it will also require entry in your hosting solution. Consequently, make sure you coordinate with your IT department so that they can perform the update as soon as the [!DNL Journey Optimizer] feature is available (on January, 30) - and be ready on February 1st, 2024.
    
-->

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
