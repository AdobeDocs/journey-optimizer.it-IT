---
solution: Journey Optimizer
product: journey optimizer
title: Gestire le preferenze dei clienti
description: Scopri come gestire le preferenze degli utenti tramite i criteri di consenso
feature: Journeys, Privacy, Consent Management, Landing Pages
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: politiche, governance, piattaforma, consenso, scudo sanitario
source-git-commit: bbea90bd21bd19941e8c8df93c8ec7a8a2769d77
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 4%

---

# Gestire le preferenze dei clienti {#preference-center}

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente disponibile solo per le organizzazioni che hanno acquistato il componente aggiuntivo Adobe **Healthcare Shield** o **Privacy and Security Shield**.

In un moderno ecosistema di automazione del marketing, i brand interagiscono con i clienti attraverso vari punti di contatto, affrontando il rischio di comunicazione irrilevante o eccessiva, che porta a disimpegno, reclami di spam e rischi di conformità. Ecco perché devono gestire le preferenze dei loro clienti per acquisire informazioni in tempo reale sul loro pubblico e fornire comunicazioni personalizzate e rispettose.

Con [!DNL Adobe Journey Optimizer], tramite l&#39;utilizzo di [criteri di consenso](consent.md), puoi rispettare le preferenze dei tuoi clienti<!-- in terms of **channels** and **topics**-->. In questo modo [!DNL Journey Optimizer] esegue il targeting solo dei clienti in base alle loro scelte<!-- their preferred channels and on the subscription topics-->, nel rispetto del loro consenso.

Per gestire le preferenze degli utenti con [!DNL Journey Optimizer], puoi:

* Recupera il consenso dei clienti per il consenso o la rinuncia a qualsiasi canale nativo in uscita. Ad esempio, creare un criterio di consenso in [!DNL Experience Platform] per escludere i clienti che non hanno acconsentito a ricevere comunicazioni per un determinato canale. Applicare quindi questo criterio di consenso in [!DNL Journey Optimizer] utilizzando una configurazione del canale e-mail. [Scopri come](consent.md#surface-marketing-actions)

  >[!NOTE]
  >
  >I canali supportati sono E-mail, Push, SMS e InApp.<!--To check-->

* Chiedi ai tuoi clienti quali argomenti desiderano abbonarsi (ad esempio il tipo di comunicazioni che accettano di ricevere o meno). [Scopri come](#manage-preferences)

>[!IMPORTANT]
>
>Il consenso ha la precedenza sulle preferenze. Ad esempio, uno dei tuoi clienti ha indicato che il loro canale preferito è la posta elettronica e che hanno accettato di ricevere newsletter<!-- they are interested in yoga-->; tuttavia, se hanno rinunciato a ricevere comunicazioni da te, non possono essere indirizzati da una newsletter e-mail che stai inviando<!-- on yoga-->.

## Registra e rispetta le preferenze {#manage-preferences}

Con i criteri di consenso in [!DNL Journey Optimizer], puoi gestire le preferenze dei tuoi clienti a livello centrale. Questo ti consente di assicurarsi di indirizzare solo i clienti in base agli argomenti selezionati, rispettando le loro scelte di consenso. Per farlo, segui la procedura indicata di seguito.

Supponiamo che desideri indirizzare i clienti attraverso percorsi e campagne in base alle loro preferenze di comunicazione su più argomenti di abbonamento (*Newsletter*, *Offerte* e *Nuovi lanci di prodotti*).

1. Definire gli attributi di preferenza con l&#39;operatore booleano a livello di profilo<!--how??-->. Ad esempio, puoi specificare:

   * *E-mail_newsletter* - Booleano (true/false)
   * *Offers_Push* - Booleano (True/False)
   * *Nuovi avvii prodotti* - Booleano (True/False)

   Questi attributi vengono acquisiti nello schema di un [set di dati](../data/get-started-datasets.md) abilitato per il profilo e mappati al [profilo cliente unificato](../audience/get-started-profiles.md).

   >[!NOTE]
   >
   >Il consenso del cliente e le preferenze di contatto sono argomenti complessi. Per informazioni su come raccogliere, elaborare e filtrare le preferenze di consenso e di contesto in [!DNL Experience Platform], si consiglia di leggere i seguenti documenti:
   >
   >* Per informazioni sui gruppi di campi dello schema necessari per raccogliere i dati sul consenso, consulta [questa pagina](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/consent/adobe/overview){target="_blank"}. Descrive come elaborare i dati sul consenso raccolti dai clienti e integrarli nei profili dei clienti memorizzati.
   >* Per ulteriori informazioni sul gruppo di campi Consenso e preferenza, consulta [questa pagina](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/profile/consents#ingest){target="_blank"}.
   >* Per aggiungere campi delle preferenze personalizzati allo schema, seguire i passaggi descritti in [questa sezione](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/consent/adobe/dataset#custom-consent){target="_blank"}.

1. Crea una pagina per acquisire le preferenze dei clienti. Utilizzare uno dei metodi seguenti:

   * Crea una pagina Web per registrare le preferenze dei tuoi clienti utilizzando [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/home){target="_blank"}.

   * Utilizza una [!DNL Journey Optimizer] [pagina di destinazione](../landing-pages/create-lp.md) che include moduli per acquisire le preferenze dei clienti tramite i dati del profilo.  [Ulteriori informazioni sui moduli](../landing-pages/lp-forms.md) <!--Forms not released/announced yet - TBC-->

     >[!NOTE]
     >
     >Assicurati che il dominio della pagina di destinazione in uso appartenga al brand superiore e non a un sotto-brand. In effetti, le preferenze raccolte vengono memorizzate nei dati del profilo, che si trovano al livello superiore del marchio.

1. In questa pagina, i clienti possono aggiornare le proprie preferenze, ad esempio gli abbonamenti per argomento, selezionando o deselezionando le caselle di controllo.

   Ogni azione attiva un evento di consenso salvato in base agli attributi di profilo corrispondenti (`true` per consenso, `false` per rinuncia) acquisendo i dati nello schema del set di dati abilitato per il profilo<!-- that contains the corresponding preference fields-->.

   <!--Record your users' preferences through the web page or landing page that you created. The data is saved against the corresponding profile, meaning that the preference data is ingested into a Profile-enabled dataset whose schema contains consent/preference fields.-->

   Ad esempio, un utente <!--whose email address is john.black@lumamail.com--> ha accettato di ricevere offerte push ma non desidera ricevere newsletter e-mail. Il profilo corrispondente viene aggiornato come segue:

   ![](assets/profile-preference-attributes.png){width=80%}

<!--The corresponding profile dataset is updated as follows:

|Attribute = Email id | Attribute = Offers_Push | Attribute = Newsletters_Email |
|---------|----------|---------|
| john.black@lumamail.com | Y | N |-->

    >[!NOTE]
    >
    >Gli eventi di consenso in arrivo vengono inseriti nel profilo del cliente, garantendo aggiornamenti in tempo reale. Ogni profilo riflette le scelte più recenti nelle preferenze di abbonamento.

1. In Adobe Experience Platform, crea un criterio personalizzato (dal menu **[!UICONTROL Privacy]** > **[!UICONTROL Criteri]**). [Scopri come](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=it#create-policy){target="_blank"}

   >[!AVAILABILITY]
   >
   >I criteri di consenso sono attualmente disponibili solo per le organizzazioni che hanno acquistato il componente aggiuntivo Adobe **Healthcare Shield** o **Privacy and Security Shield**. [Ulteriori informazioni sui criteri di consenso](consent.md)

   Per utilizzare i criteri di consenso, gli attributi di preferenza devono essere presenti nei dati del profilo. Per questo motivo è necessario definire questi attributi a livello di profilo (come descritto nel passaggio 1).

1. Scegli il tipo **[!UICONTROL Criterio di consenso]** e configura una condizione nel modo seguente. [Scopri come configurare i criteri di consenso](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=it#consent-policy){target="_blank"}

<!--Consent policies are comprised of two logical components:

* **If**: The condition that will trigger the policy check, based on a certain marketing action (email, SMS, push, custom action, etc.) being performed, the presence of certain data usage labels, or a combination of the two.

* **Then**: The consent attribute must be present for a profile to be included in the action that triggered the policy. More than one field can also be selected.-->

    Ad esempio, per inviare comunicazioni solo ai clienti che non hanno rinunciato alla ricezione di newsletter e-mail, crea un criterio personalizzato e definisci la seguente condizione:
    
    * Se **[!UICONTROL Azione di marketing]** è uguale a **[!UICONTROL E-mail]**
    
    * Then **[!UICONTROL E-mail_newsletter]** non esiste **[!UICONTROL false]** O **[!UICONTROL E-mail_newsletter]** non è uguale a **[!UICONTROL false]**
    
    ![](assets/consent-policy-email-newsletter.png){width=80%}
    
    >[!TIP]
    >
    >Il set di dati abilitato per il profilo deve includere l&#39;attributo di profilo **[!UICONTROL Newsletter_Email]** con il valore impostato su &quot;true&quot; (come descritto al passaggio 1)

1. Dopo aver creato i criteri di consenso, sfruttali in [!DNL Journey Optimizer] utilizzando [configurazioni di canale](consent.md#surface-marketing-actions) o [azioni personalizzate di percorso](consent.md#journey-custom-actions).

1. Ora puoi utilizzare queste configurazioni di canale o azioni personalizzate nei tuoi percorsi e campagne per assicurarti che le preferenze dei tuoi clienti <!--targeted--> siano rispettate.
