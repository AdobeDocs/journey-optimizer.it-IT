---
solution: Journey Optimizer
product: journey optimizer
title: Configurare i sottodomini dinamici e-mail
description: Scopri come configurare i sottodomini dinamici a livello della superficie del canale e-mail
feature: Surface, Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: impostazioni, e-mail, configurazione, sottodominio
hide: true
hidefromtoc: true
source-git-commit: c082d9329949fd8dc68929e3934daf2d9dfdbd46
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Configurare i sottodomini dinamici e-mail {#surface-personalization}

Per una maggiore flessibilità e un maggiore controllo sulle impostazioni e-mail durante la creazione di superfici e-mail, [!DNL Journey Optimizer] ti consente di definire valori personalizzati per sottodomini, intestazioni e parametri di tracciamento URL.

## Aggiungere sottodomini dinamici {#dynamic-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_surface_perso_not_available"
>title="Personalizzazione non disponibile"
>abstract="Questa superficie è stata creata senza attributi di personalizzazione. Consulta la documentazione per i passaggi da seguire per risolvere eventuali esigenze di personalizzazione."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain"
>title="Abilitare i sottodomini dinamici"
>abstract="Durante la creazione di una superficie e-mail, puoi impostare sottodomini dinamici in base alle condizioni definite utilizzando l’Editor espressioni. Puoi aggiungere fino a 50 sottodomini dinamici."

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="Alcuni sottodomini potrebbero non essere disponibili"
>abstract="Alcuni sottodomini non sono attualmente disponibili per la selezione a causa della registrazione del ciclo di feedback in sospeso. Questo processo può richiedere fino a 10 giorni lavorativi. Una volta completati, puoi scegliere tra tutti i sottodomini disponibili."

Durante la creazione di una superficie e-mail, puoi impostare sottodomini dinamici in base a condizioni specifiche.

Ad esempio, se disponi di vincoli legali per l’invio di messaggi da un indirizzo e-mail dedicato per paese, puoi utilizzare i sottodomini dinamici. Questo consente di creare una singola superficie con diversi sottodomini di invio corrispondenti a diversi paesi, anziché creare più superfici per ciascun paese. Puoi quindi eseguire il targeting dei clienti in vari paesi consolidati in una sola campagna.

Per definire i sottodomini dinamici, segui i passaggi indicati di seguito.

1. Create una superficie di canale. [Scopri come](../configuration/channel-surfaces.md)

1. Seleziona la **[!UICONTROL E-mail]** canale.

1. In **Sottodominio** , abilita **[!UICONTROL Sottodominio dinamico]** opzione.

   ![](assets/surface-email-dynamic-subdomain.png)

1. Seleziona l’icona Modifica accanto alla prima **[!UICONTROL Condizione]** campo.

1. Il [Editor espressioni](../personalization/personalization-build-expressions.md) viene aperto. In questo esempio, imposta una condizione come `Country` è uguale a `US`.

   ![](assets/surface-email-edit-condition.png)

1. Seleziona il sottodominio da associare a questa condizione. [Ulteriori informazioni sui sottodomini](../configuration/about-subdomain-delegation.md)

   >[!NOTE]
   >
   >Alcuni sottodomini non sono attualmente disponibili per la selezione a causa di elementi in sospeso [ciclo di feedback](../reports/deliverability.md#feedback-loops) registrazione. Questo processo può richiedere fino a 10 giorni lavorativi. Una volta completati, puoi scegliere tra tutti i sottodomini disponibili. <!--where FL registration happens? is it when delegating a subdomain and you're awaiting from subdomain validation? or is it on ISP side only?-->

   ![](assets/surface-email-select-subdomain.png)

   Tutti i destinatari con sede negli Stati Uniti riceveranno messaggi utilizzando il sottodominio selezionato per quel paese, il che significa che tutti gli URL coinvolti (ad esempio pagina mirror, URL di tracciamento o collegamento per annullare l’abbonamento) verranno compilati in base a quel sottodominio.

1. Imposta un altro sottodominio dinamico come desiderato. Puoi aggiungere fino a 50 elementi.

   ![](assets/surface-email-add-dynamic-subdomain.png)

1. Seleziona la [Pool IP](../configuration/ip-pools.md) per associarlo alla superficie. [Ulteriori informazioni](email-settings.md#subdomains-and-ip-pools)

Dopo aver aggiunto uno o più sottodomini dinamici a una superficie, gli elementi seguenti verranno compilati in base al sottodominio dinamico risolto per questa superficie:

* Tutti gli URL (URL della risorsa, URL della pagina mirror e URL di tracciamento)

* Il [URL per annullamento iscrizione](email-settings.md#list-unsubscribe)

* Il **Da e-mail** e **E-mail di errore** suffissi

## Personalizzare l’intestazione (#personalize-header)

Puoi anche utilizzare la personalizzazione per tutti i parametri di intestazione definiti in una superficie.

Ad esempio, se disponi di più marchi, puoi creare una singola superficie e utilizzare valori personalizzati per le intestazioni e-mail. Questo ti consente di assicurarti che tutte le e-mail inviate dai tuoi marchi diversi siano indirizzate a ciascuno dei tuoi clienti con il **Da** nomi ed e-mail. Allo stesso modo, quando i destinatari raggiungono **Rispondi** nel software client e-mail, si desidera **Rispondi** i nomi e le e-mail corrispondono al brand corretto per l’utente giusto.

Per utilizzare variabili personalizzate per i parametri di intestazione di superficie, segui i passaggi seguenti.

1. Definisci i parametri di intestazione come faresti normalmente. [Scopri come](email-settings.md#email-header)

1. Per ogni campo, seleziona l’icona Modifica.

   ![](assets/surface-email-personalize-header.png)

1. Il [Editor espressioni](../personalization/personalization-build-expressions.md) viene aperto. Definisci la condizione come desiderato e salva le modifiche.<!--In this example, set a condition such as -->

   >[!NOTE]
   >
   >Puoi selezionare solo **[!UICONTROL Attributi del profilo]** e **[!UICONTROL Funzioni di supporto]**.

1. Ripeti i passaggi precedenti per ogni parametro a cui desideri aggiungere la personalizzazione.

   >[!NOTE]
   >
   >Se hai aggiunto uno o più sottodomini dinamici alla tua superficie, il **Da e-mail** e **E-mail di errore** i suffissi verranno compilati in base al [sottodominio dinamico](#dynamic-subdomains).

<!--
## Use personalized URL tracking {#personalize-url-tracking}

To use personalized URL tracking prameters, follow the steps below.

select the profile attribute of your choice from the expression editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->
