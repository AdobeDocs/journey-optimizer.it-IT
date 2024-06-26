---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il canale SMS
description: Scopri come configurare l’ambiente per l’invio di messaggi di testo con Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: a08a28d7bfe912ff545ca559bd04b70642fe2ab5
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 37%

---

# Introduzione alle configurazione di SMS {#sms-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Configurare il provider di SMS con Journey Optimizer"
>abstract="Adobe Journey Optimizer invia messaggi di testo tramite fornitori di servizi SMS. Seleziona il provider e compila le credenziali API."

>[!CONTEXTUALHELP]
>id="ajo_admin_mms_api_header"
>title="Configurare il fornitore di MMS con Journey Optimizer"
>abstract="Adobe Journey Optimizer invia contenuti multimediali tramite fornitori di servizi MMS. Seleziona il provider e compila le credenziali API."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Configurare il fornitore di SMS/MMS con Journey Optimizer"
>abstract="Prima di inviare messaggi di testo (SMS/MMS), devi integrare le impostazioni del fornitore con Journey Optimizer. Al termine, dovrai creare una superficie SMS/MMS. Questi passaggi devono essere eseguiti da un amministratore di sistema di Adobe Journey Optimizer."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/sms/configure-sms/sms-configuration-surface" text="Creare una superficie del canale SMS"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Selezionare la configurazione del fornitore di SMS"
>abstract="Seleziona le credenziali API configurate per il fornitore di SMS."

Prima di inviare SMS o MMS, devi configurare il tuo ambiente Adobe Journey Optimizer. Per eseguire questa operazione:

1. Integra le impostazioni del provider con Journey Optimizer:
   * [Con Sinch](sms-configuration-sinch.md)
   * [Con Infobip](sms-configuration-infobip.md)
   * [Con Twilio](sms-configuration-twilio.md)
1. [Creare una superficie SMS](sms-configuration-surface.md)

Questi passaggi devono essere eseguiti da un Adobe Journey Optimizer [Amministratore di sistema](../start/path/administrator.md).

## Prerequisiti{#sms-prerequisites}

Adobe Journey Optimizer attualmente si integra con provider di terze parti che offrono servizi di messaggistica di testo indipendenti da Adobe Journey Optimizer. I provider supportati per messaggi di testo e MMS sono: **Sinch**, **Twilio** e **Infobip**.

Prima di configurare il canale SMS, è necessario creare un account con uno di questi provider per ottenere il **Token API** e **ID servizio**, che è necessario configurare la connessione tra Adobe Journey Optimizer e il provider applicabile.

L’utilizzo dei servizi di messaggistica di testo e MMS è soggetto a termini e condizioni aggiuntivi da parte del provider applicabile. In qualità di soluzioni di terze parti, Sinch, Twilio e Infobip sono disponibili per gli utenti di Adobe Journey Optimizer tramite un’integrazione. Adobe non controlla e non è responsabile per i prodotti di terze parti. Per eventuali problemi o richieste di assistenza relativi ai servizi di messaggistica di testo (SMS/MMS), contatta il provider.

>[!CAUTION]
>
>Per accedere e modificare i sottodomini SMS, devi disporre del **[!UICONTROL Gestire i sottodomini SMS]** autorizzazione per la sandbox di produzione. Ulteriori informazioni sulle autorizzazioni sono disponibili in [questa pagina](../administration/high-low-permissions.md#administration-permissions)
>

