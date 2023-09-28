---
solution: Journey Optimizer
product: journey optimizer
title: Gestire utenti e ruoli
description: Scopri come gestire utenti e ruoli
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
keywords: product, profiles, sandbox
source-git-commit: be372f8f80d304067748d539fb8e210df6280721
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 8%

---

# Gestire utenti e ruoli {#manage-permissions}

>[!IMPORTANT]
>
> Ciascuna delle procedure descritte di seguito può essere eseguita soltanto da un **[!UICONTROL Prodotto]** o **[!UICONTROL Sistema]** amministratore.

**[!UICONTROL Ruoli]** fai riferimento a una raccolta di utenti che condividono le stesse autorizzazioni e sandbox. Questi ruoli consentono di gestire facilmente l’accesso e le autorizzazioni per diversi gruppi di utenti all’interno dell’organizzazione.

Con il [!DNL Journey Optimizer] prodotto, è possibile scegliere tra una vasta gamma di **[!UICONTROL Ruoli]**, ciascuno con diversi livelli di autorizzazioni, da assegnare agli utenti. Per ulteriori informazioni sulle **[!UICONTROL Ruoli]**, fai riferimento a questo [pagina](ootb-product-profiles.md).

Quando un utente appartiene a un **[!UICONTROL Ruolo]**, gli viene concesso l’accesso alle app e ai servizi di Adobe contenuti nel prodotto.

Se i ruoli preesistenti non soddisfano le esigenze specifiche della tua organizzazione, puoi anche creare ruoli personalizzati **[!UICONTROL Ruoli]** per ottimizzare l’accesso a determinate funzionalità o oggetti nell’interfaccia. In questo modo, puoi garantire che ogni utente abbia accesso solo alle risorse e agli strumenti necessari per eseguire le proprie attività in modo efficiente.

## Assegna un ruolo {#assigning-role}

È possibile scegliere di assegnare un **[!UICONTROL Ruolo]** ai tuoi utenti.

L’elenco di tutti i ruoli predefiniti con autorizzazioni assegnate è disponibile nella sezione [Ruoli incorporati](ootb-product-profiles.md) sezione.

Per assegnare un **[!UICONTROL Ruolo]**:

1. Per assegnare un ruolo a un utente in [!DNL Permissions] prodotto, passare alla **[!UICONTROL Ruoli]** e selezionare il ruolo desiderato.

   ![](assets/do-not-localize/access_control_2.png)

1. Dalla sezione **[!UICONTROL Utenti]** , fare clic su **[!UICONTROL Aggiungi utente]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Digita il nome o l’indirizzo e-mail dell’utente o selezionalo dall’elenco e fai clic su **[!UICONTROL Salva]**.

   Se l&#39;utente non è stato creato in precedenza in [!DNL Admin Console], fare riferimento a [Aggiungi documentazione utenti](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/users.html).

   ![](assets/do-not-localize/access_control_4.png)

L’utente dovrebbe quindi ricevere un messaggio e-mail di reindirizzamento all’istanza.

Per ulteriori informazioni sulla gestione degli utenti, consulta [Documentazione sul controllo degli accessi](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=it).

Quando accedi all’istanza, l’utente visualizzerà una visualizzazione specifica a seconda delle autorizzazioni assegnate nella sezione **[!UICONTROL Ruolo]**. Se l’utente non dispone del diritto di accesso a una funzione, viene visualizzato il seguente messaggio:

`You don't have permission to access this feature. Permission needed: XX.`

## Modifica un ruolo esistente {#edit-product-profile}

Per preconfigurati o personalizzati **[!UICONTROL Ruoli]**, puoi decidere in qualsiasi momento di aggiungere o eliminare le autorizzazioni.

In questo esempio, desideri aggiungere **[!UICONTROL Autorizzazioni]** relativo al **[!UICONTROL Percorsi]** risorsa per gli utenti assegnati al visualizzatore Percorso **[!UICONTROL Ruolo]**. Gli utenti potranno quindi pubblicare i percorsi.

Tieni presente che se modifichi una **[!UICONTROL Ruolo]**, avrà un impatto su tutti gli utenti assegnati a questo **[!UICONTROL Ruolo]**.

1. Per assegnare un ruolo a un utente in [!DNL Permissions] prodotto, passare alla **[!UICONTROL Ruoli]** e selezionare il ruolo desiderato, in questo caso il visualizzatore di Percorso **[!UICONTROL Ruolo]**.
   ![](assets/do-not-localize/access_control_5.png)

1. Dal tuo **[!UICONTROL Ruolo]** dashboard, fai clic su **[!UICONTROL Modifica]**.

   ![](assets/do-not-localize/access_control_6.png)

1. Il **[!UICONTROL Risorse]** visualizza l’elenco delle risorse che si applicano al **[!UICONTROL Experience Cloud: applicazioni basate su piattaforma]** prodotto. Trascina e rilascia le risorse per assegnare le autorizzazioni.

   Dalla sezione **[!UICONTROL Percorsi]** dell&#39;elenco a discesa delle risorse, scegliamo qui il percorso Pubblica **[!UICONTROL Autorizzazione]**.

   ![](assets/do-not-localize/access_control_14.png)

1. Se necessario, in **[!UICONTROL Elementi autorizzazione inclusi]**, fai clic sull&#39;icona X accanto a rimuovere le autorizzazioni o le risorse per il tuo ruolo.

1. Al termine, fai clic su **[!UICONTROL Salva]**.

Se necessario, puoi anche creare un nuovo ruolo con autorizzazioni specifiche. Per ulteriori informazioni, consulta [Crea un nuovo ruolo](#create-product-profile).

## Creare un nuovo ruolo {#create-product-profile}

[!DNL Journey Optimizer] consente di creare **[!UICONTROL Ruoli]** e assegna un set di autorizzazioni e sandbox agli utenti. Con **[!UICONTROL Ruoli]**, puoi autorizzare o negare l’accesso a determinate funzionalità o oggetti nell’interfaccia.

Per ulteriori informazioni sulla modalità di creazione e di gestione delle sandbox, consulta la [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=it){target="_blank"}.

In questo esempio verrà creato un ruolo denominato **Percorsi di sola lettura** dove verranno concessi diritti di sola lettura per la funzione di Percorso. Gli utenti potranno solo accedere ai percorsi e visualizzarli e non potranno accedere ad altre funzioni, come **[!DNL  Decision management]** in [!DNL Journey Optimizer].

Per creare **Percorsi di sola lettura** **[!UICONTROL Ruolo]**:

1. Per assegnare un ruolo a un utente in [!DNL Permissions] prodotto, passare alla **[!UICONTROL Ruoli]** e fai clic su **[!UICONTROL Crea ruolo]**.

   ![](assets/do-not-localize/access_control_9.png)

1. Aggiungi un **[!UICONTROL Nome]** e **[!UICONTROL Descrizione]** per il tuo nuovo **[!UICONTROL Ruolo]**. Quindi, fai clic su **[!UICONTROL Conferma]**.

   ![](assets/do-not-localize/access_control_10.png)

1. Dalla sezione **[!UICONTROL Sandbox]** elenco a discesa delle risorse, scegliere le sandbox da assegnare al **[!UICONTROL Ruolo]**. [Ulteriori informazioni sulle sandbox](sandboxes.md).

   ![](assets/do-not-localize/access_control_13.png)

1. Seleziona tra le diverse risorse, ad esempio **[!DNL Journeys]**, **[!DNL Segments]** o **[!DNL Decision management]** disponibile in [!DNL Journey Optimizer] nel menu a sinistra.

   In questo punto selezioniamo il **[!UICONTROL Percorsi]** risorsa.

   ![](assets/do-not-localize/access_control_11.png)

1. Dalla sezione **[!UICONTROL Percorsi]** , selezionare le autorizzazioni da assegnare al **[!UICONTROL Ruolo]**.

   Qui selezioniamo **[!DNL View journeys]**, **[!DNL View journeys report]**  e **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. Al termine, fai clic su **[!UICONTROL Salva]**.

Il tuo **[!UICONTROL Ruolo]** viene ora creato e configurato. Ora devi assegnarla agli utenti.

Per ulteriori informazioni sulla creazione e la gestione dei ruoli, consulta [Documentazione di Admin Console](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/roles.html).
