---
solution: Journey Optimizer
product: journey optimizer
title: Modificare gli indirizzi e-mail principali
description: Scopri come determinare quale indirizzo e-mail utilizzare dal servizio profilo.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: principale, esecuzione, e-mail, destinazione, profilo, ottimizzatore
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 14%

---

# Modificare gli indirizzi primari {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="Definire l’indirizzo da utilizzare"
>abstract="Quando nel database sono disponibili diversi indirizzi e-mail o numeri di telefono (personali, professionali, ecc.), puoi scegliere a quale assegnare la priorità per l’invio."

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="Definire l’indirizzo da utilizzare"
>abstract="Modifica i campi utilizzati per determinare l’indirizzo e-mail o il numero di telefono dei profili con cui assegnare la priorità per l’invio."

Quando esegui il targeting di un profilo, nel database potrebbero essere disponibili diversi indirizzi e-mail o numeri di telefono (indirizzo e-mail professionale, numero di telefono personale, ecc.).

Con [!DNL Journey Optimizer], puoi determinare quale indirizzo e-mail o numero di telefono utilizzare dal servizio profilo e assegnare la priorità quando sono disponibili più indirizzi. Per farlo, segui la procedura indicata di seguito.

1. Accedere a  **[!UICONTROL Canali]** > **[!UICONTROL Generale]** > **[!UICONTROL Campi Esecuzioni]** menu.

   ![](assets/primary-address-execution-fields.png)

1. In questa schermata vengono visualizzati i campi attualmente utilizzati per impostazione predefinita per determinare l’indirizzo e-mail e il numero di telefono dei profili. Clic **[!UICONTROL Modifica]** per cambiarle.

   ![](assets/primary-address.png)

1. Fai clic sul campo corrente desiderato o sull’icona di modifica per selezionare un nuovo campo.

   ![](assets/primary-address-edit.png)

1. Viene visualizzato l’elenco dei campi XDM di tipo e-mail disponibili. Seleziona il campo da utilizzare.

   ![](assets/primary-address-select-field.png)

1. Clic **[!UICONTROL Salva]** per confermare la scelta.

Il campo di esecuzione viene aggiornato e verrà ora utilizzato come indirizzo principale.

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
