---
solution: Journey Optimizer
product: journey optimizer
title: Migrare un sottodominio e-mail da CNAME a una delega personalizzata
description: Scopri come migrare un sottodominio e-mail o pagina di destinazione dalla delega CNAME alla delega personalizzata in Journey Optimizer.
feature: Subdomains, Deliverability
topic: Administration
role: Admin
level: Intermediate
keywords: sottodominio, delega, migrazione, CNAME, delega personalizzata
badge: label="Disponibilità limitata" type="Informative"
source-git-commit: 316553be4f04e4fc0ae11bc767f7e48f64fc5ccd
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 5%

---

# Migrare un sottodominio e-mail da CNAME a una delega personalizzata {#migrate-cname-to-custom}

>[!AVAILABILITY]
>
>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.

Se il tuo sottodominio è attualmente configurato con [CNAME](about-subdomain-delegation.md#cname-subdomain-setup), puoi migrarlo al metodo **[!UICONTROL Delega personalizzata]** per soddisfare i criteri di sicurezza della tua azienda. In questo modo si ottiene la piena proprietà e il controllo completo dei sottodomini e dei certificati all&#39;interno di [!DNL Journey Optimizer]. [Ulteriori informazioni sui sottodomini personalizzati](delegate-custom-subdomain.md)

Come parte di questo processo, devi:

* [Elimina i record DNS esistenti](#delete-dns) dalla soluzione di hosting
* [Carica il certificato SSL](#upload-ssl-certificate) ottenuto dall&#39;autorità di certificazione
* Completa i [passaggi del ciclo di feedback](#feedback-loop) verificando la proprietà del dominio e segnalando l&#39;indirizzo e-mail
* [Copia il record di convalida URL CDN SSL](#copy-ssl-cdn-url-record) generato da Adobe nella piattaforma di hosting

Per eseguire la migrazione del sottodominio, segui i passaggi indicati di seguito.

## Prima di iniziare {#before-you-begin}

Prima di avviare il processo di migrazione, controlla le informazioni importanti riportate di seguito.

>[!IMPORTANT]
>
>È possibile migrare solo un sottodominio configurato con il metodo [CNAME](delegate-subdomain.md#cname-subdomain-setup).

* Assicurati che il metodo di delega **Personalizzato sia abilitato** per la tua organizzazione (questa funzionalità è attualmente a disponibilità limitata, contatta il tuo rappresentante Adobe per ottenere l&#39;accesso). [Ulteriori informazioni](delegate-custom-subdomain.md)
* Assicurati che nessuna configurazione di canale attiva stia utilizzando questo sottodominio. Il processo di migrazione ne interromperà la funzionalità.
* Assicurati che nessuna campagna o percorso attivo utilizzi una configurazione di canale collegata a questo sottodominio, in quanto ciò potrebbe causare interruzioni della consegna.
* Tieni presente che i tempi di inattività iniziano non appena accedi al flusso di migrazione. Il sottodominio viene spostato in **[!UICONTROL Bozza]** durante il processo e non è disponibile fino al completamento dell&#39;installazione.
* Di conseguenza, si consiglia di **eseguire i passaggi di pre-migrazione prima di avviare il processo di migrazione**, per preparare il certificato SSL e ridurre i tempi di inattività. [Ulteriori informazioni](#start-migration)

## Iniziare la migrazione {#start-migration}

Per iniziare a eseguire la migrazione di un determinato sottodominio, segui la procedura riportata di seguito.

1. Vai a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni e-mail]** > **[!UICONTROL Sottodomini]**.

1. Seleziona un sottodominio configurato con CNAME e aprilo.

1. Puoi utilizzare la sezione **[!UICONTROL Generazione CSR pre-migrazione]** per generare la CSR per inviarla all&#39;autorità di certificazione e preparare il certificato SSL all&#39;avvio del processo di migrazione. [Scopri come](#send-csr-to-ca)

   >[!IMPORTANT]
   >
   >I passaggi di pre-migrazione sono facoltativi in questa fase, ma sono vivamente consigliati. Completandoli **prima** dell&#39;avvio della migrazione, si riducono i tempi di inattività e si garantisce una transizione senza problemi.

   ![](assets/subdomain-migrate-pre-migration-csr.png){width="70%"}

1. Seleziona **[!UICONTROL Esegui migrazione ora]** nella sezione dedicata.

   <!--![](assets/subdomain-migrate-to-custom.png){width=90%}-->

1. Rivedi le [informazioni visualizzate](#before-you-begin).

   >[!WARNING]
   >
   >I tempi di inattività iniziano non appena entri nel flusso di migrazione, quindi assicurati che non influiscano sulle campagne e sui percorsi attivi.

1. Fare clic su **[!UICONTROL Sì]**. Il sottodominio passa allo stato **[!UICONTROL Bozza]** e non è disponibile fino al completamento dell&#39;installazione.

## Generare e inviare la CSR all’autorità di certificazione {#send-csr-to-ca}

Per completare la migrazione, è necessario un certificato SSL rilasciato da un’autorità di certificazione (CA). Per ricevere questo certificato SSL, devi innanzitutto generare una richiesta di firma del certificato (CSR, Certificate Signing Request) e inviarla alla CA.

Che tu abbia già avviato il processo di migrazione o meno, segui i passaggi indicati di seguito per generare e inviare la nuova CSR.

1. Fare clic su **[!UICONTROL Rigenera CSR]**.

1. Compila il modulo che visualizza e rigenera la richiesta di firma del certificato (CSR, Certificate Signing Request).

   ![](assets/subdomain-migrate-regenerate-csr.png){width="60%"}

   >[!NOTE]
   >
   >La lunghezza della chiave può essere solo 2048 o 4096 bit. Non può essere modificata dopo l’invio del sottodominio.

1. Fai clic su **[!UICONTROL Scarica CSR]** e salva il modulo nel computer locale.

1. Invialo all’autorità di certificazione (CA) per ottenere il certificato SSL. Prima di inviare questa CSR alla tua CA per la firma, ci sono alcuni punti importanti da considerare:

   * La CSR scaricata dal passaggio 3 è disponibile solo per data.subdomain.com.

   * Tuttavia, il certificato deve riguardare sia data.subdomain.com che cdn.subdomain.com come voci SAN (Subject Alternative Names) all&#39;interno di un singolo certificato. Ad esempio, se deleghi example.adobe.com, data.subdomain.com corrisponde a data.example.adobe.com e cdn.subdomain.com corrisponde a cdn.example.adobe.com.

   * I sottodomini Dati (data.example.adobe.com) e CDN (cdn.example.adobe.com) devono essere aggiunti come voci peer nello stesso certificato.

   * La maggior parte delle CA consente di aggiungere ulteriori SAN (ad esempio il sottodominio CDN) durante il processo di firma

      * Tramite il portale CA (scelta consigliata, se disponibile), oppure
      * Richiedendolo manualmente con il proprio team di supporto se l’opzione portale non è disponibile.

   * Una volta firmata, la CA rilascerà un singolo certificato che copre sia il dominio dati che il sottodominio CDN.

## Elimina record DNS esistenti {#delete-dns}

Dopo aver avviato il processo di migrazione, devi eliminare i record DNS esistenti dalla soluzione di hosting. Segui i passaggi seguenti.

1. Viene visualizzato l’elenco dei record attualmente configurati nei server DNS.

1. Passa alla soluzione di hosting del dominio ed elimina le voci CNAME esistenti dall&#39;hosting DNS.

1. Verificare che tutti i record DNS siano stati eliminati. Al termine, seleziona la casella &quot;Confermo di aver eliminato i record richiesti dal sito di hosting&quot;.

   ![](assets/subdomain-migrate-delete-dns.png){width="75%"}

## Carica il certificato SSL {#upload-ssl-certificate}

Nella sezione **[!UICONTROL Certificato SSL]**, devi caricare un nuovo certificato SSL in [!DNL Journey Optimizer].

Prima di ciò, verifica quanto segue:

* Se hai già inviato la tua CSR all&#39;autorità di certificazione come parte dei [passaggi di pre-migrazione](#start-migration), assicurati di aver ricevuto il certificato SSL.

* Se non lo hai già fatto, segui i passaggi per [generare, scaricare e inviare la CSR](#send-csr-to-ca).

<!--
    * Click **[!UICONTROL Regenerate CSR]** and fill the form to generate the Certificate Signing Request.

    * Click **[!UICONTROL Download CSR]** to save the form to your local computer.

    * Send the CSR to the Certificate Authority to get your SSL certificate.-->

1. Dopo aver recuperato il certificato SSL, fai clic su **[!UICONTROL Carica certificato]**.

   ![](assets/subdomain-migrate-ssl-certificate.png){width="75%"}

1. Carica il certificato SSL in [!DNL Journey Optimizer] in formato .pem con la catena di certificati completa. Ecco un esempio di un formato di file .pem:

   ```
   -----BEGIN CERTIFICATE-----
   MIIDXTCCAkWgAwIBAgIJALc3... (base64 encoded data)
   -----END CERTIFICATE-----
   ```

1. Seleziona la casella &quot;Confermo di aver caricato il certificato SSL&quot;.

## Ciclo di feedback completo {#feedback-loop}

Quindi, completa i passaggi del ciclo di feedback per verificare la proprietà del dominio e l’indirizzo e-mail di reporting.

![](assets/subdomain-migrate-feedback-loop.png){width="75%"}

Il processo è lo stesso della configurazione di un nuovo sottodominio personalizzato. Segui i passaggi descritti nella pagina [Configura un sottodominio personalizzato](delegate-custom-subdomain.md#feedback-loop-steps).

## Copia il record di convalida URL CDN SSL {#copy-ssl-cdn-url-record}

Per completare il processo di migrazione, copia nella piattaforma di hosting il record di convalida URL CDN SSL generato da Adobe. Il processo è lo stesso della configurazione di un nuovo sottodominio personalizzato. Segui i passaggi descritti nella pagina [Configura un sottodominio personalizzato](delegate-custom-subdomain.md#copy-ssl-cdn-url-record).

Dopo l’invio, devi attendere che Adobe esegua i controlli richiesti, che possono richiedere fino a 3 ore. [Ulteriori informazioni](delegate-subdomain.md#submit-subdomain)

Una volta che il sottodominio è nuovamente attivo, non sono necessarie modifiche alle configurazioni di canale esistenti che lo utilizzano, poiché continuano a funzionare come prima.

**Consulta anche**

* [Configurare un sottodominio personalizzato](delegate-custom-subdomain.md)
* [Metodi di delega dei sottodomini](about-subdomain-delegation.md#subdomain-delegation-methods)
