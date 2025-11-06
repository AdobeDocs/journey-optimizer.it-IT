---
solution: Journey Optimizer
product: journey optimizer
title: Generazione automatica delle varianti di contenuto (Beta)
description: Scopri come generare automaticamente le varianti di contenuto utilizzando la simulazione basata sull’intelligenza artificiale.
feature: Email, Email Rendering, Personalization, Preview, Proofs
topic: Content Management
role: User
level: Intermediate
badge: label="Beta privata" type="Informative"
hidefromtoc: true
hide: true
exl-id: 9b7fbd43-3d90-458b-8a2f-0bf0ac5437c3
source-git-commit: 45ebae048a748429a1918326526f3756a3e93c4c
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# Generazione automatica delle varianti di contenuto (Beta){#auto-generate-variants}

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata** e potrebbe non essere disponibile nel tuo ambiente. Per ottenere l’accesso, contatta il tuo rappresentante Adobe.

[!DNL Journey Optimizer] introduce una simulazione basata sull&#39;intelligenza artificiale che può generare automaticamente più varianti per testare il contenuto. Questa funzione riduce la necessità di creare manualmente le varianti, semplificando la convalida della logica di personalizzazione in modelli complessi.

Durante il rendering del contenuto per la simulazione o la verifica, il sistema analizza il contenuto e identifica tutti i token di personalizzazione e le regole di diramazione. Sostituisce i token di personalizzazione con valori significativi che forniscono un’anteprima quasi realistica del contenuto finale.

Considera un modello e-mail di Financial Services con logica di diramazione basata su **tipo investitore**, **gruppo di età**, **stato civile**, **verifica ID imposta** e **posizione**. Senza la generazione delle varianti, dovrai creare manualmente decine di varianti per convalidare tutti i percorsi. Con le varianti generate automaticamente, il sistema produce varianti rappresentative che coprono automaticamente queste condizioni.  Ogni variante generata viene sottoposta a rendering nel riquadro di anteprima, mostrando esattamente quali blocchi e condizioni vengono applicati.

## Genera varianti di contenuto

Per generare varianti per il contenuto e visualizzarle in anteprima, segui questi passaggi:

1. Apri il contenuto e seleziona **[!UICONTROL Simula contenuto]** / **[!UICONTROL Simula varianti di contenuto]**.

   ![](assets/simulate-sample.png)

2. Fare clic sul pulsante **[!UICONTROL Genera]**.

   ![](assets/simulate-generate-variant.png)

3. [!DNL Journey Optimizer] genera automaticamente varianti in base agli attributi rilevati.

4. Rivedi l’elenco delle varianti generate nel riquadro a sinistra e seleziona una variante per visualizzarne il rendering personalizzato nel riquadro di anteprima.

>[!NOTE]
>
>Questa funzionalità funziona come la funzione standard Simula varianti di contenuto. Per ulteriori informazioni sulle simulazioni delle varianti di contenuto e sui guardrail e le limitazioni associati, consulta questa sezione: [Simula varianti di contenuto](../test-approve/simulate-sample-input.md)
