---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione a Generare contenuti in Journey Optimizer
description: Scopri come accedere e lavorare con Generare contenuti in Journey Optimizer
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 1
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
TQID: https://experienceleague.adobe.com/lACM3Joa-M9aAfD0YOX4jOndjrcoiLMDAEBdFxgjt8o
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
  - id: d6e0d39b-5df3-4c72-8263-fd834397ee97
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
source-git-commit: 4bdf774d4d38b3c7d97daebade3dfb6ab0403a5e
workflow-type: tm+mt
source-wordcount: 992
ht-degree: 62%

---

# Introduzione a Genera contenuto {#gs-content-assistant}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come accedere a Genera contenuto in Adobe Journey Optimizer, impostare le autorizzazioni necessarie e comprendere i guardrail per la generazione di testo e immagini.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="Generare contenuti in Journey Optimizer"
>abstract="Dopo aver creato e personalizzato la consegna, puoi utilizzare l’intelligenza artificiale per modificare e perfezionare i contenuti. Questa funzione semplifica il processo di personalizzazione e miglioramento dei contenuti consentendoti di perfezionarli descrivendo cosa desideri generare."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="Carica risorsa del brand"
>abstract="Il menu Carica risorsa marchio consente di aggiungere qualsiasi risorsa del marchio contenente contenuti che possano fornire contesto aggiuntivo per la generazione di contenuti in Journey Optimizer o per selezionare una risorsa caricata in precedenza. Questa opzione garantisce che Generate Content abbia accesso a tutto il materiale necessario per migliorarne la funzionalità e la rilevanza."

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Condizioni per l’IA generativa di Adobe"
>abstract="L’accesso a questa funzione è soggetto al consenso alle Linee guida per l’utente dell’IA generativa di Adobe Experience Cloud. Controlla l’accuratezza degli output generati da questa funzione e assicurati che siano appropriati al tuo caso d’uso."
>additional-url="https://www.adobe.com/it/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Linee guida per l’utente sull’intelligenza artificiale generativa di Adobe"

>[!INFO]
>
>Immergiti in un’esperienza pratica con [la nostra anteprima della funzione live](https://experienceleague.adobe.com/it/apps/journey-optimizer/ai-assistant-content-accelerator){target="_blank"}, progettata per permetterti di esplorarla in prima persona e comprenderne appieno le funzionalità.


Generate Content in Adobe Journey Optimizer (Genera contenuto in), con tecnologia Microsoft Azure OpenAI e Adobe Firefly, offre suggerimenti proattivi per la variazione dei contenuti per testo e immagini. Questa nuova funzionalità fornisce una **generazione di testo e immagini basata su prompt**. La generazione di immagini è gestita con Adobe Firefly.

Genera contenuto supporta la generazione **in più lingue** consentendo di raggiungere e coinvolgere diversi tipi di pubblico globali. Genera contenuto è disponibile nelle seguenti lingue:

<table style="table-layout:fixed; margin-top: 0px; margin-bottom: 0px;">
  <tbody>
    <tr style="border: 0;background-color: #FFFFFF;">
      <td>
        <ul>
          <li>Cinese (Hong Kong)</li>
          <li>Cinese (semplificato)</li>
          <li>Cinese (Taiwan)</li>
          <li>Olandese</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Francese</li>
          <li>Tedesco</li>
          <li>Italiano</li>
          <li>Giapponese</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Norvegese</li>
          <li>Portoghese</li>
          <li>Spagnolo</li>
          <li>Svedese</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

Utilizza l’intelligenza artificiale per ottimizzare l’impatto del messaggio sperimentando con diversi titoli e immagini principali. Genera più varianti e crea un esperimento per confrontarle. Sfruttando l’**esperimento sui contenuti di Journey Optimizer**, puoi definire più trattamenti per i messaggi al fine di misurare quale funziona meglio per il tuo pubblico target. Puoi scegliere di variare il contenuto della consegna o l’oggetto. Il pubblico del messaggio viene allocato in modo casuale a ciascun trattamento per determinare quale funziona meglio nei termini della metrica specificata. Per ulteriori informazioni sull’esperimento contenuti, consulta [questa sezione](../content-management/content-experiment.md).

>[!IMPORTANT]
>
>* Prima di iniziare a utilizzare questa funzionalità, leggi l’articolo su [guardrail e limitazioni](#generative-guardrails) correlati.
>
>
>* È necessario accettare un [contratto utente](https://www.adobe.com/it/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"} prima di poter utilizzare Genera contenuto in Adobe Journey Optimizer. Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

## Accedi a Genera contenuto {#generative-access}

Per accedere a Genera contenuto in Adobe Journey Optimizer, è necessario concedere agli utenti l&#39;autorizzazione **Genera contenuto**. [Ulteriori informazioni](../administration/permissions.md)

+++  Scopri come assegnare le autorizzazioni relative alla generazione di contenuti

1. Nel prodotto **Autorizzazioni**, passa alla scheda **Ruoli** e seleziona il **Ruolo** desiderato.

1. Fai clic su **Modifica** per modificare le autorizzazioni.

1. Aggiungi la risorsa **Assistente IA**, quindi seleziona **Genera contenuto** dal menu a discesa.

   ![](assets/gen-ai-role.png){zoomable="yes"}

1. Fai clic su **Salva** per applicare le modifiche.

   Le autorizzazioni degli utenti già assegnati a questo ruolo verranno aggiornate automaticamente.

1. Per assegnare questo ruolo a nuovi utenti, passa alla scheda **Utenti** nella dashboard **Ruoli** e fai clic su **Aggiungi utente**.

1. Immetti il nome o l’indirizzo e-mail dell’utente o sceglilo dall’elenco e fai clic su **Salva**.

1. Se l’utente non è già stato creato in precedenza, consulta [questa documentazione](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/abac/permissions-ui/users).

L’utente riceverà un’e-mail con istruzioni per accedere all’istanza.

+++

## Guardrail e limitazioni {#generative-guardrails}

Di seguito sono elencate le linee guida generali per l’utilizzo di Genera contenuto in Adobe Journey Optimizer per la generazione di e-mail:

### Canali supportati

* Disponibile solo per i canali e-mail, push, web e SMS.

### Qualità dei contenuti, prompt e feedback

* La qualità del contenuto generato è fortemente influenzata dalla finalità di marketing/prompt definito. Utilizza un prompt ben definito affinché il modello di GenAI possa interpretarlo correttamente. 
* I contenuti GenAI potrebbero non essere sempre accurati: condividi il tuo feedback per permettere ai nostri tecnici di perfezionare i modelli.
* Assicurati di segnalare eventuali risultati problematici utilizzando le icone con il pollice su, il pollice giù o un flag durante la selezione delle varianti.

### Risorse per brand

* Carica la risorsa del brand in modo che sia accurata per il relativo contenuto. Altrimenti, il contenuto si basa su informazioni disponibili pubblicamente. Il contenuto caricato può essere nei seguenti formati: file PDF, JPEG, PNG o ZIP (con formati di file supportati).
* La dimensione massima per risorsa del marchio caricata è 50 MB. È possibile utilizzare anche file di dimensioni maggiori o numerose immagini, ma questo comporterà tempi di elaborazione più lunghi.
* Puoi caricare più risorse del brand, ma puoi sfruttarne una sola per una generazione specifica.

### Immagini e modelli di e-mail

* Utilizza un modello personalizzato o specifico per il brand per creare il contenuto delle e-mail utilizzando l’opzione Genera contenuto in Adobe Journey Optimizer. Si consiglia di utilizzare un modello e-mail con un massimo di 8-10 immagini.

### Uso legale e trasparenza

* L’utilizzo di Genera contenuto è soggetto alle Linee guida per l’utente di Adobe Experience Cloud Generative AI. [Ulteriori informazioni](https://www.adobe.com/it/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)
* Come parte dell’impegno di Adobe per promuovere la trasparenza nell’utilizzo di strumenti di intelligenza artificiale generativi nella creazione di contenuti multimediali, Adobe applicherà Content Credentials quando vengono scaricati o esportati contenuti o progetti che includono una risorsa generata da Firefly. [Ulteriori informazioni](https://helpx.adobe.com/it/firefly/using/content-credentials.html)
  <!--* See [Content Credentials in AI Assistant](generative-content-credentials.md) for details on which actions attach Content Credentials and what happens as your content moves.-->

### Generare contenuti per le espressioni di personalizzazione {#ai-assistant-personalization-editor-guardrails}

I seguenti guardrail si applicano a [Generare contenuto per le espressioni di personalizzazione](generative-personalization-expressions.md) in [!UICONTROL Personalization Editor] e in Email Designer.

* **Offerta e Decisioni per le esperienze**: non supportati.
* **Preferiti**: non supportati.
* **Condizioni salvate**: non supportate.
* **Frammenti di contenuto di Adobe Experience Manager**: non supportati.

## Generare funzionalità di contenuto {#generative-features}

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="generative-full-content.md">
<img alt="Generazione contenuto completo" src="assets/do-not-localize/email-genai.jpeg">
</a>
<div>
<a href="generative-full-content.md"><strong>Generare contenuto completo</strong></a>
</div>
<p>
</td>
<td>
<a href="generative-text.md">
<img alt="Generazione di testo" src="assets/do-not-localize/text-genai.jpeg">
</a>
<div><a href="generative-text.md"><strong>Generare testo</strong>
</div>
<p>
</td>
<td>
<a href="generative-image.md">
<img alt="Generazione di immagini" src="assets/do-not-localize/image-genai.jpeg">
</a>
<div>
<a href="generative-image.md"><strong>Generare immagini</strong></a>
</div>
<p></td>
</tr></table>

## Risorse aggiuntive

* **[Generare casi di utilizzo dei contenuti](generative-uc.md)** - Scopri tramite i casi di utilizzo come utilizzare Generare contenuti
* **[Genera tutorial sui contenuti](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/introduction-to-journey-optimizer/ai-assistant){target="_blank"}** - Esplora i tutorial video dettagliati sulle funzioni e best practice per la generazione di contenuti.
