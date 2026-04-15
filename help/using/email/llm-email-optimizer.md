---
title: Ottimizzare il testo delle e-mail per le caselle in entrata AI
description: Affina il livello di testo normale dell’e-mail in Journey Optimizer in modo che i clienti con casella in entrata assistita da IA possano utilizzare le offerte e i CTA quando riepilogano le intenzioni di posta o estrazione, nel Designer e-mail con Ottimizzazione con AI.
feature: Email Design
topic: Content Management, Artificial Intelligence
role: User
level: Beginner, Intermediate
exl-id: 0c2f95ce-28a0-480c-9829-b7e4975b6340
source-git-commit: 88f47d375f01eff40a0f96e9cf0353b7914a0f89
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 1%

---

# Ottimizzare il testo delle e-mail per le caselle in entrata AI {#email-text-optimizer}

[!DNL Adobe Journey Optimizer] include una funzionalità del canale e-mail che consente di strutturare una versione specifica dei messaggi per migliorare le esperienze di posta in arrivo basate sull&#39;intelligenza artificiale, ad esempio [!DNL Apple Intelligence] e [!DNL Google Gemini] in [!DNL Gmail], in modo che possano rispondere alle domande e riepilogare i messaggi in base al contenuto in modo più accurato, con risultati migliori.

Puoi utilizzare questa funzionalità per perfezionare una versione di testo dedicata dei messaggi, in modo che le esperienze della casella in entrata basate sull’intelligenza artificiale mostrino con maggiore probabilità le offerte, le chiamate all’azione e i dettagli desiderati, anziché testo generato automaticamente o contesto non correlato.

## Come funziona {#how-it-works}

Domande tipiche che i destinatari possono porre nelle esperienze casella in entrata basate sull’intelligenza artificiale sono *Di cosa si tratta?* o *Quali sono queste offerte?*.

* Le risposte fornite da questi assistenti AI possono essere un breve riepilogo (ad esempio se il messaggio è promozionale, menziona l’accesso anticipato a VIP e una vendita, e include collegamenti a categorie di prodotti), ma omettono comunque gli obiettivi di cui l’addetto marketing si preoccupa perché gli assistenti deducono da qualsiasi testo visualizzato, non necessariamente la storia completa che intendevi raccontare.

* Inoltre, gli assistenti possono cercare in modo proattivo sconti o coupon relativi al brand e inserirli nella risposta, in modo che l’utente non stia più guardando solo ciò che il tuo messaggio ha effettivamente promesso. Questo comportamento è utile agli utenti finali, ma riduce il controllo per gli esperti di marketing che hanno bisogno di risposte per tenere traccia dei termini reali dell’invio.

Per evitare questi problemi, [!DNL Journey Optimizer] crea una versione di testo aggiuntiva dei messaggi in modo che coupon, intervalli di sconti, inviti all&#39;azione e altre priorità vengano visualizzati in primo piano in una copia lineare chiara.

>[!NOTE]
>
>Questa versione di testo dedicata non corrisponde alla versione di testo normale predefinita o personalizzata dei messaggi. [Ulteriori informazioni](text-version-email.md)

L’obiettivo è quello di creare riepiloghi e domande e risposte nella casella in entrata nelle offerte e azioni definite, invece di appoggiarsi su una sottile parte di testo predefinita o su risultati web non correlati.

>[!IMPORTANT]
>
>I comportamenti esatti dell’assistente AI dipendono dal provider e dalla versione del modello della casella in entrata. Una volta recapitata l’e-mail, le risposte e i riepiloghi forniti dai client di intelligenza artificiale esterni possono essere errati, incompleti o misti con i risultati web.
>
>La funzionalità Ottimizza testo e-mail per caselle in entrata AI genera solo una versione di testo dedicata in Journey Optimizer; non garantisce come un assistente di terze parti interpreterà o visualizzerà il messaggio. Ulteriori informazioni sulle [limitazioni e rischi della posta in arrivo di terze parti AI](#inbox-ai-risks).

## Casi d’uso consigliati {#use-cases}

<!--
* **Critical details only in images** — Offers, promo codes, or deadlines shown in banners or graphics are invisible in plain text. Use the optimizer (and manual edits) so the same facts appear as text, improving extraction by AI summaries and text-only clients.
-->

* **Testo generato automaticamente denso o frammentato**: quando è difficile digitalizzare il testo normale predefinito, l&#39;ottimizzazione può produrre una narrazione lineare più chiara con offerte e collegamenti espliciti.

* **Controllo delle domande e risposte della casella in entrata**: quando si prevede che i destinatari chiedano agli assistenti *di che cosa si tratta* o *quali sono le offerte*, una versione forte della casella in entrata dell&#39;intelligenza artificiale riduce i riepiloghi parziali ed evita di fare affidamento su risposte completate dal Web che non sono legate alla copia approvata.

## Ottimizza per esperienze casella in entrata AI {#optimize-with-ai}

>[!IMPORTANT]
>
>Prima di utilizzare questa funzionalità, leggere i relativi [rischi e limitazioni](#inbox-ai-risks).
>
>Per accedere a questa funzione, devi accettare un contratto utente che visualizza la prima volta che utilizzi Generative AI in [!DNL Journey Optimizer]. Per ulteriori informazioni, leggere le [Linee guida per l&#39;utente di Adobe Experience Cloud Generative AI](https://www.adobe.com/it/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

Per ottimizzare la versione in testo normale dell&#39;e-mail per le caselle in entrata basate su IA con [!DNL Journey Optimizer], attieniti alla procedura seguente.

1. Apri l&#39;e-mail in [Invia e-mail a Designer](content-from-scratch.md) (da una campagna, un percorso o un modello, a seconda del flusso di lavoro).

1. Fai clic sul pulsante **[!UICONTROL Ottimizza per casella in entrata AI]** per generare una versione migliorata che evidenzia le informazioni chiave per la lettura e il riepilogo basati sull&#39;intelligenza artificiale.

   ![Pulsante Ottimizza per casella in entrata AI in E-mail Designer](assets/optimize-for-ai-button.png){zoomable="yes" width="80%"}

1. Se si utilizza l&#39;intelligenza artificiale generativa per la prima volta in [!DNL Journey Optimizer], verrà richiesto di accettare il contratto utente. Per ulteriori informazioni, consulta le [Linee guida per l&#39;utente di Adobe Generative AI](https://www.adobe.com/it/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

   ![Finestra di dialogo del contratto utente Generative AI in Journey Optimizer](assets/optimize-ai-inbox-agreement.png){width=50%}

   Fai clic su **[!UICONTROL Accetto]** per continuare.

1. Viene visualizzata la versione generata.

   ![Versione generata ottimizzata per le caselle in entrata IA](assets/optimize-ai-inbox-output.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >**L&#39;ottimizzazione del testo delle e-mail per le caselle in entrata AI** non modifica la progettazione, il layout o le immagini di HTML.

1. Per apportare modifiche al contenuto generato automaticamente, selezionare l&#39;opzione **[!UICONTROL Abilita modifica]** e modificare manualmente il contenuto in base alle esigenze.

1. Quando sei soddisfatto della tua versione, fai clic sul pulsante **[!UICONTROL Ottimizza e-mail]** per confermare.

1. L’e-mail è ora ottimizzata per le caselle in entrata di IA.

1. Per accedere o modificare la versione ottimizzata, fare clic sul pulsante **[!UICONTROL Casella in entrata ottimizzata per IA]**.

   ![Pulsante Riottimizza in E-mail Designer](assets/optimize-ai-inbox-optimized-button.png){zoomable="yes" width="80%"}

1. Viene visualizzata la versione ottimizzata. È possibile **[!UICONTROL Rimuovere l&#39;ottimizzazione]** o fare clic su **[!UICONTROL Riottimizzare]** per generare una nuova versione.

   ![Versione precedentemente ottimizzata in E-mail Designer](assets/optimize-ai-inbox-optimized-version.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >Se apporti modifiche al contenuto HTML originale, devi riottimizzare la versione per le caselle in entrata di IA.

## Rischi e limitazioni di IA per la casella in entrata di terze parti {#inbox-ai-risks}

La funzionalità Ottimizza posta elettronica per caselle di posta AI consente di preparare una versione dell&#39;e-mail per le modalità di elaborazione degli invii di [!DNL Journey Optimizer] da parte dei provider di cassette postali. Non controlla i prodotti di tali fornitori. Una volta recapitato un messaggio, tutte le funzionalità di intelligenza artificiale in [!DNL Gmail], [!DNL Apple] Mail, [!DNL Outlook] o altri client funzionano in base ai loro termini, modelli e criteri, non in Adobe.

* **Presentazione imprevedibile**: i riepiloghi, i messaggi di notifica e le risposte conversazionali possono omettere le offerte, determinare prezzi o date non corretti, unire contenuti con risultati Web non correlati o parafrasare in modi che non corrispondono più alla copia approvata. Il comportamento cambia quando i fornitori aggiornano i modelli o l’interfaccia utente senza preavviso.

* **Nessuna garanzia di parità con HTML**: i destinatari che si basano su anteprime o risposte di assistenza potrebbero non visualizzare mai la progettazione HTML completa, le immagini o i piè di pagina legali. Ciò in cui credono che il messaggio &quot;dice&quot; possa provenire solo da un breve riepilogo generato dall’intelligenza artificiale.

* **Privacy, conformità e utilizzo dei dati**: IA per la posta in arrivo può elaborare il contenuto dei messaggi nell&#39;infrastruttura del provider in base all&#39;informativa sulla privacy, alla conservazione e alle regole regionali del provider. Le organizzazioni dei settori regolamentati devono valutare se l&#39;utilizzo di tali funzionalità da parte del destinatario influisce sui propri obblighi, indipendentemente da come è stata creata l&#39;e-mail in [!DNL Journey Optimizer].

* **Esposizione legale e del marchio**: riepiloghi di IA non corretti o incompleti possono creare confusione nei clienti o controversie su promozioni, termini o linguaggio di rinuncia. **L&#39;ottimizzazione delle e-mail per le caselle in entrata AI** non garantisce che il modello di una terza parte riproduca fedelmente la versione ottimizzata dell&#39;e-mail.

* **[!UICONTROL Ottimizza per Posta in arrivo AI]** in [!DNL Journey Optimizer]. Il controllo della fase di authoring in E-mail Designer è separato dagli assistenti alla posta in arrivo degli utenti finali. Rivedi sempre il testo normale generato prima dell’invio.

## Argomenti correlati {#related-topics}

* [Introduzione alla progettazione delle e-mail](get-started-email-design.md)
* Per informazioni più ampie sulle funzionalità generative di Adobe, consulta [Introduzione all&#39;Assistente AI per la creazione di contenuti](../content-management/gs-generative.md).
