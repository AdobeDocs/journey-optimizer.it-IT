---
title: 'Modificare gli indirizzi e-mail principali '
description: Scopri come determinare quale indirizzo e-mail utilizzare dal servizio di profilo.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: f1ac47a0cb405eaadc5428e7e5479eaf776d7abe
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 6%

---

# Modificare gli indirizzi e-mail principali {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="Definire l’indirizzo da utilizzare"
>abstract="Puoi scegliere quale indirizzo e-mail assegnare la priorità all’invio quando nel database sono disponibili più indirizzi (personali, professionali, ecc.)."

Quando esegui il targeting di un profilo, diversi indirizzi e-mail possono essere disponibili nel database (personale, indirizzo e-mail professionale, ecc.).

Con [!DNL Journey Optimizer], puoi determinare quale indirizzo e-mail utilizzare dal servizio di profilo e assegnare una priorità quando sono disponibili più indirizzi. Per farlo, segui la procedura indicata di seguito.

1. Accedi al menu **[!UICONTROL Channels]** > **[!UICONTROL General]** > **[!UICONTROL Executions fields]**.

   ![](assets/primary-address-execution-fields.png)

1. Il campo attualmente utilizzato per impostazione predefinita per determinare gli indirizzi e-mail dei profili viene visualizzato in questa schermata. Fai clic su **[!UICONTROL Edit]** per cambiarlo.

   ![](assets/primary-address.png)

1. Fai clic sul campo corrente o sull’icona di modifica per selezionare un nuovo campo.

   ![](assets/primary-address-edit.png)

1. Viene visualizzato l’elenco dei campi XDM di tipo e-mail disponibili. Seleziona il campo da utilizzare.

   ![](assets/primary-address-field.png)

1. Fai clic su **[!UICONTROL Save]** per confermare la scelta.

   ![](assets/primary-address-save.png)

   Il campo di esecuzione viene aggiornato e verrà ora utilizzato come indirizzo principale.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
