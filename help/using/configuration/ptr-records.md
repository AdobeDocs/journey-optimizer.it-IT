---
solution: Journey Optimizer
product: journey optimizer
title: Record PTR
description: Scopri come gestire i record PTR
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 4c930792-0677-4ad5-a46c-8d40fc3c4d3a
source-git-commit: 0f69a47dccad20f3e978613b349a29f9daab94bd
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 0%

---

# Record PTR {#ptr-records}

>[!CONTEXTUALHELP]
>id="ajo_admin_ptr_record"
>title="Record PTR dei sottodomini"
>abstract="Un record puntatore (PTR) è un tipo di record DNS che fornisce il nome di dominio collegato a un indirizzo IP, in modo che i server di posta riceventi possano verificare gli indirizzi IP dei mittenti. Modifica un record PTR solo dopo le dovute considerazioni e discuti con il tuo esperto di recapito messaggi."

>[!CONTEXTUALHELP]
>id="ajo_admin_ptr_record_header"
>title="Record PTR dei sottodomini"
>abstract="Una volta delegato un sottodominio ad Adobe in Journey Optimizer, un record PTR viene creato automaticamente e associato a questo sottodominio."

## Informazioni sui record PTR {#about-ptr-records}

Un record puntatore (PTR) è un tipo di record DNS (Domain Name System) che fornisce il nome di dominio collegato a un indirizzo IP.

Con i record PTR, i server di posta riceventi possono controllare l&#39;autenticità dei server di posta inviati identificando se i loro indirizzi IP corrispondono ai nomi a cui i server si connettono.

## Accedere ai record PTR dei tuoi sottodomini {#access-ptr-records}

Una volta [viene delegato un sottodominio](delegate-subdomain.md) in Adobe Journey Optimizer, un record PTR viene creato automaticamente e associato a questo sottodominio. Puoi accedervi dalla **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL PTR records]** menu.

![](assets/ptr-records.png)

L’elenco mostra i record PTR generati per ciascun sottodominio delegato, utilizzando la sintassi seguente:

* &quot;r&quot; per la registrazione,
* &quot;xx&quot; per le ultime due cifre dell’indirizzo IP,
* nome del sottodominio.

Puoi aprire un record PTR dall’elenco per visualizzare il nome del sottodominio e l’indirizzo IP associati.

## Modificare un record PTR {#edit-ptr-record}

Puoi modificare un record PTR per modificare il sottodominio associato a un indirizzo IP.

>[!CAUTION]
>
>I record PTR sono comuni a tutti gli ambienti. Pertanto, qualsiasi modifica apportata a un record PTR influisce anche sulle sandbox di produzione.
>
>Procedi con molta attenzione durante la modifica dei record PTR. In caso di dubbio, contatta un esperto di recapito.

### Sottodomini completamente delegati {#fully-delegated-subdomains}

Per modificare un record PTR con un sottodominio [completamente delegato](delegate-subdomain.md#full-subdomain-delegation) ad Adobe, segui i passaggi seguenti.

1. Dall’elenco, fai clic sul nome di un record PTR per aprirlo.

   ![](assets/ptr-record-select.png)

1. Selezionare un sottodominio [completamente delegato](delegate-subdomain.md#full-subdomain-delegation) dall’elenco ad Adobe.

   ![](assets/ptr-record-subdomain.png)

1. Fai clic su **[!UICONTROL Save]** per confermare le modifiche.

>[!NOTE]
>
>Non è possibile modificare il **[!UICONTROL IP]** e **[!UICONTROL PTR record]** campi.

### Sottodomini delegati che utilizzano il metodo CNAME {#edit-ptr-subdomains-cname}

Per modificare un record PTR con un sottodominio delegato ad Adobe utilizzando [metodo CNAME](delegate-subdomain.md#cname-subdomain-delegation), segui i passaggi seguenti.

1. Dall’elenco, fai clic sul nome di un record PTR per aprirlo.

   ![](assets/ptr-record-select-cname.png)

1. Seleziona un sottodominio delegato ad Adobe utilizzando [metodo CNAME](delegate-subdomain.md#cname-subdomain-delegation) dall&#39;elenco.

   ![](assets/ptr-record-subdomain-cname.png)

1. È necessario creare un nuovo record DNS inoltrato sulla piattaforma di hosting. A questo scopo, copia il record generato da Adobe. Una volta fatto, seleziona la casella &quot;Confermo..&quot;.

   ![](assets/ptr-record-subdomain-confirm.png)

   >[!NOTE]
   >
   >Se ricevi questo messaggio: &quot;Crea prima il DNS di inoltro e poi riprova&quot;, segui i passaggi seguenti:
   >   * Controlla il provider DNS se il record DNS in inoltro è stato creato correttamente.
   >   * I record nel DNS potrebbero non essere sincronizzati immediatamente. Attendere qualche minuto e riprovare.


1. Fai clic su **[!UICONTROL Save]** per confermare le modifiche.

>[!NOTE]
>
>Non è possibile modificare il **[!UICONTROL IP]** e **[!UICONTROL PTR record]** campi.

## Controlla i dettagli dell&#39;aggiornamento del record PTR {#check-ptr-record-update}

Una volta confermata la modifica del record PTR, la **[!UICONTROL Processing]** accanto al nome del record PTR nell’elenco viene visualizzata l’icona .

![](assets/ptr-record-updating.png)

>[!NOTE]
>
>La [aggiornamento elaborazione](#processing) può richiedere fino a 3 ore.

Per controllare i dettagli dell&#39;aggiornamento del record PTR, fai clic sull&#39;icona accanto ad esso. Ulteriori informazioni sugli stati associati alle diverse icone in [questa sezione](#ptr-record-update-statuses).

![](assets/ptr-record-recent-update.png)

Puoi visualizzare informazioni quali lo stato dell’aggiornamento e le modifiche richieste.

![](assets/ptr-record-updates.png)

## Stato dell’aggiornamento del record PTR {#ptr-record-update-statuses}

Un aggiornamento del record PTR può avere i seguenti stati:

* ![](assets/do-not-localize/ptr-record-processing.png) **[!UICONTROL Processing]**: L&#39;aggiornamento del record PTR è stato inviato ed è in corso un processo di verifica.
* ![](assets/do-not-localize/ptr-record-success.png) **[!UICONTROL Success]**: Il record PTR aggiornato è stato verificato e il nuovo sottodominio è ora associato all’indirizzo IP.
* ![](assets/do-not-localize/ptr-record-failed.png) **[!UICONTROL Failed]**: Uno o più controlli non sono riusciti durante la verifica dell&#39;aggiornamento del record PTR.

### Elaborazione {#processing}

Verranno eseguiti diversi controlli di recapito per verificare che il nuovo sottodominio da associare all’indirizzo IP sia valido. Questo può richiedere fino a 3 ore.

>[!NOTE]
>
>Non è possibile modificare un record PTR mentre è in corso l&#39;aggiornamento. È comunque possibile fare clic sul suo nome, ma la **[!UICONTROL Subdomain]** Il campo è disabilitato. Le modifiche verranno applicate solo dopo il completamento dell&#39;aggiornamento.

Durante il processo di convalida, il vecchio sottodominio viene ancora associato all’indirizzo IP.

### Completato {#success}

Una volta completato il processo di convalida, il nuovo sottodominio viene associato automaticamente all’indirizzo IP.

### Non riuscito {#failes}

Se il processo di convalida non riesce, viene visualizzato il record PTR precedente. Il sottodominio valido precedentemente associato all’indirizzo IP rimane invariato.

I possibili tipi di errore di aggiornamento sono i seguenti:
* Errore durante la creazione di un nuovo DNS di inoltro per il record PTR
* Errore durante l&#39;aggiornamento del record
* Errore durante la riaggiunta delle affinità

In caso di errore durante l’aggiornamento, il record PTR diventa nuovamente modificabile. Puoi fare clic sul suo nome e aggiornare nuovamente il sottodominio.
