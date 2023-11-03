---
title: Creare contenuto in-app
description: Scopri come progettare contenuti in-app in Journey Optimizer
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: in-app, messaggio, progettazione, formattazione
exl-id: 7d7aa721-96aa-4ebc-a51c-e693f893f34f
source-git-commit: 03c714833930511fa734662b637d2416728073c2
workflow-type: tm+mt
source-wordcount: '1147'
ht-degree: 29%

---

# Creare contenuto in-app {#design-content}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_content"
>title="Definire il contenuto in-app"
>abstract="Personalizza il contenuto e lo stile dei messaggi in-app. Puoi anche aggiungere pulsanti di azione e multimediali, per rendere i messaggi più coinvolgenti ed efficaci."

Puoi modificare il contenuto in-app per configurare le opzioni dell’esperienza:

* In un **[!UICONTROL Campagna]**, dalla **[!UICONTROL Azione]** per configurare il contenuto del messaggio, fai clic sul pulsante **[!UICONTROL Modifica contenuto]** pulsante.

  ![](assets/edit-in-app-content.png)

* In un **[!UICONTROL Percorso]**, dal menu avanzato dell’app **[!UICONTROL Azione]**, puoi iniziare a progettare i contenuti con **[!UICONTROL Modifica contenuto]** pulsante.

  ![](assets/design_inapp_journey.png)

Il **[!UICONTROL Formattazione avanzata]** attiva/disattiva opzioni aggiuntive per personalizzare l’esperienza.

Una volta creato il messaggio in-app e definito e personalizzato il relativo contenuto, puoi rivederlo e attivarlo. Le notifiche verranno quindi inviate in base alla pianificazione della campagna. Per ulteriori informazioni, consulta [questa pagina](send-in-app.md).

## Layout messaggio {#message-layout}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_message_layout"
>title="Definire il contenuto in-app"
>abstract="Il layout del messaggio fornisce modelli comunemente utilizzati per dare una struttura al messaggio. Il layout personalizzato fornisce opzioni per caricare o comporre messaggi HTML personalizzati."

Dalla sezione **[!UICONTROL Layout messaggio]** , seleziona una delle quattro opzioni di layout disponibili a seconda delle tue esigenze di messaggistica.

![](assets/in_app_content_1.png)

* **[!UICONTROL Schermo intero]**: questo tipo di layout copre l’intero schermo dei dispositivi per il pubblico.

  Supporta i componenti per contenuti multimediali (immagine, video), di testo e i pulsanti.

* **[!UICONTROL Modale]**: questo layout viene visualizzato in una grande finestra in stile avviso. L’applicazione rimane visibile in background.

  Supporta i componenti per contenuti multimediali (immagine, video), di testo e i pulsanti.

* **[!UICONTROL Banner]**: questo tipo di layout viene visualizzato come messaggio di avviso del sistema operativo nativo.

  È possibile aggiungere solo un **[!UICONTROL Intestazione]** e un **[!UICONTROL Corpo]** al messaggio.

* **[!UICONTROL Personalizzato]**: la modalità messaggio personalizzato ti consente di importare e modificare direttamente uno dei messaggi di HTML preconfigurati.

   * Seleziona **[!UICONTROL Componi]** per inserire o incollare il codice HTML non elaborato.

     Utilizza il riquadro a sinistra per sfruttare le funzionalità di personalizzazione di Journey Optimizer. Per ulteriori informazioni al riguardo, consulta [questa sezione](../personalization/personalize.md).

   * Seleziona **[!UICONTROL Importa]** per importare il file HTML o .zip contenente il contenuto HTML.

## Scheda Contenuto {#content-tab}

Dalla sezione **Contenuto** , puoi definire e personalizzare il contenuto della notifica e lo stile della **Chiudi** pulsante. Puoi anche aggiungere un file multimediale alla notifica in-app e i pulsanti di azione da questa scheda.

### Chiudi pulsante {#close-button}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_close"
>title="Scegli lo stile del pulsante Chiudi."
>abstract="La sezione del pulsante Chiudi consente di selezionare le varianti del pulsante di chiusura messaggi e fornisce l’opzione di caricare un’immagine personalizzata."

![](assets/in_app_content_2.png)

Scegli la **[!UICONTROL Stile]** del tuo **[!UICONTROL Pulsante Chiudi]**.

Gli stili disponibili sono:

* **[!UICONTROL Semplice]**
* **[!UICONTROL Cerchio]**
* **[!UICONTROL Immagine personalizzata]** da un URL multimediale o dalle risorse.

+++Altre opzioni con formattazione avanzata

Se il **[!UICONTROL Modalità di formattazione avanzata]** è acceso, è possibile controllare **[!UICONTROL Colore]** per scegliere il colore e l&#39;opacità del pulsante.

+++

### Media {#add-media}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_media"
>title="Aggiungi contenuti multimediali al messaggio in-app per creare un’esperienza coinvolgente per l’utente finale."
>abstract="Fornisci un collegamento diretto al contenuto oppure utilizza il selettore delle risorse per scegliere i contenuti multimediali da aggiungere al tuo messaggio in Asset Essentials."

Il **[!UICONTROL Contenuti multimediali]** consente di aggiungere contenuti multimediali al messaggio in-app per creare un’esperienza coinvolgente per l’utente finale.

![](assets/in_app_content_3.png)

Digita l’URL del file multimediale o fai clic su **[!UICONTROL Seleziona risorse]** per aggiungere direttamente al messaggio in-app le risorse memorizzate nella libreria di risorse. [Ulteriori informazioni sulla gestione delle risorse](../content-management/assets-essentials.md).
Puoi anche aggiungere una **[!UICONTROL Testo alternativo]** per applicazioni di lettura dello schermo.

+++Altre opzioni con formattazione avanzata

Se il **[!UICONTROL Modalità di formattazione avanzata]** è attivato, è possibile personalizzare **[!UICONTROL Altezza massima]** e **[!UICONTROL Larghezza massima]** dei tuoi contenuti multimediali.

+++

### Intestazione e corpo {#title-body}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_content"
>title="Per comporre il messaggio, immetti il contenuto nei campi Intestazione e Corpo."
>abstract="Qui è possibile aggiungere sia l’intestazione che il corpo del testo. Per includere i token di personalizzazione, apri la finestra di dialogo di personalizzazione."

Per comporre il messaggio, inserisci il contenuto nel **[!UICONTROL Intestazione]** e **[!UICONTROL Corpo]** campi.

![](assets/in_app_content_4.png)

Utilizza il **[!UICONTROL Personalizzazione]** per aggiungere la personalizzazione. Ulteriori informazioni sulla personalizzazione in Adobe Journey Optimizer Expression Editor [in questa sezione](../personalization/personalize.md).

+++Altre opzioni con formattazione avanzata

Se il **[!UICONTROL Modalità di formattazione avanzata]** è attivato, è possibile scegliere per il **[!UICONTROL Intestazione]** e **[!UICONTROL Corpo]**:

* il **[!UICONTROL Font]**
* il **[!UICONTROL Dimensione Pt]**
* il **[!UICONTROL Colore font]**
* il **[!UICONTROL Allineamento]**
+++

### Pulsanti {#add-buttons}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_buttons"
>title="Aggiungi i pulsanti che consentono agli utenti di interagire con il messaggio in-app."
>abstract="Questa sezione consente di aggiungere pulsanti di invito all’azione al messaggio. È possibile includere testo personalizzato e destinazioni per ogni pulsante."

Aggiungi i pulsanti che consentono agli utenti di interagire con il messaggio in-app.

![](assets/in_app_content_5.png)

Per personalizzare il pulsante:

1. Modificare il campo Testo #1 pulsante (primario). È inoltre possibile utilizzare **[!UICONTROL Personalizzazione]** per definire contenuti e dati di personalizzazione.

1. Scegli il tuo **[!UICONTROL Evento di interazione]** che definisce l’azione del pulsante dopo che gli utenti hanno interagito con esso.

1. Inserisci l’URL web o il collegamento diretto nel **[!UICONTROL Target]** campo.

1. Per aggiungere più pulsanti, fare clic su **[!UICONTROL Pulsante Aggiungi]**.

+++Altre opzioni con formattazione avanzata

Se il **[!UICONTROL Modalità di formattazione avanzata]** è attivato, è possibile scegliere per il **[!UICONTROL Pulsanti]**:

* il **[!UICONTROL Font]**
* il **[!UICONTROL Dimensione Pt]**
* il **[!UICONTROL Colore font]**
* il **[!UICONTROL Allineamento]**
* il **[!UICONTROL Stile pulsante]**
* il **[!UICONTROL Raggio]**
* il **[!UICONTROL Colore pulsante]**

+++

## Scheda Impostazioni {#settings-tab}

Dalla sezione **Impostazioni** , puoi definire il layout del messaggio e visualizzare in anteprima il messaggio in-app. Puoi anche accedere alle opzioni di formattazione avanzate.

### Anteprima {#preview-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_preview"
>title="Visualizza l’anteprima del messaggio in-app."
>abstract="Si tratta dell’immagine di anteprima che verrà visualizzata quando il messaggio viene inviato al riepilogo messaggi del dispositivo."

![](assets/in_app_content_6.png)

Il **[!UICONTROL Anteprima app]** consente di aggiungere uno sfondo dietro il messaggio in-app:

* Un file multimediale da un collegamento URL.

* Una risorsa dalla libreria Assets.

* Un colore di sfondo.

### Layout {#layout-options}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_layout"
>title="Definisci il layout messaggio del messaggio in-app."
>abstract="Questa sezione ti consente di aggiungere uno sfondo al messaggio in-app. Ciò richiede che l’acquisizione dell’interfaccia utente sia abilitata."

![](assets/in_app_content_7.png)

Il **[!UICONTROL Immagine di sfondo]** consente di aggiungere uno sfondo al messaggio in-app:

* Un file multimediale da un collegamento URL.

* Un colore di sfondo.

### Messaggio {#message-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_authoring_message_advanced"
>title="Definisci le impostazioni avanzate del messaggio."
>abstract="Questa sezione ti permette di migliorare la personalizzazione dei contenuti in-app, in particolare quando è abilitata la formattazione avanzata."

![](assets/in_app_content_8.png)

L’opzione di acquisizione dell’interfaccia utente, attivata per impostazione predefinita, consente di scurire lo sfondo dietro il messaggio in-app per evidenziare lo stato attivo sul contenuto.

+++Altre opzioni con formattazione avanzata

Se il **[!UICONTROL Modalità di formattazione avanzata]** è attivato, puoi personalizzare ulteriormente il messaggio con le seguenti opzioni:

* **[!UICONTROL Personalizzare i movimenti]**: consente di personalizzare l’interazione di scorrimento dell’utente. Se l&#39;opzione Ignora è selezionata, puoi aggiungere un evento di interazione personalizzato e/o una destinazione.

* **[!UICONTROL Personalizzare l’acquisizione dell’interfaccia utente]**: consente di selezionare un colore da visualizzare nello sfondo e la relativa opacità.

* **[!UICONTROL Personalizza dimensione]**: consente di regolare la larghezza e l’altezza della notifica in-app.

* **[!UICONTROL Personalizza posizione]**: consente di personalizzare la posizione dei messaggi in-app sullo schermo degli utenti. È possibile modificare l&#39;allineamento verticale e orizzontale.

* **[!UICONTROL Personalizzare l&#39;animazione]**: consente di personalizzare le animazioni Display (Visualizzazione) e Dismiss (Ignora), ad esempio se la notifica in-app viene visualizzata da sinistra o dall’alto del dispositivo dell’utente.

* **[!UICONTROL Angolo rotondo del messaggio]**: consente di aggiungere un angolo rotondo alla notifica in-app modificando il **[!UICONTROL Raggio angolo]**.

+++

**Argomenti correlati:**

* [Creare un messaggio in-app](create-in-app.md)
* [Rapporto in-app](../reports/campaign-global-report.md#inapp-report)
* [Configurazione in-app](inapp-configuration.md)

## Video introduttivo{#video}

Il video seguente mostra come creare e testare i messaggi in-app.

>[!VIDEO](https://video.tv.adobe.com/v/3410471?quality=12&learn=on)
