---
title: 'Modificare gli indirizzi e-mail principali '
description: Scopri come determinare quale indirizzo e-mail utilizzare dal servizio di profilo.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: 5abcef4ff057bb351abaafbf4dcb99e1ab61c6a9
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Modificare gli indirizzi principali {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="Definire l’indirizzo da utilizzare"
>abstract="Quando nel database sono disponibili più indirizzi (personali, professionali, ecc.), puoi scegliere quale indirizzo dare la priorità all’invio."

Quando esegui il targeting di un profilo, diversi indirizzi e-mail o numeri di telefono possono essere disponibili nel database (indirizzo e-mail professionale, numero di telefono personale, ecc.).

Con [!DNL Journey Optimizer], puoi determinare quale indirizzo e-mail o numero di telefono utilizzare dal servizio di profilo e assegnare la priorità quando sono disponibili più indirizzi. Per farlo, segui la procedura indicata di seguito.

1. Accedi al menu **[!UICONTROL Channels]** > **[!UICONTROL General]** > **[!UICONTROL Executions fields]**.

   ![](assets/primary-address-execution-fields.png)

1. I campi attualmente utilizzati per impostazione predefinita per determinare l’indirizzo e-mail e il numero di telefono del profilo vengono visualizzati in questa schermata. Fai clic su **[!UICONTROL Edit]** per cambiarli.

   ![](assets/primary-address.png)

1. Fai clic sul campo corrente desiderato o sull’icona di modifica per selezionare un nuovo campo.

   ![](assets/primary-address-edit.png)

1. Viene visualizzato l’elenco dei campi XDM di tipo e-mail disponibili. Seleziona il campo da utilizzare.

   ![](assets/primary-address-select-field.png)

1. Fai clic su **[!UICONTROL Save]** per confermare la scelta.

Il campo di esecuzione viene aggiornato e verrà ora utilizzato come indirizzo principale.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
