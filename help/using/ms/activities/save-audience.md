---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Save audience
description: Scopri come utilizzare l’attività Fork in una campagna orchestrata
hide: true
hidefromtoc: true
exl-id: 84e34d21-dca1-4203-8539-f2b20e461936
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 63%

---

# Salva pubblico {#save-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="Salva un pubblico"
>abstract="Utilizza questa attività per aggiornare un pubblico esistente o crearne uno nuovo dalla popolazione calcolata a monte nella campagna orchestrata. I tipi di pubblico creati vengono aggiunti all’elenco dei tipi di pubblico e sono disponibili tramite il menu **Tipi di pubblico**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_saveaudience_outbound"
>title="Genera transizione in uscita"
>abstract="Utilizza questa opzione se desideri aggiungere una transizione dopo l’attività **Salva pubblico**."

L’attività **Salva pubblico** è un’attività di **targeting**. Questa attività ti consente di aggiornare un pubblico esistente o crearne uno nuovo dalla popolazione calcolata a monte in una campagna orchestrata. I tipi di pubblico creati vengono aggiunti all’elenco dei tipi di pubblico delle applicazioni e sono disponibili tramite il menu **Tipi di pubblico**.

Questa attività è essenzialmente utilizzata per mantenere i gruppi di popolazione calcolati nella stessa campagna orchestrata, convertendoli in tipi di pubblico riutilizzabili. Connettila ad altre attività di targeting, come a un’attività **Crea pubblico** o **Combina**.

## Configurare l’attività Salva pubblico{#save-audience-configuration}

Per configurare l’attività **Salva pubblico**, segui questi passaggi:

![](../assets/workflow-save-audience.png)

1. Aggiungi un&#39;attività **Save audience** alla campagna orchestrata.

1. Nell’elenco a discesa **Modalità**, seleziona l’azione da eseguire:

   * **Crea o aggiorna un pubblico esistente**: definisci un’**etichetta del pubblico**. Se il pubblico esiste già, verrà aggiornato; altrimenti verrà creato un nuovo pubblico.

   * **Aggiorna un pubblico esistente**: scegli il **Pubblico** che desideri aggiornare dall’elenco dei tipi di pubblico esistenti.

1. Seleziona la **Modalità di aggiornamento** che verrà applicata ai tipi di pubblico esistenti:

   * **Sostituisci il contenuto del pubblico con nuovi dati**: viene sostituito tutto il contenuto del pubblico. I vecchi dati vanno perduti. Vengono conservati solo i dati della transizione in entrata dell’attività Salva pubblico. Questa opzione elimina il tipo di pubblico e la dimensione di targeting del pubblico aggiornato.

   * **Completa il pubblico con i nuovi dati**: il vecchio contenuto del pubblico viene conservato e vi vengono aggiunti i dati della transizione in entrata dell’attività Salva pubblico.

1. Seleziona l’opzione **Genera una transizione in uscita** se desideri aggiungere una transizione dopo l’attività **Salva pubblico**.

Il contenuto del pubblico salvato è quindi disponibile nella relativa visualizzazione dettagliata, accessibile dal menu **Tipi di pubblico**. Le colonne disponibili in questa visualizzazione corrispondono alle colonne della transizione in entrata dell&#39;attività **Save audience** della campagna orchestrata.


## Esempio{#save-audience-example}

L’esempio seguente illustra un semplice aggiornamento del pubblico dal targeting. Viene aggiunto un modulo di pianificazione per eseguire la campagna orchestrata una volta al mese. Una query recupera tutti i profili abbonati alle diverse applicazioni disponibili. L&#39;attività **Save audience** aggiorna il pubblico eliminando i profili che hanno annullato l&#39;abbonamento al servizio dall&#39;ultima esecuzione della campagna orchestrata e aggiungendo i nuovi profili abbonati.
