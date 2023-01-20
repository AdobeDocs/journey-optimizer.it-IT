---
solution: Journey Optimizer
product: journey optimizer
title: Controllo dell’accesso basato su attributi
description: Il controllo dell’accesso basato su attributi (ABAC) consente di definire autorizzazioni per gestire l’accesso ai dati per team o gruppi di utenti specifici.
feature: Access Management
topic: Administration
role: Admin,Leader
level: Intermediate
keywords: abac, attributo, autorizzazioni, dati, accesso, sensibile, risorse
exl-id: 162b0848-313a-447e-9237-5a6dbc8102c6
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 3%

---

# Controllo dell’accesso basato su attributi {#attribute-based-access}

>[!IMPORTANT]
>
>Il controllo degli accessi basato su attributi è attualmente limitato ad alcuni utenti e verrà esteso a tutti gli ambienti con una versione futura.

Il controllo dell’accesso basato su attributi (ABAC) consente di definire autorizzazioni per gestire l’accesso ai dati per team o gruppi di utenti specifici. Il suo scopo è proteggere i beni digitali sensibili da utenti non autorizzati che consentono un&#39;ulteriore protezione dei dati personali.

In Adobe Journey Optimizer, ABAC ti consente di proteggere i dati e di concedere un accesso specifico a specifici elementi di campo, inclusi schemi Experience Data Model (XDM), attributi di profilo e segmenti.

Per un elenco più dettagliato della terminologia utilizzata con ABAC, consulta [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/overview.html).

In questo esempio, desideri aggiungere un’etichetta al **Cittadinanza** campo schema per impedire agli utenti non autorizzati di utilizzarlo. Affinché questo funzioni, devi eseguire le seguenti operazioni:

1. Crea un nuovo  **[!UICONTROL Ruolo]** e assegnarlo con il corrispondente  **[!UICONTROL Etichetta]** per consentire agli utenti di accedere e utilizzare il campo schema.

1. Assegnare un  **[!UICONTROL Etichetta]** al **Cittadinanza** campo schema in Adobe Experience Platform.

1. Utilizza la  **[!UICONTROL Campo schema]** in Adobe Journey Optimizer.

Tieni presente che **[!UICONTROL Ruoli]**, **[!UICONTROL Criteri]** e **[!UICONTROL Prodotti]** è inoltre possibile accedervi con l&#39;API di controllo accessi basata su attributi. Per ulteriori informazioni, consulta questo [documentazione](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/abac-api/overview.html).

## Creare un ruolo e assegnare etichette {#assign-role}

>[!IMPORTANT]
>
>Prima di gestire le autorizzazioni per un ruolo, è necessario creare un criterio. Per ulteriori informazioni, consulta [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/policies.html).

**[!UICONTROL Ruoli]** sono un set di utenti che condividono le stesse autorizzazioni, etichette e sandbox all’interno della tua organizzazione. Ogni utente appartenente a un **[!UICONTROL Ruolo]** ha diritto alle app e ai servizi di Adobe contenuti nel prodotto.
Puoi anche creare un tuo **[!UICONTROL Ruoli]** per ottimizzare l’accesso degli utenti a determinate funzionalità o oggetti dell’interfaccia.

Ora vogliamo concedere agli utenti selezionati l’accesso al **Cittadinanza** campo, con etichetta C2. Per farlo, dobbiamo creare una nuova **[!UICONTROL Ruolo]** con un insieme specifico di utenti e concedere loro l&#39;etichetta C2 che consente loro di utilizzare il **Cittadinanza** dettagli in **[!UICONTROL Percorso]**.

1. Da [!DNL Permissions] prodotto, seleziona **[!UICONTROL Ruolo]** dal menu del riquadro a sinistra e fai clic su **[!UICONTROL Crea ruolo]**. Puoi anche aggiungere **[!UICONTROL Etichetta]** ai ruoli incorporati.

   ![](assets/role_1.png)

1. Aggiungi un **[!UICONTROL Nome]** e **[!UICONTROL Descrizione]** al nuovo **[!UICONTROL Ruolo]** qui: Ruolo demografico limitato.

1. Dall’elenco a discesa, seleziona la **[!UICONTROL Sandbox]**.

   ![](assets/role_2.png)

1. Da **[!UICONTROL Risorse]** menu, fai clic su **[!UICONTROL Adobe Experience Platform]** per aprire le diverse funzionalità. Qui selezioniamo **[!UICONTROL Percorsi]**.

   ![](assets/role_3.png)

1. Dall’elenco a discesa, seleziona la **[!UICONTROL Autorizzazioni]** collegata alla feature selezionata, ad esempio **[!UICONTROL Visualizza percorsi]** o **[!UICONTROL Pubblicare percorsi]**.

   ![](assets/role_6.png)

1. Dopo aver salvato la nuova **[!UICONTROL Ruolo]**, fai clic su **[!UICONTROL Proprietà]** per configurare ulteriormente l’accesso al tuo ruolo.

   ![](assets/role_7.png)

1. Da **[!UICONTROL Utenti]** scheda , fai clic su **[!UICONTROL Aggiungi utenti]**.

   ![](assets/role_8.png)

1. Da **[!UICONTROL Etichette]** scheda , seleziona **[!UICONTROL Aggiungi etichetta]**.

   ![](assets/role_9.png)

1. Seleziona la **[!UICONTROL Etichette]** desideri aggiungere al tuo ruolo e fai clic su **[!UICONTROL Salva]**. Per questo esempio, concediamo all’etichetta C2 agli utenti l’accesso al campo dello schema precedentemente limitato.

   ![](assets/role_4.png)

Gli utenti nel **Ruolo limitato demografico** Il ruolo ora ha accesso agli oggetti con etichetta C2.

## Assegnare etichette a un oggetto in Adobe Experience Platform {#assign-label}

>[!WARNING]
>
>Un uso scorretto delle etichette può interrompere l’accesso alle persone e causare violazioni dei criteri.

**[!UICONTROL Etichette]** può essere utilizzato per assegnare aree di caratteristiche specifiche utilizzando il controllo di accesso basato su attributi.
In questo esempio, vogliamo limitare l’accesso al **Cittadinanza** campo . Questo campo sarà accessibile solo agli utenti con il corrispondente **[!UICONTROL Etichetta]** a  **[!UICONTROL Ruolo]**.

Puoi anche aggiungere  **[!UICONTROL Etichetta]** a  **[!UICONTROL Schema]**,  **[!UICONTROL Set di dati]** e  **[!UICONTROL Segmenti]**.

1. Crea il tuo **[!UICONTROL Schema]**. Per ulteriori informazioni, consulta [questa documentazione](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=it).

   ![](assets/label_1.png)

1. Nella nuova creazione **[!UICONTROL Schema]**, aggiungiamo prima il **[!UICONTROL Dettagli demografici]** gruppo di campi che contiene **Cittadinanza** campo .

   ![](assets/label_2.png)

1. Da **[!UICONTROL Etichette]** scheda , controlla il nome del campo con restrizioni, qui **Cittadinanza**. Quindi, dal menu del riquadro di destra, seleziona **[!UICONTROL Modifica delle etichette di governance]**.

   ![](assets/label_3.png)

1. Seleziona il corrispondente **[!UICONTROL Etichetta]**, in questo caso, il C2 - Dati non può essere esportato verso terzi. Per un elenco dettagliato delle etichette disponibili, consulta [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html#contract-labels).

   ![](assets/label_4.png)

1. Se necessario, personalizza ulteriormente lo schema, quindi abilitalo. Per i passaggi dettagliati su come abilitare lo schema, consulta [page](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#profile).

Il campo dello schema sarà ora visibile solo e può essere utilizzato solo dagli utenti che fanno parte di un ruolo impostato con l&#39;etichetta C2.
Applicando un **[!UICONTROL Etichetta]** al tuo **[!UICONTROL Nome campo]**, tieni presente che **[!UICONTROL Etichetta]** viene automaticamente applicato al **Cittadinanza** in ogni schema creato.

![](assets/label_5.png)

## Accedere agli oggetti etichettati in Adobe Journey Optimizer {#attribute-access-ajo}

Dopo aver etichettato il nostro **Cittadinanza** nome del campo in un nuovo schema e nuovo ruolo, ora possiamo vedere l&#39;impatto di questa restrizione in Adobe Journey Optimizer.
Per il nostro esempio, un primo utente X con accesso agli oggetti con etichetta C2 creerà un Percorso con una condizione che esegue il targeting delle restrizioni **[!UICONTROL Nome campo]**. Un secondo utente Y senza accesso agli oggetti con etichetta C2 dovrà quindi pubblicare il Percorso.

1. Da Adobe Journey Optimizer, devi prima configurare il **[!UICONTROL Origine dati]** con il nuovo schema.

   ![](assets/journey_1.png)

1. Aggiungi un nuovo **[!UICONTROL Gruppo di campi]** della nuova **[!UICONTROL Schema]** a **[!UICONTROL Origine dati]**. Puoi anche creare una nuova **[!UICONTROL sorgente dati]** e associati **[!UICONTROL Gruppi di campi]**.

   ![](assets/journey_2.png)

1. Dopo aver selezionato le impostazioni create in precedenza **[!UICONTROL Schema]**, fai clic su **[!UICONTROL Modifica]** dal **[!UICONTROL Campi]** categoria.

   ![](assets/journey_3.png)

1. Seleziona la **[!UICONTROL Nome campo]** volete mirare. Qui selezioniamo le restrizioni **Cittadinanza** campo .

   ![](assets/journey_4.png)

1. Quindi, crea un Percorso che invierà un’e-mail agli utenti con una nazionalità specifica. Aggiungi un **[!UICONTROL Evento]** quindi un **[!UICONTROL Condizione]**.

   ![](assets/journey_5.png)

1. Selezionare le restrizioni **Cittadinanza** per iniziare a creare l&#39;espressione.

   ![](assets/journey_6.png)

1. Modifica il **[!UICONTROL Condizione]** per indirizzare una popolazione specifica con limitazioni **Cittadinanza** campo .

   ![](assets/journey_7.png)

1. Personalizza il tuo percorso in base alle esigenze, qui aggiungiamo un **[!UICONTROL E-mail]** azione.

   ![](assets/journey_8.png)

Se l’utente Y senza accesso all’etichetta C2 oggetti deve accedere a questo percorso con questo campo limitato:

* L’utente Y non sarà in grado di utilizzare il nome del campo con restrizioni, in quanto non sarà visibile.

* L’utente Y non sarà in grado di modificare l’espressione con il nome del campo con restrizioni in modalità avanzata. Verrà visualizzato il seguente errore `The expression is invalid. Field is no longer available or you don't have enough permission to see it`.

* L’utente Y può eliminare l’espressione.

* L&#39;utente Y non sarà in grado di testare il Percorso.

* L&#39;utente Y non sarà in grado di pubblicare il Percorso.
