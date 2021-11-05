---
title: Record PTR
description: Scopri come gestire i record PTR
audience: administrators
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 4c930792-0677-4ad5-a46c-8d40fc3c4d3a
source-git-commit: 1e62715f35b50bba639657a1bef37aa61922c715
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# Record PTR

## Informazioni sui record PTR

Un record puntatore (PTR) è un tipo di record DNS (Domain Name System) che fornisce il nome di dominio collegato a un indirizzo IP.

Con i record PTR, i server di posta riceventi possono controllare l&#39;autenticità dei server di posta inviati identificando se i loro indirizzi IP corrispondono ai nomi con cui i server si connettono.

## Accedere ai record PTR dei tuoi sottodomini

Una volta delegato un sottodominio in Adobe Journey Optimizer, un record PTR viene creato automaticamente e associato a questo sottodominio. Puoi accedervi dalla **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL PTR records]** menu.

![](../assets/ptr-records.png)

L’elenco mostra i record PTR generati per ciascun sottodominio delegato, utilizzando la sintassi seguente:

* &quot;r&quot; per la registrazione,
* &quot;xx&quot; per le ultime due cifre dell’indirizzo IP,
* nome del sottodominio.

Puoi aprire un record PTR dall’elenco per visualizzare il nome del sottodominio e l’indirizzo IP associati.

## Modificare un record PTR {#edit-ptr-record}

Puoi modificare un record PTR per modificare il sottodominio associato a un indirizzo IP.

1. Dall’elenco, fai clic sul nome di un record PTR per aprirlo.

   ![](../assets/ptr-record-select.png)

1. Modifica il sottodominio come desiderato.

   ![](../assets/ptr-record-subdomain.png)

   >[!NOTE]
   >
   >Non è possibile modificare il **[!UICONTROL IP]** e **[!UICONTROL PTR record]** campi.

1. Fai clic su **[!UICONTROL SAve]** per confermare le modifiche.

Un **[!UICONTROL Updating]** accanto al nome del record PTR nell’elenco viene visualizzata l’icona .

![](../assets/ptr-record-updating.png)

Per controllare i dettagli dell&#39;aggiornamento del record PTR, fai clic sul pulsante **[!UICONTROL Updating]** o **[!UICONTROL Recent updates]** icona.

![](../assets/ptr-record-recent-update.png)

Puoi visualizzare informazioni quali lo stato dell’aggiornamento e le modifiche richieste.

![](../assets/ptr-record-updates.png)

## Aggiorna stati

Un aggiornamento del record PTR può avere i seguenti stati:

* **[!UICONTROL Processing]**: L&#39;aggiornamento del record PTR è stato inviato ed è in corso un processo di verifica.
* **[!UICONTROL Success]**: Il record PTR aggiornato è stato verificato e il nuovo sottodominio è ora associato all’indirizzo IP.
* **[!UICONTROL Failed]**: Uno o più controlli non sono riusciti durante la verifica dell&#39;aggiornamento del record PTR.

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
