---
solution: Journey Optimizer
product: journey optimizer
title: Creare contenuti dinamici
description: Scopri come aggiungere contenuto dinamico ai messaggi.
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
keywords: espressione, editor, dynamic, content
exl-id: 639ad7df-0d0f-4c9b-95d1-f3101267aae2
TQID: https://experienceleague.adobe.com/j9jmVxc9Pn53hghR-2sUGXjcczfQibs5XTGuD7gwiI4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2: id: a757b957-83f3-4a4d-9775-a93854f84f77id: e51e8901-97d9-4f7d-a835-503025a90e32
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1262
ht-degree: 12%

---

# Creare contenuti dinamici {#dynamic-content}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come utilizzare le regole condizionali per aggiungere contenuto dinamico ai messaggi, sia nelle espressioni di personalizzazione che come varianti di componenti di contenuto nel Designer e-mail.

>[!ENDSHADEBOX]

Adobe Journey Optimizer consente di sfruttare le regole condizionali create nella libreria per aggiungere contenuto dinamico ai messaggi.

Il contenuto dinamico può essere creato in qualsiasi campo in cui puoi aggiungere la personalizzazione utilizzando l’editor di personalizzazione. Ciò include l’oggetto, i collegamenti, il contenuto delle notifiche push o le rappresentazioni delle offerte di tipo testo. [Ulteriori informazioni sulla personalizzazione](personalize.md)

Inoltre, puoi utilizzare le regole condizionali nel Designer e-mail per creare più varianti di un componente di contenuto.

## Aggiungere contenuto dinamico alle espressioni {#perso-expressions}

I passaggi per aggiungere contenuto dinamico nelle espressioni sono i seguenti:

1. Passa al campo in cui desideri aggiungere contenuto dinamico, quindi apri l’editor di personalizzazione.

1. Selezionare il menu **[!UICONTROL Condizioni]** per visualizzare l&#39;elenco delle regole condizionali disponibili. Fai clic sul pulsante + accanto a una regola per aggiungerla all’espressione corrente.

   Puoi anche creare una nuova regola selezionando **[!UICONTROL Crea nuovo]**. [Scopri come creare le condizioni](create-conditions.md)

   ![](assets/conditions-expression.png)

1. Aggiungere tra i tag `{%if}` e `{%/if}` il contenuto da visualizzare se la regola condizionale è soddisfatta. Puoi aggiungere tutte le regole necessarie per creare diverse varianti di un’espressione.

   Nell’esempio seguente, sono state create due varianti per un contenuto SMS, a seconda della lingua preferita del destinatario.

   ![](assets/conditions-language-sample.png)

1. Quando il contenuto è pronto, puoi visualizzare in anteprima diverse varianti utilizzando entrambi i metodi di simulazione: fai clic su **[!UICONTROL Simula contenuto]** per testare le varianti di contenuto con dati di input di esempio o generazione automatica di IA, oppure fai clic su **[!UICONTROL Simula contenuto]**, quindi seleziona **[!UICONTROL Simula contenuto (profili AEP)]** dal menu a discesa per visualizzare in anteprima i profili di test. [Scopri come verificare e visualizzare in anteprima i messaggi](../content-management/preview-test.md)

   ![](assets/conditions-preview.png)

>[!CAUTION]
>
>Se il rendering di E-mail Designer non riesce dopo l’aggiunta di blocchi condizionali, verifica che la sintassi di ogni nuova condizione sia corretta e che non esistano istruzioni duplicate o in conflitto. Se i problemi persistono, è consigliabile ricostruire le sezioni problematiche in un nuovo modello e testare ogni blocco condizionale in modo incrementale.


## Aggiungere contenuto dinamico alle e-mail {#emails}

>[!CONTEXTUALHELP]
>id="ac_conditional_content"
>title="Contenuto condizionale"
>abstract="Utilizza le regole condizionali per creare più varianti di un componente di contenuto. Se non viene soddisfatta alcuna condizione durante l’invio del messaggio, verrà visualizzato il contenuto della variante predefinita."

>[!CONTEXTUALHELP]
>id="ac_conditional_content_select"
>title="Contenuto condizionale"
>abstract="Utilizza una regola condizionale salvata nella libreria o creane una nuova."

I passaggi per creare varianti di un componente di contenuto nel Designer e-mail sono i seguenti:

1. In [E-mail Designer](../email/content-from-scratch.md), seleziona un componente di contenuto, quindi fai clic su **[!UICONTROL Abilita contenuto condizionale]**.

   ![](assets/conditions-enable-conditional.png)

1. Il riquadro **[!UICONTROL Contenuto condizionale]** viene visualizzato a sinistra. In questo riquadro, puoi utilizzare le condizioni per creare più varianti del componente di contenuto selezionato.

   Configura la prima variante selezionando il pulsante **[!UICONTROL Seleziona condizione]**.

   ![](assets/conditions-apply.png)

1. Viene visualizzata la libreria delle condizioni. Seleziona la regola condizionale da associare alla variante, quindi fai clic su **[!UICONTROL Seleziona]**. In questo esempio, vogliamo adattare il testo del componente in base alla lingua preferita del destinatario.

   ![](assets/conditions-select.png)

   Puoi anche creare una nuova regola facendo clic su **[!UICONTROL Crea nuovo]**. [Scopri come creare le condizioni](create-conditions.md)

1. La regola condizionale è associata alla variante. Per una migliore leggibilità, rinomina la variante selezionando l&#39;azione **[!UICONTROL Rinomina]** dall&#39;icona Altre azioni.

   ![](assets/conditions-rename.png)

1. Configura il modo in cui il componente verrà visualizzato se la regola viene soddisfatta al momento dell’invio del messaggio. In questo esempio, se la lingua preferita del destinatario è il francese, il testo dovrà essere in francese.

   ![](assets/conditions-design.png)

1. Aggiungi tutte le varianti necessarie per il componente contenuto. Puoi passare in qualsiasi momento da una variante all’altra per verificare come verrà visualizzato il componente contenuto a seconda delle regole condizionali.

   >[!NOTE]
   >
   >* Se nessuna delle regole definite nelle varianti viene soddisfatta durante l&#39;invio del messaggio, il componente contenuto visualizzerà il contenuto definito nella **[!UICONTROL variante predefinita]**.
   >
   >* Il contenuto condizionale verrà valutato in base alle regole associate nell’ordine in cui vengono visualizzate le varianti. La variante predefinita viene sempre visualizzata se non sono soddisfatte altre condizioni.
   >
   >* Durante la simulazione o il rendering delle bozze per e-mail contenenti più varianti condizionali, Journey Optimizer potrebbe richiedere più tempo di elaborazione. In caso di timeout o messaggi di errore, considera di ridurre il numero totale di varianti o di semplificare le regole condizionali. Ulteriori informazioni sulla verifica del contenuto in [questa pagina](../content-management/preview-test.md).


1. Per eliminare una variante, fai clic sull&#39;icona Altre azioni accanto alla variante desiderata e seleziona **[!UICONTROL Elimina]**.

   ![](assets/conditions-delete.png)

## Riferimento rapido {#quick-reference}

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

>[!BEGINTABS]

>[!TAB Panoramica]

**TL;DR**

Questa pagina spiega come utilizzare le regole condizionali per aggiungere contenuto dinamico ai messaggi, tramite i tag di espressione nell’editor di personalizzazione o come varianti di componenti di contenuto nel Designer e-mail.

**Intenti**

* Aggiungere contenuto dinamico alle espressioni di personalizzazione utilizzando `{%if%}` / `{%/if%}` tag condizionali
* Anteprima di più varianti di contenuto dinamico tramite simulazione
* Abilitare il contenuto condizionale in un componente di contenuto Designer e-mail
* Creare più varianti di componenti ciascuna collegata a una regola condizionale
* Gestisci la variante predefinita visualizzata se non sono soddisfatte condizioni al momento dell’invio

>[!TAB Glossario]

* **Contenuto dinamico**: contenuto del messaggio che varia in base alle regole condizionali; contenuto diverso viene visualizzato a seconda che le condizioni definite siano soddisfatte o meno al momento dell&#39;invio. *(specifico per prodotto)*
* **Contenuto condizionale**: funzionalità di E-mail Designer che applica regole condizionali a un componente di contenuto, creando più varianti di visualizzazione. *(specifico per prodotto)*
* **Variante predefinita**: il contenuto visualizzato per un componente quando nessuna delle regole condizionali definite viene soddisfatta durante l&#39;invio del messaggio. *(specifico per prodotto)*
* **`{%if%}`/ `{%/if%}` tag**: sintassi dell&#39;espressione dell&#39;editor di Personalization utilizzata per racchiudere i blocchi di contenuto visualizzati solo quando viene soddisfatta una regola condizionale.

>[!TAB Terminologia]

* **Nome canonico:** contenuto dinamico — varianti: contenuto condizionale, contenuto personalizzato
* **Sinonimi:** &quot;contenuto condizionale&quot; (etichetta dell&#39;interfaccia utente di E-mail Designer) = &quot;contenuto dinamico&quot; (termine generale utilizzato in tutto)
* **Non confondere:** l&#39;aggiunta di contenuto dinamico nelle espressioni (utilizzando i tag `{%if%}` nell&#39;editor di personalizzazione) ≠ l&#39;aggiunta di contenuto dinamico nelle e-mail (creazione di varianti di componenti nel Designer e-mail — due flussi di lavoro distinti)
* **Non confondere:** &quot;Variante predefinita&quot; (visualizzata quando non sono soddisfatte regole condizionali) ≠ una variante denominata (ciascuna associata a una regola condizionale specifica)

>[!TAB Guardrail e limitazioni]

* Le varianti di contenuto condizionale vengono valutate in base alle regole associate nell’ordine in cui vengono visualizzate; la variante predefinita viene sempre visualizzata se non vengono soddisfatte altre condizioni.
* Durante la simulazione o il rendering delle bozze per le e-mail con più varianti condizionali, Journey Optimizer potrebbe richiedere più tempo di elaborazione; valuta di ridurre il numero di varianti o di semplificare le regole condizionali in caso di timeout o errori.
* Se il rendering di E-mail Designer non riesce dopo l’aggiunta di blocchi condizionali, verifica che la sintassi di ciascuna condizione sia corretta e che non esistano istruzioni duplicate o in conflitto.

>[!TAB Domande frequenti]

**D: cosa succede se nessuna delle condizioni definite viene soddisfatta al momento dell&#39;invio del messaggio?**

Il componente contenuto visualizza il contenuto definito nella variante predefinita.

**Q: in quale ordine vengono valutate le varianti di contenuto condizionale?**

Le varianti vengono valutate in base alle regole associate nell’ordine in cui vengono visualizzate. La variante predefinita viene sempre visualizzata se non sono soddisfatte altre condizioni.

**Q: dove è possibile aggiungere contenuto dinamico in Journey Optimizer?**

In qualsiasi campo in cui è possibile aggiungere la personalizzazione, incluse le righe dell’oggetto, i collegamenti, il contenuto delle notifiche push e le rappresentazioni delle offerte di tipo testo, tramite l’editor di personalizzazione e nei componenti di contenuto E-mail Designer tramite varianti condizionali.

**D: cosa devo fare se il rendering di E-mail Designer non riesce dopo l&#39;aggiunta di blocchi condizionali?**

Verifica che la sintassi di ciascuna condizione sia corretta e che non esistano istruzioni duplicate o in conflitto. Se i problemi persistono, ricompila le sezioni problematiche in un nuovo modello e testa ogni blocco condizionale in modo incrementale.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: e6005d80 -->
