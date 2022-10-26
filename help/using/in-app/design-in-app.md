---
title: Progettazione di contenuti in-app
description: Scopri come progettare il contenuto in-app in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: e7431d1b69e460471b01439c9bd2577fd69944ed
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 4%

---

# Progettazione di contenuti in-app {#design-content}

Puoi modificare il contenuto in-app per configurare le opzioni relative all’esperienza, tra cui layout e visualizzazione dei messaggi, testo e pulsanti.

Per configurare il contenuto del messaggio, fai clic sul pulsante **[!UICONTROL Modifica contenuto]** e utilizza le opzioni nella sezione destra dello schermo per progettare il contenuto dei messaggi in-app.

![](assets/edit-in-app-content.png)

La **[!UICONTROL Formattazione avanzata]** attiva le opzioni aggiuntive per personalizzare l’esperienza.

Una volta creato il messaggio in-app e il relativo contenuto definito e personalizzato, puoi rivederlo e attivarlo. Le notifiche vengono quindi inviate in base alla pianificazione della campagna. Per ulteriori informazioni, consulta [questa pagina](create-in-app.md#in-app-send).

## Layout dei messaggi {#message-layout}

Da **[!UICONTROL Layout dei messaggi]** seleziona una delle quattro opzioni di layout disponibili a seconda delle esigenze di messaggistica.

![](assets/in_app_content_1.png)

* **[!UICONTROL Schermo intero]**: Questo tipo di layout copre l’intero schermo dei dispositivi per il pubblico.

   Supporta i componenti per contenuti multimediali (immagine, video), di testo e i pulsanti.

* **[!UICONTROL modale]**: Questo layout viene visualizzato in una grande finestra in stile avviso, l&#39;applicazione rimane visibile in background.

   Supporta i componenti per contenuti multimediali (immagine, video), di testo e i pulsanti.

* **[!UICONTROL Banner]**: Questo tipo di layout viene visualizzato come messaggio di avviso del sistema operativo nativo.

   È possibile aggiungere solo un **[!UICONTROL Intestazione]** e **[!UICONTROL Corpo]** al tuo messaggio.

* **[!UICONTROL Personalizzato]**: La modalità messaggio personalizzata consente di importare e modificare direttamente uno dei messaggi HTML preconfigurati.

   * Seleziona **[!UICONTROL Componi]** per immettere o incollare il codice grezzo di HTML.

      Utilizza il riquadro a sinistra per sfruttare le funzionalità di personalizzazione di Journey Optimizer. Per ulteriori informazioni al riguardo, consulta [questa sezione](../personalization/personalize.md).

   * Seleziona **[!UICONTROL Importa]** per importare il file HTML o .zip contenente il contenuto HTML.

## Scheda Contenuto {#content-tab}

Da **Contenuto** puoi definire e personalizzare: il contenuto della notifica e lo stile della **Chiudi** pulsante . Puoi anche aggiungere un file multimediale alla notifica in-app e i pulsanti di azione da questa scheda.

### Pulsante Chiudi {#close-button}

![](assets/in_app_content_2.png)

Scegli la **[!UICONTROL Stile]** del tuo **[!UICONTROL Pulsante Chiudi]**.

Gli stili disponibili sono:

* **[!UICONTROL Semplice]**
* **[!UICONTROL Cerchio]**
* **[!UICONTROL Immagine personalizzata]** da un URL di contenuti multimediali o risorse.

+++Altre opzioni con formattazione avanzata

Se la **[!UICONTROL Modalità di formattazione avanzata]** è attivato, è possibile controllare il **[!UICONTROL Colore]** per scegliere il colore e l&#39;opacità del pulsante.

+++

### Media {#add-media}

La **[!UICONTROL Media]** consente di aggiungere contenuti multimediali al messaggio in-app per creare un’esperienza coinvolgente per l’utente finale.

![](assets/in_app_content_3.png)

Digita l’URL del contenuto multimediale o fai clic sul pulsante **[!UICONTROL Seleziona risorse]** per aggiungere direttamente al messaggio in-app le risorse memorizzate nella libreria Assets. [Ulteriori informazioni sulla gestione delle risorse](../design/assets-essentials.md).
Puoi anche aggiungere un **[!UICONTROL Testo alternativo]** per applicazioni di lettura dello schermo.

+++Altre opzioni con formattazione avanzata

Se la **[!UICONTROL Modalità di formattazione avanzata]** è attivato, è possibile personalizzare **[!UICONTROL Altezza massima]** e **[!UICONTROL Larghezza max]** dei supporti.

+++

### Intestazione e corpo {#title-body}

Per comporre il messaggio, immetti il contenuto nel **[!UICONTROL Intestazione]** e **[!UICONTROL Corpo]** campi.

![](assets/in_app_content_4.png)

Utilizza la **[!UICONTROL Personalizzazione]** per aggiungere la personalizzazione. Ulteriori informazioni sulla personalizzazione nell’editor espressioni di Adobe Journey Optimizer [in questa sezione](../personalization/personalize.md).

+++Altre opzioni con formattazione avanzata

Se la **[!UICONTROL Modalità di formattazione avanzata]** è attivato, è possibile scegliere **[!UICONTROL Intestazione]** e **[!UICONTROL Corpo]**:

* la **[!UICONTROL Font]**
* la **[!UICONTROL Dimensione della punta]**
* la **[!UICONTROL Colore font]**
* la **[!UICONTROL Allineamento]**
+++

### Pulsanti {#add-buttons}

Aggiungi pulsanti che consentano agli utenti di interagire con il messaggio in-app.

![](assets/in_app_content_5.png)

Per personalizzare il pulsante:

1. Modificare il campo di testo Pulsante 1 (primario). È inoltre possibile utilizzare **[!UICONTROL Personalizzazione]** per definire il contenuto e i dati di personalizzazione.

1. Scegli la tua **[!UICONTROL Evento di interazione]** che definisce l’azione del pulsante dopo l’interazione degli utenti con esso.

1. Inserisci l&#39;URL web o il collegamento diretto nel **[!UICONTROL Target]** campo .

1. Per aggiungere più pulsanti, fai clic su **[!UICONTROL Pulsante Aggiungi]**.

+++Altre opzioni con formattazione avanzata

Se la **[!UICONTROL Modalità di formattazione avanzata]** è attivato, è possibile scegliere **[!UICONTROL Pulsanti]**:

* la **[!UICONTROL Font]**
* la **[!UICONTROL Dimensione della punta]**
* la **[!UICONTROL Colore font]**
* la **[!UICONTROL Allineamento]**
* la **[!UICONTROL Stile pulsante]**
* la **[!UICONTROL Raggio]**
* la **[!UICONTROL Colore pulsante]**

+++

## Scheda Impostazioni {#settings-tab}

Da **Impostazioni** Puoi definire il layout del messaggio e visualizzarne l’anteprima in-app. È inoltre possibile accedere a opzioni di formattazione avanzate.

### Anteprima {#preview-tab}

![](assets/in_app_content_6.png)

La **[!UICONTROL Anteprima app]** consente di aggiungere uno sfondo al messaggio in-app:

* Un file multimediale da un collegamento URL.

* Una risorsa dalla libreria Assets.

* Colore di sfondo.

### Layout {#layout-options}

![](assets/in_app_content_7.png)

La **[!UICONTROL Immagine di sfondo]** Il campo ti consente di aggiungere uno sfondo al messaggio in-app:

* Un file multimediale da un collegamento URL.

* Colore di sfondo.

### Messaggio {#message-tab}

![](assets/in_app_content_8.png)

L’opzione di acquisizione dell’interfaccia utente, attivata per impostazione predefinita, consente di oscurare lo sfondo dietro il messaggio in-app per evidenziare lo stato attivo sul contenuto.

+++Altre opzioni con formattazione avanzata

Se la **[!UICONTROL Modalità di formattazione avanzata]** è attivato, puoi personalizzare ulteriormente il messaggio con le seguenti opzioni:

* **[!UICONTROL Personalizzare i gesti]**: ti consente di personalizzare l’interazione scorrevole dell’utente. Se è selezionata l’opzione ignora , puoi aggiungere un evento interattivo personalizzato e/o una destinazione di destinazione.

* **[!UICONTROL Personalizzare l’acquisizione dell’interfaccia utente]**: consente di selezionare un colore da visualizzare sullo sfondo e la relativa opacità.

* **[!UICONTROL Personalizza dimensioni]**: consente di regolare la larghezza e l’altezza della notifica in-app.

* **[!UICONTROL Personalizza posizione]**: ti consente di personalizzare la posizione dei messaggi in-app sullo schermo degli utenti. È possibile modificare gli allineamenti Verticale e Orizzontale.

* **[!UICONTROL Personalizzare l&#39;animazione]**: ti consente di personalizzare le animazioni Visualizza e Ignora , ad esempio se la notifica in-app viene visualizzata dalla sinistra o dalla parte superiore del dispositivo dell’utente.

* **[!UICONTROL Angolo arrotondato messaggio]**: consente di aggiungere un angolo arrotondato alla notifica in-app modificando la variabile **[!UICONTROL Raggio angolo]**.

+++

**Argomenti correlati:**

* [Creare un messaggio in-app](create-in-app.md)
* [Rapporto in-app](inapp-report.md)
* [Configurazione in-app](inapp-configuration.md)

