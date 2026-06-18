---
solution: Journey Optimizer
product: journey optimizer
title: Panoramica sulla gestione utente
description: Scopri come definire e gestire le autorizzazioni
feature: Access Management
topic: Administration
role: Admin, Developer
level: Intermediate
keywords: autorizzazioni, diritti, restrizioni, accesso, sandbox
exl-id: b8e266b1-d8eb-4c77-9341-9761b82609b0
TQID: https://experienceleague.adobe.com/VRUXM-o41h44PxMAKyafwqSHKmduyt48j4sr11Gh-EQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
subfeature_v2:
  - id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: cbcb1cb0abbb8d4c6ea173c4deff071d0081da4e
workflow-type: tm+mt
source-wordcount: 413
ht-degree: 10%

---

# Introduzione al controllo degli accessi {#permissions-overview}

>[!BEGINSHADEBOX]

**In questa pagina:** Acquisisci familiarità con i concetti fondamentali del controllo di accesso in Journey Optimizer, inclusi ruoli, autorizzazioni, sandbox e controllo di accesso basato su oggetti e attributi, in modo da poter pianificare come concedere agli utenti il diritto di accesso.

>[!ENDSHADEBOX]

[!DNL Journey Optimizer] consente di definire e gestire le autorizzazioni assegnate a utenti diversi. Le autorizzazioni sono un insieme di diritti e restrizioni che autorizzano o negano l’accesso alle funzionalità interne al prodotto.

Il controllo degli accessi per [!DNL Journey Optimizer] viene fornito tramite **Autorizzazioni** in [!DNL Adobe CX Enterprise]. Questa funzionalità sfrutta ruoli e criteri, che collegano gli utenti con autorizzazioni e sandbox.

Per configurare il controllo degli accessi per Journey Optimizer, è necessario disporre dei privilegi di amministratore di sistema o di prodotto per la propria organizzazione. Il ruolo minimo che può concedere o revocare le autorizzazioni è quello di amministratore di prodotto. Altri ruoli di amministratore che possono gestire le autorizzazioni sono amministratori di sistema (senza restrizioni). Per ulteriori informazioni, consulta l&#39;[articolo del Centro assistenza Adobe](https://helpx.adobe.com/it/enterprise/using/admin-roles.html){target="_blank"} sui ruoli amministrativi.

<!--
 A high-level workflow for gaining and assigning access permissions can be summarized as follows:

* After licensing [!DNL Journey Optimizer], an email is sent to the administrator specified during licensing.
* The administrator logs in to Adobe Admin Console and selects [!DNL Journey Optimizer] from the list of products on the overview page.
* To grant access to [!DNL Journey Optimizer], it is recommended that the administrator add users to the default product profile
* In Experience Platform Permissions, the administrator can create new roles or edit the permissions and users for any existing roles.
* When creating or editing a role, the administrator adds users to the role using the users tab, and grants permissions to these users (such as "Read Datasets" or "Manage Schemas") by editing the role's permissions. Similarly, the administrator can assign access to sandboxes using the same editing option.
* When users log in to the Journey Optimizer user interface, their access to capabilities is driven by the permissions that have been granted to them from the previous step. For example, if a user does not have the View Datasets permission, the Datasets tab in the side menu will not be visible to that user.
-->


La gestione degli utenti in [!DNL Journey Optimizer] si basa sui seguenti concetti chiave:

* **[!UICONTROL Ruoli]**: i ruoli fanno riferimento a una raccolta di utenti che condividono le stesse autorizzazioni e sandbox. Questi ruoli consentono di gestire facilmente l’accesso e le autorizzazioni per diversi gruppi di utenti all’interno dell’organizzazione. Un ruolo viene fornito con un set di diritti unitari (autorizzazioni) che consente agli utenti di accedere a determinate funzionalità o oggetti nell’interfaccia.
Con [!DNL Journey Optimizer] puoi scegliere tra una serie di **[!UICONTROL Ruoli]** preesistenti, ciascuno con diversi livelli di autorizzazioni, da assegnare agli utenti. Ulteriori informazioni sui **Ruoli incorporati** disponibili in [questa pagina](ootb-product-profiles.md).

* **[!UICONTROL Autorizzazioni]**: le autorizzazioni sono diritti unitari che ti consentono di definire le autorizzazioni assegnate a **[!UICONTROL Ruoli]**. Ogni autorizzazione viene raccolta nelle risorse, ad esempio Percorso o Offerte, che rappresentano le diverse funzionalità o oggetti in [!DNL Journey Optimizer]. Per ulteriori informazioni, consulta la sezione [Livelli di autorizzazione](high-low-permissions.md).

  ![](assets/do-not-localize/permissions_2.png)

* **[!UICONTROL Sandbox]**: le sandbox virtuali suddividono le istanze in ambienti virtuali separati e isolati. Le sandbox vengono assegnate tramite i ruoli in Autorizzazioni. Ulteriori informazioni sull&#39;utilizzo di [sandbox](sandboxes.md).

* **Controllo dell&#39;accesso basato su oggetti**: etichette per limitare l&#39;accesso a un oggetto. Questo approccio protegge le risorse digitali sensibili da utenti non autorizzati e garantisce un’ulteriore protezione dei dati personali. Ulteriori informazioni sulla [Gestione degli accessi basata su oggetti](object-based-access.md).

* **Controllo dell&#39;accesso basato su attributi**: autorizzazioni per gestire l&#39;accesso ai dati per team o gruppi di utenti specifici. Il controllo dell&#39;accesso basato su attributi consente agli amministratori di controllare l&#39;accesso a oggetti e/o funzionalità specifiche in base agli attributi. Gli attributi possono essere metadati aggiunti a un oggetto, ad esempio un’etichetta aggiunta a un campo o a un segmento dello schema. Un amministratore definisce i criteri di accesso che includono attributi per gestire le autorizzazioni di accesso degli utenti. Ulteriori informazioni sulla [Gestione degli accessi basata su attributi](attribute-based-access.md).


## Argomenti di approfondimento

Ora che conosci i concetti del controllo di accesso in **[!DNL Journey Optimizer]**, è ora di approfondire queste sezioni della documentazione per iniziare a configurare le autorizzazioni.


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="permissions.md">
<img alt="Autorizzazioni" src="assets/do-not-localize/role.jpg">
</a>
<div>
<a href="permissions.md"><strong>Concedi l'accesso</strong></a>
</div>
<p>
</td>
<td>
<a href="ootb-permissions.md">
<img alt="Autorizzazioni incorporate" src="assets/do-not-localize/select.jpg">
</a>
<div>
<a href="ootb-permissions.md"><strong>Autorizzazioni incorporate</strong></a>
</div>
<p>
</td>
<td>
<a href="sandboxes.md">
<img alt="gestire le sandbox" src="assets/do-not-localize/sandboxes.jpg">
</a>
<div>
<a href="sandboxes.md"><strong>Gestione sandbox</strong></a>
</div>
<p></td>
<td>
<a href="attribute-based-access.md">
<img alt="Controllo degli accessi basato su attributi" src="assets/do-not-localize/data-access.jpeg">
</a>
<div>
<a href="attribute-based-access.md"><strong>Controllo dell'accesso basato su attributi</strong></a>
</div>
<p>
</td>
</tr></table>