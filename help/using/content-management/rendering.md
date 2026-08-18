---
title: Testare il rendering delle e-mail
description: Scopri come testare il rendering di e-mail e comprendere le limitazioni di rendering note tra client e ambienti e-mail.
feature: Preview
role: User
level: Beginner
exl-id: fe077a8b-9788-4723-a1e7-32816a879af9
feature_v2: []
subfeature_v2: id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
source-git-commit: ca053767a216de5f43415c94eb7dd24cffe9dff7
workflow-type: tm+mt
source-wordcount: 405
ht-degree: 9%

---

# Testare il rendering delle e-mail {#email-rendering}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come collegare il tuo account Litmus a Adobe Journey Optimizer per testare il rendering di e-mail tra i client e-mail più diffusi e comprendere le limitazioni di rendering note, inclusi gli ambienti di browser web per dispositivi mobili.

>[!ENDSHADEBOX]

Puoi sfruttare il tuo account **Litmus** in [!DNL Journey Optimizer] per visualizzare all&#39;istante l&#39;anteprima del **rendering di e-mail** nei client e-mail più diffusi. Puoi quindi verificare che il contenuto dell’e-mail si presenti e funzioni correttamente in ogni casella in entrata.

Per verificare il rendering di e-mail, effettua le seguenti operazioni:

1. Dalla schermata Modifica contenuto del messaggio o nel Designer e-mail, fai clic su **[!UICONTROL Simula contenuto]**, quindi seleziona **[!UICONTROL Simula contenuto (profili AEP)]** dal menu a discesa.

1. Seleziona il pulsante **[!UICONTROL Rendering dell’e-mail]**.

   ![](../email/assets/email-rendering-button.png)

1. Fai clic su **Connetti il tuo account Litmus** nella sezione superiore destra.

   ![](../email/assets/email-rendering-litmus.png)

1. Immetti le credenziali e accedi.

   ![](../email/assets/email-rendering-credentials.png)

1. Fai clic su **Esegui test** per generare anteprime e-mail.

1. Verifica il contenuto delle e-mail nei client desktop, mobili e basati su web più diffusi.

   ![](../email/assets/email-rendering-previews.png)

>[!CAUTION]
>
>Quando connetti il tuo account **Litmus** con [!DNL Journey Optimizer], accetti che i messaggi di prova vengano inviati a Litmus: una volta inviati, questi messaggi non vengono più gestiti da Adobe. Di conseguenza, i criteri di conservazione dei dati Litmus si applicano a queste e-mail, inclusi i dati di personalizzazione che possono essere inclusi in questi messaggi di test.

## Limitazioni del browser web mobile {#rendering-limitations}

Il rendering di e-mail può essere diverso quando i destinatari aprono Gmail o Outlook **tramite un browser Web mobile** (ad esempio, Chrome su un telefono), anziché utilizzare un&#39;app mobile nativa o un client desktop. Si tratta di una limitazione nota degli ambienti di posta sul web mobile e non è specifica di Journey Optimizer.

Questa differenza di rendering deriva dal comportamento dei client di posta sul web all’interno di un browser mobile. Il browser esegue prima il rendering dell’interfaccia utente completa della posta sul desktop, posizionando l’e-mail a due livelli di profondità, oltre la portata di qualsiasi query CSS o multimediale responsive. Gmail Web inoltre elimina i blocchi CSS `<style>` e racchiude il contenuto delle e-mail nel proprio `<div>`, che può sovrascrivere gli stili e creare conflitti di allineamento.

I sintomi tipici includono lo spostamento dell’allineamento del testo (il testo allineato a sinistra appare centrato), linee di separazione bianche supplementari tra le sezioni di contenuto e un layout complessivo diverso dalla struttura del modello.

Questi problemi si verificano solo in Gmail Web e Outlook Web quando si accede tramite un browser mobile. Outlook e le app native per dispositivi mobili Gmail, così come tutti i client desktop, non subiscono modifiche.

>[!TIP]
>
>Per ridurre al minimo l&#39;impatto:
>
>* Utilizza layout semplici basati su tabelle con CSS completamente allineato.
>
>* Evita di fare affidamento su query multimediali o blocchi `<style>` per proprietà di layout critiche come l&#39;allineamento del testo.
