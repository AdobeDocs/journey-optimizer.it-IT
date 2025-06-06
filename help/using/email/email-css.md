---
solution: Journey Optimizer
product: journey optimizer
title: Aggiungere CSS personalizzato al contenuto dell’e-mail
description: Scopri come aggiungere CSS personalizzato al contenuto delle e-mail direttamente nel Designer e-mail in Journey Optimizer
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: css, editor, riepilogo, e-mail
source-git-commit: feb3576c230f2fb28ab031f87cc5f99263329b57
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 3%

---

# Aggiungere metadati al contenuto dell’e-mail {#email-metadata}

>[!CONTEXTUALHELP]
>id="ac_edition_css"
>title="Aggiungi CSS personalizzato"
>abstract="xxx."

Durante la progettazione delle e-mail, puoi aggiungere CSS personalizzati direttamente all&#39;interno di [!DNL Journey Optimizer] [E-mail Designer](get-started-email-design.md).

Nell’area di testo Aggiungi CSS personalizzato è prevista una stringa CSS valida.

![](assets/email-body-css.png)

Condizioni di disponibilità

La funzione Aggiungi CSS personalizzato è disponibile solo quando nell’editor è definito un contenuto. Per visualizzare la sezione Aggiungi CSS personalizzato, l’utente deve aggiungere contenuto nell’editor. Se l’utente rimuove tutto il contenuto, la sezione scompare e il css personalizzato non viene applicato. Se l’utente torna a aggiungere contenuti, la sezione sarà disponibile e verrà applicato il css personalizzato.

**Esempi di input CSS non validi**

Impossibile salvare un file CSS non valido. Se il file CSS non è valido, verrà visualizzato un avviso popup rosso per indicare che il file CSS non può essere salvato.

`<style>` non è accettato


```
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


parentesi graffa mancante non valida

```
body {
 background: red; 
```
