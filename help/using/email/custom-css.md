---
solution: Journey Optimizer
product: journey optimizer
title: Aggiungere un CSS personalizzato al contenuto dell’e-mail
description: Scopri come aggiungere CSS personalizzato al contenuto delle e-mail direttamente nel Designer e-mail in Journey Optimizer
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: css, editor, riepilogo, e-mail
exl-id: e4645bc7-fb99-4fcc-8d0e-bf8b9efc828e
source-git-commit: 5593758448216efcc82971b1072b7fc8c9303572
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 7%

---

# Aggiungere un CSS personalizzato al contenuto dell’e-mail {#email-metadata}

>[!CONTEXTUALHELP]
>id="ac_edition_css"
>title="Inserire il proprio CSS"
>abstract="Per una maggiore flessibilità e controllo sull’aspetto del contenuto, puoi aggiungere un CSS personalizzato direttamente nell’E-mail designer per applicare uno stile avanzato e specifico."

Durante la progettazione delle e-mail, puoi aggiungere CSS personalizzati direttamente all&#39;interno di [!DNL Journey Optimizer] [E-mail Designer](get-started-email-design.md). Questa funzionalità consente di applicare uno stile avanzato e specifico, per una maggiore flessibilità e un maggiore controllo sull’aspetto del contenuto.

## Definire CSS personalizzato {#define-custom-css}

Per aggiungere CSS personalizzati al contenuto delle e-mail, segui i passaggi indicati di seguito.

1. Assicurati che nel Designer e-mail siano definiti alcuni contenuti aggiungendo almeno un [componente](content-components.md).

1. Seleziona **[!UICONTROL Corpo]** dalla **[!UICONTROL Struttura di navigazione]** a sinistra o nella parte superiore del riquadro di destra. La sezione **[!UICONTROL Stili CSS]** viene visualizzata a destra.

   ![Seleziona il pulsante Aggiungi CSS personalizzato](assets/email-body-css-styles.png){width="85%"}

   >[!NOTE]
   >
   >La sezione **[!UICONTROL Stili CSS]** è disponibile solo se il contenuto è già presente nell&#39;editor.

1. Fai clic sul pulsante **[!UICONTROL Aggiungi CSS personalizzato]**.

   >[!NOTE]
   >
   >Il pulsante **[!UICONTROL Aggiungi CSS personalizzato]** è disponibile solo quando è selezionato **[!UICONTROL Corpo]**. Tuttavia, puoi applicare stili CSS personalizzati a tutti i componenti all’interno del contenuto.

1. Inserisci il codice CSS nell’area di testo dedicata visualizzata. Assicurati che il CSS personalizzato sia valido e che segua la sintassi corretta. [Ulteriori informazioni](#use-valid-css)

   ![Inserisci CSS personalizzato nell&#39;area di testo dedicata](assets/email-body-custom-css.png){width="65%"}

   >[!NOTE]
   >
   >Quando si utilizza un [modello con contenuto bloccato](../content-management/content-locking.md#use), non è possibile aggiungere CSS personalizzato al contenuto. L&#39;etichetta del pulsante diventa **[!UICONTROL Visualizza CSS personalizzato]** ed eventuali CSS personalizzati già presenti nel contenuto sono di sola lettura.

1. Salva il CSS personalizzato e verifica che il CSS personalizzato sia applicato correttamente al contenuto. In caso contrario, controllare la sezione [Risoluzione dei problemi](#troubleshooting).

   ![Seleziona il pulsante Aggiungi CSS personalizzato](assets/email-body-custom-css-applied.png){width="85%"}

1. Se rimuovi tutto il contenuto, la sezione scompare e non viene più applicato il CSS personalizzato definito in precedenza.

1. Aggiungi nuovamente il contenuto all&#39;editor per visualizzare nuovamente la sezione **[!UICONTROL Stili CSS]**. Il CSS personalizzato viene applicato nuovamente.

## Assicurati di utilizzare CSS valido {#use-valid-css}

È possibile immettere qualsiasi stringa CSS valida nell&#39;area di testo **[!UICONTROL Aggiungi CSS personalizzato]**. I file CSS formattati correttamente vengono applicati immediatamente al contenuto.

>[!CAUTION]
>
>Gli utenti sono responsabili della sicurezza dei CSS personalizzati. Assicurati che il CSS non introduca vulnerabilità o conflitti con il contenuto esistente.
>
>Evita l’utilizzo di CSS che potrebbero interrompere involontariamente il layout o la funzionalità del contenuto.

+++ Esempi di CSS

Di seguito sono riportati alcuni esempi di CSS validi.

```css
.acr-component[data-component-id="form"] {
  display: flex;
  justify-content: center;
  background: none;
}

.acr-Form {
  width: 100%;
  padding: 20px 100px;
  border-spacing: 0px 8px;
  box-sizing: border-box;
  margin: 0;
}

.acr-Form .spectrum-FieldLabel {
  width: 20%;
}

.acr-Form.spectrum-Form--labelsAbove .spectrum-FieldLabel,
.acr-Form [data-form-item="checkbox"] .spectrum-FieldLabel {
  width: auto;
}

.acr-Form .spectrum-Textfield {
  width: 100%;
}

#acr-form-error,
#acr-form-confirmation {
  width: 100%;
  padding: var(--spectrum-global-dimension-static-size-500);
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  gap: var(--spectrum-global-dimension-static-size-200);
}

.spectrum-Form-item.is-required .spectrum-FieldLabel:after{
  content: '*';
  font-size: 1.25rem;
  margin-left: 5px;
  position: absolute;
}

/* Error field placeholder */
.spectrum-HelpText {
  display: none !important;
}

.spectrum-HelpText.is-invalid,
.is-invalid ~ .spectrum-HelpText {
  display: flex !important;
}
```

```css
@media only screen and (min-width: 600px) {
  .acr-paragraph-1 {
    width: 100% !important;
  }
}
```

+++


+++ Esempi di CSS non valido

Se viene immesso un CSS non valido, viene visualizzato un messaggio di errore che indica che il CSS non può essere salvato. Di seguito sono riportati alcuni esempi di file CSS non validi.

L&#39;utilizzo di `<style>` tag non è accettato:

```html
<style type="text/css">
  .acr-Form {
    width: 100%;
    padding: 20px 100px;
    border-spacing: 0px 8px;
    box-sizing: border-box;
    margin: 0;
  }
</style>
```

Sintassi non valida, ad esempio parentesi graffe mancanti, non accettata:

```css
body {
  background: red;
```

+++

## Implementazione tecnica {#implementation}

Il file CSS personalizzato viene aggiunto alla fine della sezione `<head>` come parte di un tag `<style>` con l&#39;attributo `data-name="global-custom"`, come nell&#39;esempio seguente. In questo modo gli stili personalizzati vengono applicati globalmente al contenuto.

+++ Vedi esempio

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <meta name="content-version" content="3.3.31">
    <meta name="x-apple-disable-message-reformatting">
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    <style data-name="default" type="text/css">
      td { padding: 0; }
      th { font-weight: normal; }
    </style>
    <style data-name="grid" type="text/css">
      .acr-grid-table { width: 100%; }
    </style>
    <style data-name="acr-theme" type="text/css" data-theme="default" data-variant="0">
      body { margin: 0; font-family: Arial; }
    </style>
    <style data-name="media-default-max-width-500px" type="text/css">
      @media screen and (max-width: 500px) {
        body { width: 100% !important; }
      }
    </style>
    <style data-name="global-custom" type="text/css">
      /* Add you custom CSS here */
    </style>
  </head>
  <body>
    <!-- Minimal content -->
  </body>
</html>
```

+++


Il file CSS personalizzato non viene interpretato o convalidato dal riquadro **[!UICONTROL Impostazioni]** di E-mail Designer. È completamente indipendente e può essere modificata solo tramite l&#39;opzione **[!UICONTROL Aggiungi CSS personalizzato]**.

### Guardrail - Contenuto importato

Se desideri utilizzare CSS personalizzati con il contenuto importato nel Designer e-mail, considera quanto segue:

* Se si importa contenuto HTML esterno, inclusi i file CSS, a meno che non si converta tale contenuto, verrà attivata la **[!UICONTROL modalità di compatibilità]**, in cui la sezione **[!UICONTROL Stili CSS]** non è disponibile. [Ulteriori informazioni sull&#39;importazione di contenuto esistente](existing-content.md)

* Se si importa contenuto creato con il Designer e-mail, inclusi i CSS applicati tramite l&#39;opzione **[!UICONTROL Aggiungi CSS personalizzato]**, i CSS applicati in precedenza saranno visibili e modificabili dalla stessa opzione.

<!--
* If importing content created with the Email Designer with CSS applied externally, the CSS code previously applied cannot be accessed within the **[!UICONTROL Add custom CSS]** pop-up window, but you can still override it with new custom CSS.-->

## Risoluzione dei problemi {#troubleshooting}

Se il CSS personalizzato non è applicato, considera le opzioni seguenti.

* Assicurati che il CSS sia valido e privo di errori di sintassi (ad esempio parentesi graffe mancanti, nomi di proprietà errati). [Scopri come](#use-valid-css)

* Verifica che il tuo CSS sia stato aggiunto al tag `<style>` con l&#39;attributo `data-name="global-custom"`.

* Verificare se l&#39;attributo `global-custom` del tag di stile `data-disabled` è impostato su `true`. In questo caso, il CSS personalizzato non viene applicato.

+++ Ad esempio:

  ```html
  <style data-name="global-custom" type="text/css" data-disabled="true"> body: { color: red; } </style>
  ```

+++

* Assicurati che il tuo CSS non sia sovrascritto da altre regole CSS, incluso qualsiasi [tema](apply-email-themes.md) applicato al contenuto.

   * Utilizza gli strumenti di sviluppo del browser per esaminare il contenuto e verificare che i CSS stiano eseguendo il targeting dei selettori corretti.

   * Prendi in considerazione l&#39;aggiunta di `!important` alle tue dichiarazioni per assicurarti che abbiano la precedenza.

+++ Ad esempio:

     ```css
     .acr-Form {
       background: red !important;
     }
     ```

+++
