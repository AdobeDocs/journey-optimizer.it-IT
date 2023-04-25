---
solution: Journey Optimizer
product: journey optimizer
title: Crea modelli di contenuto
description: Scopri come creare modelli per riutilizzare i contenuti nelle campagne e nei percorsi Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 327de13a-1c99-4d5e-86cf-8180fb7aaf23
source-git-commit: cda4c1d88fedc75c7fded9971e45fdc9740346c4
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 11%

---

# Utilizzare i modelli di contenuto  {#content-templates}

Per un processo di progettazione accelerato e migliorato, è possibile creare modelli autonomi per riutilizzare facilmente i contenuti personalizzati in [!DNL Journey Optimizer] campagne e percorsi.

Questa funzionalità consente agli utenti orientati ai contenuti di lavorare su modelli esterni a campagne o percorsi. Gli utenti di marketing possono quindi riutilizzare e adattare questi modelli di contenuto indipendenti all’interno dei propri percorsi o campagne.

Ad esempio, un utente all’interno dell’azienda è responsabile solo del contenuto e pertanto non ha accesso a campagne o percorsi. Tuttavia, questo utente può creare un modello e-mail che gli addetti al marketing della tua organizzazione potranno selezionare per l’uso in tutte le e-mail come punto di partenza.

➡️ [Scopri come creare e utilizzare i modelli in questo video](#video-templates)

>[!CAUTION]
>
>Per creare, modificare ed eliminare modelli di contenuto, è necessario disporre dei **[!DNL Manage Library Items]** autorizzazione inclusa nel **[!DNL Content Library Manager]** profilo di prodotto. [Ulteriori informazioni](../administration/ootb-product-profiles.md#content-library-manager)

## Accesso e gestione dei modelli {#access-manage-templates}

Per accedere all’elenco dei modelli di contenuto, seleziona **[!UICONTROL Gestione dei contenuti]** > **[!UICONTROL Modelli di contenuto]** dal menu a sinistra.

![](assets/content-template-list.png)

Tutti i modelli creati sulla sandbox corrente, da un percorso o da una campagna utilizzando [Salva come modello](#save-as-template) da **[!UICONTROL Modelli di contenuto]** menu - vengono visualizzati.

Puoi ordinare i modelli di contenuto per creazione o data di modifica. Puoi anche scegliere di visualizzare solo gli elementi creati o modificati.

![](assets/content-template-list-filters.png)

Per modificare un contenuto del modello, fai clic sull’elemento desiderato dall’elenco e seleziona **[!UICONTROL Modifica contenuto]**.

![](assets/content-template-list-edit.png)

Per eliminare un modello, seleziona l’icona del cestino accanto al modello desiderato.

![](assets/content-template-list-delete.png)

>[!NOTE]
>
>Quando un modello viene modificato o eliminato, le campagne o i percorsi, comprese le e-mail create utilizzando questo modello, non sono interessati.

## Crea modelli di contenuto {#create-content-templates}

>[!CONTEXTUALHELP]
>id="ajo_create_template"
>title="Definire un modello di contenuto personalizzato"
>abstract="Crea da zero un modello personalizzato autonomo per rendere i contenuti riutilizzabili in più percorsi e campagne."

Esistono due modi per creare modelli di contenuto:

* Crea da zero un modello di contenuto utilizzando la barra a sinistra **[!UICONTROL Modelli di contenuto]** menu. [Scopri come](#create-template-from-scratch)

* Durante la progettazione di un’e-mail all’interno di una campagna o di un percorso, salva il contenuto dell’e-mail come modello. [Scopri come](#save-as-template)

Una volta salvato, il modello di contenuto è disponibile per l’utilizzo in una campagna o in un percorso. Creato da zero o da un’e-mail precedente, ora puoi utilizzare questo modello durante la creazione di qualsiasi [email](get-started-email-design.md) entro [!DNL Journey Optimizer]. [Scopri come](email-templates.md)

>[!NOTE]
>
>* Le modifiche apportate ai modelli di contenuto non vengono propagate a campagne o percorsi, siano essi in diretta o in bozza.
>
>* Allo stesso modo, quando i modelli vengono utilizzati in una campagna o in un percorso, le modifiche apportate al contenuto della campagna e del percorso non influiscono sul modello di contenuto utilizzato in precedenza.


### Crea modello da zero {#create-template-from-scratch}

Per creare un modello di contenuto da zero, segui la procedura seguente.

1. Accedi all’elenco dei modelli di contenuto tramite **[!UICONTROL Gestione dei contenuti]** > **[!UICONTROL Modelli di contenuto]** menu a sinistra.

   ![](assets/content-template-list.png)

1. Seleziona **[!UICONTROL Crea modello]**.

1. Compila i dettagli del modello.

   ![](assets/content-template-details.png)

   >[!NOTE]
   >
   >Attualmente solo il **E-mail** canale e **HTML** sono supportati.

1. Per assegnare etichette di utilizzo dati personalizzate o di base al modello, seleziona **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni su Object Level Access Control (OLAC)](../administration/object-based-access.md).

1. Fai clic su **[!UICONTROL Crea]** e scegli come desideri progettare il tuo messaggio e-mail dalle diverse opzioni:

   * [Progettazione dell&#39;e-mail da zero](content-from-scratch.md) tramite l’interfaccia di E-mail Designer.

   * [Codice o copia-incolla raw HTML](code-content.md) direttamente in E-mail Designer.

   * [Importare contenuto HTML esistente](existing-content.md) da un file o da una cartella .zip.

   * Utilizza il contenuto esistente da un elenco di modelli incorporati o personalizzati. I passaggi per utilizzare un modello di contenuto in un’e-mail sono descritti in [questa sezione](email-templates.md).

   ![](assets/content-template-design.png)

1. La [E-mail Designer](get-started-email-design.md) viene visualizzato. Modifica il contenuto in base alle esigenze, nello stesso modo che faresti per qualsiasi e-mail all’interno di un percorso o di una campagna, in base all’opzione selezionata.

   Se necessario, puoi eseguire il test del contenuto. [Scopri come](#test-template)

1. Una volta pronto il modello, fai clic su **[!UICONTROL Salva]**.

1. Se necessario, fai clic sulla freccia accanto al nome del modello per tornare al **[!UICONTROL Dettagli]** visualizza e modifica il modello.

   ![](assets/content-template-designer-back.png)

Questo modello è ora pronto per essere utilizzato per la creazione di qualsiasi e-mail all’interno di [!DNL Journey Optimizer]. [Scopri come](email-templates.md)

### Salva come modello {#save-as-template}

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="Scopri come effettuare la migrazione dei messaggi"
>abstract="Il 25 luglio 2022 il menu Messaggi è stato rimosso e i messaggi vengono ora creati direttamente da un percorso. Per riutilizzare i messaggi precedenti nei percorsi, devi salvarli come modelli."

Durante la progettazione di un [email](get-started-email-design.md) in una campagna o in un percorso, puoi salvare il contenuto delle e-mail per riutilizzarlo in futuro. Per farlo, segui la procedura indicata di seguito.

1. In E-mail Designer, fai clic sull’ellissi in alto a destra dello schermo.

1. Seleziona **[!UICONTROL Salva come modello di contenuto]** dal menu a discesa.

   ![](assets/email_designer-save-template.png)

1. Aggiungi un nome e una descrizione per questo modello.

   ![](assets/email_designer-template-name.png)

1. Fai clic su **[!UICONTROL Salva]**.

1. Il modello viene salvato nel **[!UICONTROL Modelli di contenuto]** elenco, accessibile dal [!DNL Journey Optimizer] menu dedicato. Diventa un modello di contenuto autonomo accessibile, modificato ed eliminato come qualsiasi altro elemento di tale elenco. [Ulteriori informazioni](#access-manage-templates)

È ora possibile utilizzare questo modello durante la creazione di qualsiasi [email](get-started-email-design.md) entro [!DNL Journey Optimizer]. [Scopri come](email-templates.md)

>[!NOTE]
>
>Qualsiasi modifica a quel nuovo modello non viene propagata all’e-mail da cui proviene. Allo stesso modo, quando il contenuto originale viene modificato all’interno dell’e-mail, il nuovo modello non viene modificato.

## Test del modello di contenuto {#test-template}

Puoi verificare il rendering di qualsiasi modello di contenuto e-mail, creato da zero o da un’e-mail. A questo scopo, segui i passaggi riportati qui sotto.

>[!CAUTION]
>
>Per simulare il contenuto, è necessario disporre della **[!DNL Manage Simulate Content]** autorizzazione inclusa nel **[!DNL Content Library Manager]** profilo di prodotto. [Ulteriori informazioni](../administration/ootb-product-profiles.md#content-library-manager)

1. Accedi all’elenco dei modelli di contenuto tramite **[!UICONTROL Gestione dei contenuti]** > **[!UICONTROL Modelli di contenuto]** e selezionare un modello.

1. Fai clic su **[!UICONTROL Modifica contenuto]** dal **[!UICONTROL Proprietà del modello]**.

1. Fai clic su **[!UICONTROL Simula contenuto]** e seleziona un profilo di test per controllare il rendering delle e-mail. È possibile scegliere la visualizzazione su desktop o dispositivo mobile. [Ulteriori informazioni](preview.md)

   ![](assets/content-template-stimulate.png)

1. Puoi inviare una bozza per testare il contenuto e farla approvare da alcuni utenti interni prima di utilizzarla in un percorso o in una campagna.

   * A tale scopo, fai clic sul pulsante **[!UICONTROL Invia bozza]** e segui i passaggi descritti in [questa sezione](preview.md#send-proofs).

   * Prima di inviare la bozza, devi selezionare la [superficie e-mail](../configuration/channel-surfaces.md) che verrà utilizzato per testare il contenuto.

      ![](assets/content-template-stimulate-proof-surface.png)

## Video introduttivo {#video-templates}

Scopri come creare, modificare e utilizzare modelli di contenuto in [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3413743/?quality=12)
