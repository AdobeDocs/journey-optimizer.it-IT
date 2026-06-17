---
solution: Journey Optimizer
product: journey optimizer
title: Azioni di audit sulle risorse di Journey Optimizer
description: Scopri come tenere traccia delle azioni eseguite sulle risorse Journey Optimizer.
feature: Monitoring
role: User
level: Intermediate
exl-id: 759b014a-c834-4331-bffd-5bc159ec555d
TQID: https://experienceleague.adobe.com/Usk3qin9P4IZlKw-gEI4zaKO-aRtaKq9-0GMVlOecjA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2:
  - id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56
  - id: f365ec33-2b99-4b7f-b4ee-c743dd7f615f
  - id: c8d5f2ce-ba44-43e9-a2bf-94a3d7d85ec3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 4e89993a998268ae2810c949d0669bf6dc458dd6
workflow-type: tm+mt
source-wordcount: 380
ht-degree: 90%

---

# Azioni di audit sulle risorse di Journey Optimizer {#track-changes}

>[!BEGINSHADEBOX]

**In questa pagina:** esamina i registri di controllo che registrano le azioni degli utenti sulle risorse Journey Optimizer, in modo da aumentare la visibilità, risolvere i problemi e dimostrare la conformità alle normative e ai criteri di gestione dei dati.

>[!ENDSHADEBOX]

## Informazioni sui registri di controllo {#audit-logs}

>[!IMPORTANT]
>
>Per visualizzare ed esportare il registro di controllo, è necessario disporre dell’autorizzazione **[!DNL View User Activity Log]**. [Ulteriori informazioni](../administration/ootb-product-profiles.md)

Con Journey Optimizer puoi identificare le azioni eseguite dagli utenti nel sistema su vari servizi e funzionalità come percorsi, messaggi, pagine di destinazione, ecc.

Questo consente di aumentare la visibilità delle attività eseguite nel sistema, risolvere i problemi e aiutare la tua azienda a rispettare le normative e le politiche aziendali di gestione dei dati.

Ogni azione viene registrata con i metadati nei “registri di controllo”, accessibili in Adobe Experience Platform. Per ulteriori informazioni sui registri di controllo, tra cui come visualizzarli e gestirli nell’interfaccia utente o nell’API, consulta la [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html?lang=it).

![](assets/audit-logs.png)

## Tipi di eventi acquisiti dai registri di controllo {#events}

La tabella seguente presenta le azioni che vengono riportate nei registri di controllo per le diverse risorse Journey Optimizer. L’elenco completo delle azioni riportate nei registri di controllo è disponibile nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html?lang=it#category).

>[!NOTE]
>
>I registri di controllo relativi alla **gestione delle decisioni** sono visibili solo dal file CSV scaricabile tramite il pulsante **[!UICONTROL Scarica registro]**.

| Risorsa | Azione |
|-----------|------------------|
| Campagna AJO | Crea / Elimina / Aggiorna / Attiva / Interrompi |
| Impostazione generale del canale AJO | Crea/Elimina/Aggiorna |
| Pool IP AJO | Crea/Elimina/Aggiorna |
| Pagina di destinazione AJO | Crea/Elimina/Aggiorna/Pubblica/Annulla pubblicazione |
| Modello HTML della pagina di destinazione AJO | Crea/Elimina/Aggiorna |
| Predefinito pagina di destinazione AJO | Crea/Elimina/Aggiorna |
| Sottodominio della pagina di destinazione AJO | Crea/Elimina/Aggiorna |
| Predefinito messaggio AJO | Crea/Elimina/Aggiorna |
| Record PTR AJO | Crea/Elimina/Aggiorna |
| Modello di espressione salvata AJO | Crea/Elimina/Aggiorna |
| Credenziali API SMS AJO | Crea/Elimina/Aggiorna |
| Sottodominio AJO | Crea/Elimina/Aggiorna |
| Elenco di soppressione AJO | Crea/Elimina/Scarica CSV |
| Gruppo di campi | Crea/Elimina/Aggiorna |
| Percorso | Crea/Elimina/Aggiorna/Interrompi/Pubblica |
| Azione personalizzata percorso | Crea/Elimina/Aggiorna |
| Origine dati percorso | Crea/Elimina/Aggiorna |
| Evento percorso | Crea/Elimina/Aggiorna |
| Frammento di percorso | Crea/Elimina/Aggiorna/Attiva/Archivia |
| Regola di frequenza dei messaggi | Crea/Elimina/Aggiorna |
| Strategia di classificazione | Crea/Elimina/Aggiorna |
