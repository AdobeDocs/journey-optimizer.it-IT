---
solution: Journey Optimizer
product: Journey Optimizer
title: Delegare i sottodomini e-mail
description: Delegare i sottodomini e-mail
redpen-status: CREATED_||_2025-08-11_21-07-51
exl-id: 7df9b8e2-136a-4ffc-9243-53c7be026d81
source-git-commit: bb50d06e86f9399dfd295b8091aa637abcaea4a8
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 41%

---

# Delegare i sottodomini e-mail{#section-overview}

La delega dei sottodomini e-mail è un passaggio fondamentale della [configurazione del canale](../using/configuration/get-started-configuration.md), necessaria prima che tu possa inviare e-mail da Journey Optimizer. I sottodomini consentono di isolare i tipi di traffico (ad esempio marketing e transazioni), proteggere la reputazione del dominio principale e velocizzare il [riscaldamento dell&#39;IP](../using/configuration/ip-warmup-gs.md). Lavorano insieme alla [configurazione del canale e-mail](../using/email/get-started-email-config.md) e al [monitoraggio del recapito messaggi](../using/reports/deliverability.md) per garantire che i messaggi raggiungano le caselle in entrata.

Puoi scegliere tra diversi metodi di installazione: **delega completa** (Adobe gestisce DNS), **configurazione CNAME** o **delega personalizzata** (possiedi certificati e DNS). Se inizi con CNAME, in seguito potrai [migrare alla delega personalizzata](../using/configuration/custom-subdomain-migration.md) per una sicurezza più severa. Questa sezione tratta anche i record DMARC e PTR, i record TXT di Google per Gmail e i pool IP. Per indicazioni più ampie sul recapito messaggi, vedere [Introduzione al recapito messaggi](../using/reports/deliverability.md) e [Monitorare gli indirizzi e-mail](monitor-reputation-landing-page.md).

## Delegare i sottodomini e-mail

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=it)

Introduzione alla delega dei sottodomini

Scopri i vantaggi, i metodi di configurazione e le considerazioni per la delega dei sottodomini in Adobe Journey Optimizer.

[Inizia la delega dei sottodomini](../using/configuration/about-subdomain-delegation.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=it)

Delegare un sottodominio

Linee guida dettagliate per la delega dei sottodomini ad Adobe, inclusa la delega completa e la configurazione del CNAME.

[Scopri come delegare](../using/configuration/delegate-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/screwdriver-wrench.svg?lang=it)

Configurare un sottodominio personalizzato

Assumi la piena proprietà dei sottodomini con delega personalizzata: carica i tuoi certificati SSL e mantieni il controllo completo sulla configurazione del dominio.

[Configurare un sottodominio personalizzato](../using/configuration/delegate-custom-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=it)

Migrare da CNAME a Delega personalizzata

Esegui la migrazione dei sottodomini configurati da CNAME esistenti alla delega personalizzata per soddisfare i criteri di sicurezza e ottenere il controllo completo sui certificati.

[Migrare il sottodominio](../using/configuration/custom-subdomain-migration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=it)

Configurare i record DMARC

Configura i record DMARC per migliorare la sicurezza e la recapitabilità delle e-mail per i sottodomini delegati.

[Configura DMARC ora](../using/configuration/dmarc-record.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=it)

Aggiungere un record TXT di Google

Verifica i sottodomini per la recapitabilità relativa a Gmail aggiungendo record TXT di Google in Adobe Journey Optimizer.

[Aggiungi record TXT di Google](../using/configuration/google-txt.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=it)

Accedere ai record PTR e modificarli

Gestisci i record PTR per i sottodomini delegati, incluse le informazioni sulla modifica e sugli stati di aggiornamento.

[Modifica record PTR](../using/configuration/ptr-records.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=it)

Creare i pool IP

Raggruppa gli indirizzi IP per migliorare la recapitabilità delle e-mail e gestire in modo efficace la reputazione del sottodominio.

[Creare i pool IP](../using/configuration/ip-pools.md)
:::

::::

## Risorse aggiuntive

- **[Configurare i sottodomini della pagina di destinazione](../using/landing-pages/lp-subdomains.md)** - Configurare i sottodomini per le pagine di destinazione e i moduli di abbonamento.
- **[Configura sottodomini Web](../using/web/web-delegated-subdomains.md)** - Delega sottodomini per esperienze Web e monitoraggio.
- **[Introduzione alla configurazione dei canali](../using/configuration/get-started-configuration.md)** - Panoramica di tutti i passaggi di configurazione dei canali, inclusa la delega dei sottodomini.
