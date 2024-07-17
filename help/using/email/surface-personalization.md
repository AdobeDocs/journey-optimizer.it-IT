---
solution: Journey Optimizer
product: journey optimizer
title: Personalizzare le impostazioni della superficie e-mail
description: Scopri come definire valori personalizzati per le impostazioni a livello di superficie del canale e-mail
feature: Surface, Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: impostazioni, e-mail, configurazione, sottodominio
badge: label="Disponibilità limitata"
exl-id: 1e004a76-5d6d-43a1-b198-5c9b41f5332c
source-git-commit: 2cd62c97bef156d0c1e7dda8a962be789f8131de
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 17%

---

# Personalizzare le impostazioni della superficie e-mail {#surface-personalization}

Per una maggiore flessibilità e un maggiore controllo sulle impostazioni delle e-mail, [!DNL Journey Optimizer] ti consente di definire valori personalizzati per sottodomini e intestazioni<!--and URL tracking parameters--> durante la creazione di superfici e-mail.

>[!AVAILABILITY]
>
>La personalizzazione della superficie e-mail è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.

## Aggiungi i sottodomini dinamici {#dynamic-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_surface_perso_not_available"
>title="Personalizzazione non disponibile"
>abstract="Questa superficie è stata creata senza alcun attributo di personalizzazione. Fai riferimento alla documentazione per i passaggi da risolvere se è necessaria la personalizzazione."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain"
>title="Abilita i sottodomini dinamici"
>abstract="Quando crei una superficie e-mail, puoi impostare sottodomini dinamici in base alle condizioni da te definite utilizzando l’editor di personalizzazione. Puoi aggiungere fino a 50 sottodomini dinamici."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="Alcuni sottodomini potrebbero non essere disponibili"
>abstract="Alcuni sottodomini non sono attualmente disponibili per la selezione a causa della registrazione del ciclo di feedback in sospeso. Questo processo può richiedere fino a 10 giorni lavorativi. Una volta completato, puoi scegliere tra tutti i sottodomini disponibili."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation" text="Introduzione alla delega dei sottodomini"

Durante la creazione di una superficie e-mail, puoi impostare sottodomini dinamici in base a condizioni specifiche.

Ad esempio, se disponi di vincoli legali per l’invio di messaggi da un indirizzo e-mail dedicato per paese, puoi utilizzare i sottodomini dinamici. Questo consente di creare una singola superficie con diversi sottodomini di invio corrispondenti a diversi paesi, anziché creare più superfici per ciascun paese. Puoi quindi eseguire il targeting dei clienti in vari paesi consolidati in una sola campagna.

Per definire i sottodomini dinamici in una superficie di canale e-mail, segui i passaggi indicati di seguito.

1. Prima di creare una superficie, imposta i sottodomini da utilizzare per l’invio delle e-mail in base al caso d’uso. [Scopri come](../configuration/about-subdomain-delegation.md)

   Ad esempio, supponiamo che tu voglia utilizzare sottodomini diversi per paesi diversi: imposta un sottodominio specifico per gli Stati Uniti, uno specifico per il Regno Unito, ecc.

1. Create una superficie di canale. [Scopri come](../configuration/channel-surfaces.md)

1. Seleziona il canale **[!UICONTROL E-mail]**.

1. Nella sezione **Sottodominio**, abilita l&#39;opzione **[!UICONTROL Sottodominio dinamico]**.

   ![](assets/surface-email-dynamic-subdomain.png)

1. Selezionare l&#39;icona Modifica accanto al primo campo **[!UICONTROL Condizione]**.

1. Verrà aperto l&#39;[editor di personalizzazione](../personalization/personalization-build-expressions.md). In questo esempio, impostare una condizione come `Country` è uguale a `US`.

   ![](assets/surface-email-edit-condition.png)

1. Seleziona il sottodominio da associare a questa condizione. [Ulteriori informazioni sui sottodomini](../configuration/about-subdomain-delegation.md)

   >[!NOTE]
   >
   >Alcuni sottodomini non sono attualmente disponibili per la selezione a causa della registrazione del [ciclo di feedback](../reports/deliverability.md#feedback-loops) in sospeso. Questo processo può richiedere fino a 10 giorni lavorativi. Una volta completati, puoi scegliere tra tutti i sottodomini disponibili. <!--where FL registration happens? is it when delegating a subdomain and you're awaiting from subdomain validation? or is it on ISP side only?-->

   ![](assets/surface-email-select-subdomain.png)

   Tutti i destinatari con sede negli Stati Uniti riceveranno messaggi utilizzando il sottodominio selezionato per quel paese, il che significa che tutti gli URL coinvolti (ad esempio pagina mirror, URL di tracciamento o collegamento per annullare l’abbonamento) saranno compilati in base a quel sottodominio.

1. Imposta altri sottodomini dinamici come desiderato. Puoi aggiungere fino a 50 elementi.

   ![](assets/surface-email-add-dynamic-subdomain.png)

   <!--Select the [IP pool](../configuration/ip-pools.md) to associate with the surface. [Learn more](email-settings.md#subdomains-and-ip-pools)-->

1. Definisci tutte le altre [impostazioni e-mail](email-settings.md) e [invia](../configuration/channel-surfaces.md#create-channel-surface) la tua superficie.

Dopo aver aggiunto uno o più sottodomini dinamici a una superficie, gli elementi seguenti verranno compilati in base al sottodominio dinamico risolto per questa superficie:

* Tutti gli URL (URL della risorsa, URL della pagina mirror e URL di tracciamento)

* L&#39;[URL per annullare l&#39;abbonamento](email-settings.md#list-unsubscribe)

* I suffissi **Da e-mail** e **E-mail di errore**

>[!NOTE]
>
>Se imposti sottodomini dinamici e poi disabiliti l&#39;opzione **[!UICONTROL Sottodominio dinamico]**, tutti i valori dinamici vengono rimossi. Seleziona un sottodominio e invia la superficie per rendere effettive le modifiche.

## Personalizzare l’intestazione {#personalize-header}

Puoi anche utilizzare la personalizzazione per tutti i parametri di intestazione definiti in una superficie.

Ad esempio, se disponi di più marchi, puoi creare una singola superficie e utilizzare valori personalizzati per le intestazioni e-mail. Questo ti consente di verificare che tutte le e-mail inviate dai tuoi marchi diversi siano indirizzate a ciascuno dei tuoi clienti con i nomi e le e-mail **From** corretti. Allo stesso modo, quando i destinatari hanno premuto il pulsante **Rispondi** nel software client di posta elettronica, si desidera che i nomi e le e-mail di **Rispondi a** corrispondano al marchio corretto per l&#39;utente corretto.

Per utilizzare variabili personalizzate per i parametri di intestazione di superficie, segui i passaggi seguenti.

>[!NOTE]
>
>Puoi personalizzare tutti i campi **[!UICONTROL Parametri intestazione]**, ad eccezione del campo **[!UICONTROL Prefisso e-mail errore]**.


1. Definisci i parametri di intestazione come faresti normalmente. [Scopri come](email-settings.md#email-header)

1. Per ogni campo, seleziona l’icona Modifica.

   ![](assets/surface-email-personalize-header.png)

1. Verrà aperto l&#39;[editor di personalizzazione](../personalization/personalization-build-expressions.md). Definisci la condizione come desiderato e salva le modifiche.

   Ad esempio, imposta una condizione per cui ogni destinatario riceve un’e-mail dal proprio rappresentante del marchio.

   >[!NOTE]
   >
   >È possibile selezionare solo **[!UICONTROL Attributi profilo]** e **[!UICONTROL Funzioni helper]**.

1. Ripeti i passaggi precedenti per ogni parametro a cui desideri aggiungere la personalizzazione.

>[!NOTE]
>
>Se hai aggiunto uno o più sottodomini dinamici alla tua superficie, i suffissi **Da e-mail** e **E-mail di errore** verranno compilati in base al [sottodominio dinamico](#dynamic-subdomains) risolto.

<!--
## Use personalized URL tracking {#personalize-url-tracking}

To use personalized URL tracking prameters, follow the steps below.

1. Select the profile attribute of your choice from the personalization editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->

## Visualizza dettagli superficie {#view-surface-details}

Quando utilizzi una superficie con impostazioni personalizzate in una campagna o in una superficie, puoi visualizzarne i dettagli direttamente all’interno della campagna o della superficie. Segui i passaggi seguenti.

1. Crea una [campagna](../campaigns/create-campaign.md) o [percorso](../building-journeys/journey-gs.md) per e-mail.

1. Selezionare il pulsante **[!UICONTROL Modifica contenuto]**.

1. Fare clic sul pulsante **[!UICONTROL Visualizza dettagli superficie]**.

   ![](assets/campaign-view-surface-details.png)

1. Viene visualizzata la finestra **[!UICONTROL Impostazioni consegna]**. Puoi visualizzare tutte le impostazioni della superficie, inclusi i sottodomini dinamici e i parametri di intestazione personalizzati.

   >[!NOTE]
   >
   >Tutte le informazioni visualizzate in questa schermata sono di sola lettura.

1. Seleziona **[!UICONTROL Espandi]** per visualizzare i dettagli dei sottodomini dinamici.

   ![](assets/campaign-delivery-settings-subdomain-expand.png)
