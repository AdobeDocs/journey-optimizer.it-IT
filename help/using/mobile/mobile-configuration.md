---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il canale SMS
description: Scopri come configurare l’ambiente per l’invio di messaggi mobili con Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
TQID: https://experienceleague.adobe.com/dO8HoRdGLuYVFN2YVjRCiFJQHmWHApROU8qz2-hKmTs
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: e30b0a1a-b594-47b8-af94-1e3a2be6df11id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 432
ht-degree: 30%

---

# Introduzione alla configurazione per dispositivi mobili {#sms-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="Configurare il provider di SMS con Journey Optimizer"
>abstract="Adobe Journey Optimizer invia messaggi mobili tramite i provider di servizi SMS. Seleziona il provider e compila le credenziali API."

>[!CONTEXTUALHELP]
>id="ajo_admin_mms_api_header"
>title="Configurare il fornitore di MMS con Journey Optimizer"
>abstract="Adobe Journey Optimizer invia contenuti multimediali tramite fornitori di servizi MMS. Seleziona il provider e compila le credenziali API."

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="Configurare il provider SMS/RCS/MMS con Journey Optimizer"
>abstract="Prima di inviare messaggi mobili (SMS/RCS/MMS), è necessario integrare le impostazioni del provider con Journey Optimizer. Al termine, devi creare una configurazione SMS/RCS/MMS. Questi passaggi devono essere eseguiti da un amministratore di sistema di Adobe Journey Optimizer."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/channels/sms/configure-sms/sms-configuration-surface" text="Crea una configurazione del canale SMS"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="Selezionare la configurazione del fornitore di SMS"
>abstract="Seleziona le credenziali API configurate per il fornitore di SMS."

>[!CONTEXTUALHELP]
>id="ajo_admin_fuzzy_opt_out"
>title="Rinuncia parziale"
>abstract="Quando l’opzione Rinuncia parziale è abilitata, rileva i messaggi in entrata che sono molto simili alle parole chiave definite per la rinuncia (ad esempio, CANCIL) e invia automaticamente una risposta con richiesta di conferma per verificare l’intento dell’utente di annullare l’iscrizione. Se l’utente conferma tramite il prompt definito, l’iscrizione viene annullata."

Prima di inviare SMS, MMS o RCS, devi configurare il tuo ambiente Adobe Journey Optimizer. Per eseguire questa operazione:

1. Integra le impostazioni del provider con Journey Optimizer.
I passaggi dipendono dal provider SMS. Sfoglia i collegamenti riportati di seguito per accedere alla documentazione dettagliata:
   * [Infobip](mobile-configuration-infobip.md)
   * [Sinch](mobile-configuration-sinch.md)
   * [Twilio](mobile-configuration-twilio.md)
   * [Provider personalizzato](mobile-configuration-custom.md)
1. [Creare webhook](mobile-webhook.md)
1. [Creare una configurazione per dispositivi mobili](mobile-configuration-surface.md)

Questi passaggi devono essere eseguiti da un [amministratore di sistema](../start/path/administrator.md) di Adobe Journey Optimizer.

## Prerequisiti{#sms-prerequisites}

Adobe Journey Optimizer attualmente si integra con provider di terze parti che offrono servizi di messaggistica mobile indipendenti da Adobe Journey Optimizer. I provider supportati per Mobile Messaging e MMS sono: **Sinch**, **Twilio** e **Infobip**. È possibile configurare altri provider di messaggistica utilizzando la [configurazione provider personalizzata](mobile-configuration-custom.md).

Prima di configurare il canale mobile, è necessario creare un account con uno di questi provider per ottenere il **token API** e l&#39;**ID servizio**, che è necessario configurare per la connessione tra Adobe Journey Optimizer e il provider applicabile.

L’utilizzo dei servizi di messaggistica mobile e MMS è soggetto a termini e condizioni aggiuntivi da parte del provider applicabile. In qualità di soluzioni di terze parti, Sinch, Twilio e Infobip sono disponibili per gli utenti di Adobe Journey Optimizer tramite un’integrazione. Adobe non controlla e non è responsabile per i prodotti di terze parti. Per qualsiasi problema o richiesta di assistenza relativa ai servizi di messaggistica mobile, contatta il provider di servizi.

>[!CAUTION]
>
>Per accedere e modificare i sottodomini SMS, devi disporre dell&#39;autorizzazione **[!UICONTROL Gestione sottodomini SMS]** nella sandbox di produzione. Ulteriori informazioni sulle autorizzazioni in [questa pagina](../administration/high-low-permissions.md#administration-permissions).
>

