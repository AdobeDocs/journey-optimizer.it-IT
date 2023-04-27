---
solution: Journey Optimizer
product: journey optimizer
title: Modificare gli indirizzi di esecuzione
description: Scopri come determinare quale indirizzo e-mail utilizzare dal servizio di profilo.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: primario, esecuzione, e-mail, target, profilo, ottimizzatore
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 23%

---

# Modificare gli indirizzi di esecuzione {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="Definire l’indirizzo da utilizzare"
>abstract="Quando nel database sono disponibili diversi indirizzi e-mail o numeri di telefono (personali, professionali, ecc.), puoi scegliere a quale assegnare la priorità per l’invio."

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="Definire l’indirizzo da utilizzare"
>abstract="Modifica i campi utilizzati per determinare l’indirizzo e-mail o il numero di telefono dei profili in modo da assegnare la priorità per l’invio."

Quando esegui il targeting di un profilo, diversi indirizzi e-mail o numeri di telefono possono essere disponibili nel database (indirizzo e-mail professionale, numero di telefono personale, ecc.).

In tal caso, [!DNL Journey Optimizer] utilizza **[!UICONTROL Campi di esecuzione]** per determinare quale indirizzo e-mail o numero di telefono utilizzare dal servizio profilo in priorità.

Per controllare i campi attualmente utilizzati per impostazione predefinita, accedi al **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Generale]** > **[!UICONTROL Campi esecuzioni]** menu.

![](assets/primary-address-execution-fields.png)

I valori correnti vengono utilizzati per tutte le consegne a livello di sandbox. Se necessario, puoi aggiornare questi campi.

Nella maggior parte dei casi, modificherai un campo di esecuzione a livello globale e definirai un valore da utilizzare per tutti i messaggi e-mail o SMS. <!--[Learn how](#admin-settings)-->

<!--In some specific use cases only, you can override the value set globally and define a different value at the journey level. [Learn more](#journey-parameters)-->

## Aggiornare le impostazioni di amministrazione {#admin-settings}

Per modificare i campi di esecuzione a livello globale a livello di sandbox, segui i passaggi seguenti.

1. Accedere al  **[!UICONTROL Canali]** > **[!UICONTROL Generale]** > **[!UICONTROL Campi esecuzioni]** menu.

1. Fai clic su **[!UICONTROL Modifica]** per modificare i valori predefiniti.

   ![](assets/primary-address.png)

1. Fai clic sul campo corrente desiderato o sull’icona di modifica per selezionare un nuovo campo.

   ![](assets/primary-address-edit.png)

1. Viene visualizzato l’elenco dei campi XDM di tipo e-mail disponibili. Seleziona il campo da utilizzare.

   ![](assets/primary-address-select-field.png)

1. Fai clic su **[!UICONTROL Salva]** per confermare la scelta.

Il campo di esecuzione viene aggiornato e verrà ora utilizzato come indirizzo principale.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->

## Ignorare un valore nei parametri del percorso {#journey-parameters}

Solo per casi d’uso specifici, puoi sovrascrivere il campo di esecuzione impostato a livello globale e definire un valore diverso a livello di percorso, in particolare per il canale e-mail.

Quando si aggiunge un **[!UICONTROL E-mail]** a un [percorso](../email/create-email.md#create-email-journey-campaign), l’indirizzo e-mail principale viene visualizzato sotto i parametri avanzati del percorso.

In alcuni contesti specifici, è possibile ignorare questo valore utilizzando il **[!UICONTROL Abilita sostituzione parametro]** a destra della **[!UICONTROL indirizzo]** campo .

![](assets/journey-enable-parameter-override.png)

>[!CAUTION]
>
>La sostituzione dell’indirizzo e-mail deve essere utilizzata solo per casi d’uso specifici. Nella maggior parte dei casi, non è necessario modificare l’indirizzo e-mail perché il valore definito come indirizzo principale nei **[!UICONTROL campi di esecuzione]** è quello che deve essere utilizzato.

L’override di questo valore può essere utile, ad esempio, per:

* Test di un’e-mail. Puoi aggiungere il tuo indirizzo e-mail: dopo aver pubblicato il percorso, l’e-mail ti viene inviata.
* Invia un messaggio e-mail agli abbonati di un elenco. Per ulteriori informazioni, consulta [questo caso d’uso](../building-journeys/message-to-subscribers-uc.md).
