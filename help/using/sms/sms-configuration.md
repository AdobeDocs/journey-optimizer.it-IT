---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il canale SMS
description: Scopri come configurare l’ambiente per l’invio di messaggi di testo con Journey Optimizer
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 7b1be144776fd11cd4aa90aa315eee60b1acc40f
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 41%

---

# Introduzione alla configurazione di SMS/MMS/RCS {#sms-configuration}

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
>abstract="Prima di inviare messaggi di testo (SMS/MMS), devi integrare le impostazioni del fornitore con Journey Optimizer. Al termine, sarà necessario creare una configurazione SMS/MMS. Questi passaggi devono essere eseguiti da un amministratore di sistema di Adobe Journey Optimizer."
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
   * [Infobip](sms-configuration-infobip.md)
   * [Sinch](sms-configuration-sinch.md)
   * [Twilio](sms-configuration-twilio.md)
   * [Provider personalizzato](sms-configuration-custom.md)
1. [Creare una configurazione SMS](sms-configuration-surface.md)

Questi passaggi devono essere eseguiti da un [amministratore di sistema](../start/path/administrator.md) di Adobe Journey Optimizer.

## Prerequisiti{#sms-prerequisites}

Adobe Journey Optimizer attualmente si integra con provider di terze parti che offrono servizi di messaggistica di testo indipendenti da Adobe Journey Optimizer. I provider supportati per i messaggi di testo e MMS sono: **Sinch**, **Twilio** e **Infobip**. È possibile configurare altri provider di messaggistica utilizzando la [configurazione provider personalizzata](sms-configuration-custom.md).

Prima di configurare il canale SMS, è necessario creare un account con uno di questi provider per ottenere il **token API** e l&#39;**ID servizio**, che è necessario configurare la connessione tra Adobe Journey Optimizer e il provider applicabile.

L’utilizzo dei servizi di messaggistica di testo e MMS è soggetto a termini e condizioni aggiuntivi da parte del provider applicabile. In qualità di soluzioni di terze parti, Sinch, Twilio e Infobip sono disponibili per gli utenti di Adobe Journey Optimizer tramite un’integrazione. Adobe non controlla e non è responsabile per i prodotti di terze parti. Per eventuali problemi o richieste di assistenza relativi ai servizi di messaggistica di testo (SMS/MMS), contatta il provider.

>[!CAUTION]
>
>Per accedere e modificare i sottodomini SMS, devi disporre dell&#39;autorizzazione **[!UICONTROL Gestione sottodomini SMS]** nella sandbox di produzione. Ulteriori informazioni sulle autorizzazioni in [questa pagina](../administration/high-low-permissions.md#administration-permissions).
>

