---
title: Creare contenuti in-app per il web
description: Scopri come progettare contenuti in-app web
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: in-app, messaggio, creazione, inizio
hide: true
hidefromtoc: true
source-git-commit: 722d37dc4bcb9ab7983ea336aa0b12a6a09e01dc
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 7%

---

# Creare contenuti in-app per il web {#in-app-web-design}

>[!BEGINSHADEBOX]

**Sommario**

* [Configurare il canale Web in-app](configure-in-app-web.md)
* [Creare la campagna di messaggi in-app Web](create-in-app-web.md)
* Creare contenuti in-app per il web

>[!ENDSHADEBOX]

Per modificare il contenuto del messaggio in-app, fai clic sul pulsante **[!UICONTROL Modifica contenuto]** nel menu **[!UICONTROL Azione]** della tua campagna.

![](assets/in_app_web_surface_7.png)

L&#39;opzione **[!UICONTROL Formattazione avanzata]** attiva altre opzioni per personalizzare l&#39;esperienza.

Una volta creato il messaggio in-app e definito e personalizzato il relativo contenuto, puoi rivederlo e attivarlo. Le notifiche verranno quindi inviate in base alla pianificazione della campagna. Ulteriori informazioni sono disponibili in [questa pagina](send-in-app.md).

## Layout messaggio {#message-layout}

Dalla sezione **[!UICONTROL Layout messaggio]**, seleziona una delle quattro opzioni di layout disponibili a seconda delle tue esigenze di messaggistica.

![](assets/in_app_web_design_1.png)

* **[!UICONTROL Schermo intero]**: questo tipo di layout copre l&#39;intero schermo dei dispositivi per il pubblico.

  Supporta i componenti per contenuti multimediali (immagine, video), di testo e i pulsanti.

* **[!UICONTROL Modale]**: questo layout viene visualizzato in una grande finestra in stile avviso. L&#39;applicazione rimane visibile in background.

  Supporta i componenti per contenuti multimediali (immagine, video), di testo e i pulsanti.

* **[!UICONTROL Banner]**: questo tipo di layout viene visualizzato come messaggio di avviso del sistema operativo nativo.

  Puoi aggiungere al messaggio solo un **[!UICONTROL Intestazione]** e un **[!UICONTROL Corpo]**.

* **[!UICONTROL Personalizzato]**: la modalità messaggio personalizzato ti consente di importare e modificare direttamente uno dei messaggi di HTML preconfigurati.

   * Seleziona **[!UICONTROL Componi]** per immettere o incollare il codice HTML non elaborato.

     Utilizza il riquadro a sinistra per sfruttare le funzionalità di personalizzazione di Journey Optimizer. Per ulteriori informazioni al riguardo, consulta [questa sezione](../personalization/personalize.md).

   * Seleziona **[!UICONTROL Importa]** per importare il file HTML o .zip contenente il contenuto di HTML.

## Scheda Contenuto {#content-tab}

Dalla scheda **Contenuto**, puoi definire e personalizzare il contenuto della notifica e lo stile del pulsante **Chiudi**. Puoi anche aggiungere un file multimediale alla notifica in-app e i pulsanti di azione da questa scheda.

### Chiudi pulsante {#close-button}

![](assets/in_app_web_design_2.png)

Scegli lo **[!UICONTROL stile]** del **[!UICONTROL pulsante Chiudi]**.

Gli stili disponibili sono:

* **[!UICONTROL Semplice]**
* **[!UICONTROL Cerchio]**
* **[!UICONTROL Immagine personalizzata]** da un URL multimediale o dal tuo Assets.

+++Altre opzioni con formattazione avanzata

Se la modalità di formattazione **[!UICONTROL Avanzata]** è attivata, è possibile selezionare l&#39;opzione **[!UICONTROL Colore]** per scegliere il colore e l&#39;opacità del pulsante.

+++

### Media {#add-media}

Il campo **[!UICONTROL Media]** consente di aggiungere contenuti multimediali al messaggio in-app per creare un&#39;esperienza coinvolgente per l&#39;utente finale.

![](assets/in_app_web_design_3.png)

Digita l&#39;URL del file multimediale o fai clic sull&#39;icona **[!UICONTROL Seleziona Assets]** per aggiungere direttamente al messaggio in-app le risorse memorizzate nella libreria Assets. <!--[Learn more about asset management](../content-management/assets-essentials.md).-->

È inoltre possibile aggiungere un **[!UICONTROL testo alternativo]** per le applicazioni di lettura dello schermo.

+++Altre opzioni con formattazione avanzata

Se la **[!UICONTROL modalità di formattazione avanzata]** è attivata, puoi personalizzare **[!UICONTROL l&#39;altezza massima]** e **[!UICONTROL la larghezza massima]** del contenuto multimediale.

+++

### Contenuto {#title-body}

Per comporre il messaggio, immetti il contenuto nei campi **[!UICONTROL Intestazione]** e **[!UICONTROL Corpo]**.

![](assets/in_app_web_design_4.png)

Utilizza l&#39;icona **[!UICONTROL Personalization]** per aggiungere la personalizzazione. Ulteriori informazioni sulla personalizzazione nell&#39;editor di personalizzazione di Adobe Journey Optimizer [in questa sezione](../personalization/personalize.md).

+++Altre opzioni con formattazione avanzata

Se la **[!UICONTROL modalità di formattazione avanzata]** è attivata, puoi scegliere per **[!UICONTROL Intestazione]** e **[!UICONTROL Corpo]**:

* **[!UICONTROL Carattere]**
* la **[!UICONTROL Dimensione punto]**
* **[!UICONTROL Colore carattere]**
* **[!UICONTROL Allineamento]**
+++

### Pulsanti {#add-buttons}

Aggiungi i pulsanti che consentono agli utenti di interagire con il messaggio in-app.

![](assets/in_app_web_design_5.png)

Per personalizzare il pulsante:

1. Modificare il campo Testo #1 pulsante (primario). Puoi anche utilizzare l&#39;icona **[!UICONTROL Personalization]** per definire i dati di contenuto e personalizzazione.

1. Scegli il tuo **[!UICONTROL evento di interazione]** che definisce l&#39;azione del pulsante dopo che gli utenti hanno interagito con esso.

1. Immetti l&#39;URL Web o il collegamento diretto nel campo **[!UICONTROL Target]**.

1. Per aggiungere più pulsanti, fare clic su **[!UICONTROL Aggiungi pulsante]**.

+++Altre opzioni con formattazione avanzata

Se la **[!UICONTROL modalità di formattazione avanzata]** è attivata, puoi scegliere i **[!UICONTROL pulsanti]**:

* **[!UICONTROL Carattere]**
* la **[!UICONTROL Dimensione punto]**
* **[!UICONTROL Colore carattere]**
* **[!UICONTROL Allineamento]**
* lo stile **[!UICONTROL Pulsante]**
* il **[!UICONTROL Raggio]**
* il **[!UICONTROL colore pulsante]**

+++

## Scheda Impostazioni {#settings-tab}

Dalla scheda **Impostazioni**, puoi definire il layout del messaggio e visualizzare l&#39;anteprima del messaggio in-app. Puoi anche accedere alle opzioni di formattazione avanzate.

### Layout {#layout-options}

![](assets/in_app_web_design_6.png)

Il campo **[!UICONTROL Immagine di sfondo]** consente di aggiungere uno sfondo al messaggio in-app:

* Un file multimediale da un collegamento URL.

* Un colore di sfondo.

### Messaggio {#message-tab}

![](assets/in_app_web_design_7.png)

L’opzione di acquisizione dell’interfaccia utente, attivata per impostazione predefinita, consente di scurire lo sfondo dietro il messaggio in-app per evidenziare lo stato attivo sul contenuto.

+++Altre opzioni con formattazione avanzata

Se la **[!UICONTROL modalità di formattazione avanzata]** è attivata, è possibile personalizzare ulteriormente il messaggio con le opzioni seguenti:

* **[!UICONTROL Personalizza acquisizione interfaccia utente]**: consente di selezionare un colore da visualizzare nello sfondo e la relativa opacità.

* **[!UICONTROL Personalizza dimensione]**: consente di regolare la larghezza e l&#39;altezza della notifica in-app.

* **[!UICONTROL Personalizza posizione]**: ti consente di personalizzare la posizione dei messaggi in-app sullo schermo degli utenti. È possibile modificare l&#39;allineamento verticale e orizzontale.

* **[!UICONTROL Angolo circolare messaggio]**: consente di aggiungere un angolo circolare alla notifica in-app modificando il **[!UICONTROL Raggio angolo]**.

+++

**Argomenti correlati:**

* [Testare e inviare il messaggio in-app](send-in-app.md)
* [Rapporto in-app](../reports/campaign-global-report-cja-inapp.md)
* [Configurazione in-app](inapp-configuration.md)