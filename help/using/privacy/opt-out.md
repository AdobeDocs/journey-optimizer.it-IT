---
solution: Journey Optimizer
product: journey optimizer
title: Gestire la rinuncia
description: Scopri come gestire la rinuncia e la privacy
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: c5bae757-a109-45f8-bf8d-182044a73cca
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---

# Gestire la rinuncia {#consent}

## Informazioni sulla gestione delle rinunce {#about}

Fornire ai destinatari la possibilità di annullare l’iscrizione alla ricezione di comunicazioni da un marchio è un requisito legale. Ulteriori informazioni sulla legislazione applicabile nel [Documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target=&quot;_blank&quot;}.

**Perché è importante?**

* Il mancato rispetto di queste normative introduce rischi legali normativi per il tuo marchio.
* Ti aiuta a evitare l’invio di comunicazioni non richieste ai destinatari, il che potrebbe far sì che contrassegnino i tuoi messaggi come spam e danneggino la tua reputazione.

## Gestione delle rinunce in Journey Optimizer {#opt-out-ajo}

Quando invii messaggi da percorsi o campagne, devi sempre assicurarti che i clienti possano annullare l’iscrizione a comunicazioni future. Una volta annullato l’abbonamento, i profili vengono rimossi automaticamente dal pubblico dei messaggi di marketing futuri.

Quando **[!DNL Journey Optimizer]** fornisce modi per gestire la rinuncia nelle e-mail e nei messaggi SMS, le notifiche push non richiedono alcuna azione da parte dell’utente, in quanto i destinatari possono annullare l’iscrizione tramite i propri dispositivi. Ad esempio, al momento del download o dell’utilizzo dell’app, possono scegliere di interrompere le notifiche. Analogamente, possono modificare le impostazioni di notifica tramite il sistema operativo mobile.

Scopri come gestire la rinuncia nei messaggi e-mail e SMS di Journey Optimizer in queste sezioni:

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="../email/email-opt-out.md">
<img alt="Lead" src="../assets/do-not-localize/privacy-email-optout.jpeg" width="50%&gt;
&lt;/a&gt;
&lt;div&gt;&lt;a href=" ../email/email-opt-out.md"><strong>Gestione della rinuncia e-mail</strong>
</div>
<p>
</td>
<td>
<a href="../sms/sms-opt-out.md">
<img alt="Infrequente" src="../assets/do-not-localize/privacy-sms-opt-out.jpeg" width="50%&gt;
&lt;/a&gt;
&lt;div&gt;
&lt;a href=" ../sms/sms-opt-out.md"><strong>Gestione della rinuncia agli SMS</strong></a>
</div>
<p></td>
</tr></table>

>[!NOTE]
>
>In [!DNL Journey Optimizer], il consenso viene gestito da Experience Platform [Schema di consenso](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html){target=&quot;_blank&quot;}. Per impostazione predefinita, il valore del campo di consenso è vuoto e viene trattato come consenso alla ricezione delle comunicazioni. Puoi modificare questo valore predefinito durante l’onboarding in uno dei possibili valori elencati [qui](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/consents.html#choice-values){target=&quot;_blank&quot;}.