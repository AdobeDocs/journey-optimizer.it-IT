---
title: Ottimizzare il testo delle e-mail per le caselle in entrata AI
description: Affina il livello di testo normale dell’e-mail in Journey Optimizer in modo che i clienti con casella in entrata assistita da IA possano utilizzare le offerte e i CTA quando riepilogano le intenzioni di posta o estrazione, nel Designer e-mail con Ottimizzazione con AI.
feature: Email Design
topic: Content Management, Artificial Intelligence
role: User
level: Beginner, Intermediate
exl-id: 0c2f95ce-28a0-480c-9829-b7e4975b6340
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 1%

---

# Ottimizzare il testo delle e-mail per le caselle in entrata AI {#email-text-optimizer}

[!DNL Adobe Journey Optimizer] include una funzionalità del canale e-mail che consente di strutturare la [versione testo](../email/text-version-email.md) dei messaggi per migliorare le esperienze di posta in arrivo basate sull&#39;intelligenza artificiale, ad esempio [!DNL Apple Intelligence] e [!DNL Google Gemini] in [!DNL Gmail], in modo che possano rispondere alle domande e riepilogare i messaggi in base al contenuto in modo più accurato, con risultati migliori.

>[!NOTE]
>
>Questa funzionalità cambia solo il testo normale, non la versione HTML del contenuto dell’e-mail.

Con questo strumento di ottimizzazione del testo delle e-mail, puoi verificare che la versione in testo normale del contenuto delle e-mail sia migliorata per le esperienze di casella in entrata basate sull’intelligenza artificiale, in modo che le informazioni fornite alle funzioni di intelligenza artificiale di questi provider di caselle in entrata siano esattamente quelle che desideri fornire.

## Come funziona {#how-it-works}

Domande tipiche che i destinatari possono porre nelle esperienze casella in entrata basate sull’intelligenza artificiale sono *Di cosa si tratta?* o *Quali sono queste offerte?*.

* Le risposte fornite da questi assistenti AI possono essere un breve riepilogo (ad esempio se il messaggio è promozionale, menziona l’accesso anticipato a VIP e una vendita, e include collegamenti a categorie di prodotti), ma omettono comunque gli obiettivi di cui l’addetto marketing si preoccupa perché gli assistenti deducono da qualsiasi testo visualizzato, non necessariamente la storia completa che intendevi raccontare.

* Inoltre, gli assistenti possono cercare in modo proattivo sconti o coupon relativi al brand e inserirli nella risposta, in modo che l’utente non stia più guardando solo ciò che il tuo messaggio ha effettivamente promesso. Questo comportamento è utile agli utenti finali, ma riduce il controllo per gli esperti di marketing che hanno bisogno di risposte per tenere traccia dei termini reali dell’invio.

Per evitare questi problemi, [!DNL Journey Optimizer] riscrive il testo normale in modo che coupon, intervalli di sconti, inviti all&#39;azione e altre priorità vengano visualizzati in primo piano in una copia lineare chiara. L’obiettivo è quello di creare riepiloghi e domande e risposte nella casella in entrata nelle offerte e azioni definite, invece di appoggiarsi su una sottile parte di testo predefinita o su risultati web non correlati.

>[!IMPORTANT]
>
>I comportamenti esatti dell’assistente AI dipendono dal provider e dalla versione del modello della casella in entrata. Una volta recapitata l’e-mail, le risposte e i riepiloghi forniti dai client di intelligenza artificiale esterni possono essere errati, incompleti o misti con i risultati web.
>
>La funzionalità Ottimizza testo e-mail per caselle in entrata AI migliora solo il testo normale creato in Journey Optimizer; non garantisce come un assistente di terze parti interpreterà o visualizzerà il messaggio. Ulteriori informazioni sulle [limitazioni e rischi della posta in arrivo di terze parti AI](#inbox-ai-risks).

## Casi d’uso consigliati {#use-cases}

<!--
* **Critical details only in images** — Offers, promo codes, or deadlines shown in banners or graphics are invisible in plain text. Use the optimizer (and manual edits) so the same facts appear as text, improving extraction by AI summaries and text-only clients.
-->

* **Testo generato automaticamente denso o frammentato**: quando è difficile digitalizzare il testo normale predefinito, l&#39;ottimizzazione può produrre una narrazione lineare più chiara con offerte e collegamenti espliciti.

* **Controllo delle domande e risposte della casella in entrata**: se si prevede che i destinatari chiedano agli assistenti *di che cosa si tratta* o *quali sono le offerte*, una versione in testo normale forte riduce i riepiloghi parziali e riduce la dipendenza dalle risposte completate dal Web che non sono legate alla copia approvata.

## Ottimizza per esperienze casella in entrata AI {#optimize-with-ai}

>[!IMPORTANT]
>
>Prima di iniziare a utilizzare questa funzionalità, leggi i relativi [rischi e limitazioni](#inbox-ai-risks).
>
>Per accedere a questa funzione, devi accettare un contratto utente che visualizza la prima volta che utilizzi Generative AI in [!DNL Journey Optimizer]. Per ulteriori informazioni, leggere le [Linee guida per l&#39;utente di Adobe Experience Cloud Generative AI](https://www.adobe.com/it/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

Per ottimizzare la versione in testo normale dell&#39;e-mail per le caselle in entrata basate su IA con [!DNL Journey Optimizer], attieniti alla procedura seguente.

1. Apri l&#39;e-mail in [Invia e-mail a Designer](../email/content-from-scratch.md) (da una campagna, un percorso o un modello, a seconda del flusso di lavoro).

1. Seleziona l&#39;icona **[!UICONTROL Testo normale]** per aprire la versione testuale dell&#39;e-mail. [Ulteriori informazioni](../email/text-version-email.md)

   ![Seleziona l&#39;icona Testo normale per aprire la versione testuale dell&#39;e-mail](assets/text-optimizer-text-icon.png){zoomable="yes"}

1. Viene visualizzata la versione testuale dell’e-mail. Fai clic sul pulsante **[!UICONTROL Ottimizza per casella in entrata AI]** per generare una versione di testo normale migliorata che evidenzia le informazioni chiave per la lettura e il riepilogo basati sull&#39;intelligenza artificiale.

   ![Pulsante Ottimizza per casella in entrata IA nella visualizzazione della versione del testo](assets/text-optimizer-for-ai-button.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >Facendo clic sul pulsante **[!UICONTROL Ottimizza per Posta in arrivo AI]**, l&#39;opzione **[!UICONTROL Sincronizza con HTML]** viene disabilitata automaticamente. [Ulteriori informazioni](../email/text-version-email.md#plain-text-custom)

1. Se si utilizza l&#39;intelligenza artificiale generativa per la prima volta in [!DNL Journey Optimizer], verrà richiesto di accettare il contratto utente. Per ulteriori informazioni, consulta le [Linee guida per l&#39;utente di Adobe Generative AI](https://www.adobe.com/it/legal/licenses-terms/adobe-gen-ai-user-guidelines.html){target="_blank"}.

   ![Finestra di dialogo del contratto utente Generative AI in Journey Optimizer](assets/text-optimizer-agreement.png){width=50%}

   Fai clic su **[!UICONTROL Accetto]** per continuare.

1. Viene visualizzato il testo generato. Rivedi le modifiche, se necessario modificale, quindi salva l’e-mail come di consueto.

   ![Testo generato nella visualizzazione versione testo](assets/text-optimizer-output.png){zoomable="yes" width="80%"}

   >[!NOTE]
   >
   >L’ottimizzatore del testo dell’e-mail aggiorna solo il corpo del testo normale. Non modifica il design, il layout o le immagini del HTML.

1. Puoi tornare alla versione HTML dell&#39;e-mail in qualsiasi momento facendo clic sull&#39;icona **[!UICONTROL Passa alla visualizzazione desktop]**. Le modifiche apportate alla versione di testo vengono mantenute.

   >[!CAUTION]
   >
   >Se si abilita nuovamente l&#39;opzione **[!UICONTROL Sincronizza con HTML]**, le modifiche andranno perse e sostituite con il contenuto di testo generato dalla versione di HTML.

## Rischi e limitazioni di IA per la casella in entrata di terze parti {#inbox-ai-risks}

La funzionalità Ottimizza testo e-mail per caselle in entrata AI consente di preparare testo normale per le modalità di elaborazione degli invii di [!DNL Journey Optimizer] da parte dei provider di cassette postali. Non controlla i prodotti di tali fornitori. Una volta recapitato un messaggio, tutte le funzionalità di intelligenza artificiale in [!DNL Gmail], [!DNL Apple] Mail, [!DNL Outlook] o altri client funzionano in base ai loro termini, modelli e criteri, non in Adobe.

* **Presentazione imprevedibile**: i riepiloghi, i messaggi di notifica e le risposte conversazionali possono omettere le offerte, determinare prezzi o date non corretti, unire contenuti con risultati Web non correlati o parafrasare in modi che non corrispondono più alla copia approvata. Il comportamento cambia quando i fornitori aggiornano i modelli o l’interfaccia utente senza preavviso.

* **Nessuna garanzia di parità con HTML**: i destinatari che si basano su anteprime o risposte di assistenza potrebbero non visualizzare mai la progettazione HTML completa, le immagini o i piè di pagina legali. Ciò in cui credono che il messaggio &quot;dice&quot; possa provenire solo da un breve riepilogo generato dall’intelligenza artificiale.

* **Privacy, conformità e utilizzo dei dati**: IA per la posta in arrivo può elaborare il contenuto dei messaggi nell&#39;infrastruttura del provider in base all&#39;informativa sulla privacy, alla conservazione e alle regole regionali del provider. Le organizzazioni dei settori regolamentati devono valutare se l&#39;utilizzo di tali funzionalità da parte del destinatario influisce sui propri obblighi, indipendentemente da come è stata creata l&#39;e-mail in [!DNL Journey Optimizer].

* **Esposizione legale e del marchio**: riepiloghi di IA non corretti o incompleti possono creare confusione nei clienti o controversie su promozioni, termini o linguaggio di rinuncia. L&#39;ottimizzatore migliora il livello di testo fornito, ma non garantisce che il modello di una terza parte lo riproduca fedelmente.

* **[!UICONTROL Ottimizza per casella in entrata AI]** in [!DNL Journey Optimizer]. L&#39;azione relativa al momento dell&#39;authoring in E-mail Designer è un sistema separato dagli assistenti alla casella in entrata degli utenti finali. Rivedi sempre il testo normale generato prima dell’invio.

## Argomenti correlati {#related-topics}

* [Gestire la versione testuale di un messaggio e-mail](../email/text-version-email.md)
* [Introduzione alla progettazione delle e-mail](../email/get-started-email-design.md)
* Per informazioni più ampie sulle funzionalità generative di Adobe, consulta [Introduzione all&#39;Assistente AI per la creazione di contenuti](gs-generative.md).
