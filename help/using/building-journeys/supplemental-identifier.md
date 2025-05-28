---
title: Identificatore supplementare nei percorsi attivati da eventi
description: Scopri come utilizzare l’identificatore supplementare nei percorsi attivati da eventi.
badge: label="Disponibilità limitata" type="Informative"
exl-id: f6ebd706-4402-448a-a538-e9a4c2cf0f8b
source-git-commit: e7f4959ceaa238e39858196b08d739053b21835c
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 7%

---

# Identificatore supplementare nei percorsi attivati da eventi {#supplemental-id}

>[!CONTEXTUALHELP]
>id="ajo_journey_parameters_supplemental_identifier"
>title="Usare un identificatore supplementare"
>abstract="L’identificatore supplementare è un identificatore secondario che fornisce contesto aggiuntivo per l’esecuzione di un percorso. Per definirlo, seleziona il campo da utilizzare come identificatore supplementare e scegli uno spazio dei nomi da associare."

>[!AVAILABILITY]
>
>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per ottenere l’accesso, contatta il tuo rappresentante Adobe.

Per impostazione predefinita, i percorsi attivati da eventi vengono eseguiti nel contesto di un **ID profilo**. Questo significa che, se il profilo è attivo in un dato percorso, non potrà rientrare in un altro percorso. Per evitare questo problema, Journey Optimizer ti consente di acquisire un **identificatore supplementare** negli eventi, ad esempio un ID ordine, un ID abbonamento, un ID prescrizione, oltre all&#39;ID profilo.
In questo esempio, è stato aggiunto un ID prenotazione come identificatore supplementare.

![](assets/event-supplemental-id.png){width=40% zoomable}

In questo modo, i percorsi attivati dall’evento vengono eseguiti nel contesto dell’ID profilo associato all’identificatore supplementare (in questo caso, l’ID prenotazione). Viene eseguita un’istanza del percorso per ogni iterazione dell’identificatore supplementare. Questo consente più ingressi dello stesso ID profilo nei percorsi se sono state effettuate prenotazioni diverse.

Inoltre, Journey Optimizer consente di sfruttare gli attributi dell’identificatore supplementare (ad esempio, numero di prenotazione, data di rinnovo della prescrizione, tipo di prodotto) per la personalizzazione dei messaggi, garantendo comunicazioni altamente pertinenti. <!--Example: A healthcare provider can send renewal reminders for each prescription in a patient's profile.-->

## Guardrail e limitazioni

* **Limiti di istanze simultanee**: i profili non possono avere più di 10 istanze di percorso simultanee.

<!--* **Array depth**: Supplemental identifier objects can have a maximum depth of 3 levels (2 levels of nesting).

    +++Example

    ```
    [
    (level 1) "Atorvastatin" : {
    "description" : "used to lower cholesterol",
    "renewal_date" : "11/20/25",
    "dosage" : "10mg"
    (level 2) "ingredients" : [
    (level 3) "Atorvastatin calcium",
    "lactose monohydrate",
    "microcrystalline cellulose",
    "other" ]
    }
    ]
    ```

    +++
-->
* **Criteri di uscita**: se attivato, il criterio di uscita determinerebbe l&#39;uscita dal percorso di tutte le istanze del profilo. Non sarebbe contestuale alla combinazione di ID profilo + identificatore supplementare.

* **Regole di frequenza**: ogni istanza di percorso creata da conteggi di utilizzo dell&#39;identificatore supplementari ai limiti di frequenza, anche se un singolo evento genera più istanze di percorso.

* **Tipo di dati e struttura dello schema**: l&#39;identificatore supplementare deve essere di tipo `string`. Può essere un attributo di stringa indipendente oppure un attributo di stringa all&#39;interno di una matrice di oggetti. L&#39;attributo di stringa indipendente darà luogo a una singola istanza di percorso, mentre l&#39;attributo di stringa all&#39;interno di una matrice di oggetti darà luogo a un&#39;istanza di percorso univoca per iterazione della matrice di oggetti. Gli array di stringhe e le mappe non sono supportati.

## Aggiungere un identificatore supplementare e sfruttarlo in un percorso

Per utilizzare un identificatore supplementare in un percorso, effettua le seguenti operazioni:

1. **Contrassegna l&#39;attributo come identificatore nello schema evento**

   1. Accedi allo schema dell’evento e individua l’attributo che desideri utilizzare come identificatore supplementare (ad esempio, ID prenotazione, ID abbonamento) e contrassegnalo come ID. [Scopri come utilizzare gli schemi](../data/get-started-schemas.md)

   1. Contrassegna l&#39;identificatore come **[!UICONTROL Identità]**.

      ![](assets/supplemental-ID-schema.png)

      >[!IMPORTANT]
      >
      >Assicurarsi di non contrassegnare l&#39;attributo come **Identità primaria**.

   1. Seleziona lo spazio dei nomi da associare all’ID supplementare. Deve essere uno spazio dei nomi non relativo all’identificatore della persona.

1. **Aggiungi l&#39;ID supplementare all&#39;evento**

   1. Crea o modifica l’evento desiderato. [Scopri come configurare un evento unitario](../event/about-creating.md)

   1. Nella schermata di configurazione dell&#39;evento, selezionare l&#39;opzione **[!UICONTROL Usa identificatore supplementare]**.

      ![](assets/supplemental-ID-event.png)

   1. Utilizza l’editor espressioni per selezionare l’attributo contrassegnato come ID supplementare.

   1. Dopo aver selezionato l’ID supplementare, lo spazio dei nomi associato viene visualizzato nella schermata di configurazione dell’evento come di sola lettura.

1. **Aggiungi l&#39;evento al percorso**

   Trascina l’evento configurato nell’area di lavoro del percorso. Attiva la voce percorso in base sia all’ID profilo che all’ID supplementare.

   ![](assets/supplemental-ID-journey.png)

1. **Utilizzo degli attributi ID supplementari**

   Utilizza l’editor di espressioni e l’editor di personalizzazione per fare riferimento agli attributi dell’identificatore supplementare per la personalizzazione o la logica condizionale. Gli attributi sono accessibili dal menu **[!UICONTROL Attributi contestuali]**.

   ![](assets/supplemental-ID-perso.png)

   >[!NOTE]
   >
   >Se utilizzi array (ad esempio, più prescrizioni o criteri), utilizza una formula per estrarre elementi specifici.

+++ Vedi esempi

   In un array di oggetti con ID supplementare come `bookingNum` e un attributo allo stesso livello denominato `bookingCountry`, il percorso eseguirà un&#39;iterazione nell&#39;oggetto array in base al bookingNum e creerà un&#39;istanza di percorso per ogni oggetto.

   * L&#39;espressione seguente nell&#39;attività condizione eseguirà un&#39;iterazione nella matrice di oggetti e verificherà se il valore di `bookingCountry` è uguale a &quot;FR&quot;:

     ```
     @event{<event_name>.<object_path>.<object_array_name>.all(currentEventField.<attribute_path>.bookingNum==${supplementalId}).at(0).<attribute_path>.bookingCountry}=="FR"
     ```

   * L&#39;espressione seguente nell&#39;editor di personalizzazione e-mail eseguirà un&#39;iterazione nell&#39;array di oggetti, estrae `bookingCountry` applicabile all&#39;istanza di percorso corrente e lo visualizza nel contenuto:

     ```
     {{#each context.journey.events.<event_ID>.<object_path>.<object_array_name> as |l|}} 
     
     {%#if l.<attribute_path>.bookingNum = context.journey.technicalProperties.supplementalId%} {{l.<attribute_path>.bookingCountry}}  {%/if%}
     
     {{/each}}
     ```

   * Esempio dell’evento utilizzato per attivare il percorso:

     ```
     "bookingList": [
           {
               "bookingInfo": {
                   "bookingNum": "x1",
                         "bookingCountry": "US"
               }
           },
           {
               "bookingInfo": {
                   "bookingNum": "x2",
                   "bookingCountry": "FR"
               }
           }
       ]
     ```

+++

1. **Pubblica il percorso**

   Una volta configurato, pubblica il percorso per iniziare a utilizzare più voci simultanee in base a identificatori supplementari.

## Casi d’uso di esempio

### **Notifiche di rinnovo criteri**

* **Scenario**: un provider di assicurazioni invia promemoria di rinnovo per ogni polizza attiva detenuta da un cliente.
* **Esecuzione**:
   * Voce principale: John.
   * ID supplementari: `"AutoPolicy123", "HomePolicy456"`.
   * Il percorso viene eseguito separatamente per ogni criterio, con date di rinnovo personalizzate, dettagli sulla copertura e informazioni sui premi.

### **Gestione abbonamenti**

* **Scenario**: un servizio di sottoscrizione invia messaggi personalizzati per ogni sottoscrizione quando viene attivato un evento per tale sottoscrizione.
* **Esecuzione**:
   * Voce principale: Jane.
   * ID supplementari: `"Luma Yoga Program ", "Luma Fitness Program"`.
   * Ogni evento include un ID abbonamento e i dettagli relativi a tale abbonamento. Il percorso viene eseguito separatamente per ogni evento/abbonamento, consentendo offerte di rinnovo personalizzate per abbonamento.

### **Consigli di prodotto**

* **Scenario**: una piattaforma di e-commerce invia consigli basati su prodotti specifici acquistati da un cliente.
* **Esecuzione**:
   * Voce principale: Alex.
   * ID supplementari: `"productID1234", "productID5678"`.
   * Il percorso viene eseguito separatamente per ciascun prodotto, con opportunità di upselling personalizzate.
