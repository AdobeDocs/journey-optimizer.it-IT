---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il canale SMS
description: Scopri come configurare l'ambiente per l'invio di messaggi di testo con Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: a08a28d7bfe912ff545ca559bd04b70642fe2ab5
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 37%

---

# Introduzione alla configurazione di SMS {#sms-configuration}

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

Prima di inviare SMS o MMS, è necessario configurare l&#39;ambiente Adobe Systems Journey Optimizer. Per effettuare ciò:

1. Integrare le impostazioni del provider con Journey Optimizer:
   * [Con gli Sinch](sms-configuration-sinch.md)
   * [Con Infobip](sms-configuration-infobip.md)
   * [Con Twilio](sms-configuration-twilio.md)
1. [Crea una superficie SMS](sms-configuration-surface.md)

Questi passaggi devono essere eseguiti da un amministratore](../start/path/administrator.md) di sistema di Adobe Systems Journey Optimizer[.

## Prerequisiti{#sms-prerequisites}

Adobe Systems Journey Optimizer attualmente si integra con fornitori di terze parti che offrono servizi SMS indipendenti da Adobe Systems Journey Optimizer. I provider supportati per SMS e MMS sono: **Sinch**, **Twilio** e **Infobip**.

Prima della configurazione del canale SMS, è necessario creare un account con uno di questi provider per ottenere il token **API e** l&#39;ID **** del servizio, necessari per configurare la connessione tra Adobe Systems Journey Optimizer e il provider applicabile.

L&#39;utilizzo dei servizi SMS e MMS è soggetto a termini e condizioni aggiuntivi da parte del fornitore applicabile. Come soluzioni di terze parti, Sinch, Twilio e Infobip sono disponibili per Adobe Systems utenti di Journey Optimizer tramite un&#39;integrazione. Adobe Systems non controlla e non è responsabile per i prodotti di terze parti. Per qualsiasi problema o richiesta di assistenza relativa ai servizi SMS (SMS/MMS), contatta il tuo provider.

>[!CAUTION]
>
>Per accesso e modificare i sottodomini SMS, devi disporre dell&#39;autorizzazione **[!UICONTROL Gestisci sottodomini]** SMS nella sandbox di produzione. Ulteriori informazioni sulle autorizzazioni sono disponibili in [questa pagina](../administration/high-low-permissions.md#administration-permissions)
>

