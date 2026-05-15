---
solution: Journey Optimizer
product: journey optimizer
title: Gestione dei tag nei percorsi
description: Gestione dei tag nei percorsi
feature: Journeys, Tags
topic: Content Management
role: User
level: Intermediate
keywords: percorso, tag
exl-id: 44c255d1-121c-47d4-b407-161626ca3cb4
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/O8Igbj-JJGr0aej8xbSvZ51xkcJq8LeJ9JiveyBjBqQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
  - id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 642
ht-degree: 14%

---

# Gestione dei tag nei percorsi {#journey_tags}

In qualità di utente Journey Optimizer, puoi organizzare i percorsi utilizzando i tag. I tag rappresentano un modo rapido e semplice di classificare gli oggetti per migliorare la ricerca.

## Tag e convenzioni di denominazione {#tags-vs-naming}

I team si basano spesso su convenzioni di denominazione complesse per memorizzare i metadati direttamente nei nomi dei percorsi, ad esempio: *Marketing del ciclo di vita - Istruzione - Onboarding dei clienti V2 - Istruzione delle app - T3 2025*. Anche se ben intenzionato, questo approccio presenta una debolezza chiave: con il lavoro che si estende tra i membri del gruppo, la convenzione viene raramente applicata in modo coerente e gli elenchi dei percorsi diventano difficili da navigare.

**Le categorie di tag** in Journey Optimizer offrono un&#39;alternativa migliore. Invece di codificare i metadati nel nome, alleghi tag categorizzati a ciascun percorso (ad esempio team, finalità, fase, trimestre) e utilizza i filtri per individuarli. I nomi dei percorsi possono quindi concentrarsi su ciò che conta realmente: la tappa del cliente.

Vantaggi delle categorie di tag rispetto alle convenzioni di denominazione:

* **Coerenza**: i tag sono selezionati da un elenco controllato, non vengono digitati liberamente.
* **Filtrabilità**: è possibile utilizzare qualsiasi combinazione di valori di tag per suddividere immediatamente l&#39;elenco dei percorsi.
* **Chiarezza**: i nomi dei percorsi rimangono brevi e incentrati sulle milestone.
* **Scalabilità**: l&#39;aggiunta di una nuova dimensione di metadati implica la creazione di una nuova categoria di tag, senza la riscrittura di una convenzione di denominazione.

Per un flusso di lavoro di configurazione consigliato, vedere [Configurare le categorie di tag per la gestione dei percorsi](#tags-setup) di seguito.

## Aggiungere tag a un percorso

Il campo **Tag**, nelle proprietà del percorso, consente di definire i tag per il percorso. Puoi selezionare un tag esistente o crearne uno nuovo. Inizia a digitare il nome del tag desiderato e selezionalo dall’elenco. Se non è disponibile, fai clic su **Crea** per crearne uno nuovo e aggiungerlo al percorso. Puoi definire tutti i tag necessari.

![Pannello Tag nelle proprietà del percorso per la categorizzazione e l&#39;organizzazione](assets/tags1.png)

L’elenco dei tag definiti viene visualizzato sotto il campo **Tag**.

>[!NOTE]
>
> I tag non distinguono l’uso di maiuscole e minuscole
> 
> Se si duplica o si crea una nuova versione di un percorso, i tag vengono mantenuti.

## Filtrare i tag

L’elenco Percorso presenta una colonna dedicata che consente di visualizzare facilmente i tag.

È inoltre disponibile un filtro per visualizzare solo i percorsi con determinati tag.

![Elenco a discesa dei tag selezionati con i tag disponibili per la classificazione di percorso](assets/tags2.png)

Puoi aggiungere o rimuovere tag da qualsiasi tipo di percorso (live, draft, ecc.). Fai clic sull&#39;icona **Altre azioni** accanto al percorso e seleziona **Modifica tag**.

![Elenco Percorsi filtrato per tag che mostrano percorsi categorizzati](assets/tags3.png)

## Gestire i tag

Gli amministratori possono eliminare i tag e organizzarli per categorie utilizzando il menu **Tag**, sotto **AMMINISTRAZIONE**. Consulta questa [documentazione](https://experienceleague.adobe.com/docs/experience-platform/administrative-tags/overview.html?lang=it).

>[!NOTE]
>
> I tag definiti in percorsi vengono aggiunti alla categoria &quot;Non categorizzato&quot; incorporata.

## Impostare categorie di tag per la gestione dei percorsi {#tags-setup}

Segui questi passaggi per sostituire una convenzione di denominazione complessa con un approccio basato su tag all’interno del team.

**Passaggio 1 — Creare categorie di tag (amministratore)**

In **[!UICONTROL Amministrazione]** > **[!UICONTROL Tag]**, crea una categoria per ogni attributo di metadati attualmente codificato dal team nei nomi dei percorsi, ad esempio: *Team*, *Obiettivo di marketing*, *Campagna*, *Fase*, *Trimestre*.

**Passaggio 2 — Popola ogni categoria con i valori dei tag (Admin)**

All’interno di ogni categoria, crea i tag che rappresentano tutti i valori possibili. Ad esempio, la categoria *Fase* potrebbe contenere: *Informazioni*, *Onboarding*, *Conservazione*, *Riconoscimento*.

**Passaggio 3: applicare i tag durante la creazione di percorsi (professionisti)**

Ogni volta che viene creato un nuovo percorso, selezionare il tag appropriato da ogni categoria nelle proprietà del percorso. In genere, un percorso ha un tag per categoria.

**Passaggio 4 — Assegnare un nome ai percorsi per l&#39;attività cardine, filtrare in base ai tag**

Mantieni il nome del percorso incentrato sulla milestone del cliente che gestisce (ad esempio *Prima transazione fedeltà*). Utilizzare i filtri tag nell&#39;elenco percorso per individuare i percorsi in base a qualsiasi combinazione di metadati, senza fare affidamento sull&#39;analisi del nome.

>[!TIP]
>
>Per una discussione più ampia su questo approccio e sui relativi vantaggi su larga scala, consulta [Best practice per percorsi avanzati in Journey Optimizer](https://experienceleague.adobe.com/it/perspectives/best-practices-for-advanced-journeys-in-journey-optimizer){target="_blank"}.
