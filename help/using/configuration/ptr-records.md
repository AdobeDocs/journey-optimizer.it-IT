---
title: Record PTR
description: Scopri come gestire i record PTR
audience: administrators
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 4c930792-0677-4ad5-a46c-8d40fc3c4d3a
source-git-commit: cbb9aa1df7efd60407f4538edf519d96780c4961
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---

# Record PTR

## Informazioni sui record PTR

Un record puntatore (PTR) è un tipo di record DNS (Domain Name System) che fornisce il nome di dominio collegato a un indirizzo IP.

Con i record PTR, i server di posta riceventi possono controllare l&#39;autenticità dei server di posta inviati identificando se i loro indirizzi IP corrispondono ai nomi con cui i server si connettono.

## Accedere ai record PTR dei tuoi sottodomini

Una volta [viene delegato un sottodominio](delegate-subdomain.md) in Adobe Journey Optimizer, viene creato automaticamente un record PTR associato a questo sottodominio. Puoi accedervi dalla **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL PTR records]** menu.

![](../assets/ptr-records.png)

L’elenco mostra i record PTR generati per ciascun sottodominio delegato, utilizzando la sintassi seguente:

* &quot;r&quot; per la registrazione,
* &quot;xx&quot; per le ultime due cifre dell’indirizzo IP,
* nome del sottodominio.

Puoi aprire un record PTR dall’elenco per visualizzare il nome del sottodominio e l’indirizzo IP associati.

## Modificare un record PTR {#edit-ptr-record}

Puoi modificare un record PTR per modificare il sottodominio associato a un indirizzo IP.

>[!NOTE]
>
>Non è possibile modificare il **[!UICONTROL IP]** e **[!UICONTROL PTR record]** campi.

### Sottodomini completamente delegati

Per modificare un record PTR con un sottodominio [completamente delegato](delegate-subdomain.md#full-subdomain-delegation) ad Adobe, segui i passaggi seguenti.

1. Dall’elenco, fai clic sul nome di un record PTR per aprirlo.

   ![](../assets/ptr-record-select.png)

1. Selezionare un sottodominio [completamente delegato](delegate-subdomain.md#full-subdomain-delegation) all&#39;Adobe dall&#39;elenco.

   ![](../assets/ptr-record-subdomain.png)

1. Fai clic su **[!UICONTROL Save]** per confermare le modifiche.

### Sottodomini delegati che utilizzano il metodo CNAME {#edit-ptr-subdomains-cname}

Per modificare un record PTR con un sottodominio delegato ad Adobe utilizzando [metodo CNAME](delegate-subdomain.md#cname-subdomain-delegation), segui i passaggi seguenti.

1. Dall’elenco, fai clic sul nome di un record PTR per aprirlo.

   ![](../assets/ptr-record-select-cname.png)

1. Seleziona un sottodominio delegato ad Adobe utilizzando [metodo CNAME](delegate-subdomain.md#cname-subdomain-delegation) dall&#39;elenco.

   ![](../assets/ptr-record-subdomain-cname.png)

1. È necessario creare un nuovo record DNS inoltrato sulla piattaforma di hosting. A questo scopo, copia il record generato da Adobe. Una volta fatto, seleziona la casella &quot;Confermo..&quot;.

   ![](../assets/ptr-record-subdomain-confirm.png)

   >[!NOTE]
   >
   >Se ricevi questo messaggio: &quot;Crea prima il DNS di inoltro e poi riprova&quot;, segui i passaggi seguenti:
   >   * Controlla il provider DNS se il record DNS in inoltro è stato creato correttamente.
   >   * I record nel DNS potrebbero non essere sincronizzati immediatamente. Attendere qualche minuto e riprovare.


1. Fai clic su **[!UICONTROL Save]** per confermare le modifiche.

## Controlla i dettagli dell&#39;aggiornamento del record PTR

A **[!UICONTROL Processing]** accanto al nome del record PTR nell’elenco viene visualizzata l’icona .

![](../assets/ptr-record-updating.png)

Per controllare i dettagli dell&#39;aggiornamento del record PTR, fai clic sul pulsante **[!UICONTROL Updating]** o **[!UICONTROL Recent updates]** icona.

![](../assets/ptr-record-recent-update.png)

Puoi visualizzare informazioni quali lo stato dell’aggiornamento e le modifiche richieste.

![](../assets/ptr-record-updates.png)

## Stato dell’aggiornamento del record PTR

Un aggiornamento del record PTR può avere i seguenti stati:

* ![](../assets/do-not-localize/ptr-record-processing.png) **[!UICONTROL Processing]**: L&#39;aggiornamento del record PTR è stato inviato ed è in corso un processo di verifica.
* ![](../assets/do-not-localize/ptr-record-success.png) **[!UICONTROL Success]**: Il record PTR aggiornato è stato verificato e il nuovo sottodominio è ora associato all’indirizzo IP.
* ![](../assets/do-not-localize/ptr-record-failed.png) **[!UICONTROL Failed]**: Uno o più controlli non sono riusciti durante la verifica dell&#39;aggiornamento del record PTR.

### Elaborazione

Verranno eseguiti diversi controlli di recapito per verificare che il nuovo sottodominio da associare all’indirizzo IP sia valido. <!--The processing time is around **48h-72h**, and can take up to **7-10 days**. Learn more on the checks performed during the validation cycle in [this section](#create-message-preset).-->

>[!NOTE]
>
>Non è possibile modificare un record PTR mentre è in corso l&#39;aggiornamento. È comunque possibile fare clic sul suo nome, ma la **[!UICONTROL Subdomain]** Il campo è disabilitato. Le modifiche verranno applicate solo dopo il completamento dell&#39;aggiornamento.

Durante il processo di convalida, il vecchio sottodominio viene ancora associato all’indirizzo IP.

### Operazione riuscita

Una volta completato il processo di convalida, il nuovo sottodominio viene associato automaticamente all’indirizzo IP.

### Non riuscito

Se il processo di convalida non riesce, viene visualizzato il record PTR precedente. Il sottodominio valido precedentemente associato all’indirizzo IP rimane invariato.

I possibili tipi di errore di aggiornamento sono i seguenti:
* Errore durante la creazione di un nuovo DNS di inoltro per il record PTR
* Errore durante l&#39;aggiornamento del record
* Errore durante la riaggiunta delle affinità

In caso di errore durante l’aggiornamento, il record PTR diventa nuovamente modificabile. Puoi fare clic sul suo nome e aggiornare nuovamente il sottodominio.
