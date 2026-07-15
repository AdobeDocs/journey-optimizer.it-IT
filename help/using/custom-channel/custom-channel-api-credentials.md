---
title: Gestire le credenziali API per i canali personalizzati
description: Scopri come gestire le credenziali API per i canali personalizzati in Adobe Journey Optimizer.
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Disponibilità limitata" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 4%

---


# Gestire le credenziali API {#api-credentials}

Quando si crea un canale personalizzato con un tipo di autenticazione diverso da **Nessuno**, viene generato automaticamente un set iniziale di credenziali API quando il canale viene attivato.

Puoi visualizzare, gestire e modificare le credenziali da **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Generatore canali]** > **[!UICONTROL Credenziali API]**.

![Credenziali API](assets/custom_channel_api_credentials.png){width="100%"}

L’utilizzo di più credenziali per lo stesso canale consente di allegare valori di autenticazione diversi a configurazioni di canale diverse, ad esempio per marchi o casi di utilizzo diversi, senza duplicare la definizione del canale.

Per modificare un set di credenziali esistente, fare clic su un elemento nell&#39;elenco di inventario. Tutti i campi sono modificabili.

Per creare credenziali aggiuntive per lo stesso canale, segui la procedura riportata di seguito.

1. Nell&#39;elenco **[!UICONTROL Credenziali API]** fare clic su **[!UICONTROL Crea credenziali API]**.

1. Immetti un nome e una descrizione.

   ![Crea credenziali API](assets/custom_channel_create_api_credentials.png){width="100%"}

1. Selezionare il **[!UICONTROL canale]** per il quale si stanno creando le credenziali.

   >[!NOTE]
   >
   >Nell&#39;elenco a discesa vengono visualizzati solo i canali personalizzati attivati con un tipo di autenticazione diverso da **Nessuno**.

1. Selezionare il tipo di autenticazione **** dall&#39;elenco.
1. Compila i campi specifici dell’autenticazione:
   * **[!UICONTROL Chiave API]** - Fornisci il nome, il valore e la posizione della chiave (parametro o intestazione di query).
   * **[!UICONTROL Autenticazione di base]** - Specificare nome utente e password.
   * **[!UICONTROL OAuth 2.0]** - Configura il payload per l&#39;autenticazione OAuth 2.0.
1. Fai clic su **[!UICONTROL Salva]**.

## Passaggi successivi {#next-steps}

* [Delega un sottodominio](custom-channel-subdomains.md) (facoltativo, obbligatorio per il tracciamento dei collegamenti)
* [Creare una configurazione dei canali](custom-channel-configuration.md)
