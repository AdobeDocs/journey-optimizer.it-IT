---
title: Creare contenuto in-app
description: Scopri come progettare contenuti in-app in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: in-app, messaggio, progettazione, formattazione
exl-id: 7d7aa721-96aa-4ebc-a51c-e693f893f34f
source-git-commit: 39953bb09a699ed4fd07db26a3f2e54f4e2cacd7
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 6%

---

# Creare contenuto in-app {#design-content}

Puoi modificare il contenuto in-app per configurare le opzioni dell’esperienza:

* In un **[!UICONTROL Campagna]**, dalla **[!UICONTROL Azione]** per configurare il contenuto del messaggio, fai clic sul pulsante **[!UICONTROL Modifica contenuto]** pulsante.

  ![](assets/edit-in-app-content.png)

* In un **[!UICONTROL Percorso]**, dal menu avanzato dell’app **[!UICONTROL Azione]**, puoi iniziare a progettare i contenuti con **[!UICONTROL Modifica contenuto]** pulsante.

  ![](assets/design_inapp_journey.png)

Il **[!UICONTROL Formattazione avanzata]** attiva/disattiva opzioni aggiuntive per personalizzare l’esperienza.

Una volta creato il messaggio in-app e definito e personalizzato il relativo contenuto, puoi rivederlo e attivarlo. Le notifiche verranno quindi inviate in base alla pianificazione della campagna. Per ulteriori informazioni, consulta [questa pagina](send-in-app.md).

## Layout dei messaggi {#message-layout}

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

Dalla sezione **Contenuto** , puoi definire e personalizzare: il contenuto della notifica e lo stile della **Chiudi** pulsante. Puoi anche aggiungere un file multimediale alla notifica in-app e i pulsanti di azione da questa scheda.

### Pulsante Chiudi {#close-button}

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

Il **[!UICONTROL Contenuti multimediali]** consente di aggiungere contenuti multimediali al messaggio in-app per creare un’esperienza coinvolgente per l’utente finale.

![](assets/in_app_content_3.png)

Digita l’URL del file multimediale o fai clic su **[!UICONTROL Seleziona risorse]** per aggiungere direttamente al messaggio in-app le risorse memorizzate nella libreria di risorse. [Ulteriori informazioni sulla gestione delle risorse](../content-management/assets-essentials.md).
Puoi anche aggiungere una **[!UICONTROL Testo alternativo]** per applicazioni di lettura dello schermo.

+++Altre opzioni con formattazione avanzata

Se il **[!UICONTROL Modalità di formattazione avanzata]** è attivato, è possibile personalizzare **[!UICONTROL Altezza massima]** e **[!UICONTROL Larghezza massima]** dei tuoi contenuti multimediali.

+++

### Intestazione e corpo {#title-body}

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

![](assets/in_app_content_6.png)

Il **[!UICONTROL Anteprima app]** consente di aggiungere uno sfondo dietro il messaggio in-app:

* Un file multimediale da un collegamento URL.

* Una risorsa dalla libreria Assets.

* Un colore di sfondo.

### Layout {#layout-options}

![](assets/in_app_content_7.png)

Il **[!UICONTROL Immagine di sfondo]** consente di aggiungere uno sfondo al messaggio in-app:

* Un file multimediale da un collegamento URL.

* Un colore di sfondo.

### Messaggio {#message-tab}

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
