---
solution: Journey Optimizer
product: journey optimizer
title: Azioni di audit sulle risorse di Journey Optimizer
description: Scopri come tenere traccia delle azioni eseguite sulle risorse Journey Optimizer.
feature: Monitoring
role: User
level: Intermediate
exl-id: 759b014a-c834-4331-bffd-5bc159ec555d
source-git-commit: 78675ca22d8ee9a93d9af128d5708c305523da78
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 89%

---

# Azioni di audit sulle risorse di Journey Optimizer {#track-changes}

## Informazioni sui registri di audit {#audit-logs}

>[!IMPORTANT]
>
>Per visualizzare ed esportare il registro di controllo, è necessario disporre della **[!DNL View User Activity Log]** permesso concesso. [Ulteriori informazioni](../administration/ootb-product-profiles.md)

Con Journey Optimizer puoi identificare le azioni eseguite dagli utenti nel sistema su vari servizi e funzionalità come percorsi, messaggi, pagine di destinazione, ecc.

Questo consente di aumentare la visibilità delle attività eseguite nel sistema, risolvere i problemi e aiutare la tua azienda a rispettare le normative e le politiche aziendali di gestione dei dati.

Ogni azione viene registrata con i metadati nei “registri di audit”, accessibili in Adobe Experience Platform. Per ulteriori informazioni sui registri di controllo, tra cui come visualizzarli e gestirli nell’interfaccia utente o nell’API, consulta [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html?lang=it).

![](assets/audit-logs.png)

## Tipi di eventi acquisiti dai registri di audit {#events}

La tabella seguente presenta le azioni che vengono riportate nei registri di audit per le diverse risorse Journey Optimizer.

>[!NOTE]
>
>L’elenco completo delle azioni riportate nei registri di audit è disponibile nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html?lang=it#category).

| Risorsa | Azione |
|-----------|------------------|
| Campagna AJO | Crea / Elimina / Aggiorna / Attiva / Interrompi |
| Impostazione generale del canale AJO | Crea/Elimina/Aggiorna |
| Pool IP AJO | Crea/Elimina/Aggiorna |
| Pagina di destinazione AJO | Crea/Elimina/Aggiorna/Pubblica/Annulla pubblicazione |
| Modello HTML della pagina di destinazione AJO | Crea/Elimina/Aggiorna |
| Predefinito pagina di destinazione AJO | Crea/Elimina/Aggiorna |
| Sottodominio della pagina di destinazione AJO | Crea/Elimina/Aggiorna |
| Messaggio AJO | Crea/Elimina/Aggiorna/Pubblica |
| Predefinito messaggio AJO | Crea/Elimina/Aggiorna |
| Record PTR AJO | Crea/Elimina/Aggiorna |
| Modello di espressione salvata AJO | Crea/Elimina/Aggiorna |
| Credenziali API SMS AJO | Crea/Elimina/Aggiorna |
| Sottodominio AJO | Crea/Elimina/Aggiorna |
| Elenco di soppressione AJO | Crea/Elimina/Scarica CSV |
| Gruppo di campi | Crea/Elimina/Aggiorna |
| Percorso | Crea/Elimina/Aggiorna/Arresta/Pubblica |
| Azione personalizzata percorso | Crea/Elimina/Aggiorna |
| Origine dati percorso | Crea/Elimina/Aggiorna |
| Evento percorso | Crea/Elimina/Aggiorna |
| Regola di frequenza dei messaggi | Crea/Elimina/Aggiorna |
| Strategia di classificazione | Crea/Elimina/Aggiorna |
