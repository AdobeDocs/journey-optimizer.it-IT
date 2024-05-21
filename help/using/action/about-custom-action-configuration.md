---
solution: Journey Optimizer
product: journey optimizer
title: Configurare un’azione personalizzata
description: Scopri come configurare un’azione personalizzata
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: azione, terze parti, personalizzato, percorsi, API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 12423d9fe07e5c757154ae4f732ff20ec6dc2427
workflow-type: tm+mt
source-wordcount: '1799'
ht-degree: 17%

---

# Configurare un’azione personalizzata {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="Azioni personalizzate"
>abstract="Se utilizzi un sistema di terze parti per l’invio di messaggi o desideri che i percorsi inviino chiamate API a un sistema di terze parti, utilizza azioni personalizzate per configurarne la connessione al tuo percorso. Ad esempio, mediante azioni personalizzate è possibile connettersi ai seguenti sistemi: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com), Firebase, ecc."

Se utilizzi un sistema di terze parti per l’invio di messaggi o desideri che i percorsi inviino chiamate API a un sistema di terze parti, utilizza azioni personalizzate per configurarne la connessione al tuo percorso. Ad esempio, è possibile connettersi ai seguenti sistemi con azioni personalizzate: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase, ecc.

Le azioni personalizzate sono azioni aggiuntive definite dagli utenti tecnici e rese disponibili agli esperti di marketing. Una volta configurate, vengono visualizzate nella palette a sinistra del percorso, nel **[!UICONTROL Azione]** categoria. Per ulteriori informazioni, consulta [questa pagina](../building-journeys/about-journey-activities.md#action-activities).

## Limitazioni{#custom-actions-limitations}

Le azioni personalizzate presentano alcune limitazioni elencate in [questa pagina](../start/guardrails.md).

Nei parametri delle azioni personalizzati, puoi trasmettere una semplice raccolta e un insieme di oggetti. Ulteriori informazioni sulle limitazioni della raccolta in [questa pagina](../building-journeys/collections.md#limitations).

Inoltre, i parametri delle azioni personalizzate hanno un formato previsto (ad esempio, stringa, decimale, ecc.). Devi fare attenzione a rispettare questi formati previsti. Ulteriori informazioni [caso d’uso](../building-journeys/collections.md).

Le azioni personalizzate supportano il formato JSON solo quando si utilizza [richiesta](../action/about-custom-action-configuration.md#define-the-message-parameters) o [payload di risposta](../action/action-response.md).

## Best practice{#custom-action-enhancements-best-practices}

Quando scegli un endpoint per il targeting utilizzando un’azione personalizzata, assicurati che:

* Questo endpoint possa supportare la velocità effettiva del percorso utilizzando le configurazioni della [API di limitazione](../configuration/throttling.md) o [API di limitazione di utilizzo](../configuration/capping.md) per limitarlo. Fai attenzione che una configurazione di limitazione non può scendere al di sotto di 200 TPS. Qualsiasi endpoint di destinazione dovrà supportare almeno 200 TPS.
* Questo endpoint deve avere un tempo di risposta il più basso possibile. A seconda della velocità effettiva prevista, avere un tempo di risposta elevato potrebbe influire sulla velocità effettiva.

Per tutte le azioni personalizzate viene definito un limite massimo di 300.000 chiamate in un minuto. Inoltre, il limite predefinito viene eseguito per host e per sandbox. Ad esempio, se in una sandbox hai due endpoint con lo stesso host (ad esempio: `https://www.adobe.com/endpoint1` e `https://www.adobe.com/endpoint2`), il limite verrà applicato a tutti gli endpoint nell’host adobe.com. &quot;endpoint1&quot; ed &quot;endpoint2&quot; condivideranno la stessa configurazione di limitazione e il fatto che un endpoint raggiunga il limite avrà un impatto sull’altro endpoint.

Questo limite è stato impostato in base all’utilizzo da parte della clientela, per proteggere gli endpoint esterni interessati dalle azioni personalizzate. Devi tenerne conto nei percorsi basati sul pubblico definendo una velocità di lettura appropriata (5000 profili al secondo quando vengono utilizzate le azioni personalizzate). Se necessario, puoi ignorare questa impostazione definendo un limite di limitazione di utilizzo o di limitazione maggiore tramite le rispettive API. Consulta [questa pagina](../configuration/external-systems.md).

Non eseguire il targeting degli endpoint pubblici con azioni personalizzate per vari motivi:

* Senza limiti o limitazioni corretti, esiste il rischio di inviare troppe chiamate a un endpoint pubblico che potrebbe non supportare tale volume.
* I dati del profilo possono essere inviati tramite azioni personalizzate, pertanto il targeting di un endpoint pubblico potrebbe causare la condivisione involontaria di informazioni personali esternamente.
* Non hai alcun controllo sui dati restituiti dagli endpoint pubblici. Se un endpoint modifica la propria API o inizia a inviare informazioni errate, queste saranno rese disponibili nelle comunicazioni inviate, con potenziali effetti negativi.

## Consenso e governance dei dati {#privacy}

In Journey Optimizer, puoi applicare la governance dei dati e i criteri di consenso alle azioni personalizzate per impedire l’esportazione di campi specifici in sistemi di terze parti o escludere clienti che non hanno acconsentito a ricevere comunicazioni e-mail, push o SMS. Per ulteriori informazioni, consulta le pagine seguenti:

* [Governance dei dati](../action/action-privacy.md).
* [Consenso](../action/action-privacy.md).


## Passaggi di configurazione {#configuration-steps}

Di seguito sono riportati i passaggi principali necessari per configurare un’azione personalizzata:

1. Nella sezione del menu ADMINISTRATION, selezionare **[!UICONTROL Configurazioni]**. In  **[!UICONTROL Azioni]** , fare clic su **[!UICONTROL Gestisci]**. Clic **[!UICONTROL Crea azione]** per creare una nuova azione. Il riquadro di configurazione delle azioni si apre sul lato destro dello schermo.

   ![](assets/custom2.png)

1. Immetti un nome per l&#39;azione.

   >[!NOTE]
   >
   >Sono consentiti solo caratteri alfanumerici e trattini bassi. La lunghezza massima è di 30 caratteri.

1. Aggiungi una descrizione all’azione. Questo passaggio è facoltativo.
1. Il numero di percorsi che utilizzano questa azione viene visualizzato nel **[!UICONTROL Utilizzato in]** campo. Puoi fare clic su **[!UICONTROL Visualizza percorsi]** per visualizzare l&#39;elenco dei percorsi che utilizzano questa azione.
1. Definisci i diversi **[!UICONTROL Configurazione URL]** parametri. Consulta [questa pagina](../action/about-custom-action-configuration.md#url-configuration).
1. Configurare **[!UICONTROL Autenticazione]** sezione. Questa configurazione è la stessa delle origini dati.  Consulta [questa sezione](../datasource/external-data-sources.md#custom-authentication-mode).
1. Definisci il **[!UICONTROL Parametri azione]**. Consulta [questa pagina](../action/about-custom-action-configuration.md#define-the-message-parameters).
1. Fai clic su **[!UICONTROL Salva]**.

   L’azione personalizzata è ora configurata ed è pronta per essere utilizzata nei percorsi. Consulta [questa pagina](../building-journeys/about-journey-activities.md#action-activities).

   >[!NOTE]
   >
   >Quando un’azione personalizzata viene utilizzata in un percorso, la maggior parte dei parametri è di sola lettura. È possibile modificare solo **[!UICONTROL Nome]**, **[!UICONTROL Descrizione]**, **[!UICONTROL URL]** campi e **[!UICONTROL Autenticazione]** sezione.

## Configurazione endpoint {#url-configuration}

Durante la configurazione di un’azione personalizzata, devi definire quanto segue **[!UICONTROL Configurazione endpoint]** parametri:

![](assets/action-response1bis.png){width="70%" align="left"}

1. In **[!UICONTROL URL]** , specifica l’URL del servizio esterno:

   * Se l’URL è statico, inseriscilo in questo campo.

   * Se l&#39;URL include un percorso dinamico, immettere solo la parte statica dell&#39;URL, ovvero lo schema, l&#39;host, la porta e, facoltativamente, una parte statica del percorso.

     Esempio: `https://xxx.yyy.com/somethingstatic/`

     Specificherai il percorso dinamico dell’URL quando aggiungi l’azione personalizzata a un percorso. [Ulteriori informazioni](../building-journeys/using-custom-actions.md).

   >[!NOTE]
   >
   >Per motivi di sicurezza, si consiglia vivamente di utilizzare lo schema HTTPS per l’URL. Non consentiamo l’uso di indirizzi Adobe non pubblici e l’uso di indirizzi IP.
   >
   >Durante la definizione di un’azione personalizzata sono consentite solo le porte predefinite: 80 per http e 443 per https.

1. Seleziona la chiamata **[!UICONTROL Metodo]**: può essere **[!UICONTROL POST]**, **[!UICONTROL GET]** o **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > Il **DELETE** metodo non supportato. Se devi aggiornare una risorsa esistente, seleziona la **PUT** metodo.

1. Definisci le intestazioni e i parametri di query:

   * In **[!UICONTROL Intestazioni]** , fare clic su **[!UICONTROL Aggiungere un campo intestazione]** per definire le intestazioni HTTP del messaggio di richiesta da inviare al servizio esterno. Il **[!UICONTROL Content-Type]** e **[!UICONTROL Charset]** i campi dell’intestazione sono impostati per impostazione predefinita. Non è possibile eliminare questi campi. Solo il **[!UICONTROL Content-Type]** l’intestazione può essere modificata. Il suo valore deve rispettare il formato JSON. Di seguito è riportato il valore predefinito:

   ![](assets/content-type-header.png)

   * In **[!UICONTROL Parametri di query]** , fare clic su **[!UICONTROL Aggiungere un campo Parametro query]** per definire i parametri che desideri aggiungere all’URL.

   ![](assets/journeyurlconfiguration2bis.png)

1. Immettere l&#39;etichetta o il nome del campo.

1. Selezionare il tipo: **[!UICONTROL Costante]** o **[!UICONTROL Variabile]**. Se hai selezionato **[!UICONTROL Costante]**, quindi inserisci il valore costante nel **[!UICONTROL Valore]** campo. Se hai selezionato **[!UICONTROL Variabile]**, quindi specificherai questa variabile quando aggiungi l’azione personalizzata a un percorso. [Ulteriori informazioni](../building-journeys/using-custom-actions.md).

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >Dopo aver aggiunto l’azione personalizzata a un percorso, puoi comunque aggiungere campi di intestazione o parametri di query se il percorso si trova nello stato Bozza. Se non desideri che le modifiche alla configurazione influiscano sul percorso, duplica l’azione personalizzata e aggiungi i campi alla nuova azione personalizzata.
   >
   >Le intestazioni vengono convalidate in base alle regole di analisi dei campi. Ulteriori informazioni in [questa documentazione](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## Definire i parametri di payload {#define-the-message-parameters}

1. In **[!UICONTROL Richiesta]** incolla un esempio del payload JSON da inviare al servizio esterno. Questo campo è facoltativo e disponibile solo per i metodi di chiamata POST e PUT.

1. In **[!UICONTROL Risposta]** incolla un esempio del payload restituito dalla chiamata. Questo campo è facoltativo e disponibile per tutti i metodi di chiamata. Per informazioni dettagliate su come sfruttare le risposte alle chiamate API nelle azioni personalizzate, consulta [questa pagina](../action/action-response.md).

>[!NOTE]
>
>La funzionalità di risposta è attualmente disponibile in versione beta.

![](assets/action-response2bis.png){width="70%" align="left"}

>[!NOTE]
>
>L’esempio di payload non può contenere valori Null. I nomi dei campi nel payload non possono contenere un &quot;.&quot; aggiuntivo. Non possono iniziare con il carattere &quot;$&quot;.

Potrai definire il tipo di parametro (ad esempio stringa, numero intero e così via).

Puoi anche scegliere se specificare se un parametro è una costante o una variabile:

* **Costante** significa che il valore del parametro è definito nel riquadro di configurazione dell’azione da un utente tecnico. Il valore sarà sempre lo stesso tra i percorsi. Non varia e l’addetto marketing non la vede quando utilizza l’azione personalizzata nel percorso. Potrebbe essere ad esempio un ID previsto dal sistema di terze parti. In tal caso, il campo a destra della costante/variabile di attivazione è il valore passato.
* **Variabile** indica che il valore del parametro varia. Gli addetti al marketing che utilizzano questa azione personalizzata in un percorso saranno liberi di trasmettere il valore desiderato o di specificare dove recuperare il valore per questo parametro (ad esempio dall’evento, da Adobe Experience Platform, ecc.). In tal caso, il campo a destra della costante/variabile di attivazione è l’etichetta che gli addetti al marketing vedranno nel percorso per denominare questo parametro.

![](assets/customactionpayloadmessage2.png)

## Supporto del protocollo mTLS {#mtls-protocol-support}

Ora puoi utilizzare Mutual Transport Layer Security (mTLS) per garantire una maggiore sicurezza nelle connessioni in uscita alle destinazioni API HTTP e nelle azioni personalizzate di Adobe Journey Optimizer. mTLS è un metodo di sicurezza end-to-end per l’autenticazione reciproca che garantisce che entrambe le parti che condividono le informazioni siano chi affermano di essere prima che i dati vengano condivisi. mTLS include un ulteriore passaggio rispetto a TLS, in cui il server richiede anche il certificato del client e lo verifica alla loro fine.

In Adobe Journey Optimizer, mTLS viene utilizzato insieme alle azioni personalizzate. Per abilitare mTLS non è necessaria alcuna configurazione aggiuntiva per le azioni personalizzate di Adobe Journey Optimizer. Quando l’endpoint per un’azione personalizzata è abilitato per mTLS, il sistema recupera il certificato dal keystore di Adobe Experience Platform e lo fornisce automaticamente all’endpoint (come è richiesto per le connessioni mTLS).

Se desideri utilizzare mTLS con questi flussi di lavoro di destinazione Adobe Journey Optimizer e Experienci Platform HTTP API, per l’indirizzo del server inserito nell’interfaccia utente delle azioni dei clienti Adobe Journey Optimizer o nell’interfaccia utente delle destinazioni è necessario che i protocolli TLS siano disabilitati e che sia abilitato solo mTLS. Se il protocollo TLS 1.2 è ancora abilitato su tale endpoint, non viene inviato alcun certificato per l’autenticazione client. Ciò significa che per utilizzare mTLS con questi flussi di lavoro, l’endpoint del server &quot;ricevente&quot; deve essere un mTLS **solo** endpoint di connessione abilitato.

>[!IMPORTANT]
>
>Non è richiesta alcuna configurazione aggiuntiva nell’azione personalizzata o nel percorso Adobe Journey Optimizer per attivare mTLS; questo processo si verifica automaticamente quando viene rilevato un endpoint abilitato per mTLS. Il Nome comune (CN) e i Nomi alternativi dei soggetti (SAN) per ciascun certificato sono disponibili nella documentazione come parte del certificato e possono essere utilizzati come livello aggiuntivo di convalida della proprietà, se lo si desidera.
>
>La RFC 2818, pubblicata nel maggio 2000, depreca l&#39;uso del campo Common Name (CN) nei certificati HTTPS per la verifica del nome del soggetto. Consiglia invece di utilizzare l’estensione &quot;Subject Alternative Name&quot; (SAN) del tipo &quot;dns name&quot;.

Se desideri verificare il CN o la SAN per eseguire un’ulteriore convalida di terze parti, puoi scaricare i certificati pertinenti qui:

```
Prod:
{
    "serviceName": "AJO Journeys",
    "publicCertificate": "-----BEGIN CERTIFICATE-----
MIIG9TCCBd2gAwIBAgIQBX+pDP5hB0gqDzFKyq5wLjANBgkqhkiG9w0BAQsFADBZ
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMTMwMQYDVQQDEypE
aWdpQ2VydCBHbG9iYWwgRzIgVExTIFJTQSBTSEEyNTYgMjAyMCBDQTEwHhcNMjQw
NTA5MDAwMDAwWhcNMjUwNjA5MjM1OTU5WjB0MQswCQYDVQQGEwJVUzETMBEGA1UE
CBMKQ2FsaWZvcm5pYTERMA8GA1UEBxMIU2FuIEpvc2UxEzARBgNVBAoTCkFkb2Jl
IEluYy4xKDAmBgNVBAMTH2Fqby1qb3VybmV5cy5hZXAtbXRscy5hZG9iZS5jb20w
ggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDaI8HZHzbmPEgTy9O7cYmq
ZVX5283Gw7j7v4/O810jZXItBDmsSiWotvTgAT0s2oZMZZ6tGPbQB7hL+xJJ+yu2
HxFl1WzB4UGHJ+UbrL94hI930xQs0FVgSOGgIarj5HucF2ZxwHIkVHY5whrOq9t4
UxFBG0siUPQrTzV9GfA0wREElugpTbwaM8CTWwOQ9ekroOD2C5zAcLTycXFtSMiU
B4L4u38S9hGoBByzzKv9GnUMQudvt/s5zsGykZgEEYeN6IitfVO6BOD9jT94Aytx
/O3XH5w8v4KNTn+An99bXFmyg3JRUFSYZFxha8s1f6uu0XbdToQ+ao0WkE06nMmV
AgMBAAGjggOcMIIDmDAfBgNVHSMEGDAWgBR0hYDAZsffN97PvSk3qgMdvu3NFzAd
BgNVHQ4EFgQUn8OqtzccNdrsb+fbRnTHmtTZxLMwKgYDVR0RBCMwIYIfYWpvLWpv
dXJuZXlzLmFlcC1tdGxzLmFkb2JlLmNvbTA+BgNVHSAENzA1MDMGBmeBDAECAjAp
MCcGCCsGAQUFBwIBFhtodHRwOi8vd3d3LmRpZ2ljZXJ0LmNvbS9DUFMwDgYDVR0P
AQH/BAQDAgWgMB0GA1UdJQQWMBQGCCsGAQUFBwMBBggrBgEFBQcDAjCBnwYDVR0f
BIGXMIGUMEigRqBEhkJodHRwOi8vY3JsMy5kaWdpY2VydC5jb20vRGlnaUNlcnRH
bG9iYWxHMlRMU1JTQVNIQTI1NjIwMjBDQTEtMS5jcmwwSKBGoESGQmh0dHA6Ly9j
cmw0LmRpZ2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbEcyVExTUlNBU0hBMjU2MjAy
MENBMS0xLmNybDCBhwYIKwYBBQUHAQEEezB5MCQGCCsGAQUFBzABhhhodHRwOi8v
b2NzcC5kaWdpY2VydC5jb20wUQYIKwYBBQUHMAKGRWh0dHA6Ly9jYWNlcnRzLmRp
Z2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbEcyVExTUlNBU0hBMjU2MjAyMENBMS0x
LmNydDAMBgNVHRMBAf8EAjAAMIIBfwYKKwYBBAHWeQIEAgSCAW8EggFrAWkAdwBO
daMnXJoQwzhbbNTfP1LrHfDgjhuNacCx+mSxYpo53wAAAY9ecsWsAAAEAwBIMEYC
IQDQclgq89ZVlwdYBJFEIs8q4WIcZ9Siw+jb9OgCrz+wjwIhALQLnC1WyT+dHjvY
FvZjc99WkjnEwhIevj/Rz7r0EzhmAHUAfVkeEuF4KnscYWd8Xv340IdcFKBOlZ65
Ay/ZDowuebgAAAGPXnLF5AAABAMARjBEAiBy9cNT3CnmSMOdJe+JbG8f7ha1UGgN
TdDlaR9x9fKmKQIgNmGjz5AzP1evB2G1TTvVLkHfWQw0864c4F23WSV+6TsAdwDP
EVbu1S58r/OHW9lpLpvpGnFnSrAX7KwB0lt3zsw7CAAAAY9ecsYnAAAEAwBIMEYC
IQCTcB7s1xDP8Olif3jj4X8jHgVxv5C3bTvG6wDYBByfcQIhAOt8PhR6tWSLtF1V
HB8r7dns7Oth1+QT7WMonQZsP/3WMA0GCSqGSIb3DQEBCwUAA4IBAQAjTy45fbQV
aVTZ71wcIyHnkJfq/8SSc/UNT5//6AMiV6kb3YsFW1+EaQ1wPHZS0Qfjs7aIsXi5
f2TCGps8onELNpOfFfptrOCMfcYGMvV1wPCBy+kuoGY/YRZlsdNUTTzQAGztfRev
79w+XIDzioCrY+sfyUkkw+N/F7/RIjzMKjP6onSfuD+5WjqVKq9kFE0fCyJixedV
BPoPM4Cktgvc9SsK17JmLWkg+V2yH1eDzmjF3sR0/dcmoAM0qgV/CDuhIIqX2o7m
3/aQSNsPUpgBVbkz+SjEtchmw8DXW/Kro8QVulsXdbkiLTOj4JopxdOzrbKgWMwr
pIw7KKJoktDk
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIIEyDCCA7CgAwIBAgIQDPW9BitWAvR6uFAsI8zwZjANBgkqhkiG9w0BAQsFADBh
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3
d3cuZGlnaWNlcnQuY29tMSAwHgYDVQQDExdEaWdpQ2VydCBHbG9iYWwgUm9vdCBH
MjAeFw0yMTAzMzAwMDAwMDBaFw0zMTAzMjkyMzU5NTlaMFkxCzAJBgNVBAYTAlVT
MRUwEwYDVQQKEwxEaWdpQ2VydCBJbmMxMzAxBgNVBAMTKkRpZ2lDZXJ0IEdsb2Jh
bCBHMiBUTFMgUlNBIFNIQTI1NiAyMDIwIENBMTCCASIwDQYJKoZIhvcNAQEBBQAD
ggEPADCCAQoCggEBAMz3EGJPprtjb+2QUlbFbSd7ehJWivH0+dbn4Y+9lavyYEEV
cNsSAPonCrVXOFt9slGTcZUOakGUWzUb+nv6u8W+JDD+Vu/E832X4xT1FE3LpxDy
FuqrIvAxIhFhaZAmunjZlx/jfWardUSVc8is/+9dCopZQ+GssjoP80j812s3wWPc
3kbW20X+fSP9kOhRBx5Ro1/tSUZUfyyIxfQTnJcVPAPooTncaQwywa8WV0yUR0J8
osicfebUTVSvQpmowQTCd5zWSOTOEeAqgJnwQ3DPP3Zr0UxJqyRewg2C/Uaoq2yT
zGJSQnWS+Jr6Xl6ysGHlHx+5fwmY6D36g39HaaECAwEAAaOCAYIwggF+MBIGA1Ud
EwEB/wQIMAYBAf8CAQAwHQYDVR0OBBYEFHSFgMBmx9833s+9KTeqAx2+7c0XMB8G
A1UdIwQYMBaAFE4iVCAYlebjbuYP+vq5Eu0GF485MA4GA1UdDwEB/wQEAwIBhjAd
BgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwdgYIKwYBBQUHAQEEajBoMCQG
CCsGAQUFBzABhhhodHRwOi8vb2NzcC5kaWdpY2VydC5jb20wQAYIKwYBBQUHMAKG
NGh0dHA6Ly9jYWNlcnRzLmRpZ2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbFJvb3RH
Mi5jcnQwQgYDVR0fBDswOTA3oDWgM4YxaHR0cDovL2NybDMuZGlnaWNlcnQuY29t
L0RpZ2lDZXJ0R2xvYmFsUm9vdEcyLmNybDA9BgNVHSAENjA0MAsGCWCGSAGG/WwC
ATAHBgVngQwBATAIBgZngQwBAgEwCAYGZ4EMAQICMAgGBmeBDAECAzANBgkqhkiG
9w0BAQsFAAOCAQEAkPFwyyiXaZd8dP3A+iZ7U6utzWX9upwGnIrXWkOH7U1MVl+t
wcW1BSAuWdH/SvWgKtiwla3JLko716f2b4gp/DA/JIS7w7d7kwcsr4drdjPtAFVS
slme5LnQ89/nD/7d+MS5EHKBCQRfz5eeLjJ1js+aWNJXMX43AYGyZm0pGrFmCW3R
bpD0ufovARTFXFZkAdl9h6g4U5+LXUZtXMYnhIHUfoyMo5tS58aI7Dd8KvvwVVo4
chDYABPPTHPbqjc1qCmBaZx2vN4Ye5DUys/vZwP9BFohFrH/6j/f3IL16/RZkiMN
JCqVJUzKoZHm1Lesh3Sz8W2jmdv51b2EQJ8HmA==
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIIDjjCCAnagAwIBAgIQAzrx5qcRqaC7KGSxHQn65TANBgkqhkiG9w0BAQsFADBh
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3
d3cuZGlnaWNlcnQuY29tMSAwHgYDVQQDExdEaWdpQ2VydCBHbG9iYWwgUm9vdCBH
MjAeFw0xMzA4MDExMjAwMDBaFw0zODAxMTUxMjAwMDBaMGExCzAJBgNVBAYTAlVT
MRUwEwYDVQQKEwxEaWdpQ2VydCBJbmMxGTAXBgNVBAsTEHd3dy5kaWdpY2VydC5j
b20xIDAeBgNVBAMTF0RpZ2lDZXJ0IEdsb2JhbCBSb290IEcyMIIBIjANBgkqhkiG
9w0BAQEFAAOCAQ8AMIIBCgKCAQEAuzfNNNx7a8myaJCtSnX/RrohCgiN9RlUyfuI
2/Ou8jqJkTx65qsGGmvPrC3oXgkkRLpimn7Wo6h+4FR1IAWsULecYxpsMNzaHxmx
1x7e/dfgy5SDN67sH0NO3Xss0r0upS/kqbitOtSZpLYl6ZtrAGCSYP9PIUkY92eQ
q2EGnI/yuum06ZIya7XzV+hdG82MHauVBJVJ8zUtluNJbd134/tJS7SsVQepj5Wz
tCO7TG1F8PapspUwtP1MVYwnSlcUfIKdzXOS0xZKBgyMUNGPHgm+F6HmIcr9g+UQ
vIOlCsRnKPZzFBQ9RnbDhxSJITRNrw9FDKZJobq7nMWxM4MphQIDAQABo0IwQDAP
BgNVHRMBAf8EBTADAQH/MA4GA1UdDwEB/wQEAwIBhjAdBgNVHQ4EFgQUTiJUIBiV
5uNu5g/6+rkS7QYXjzkwDQYJKoZIhvcNAQELBQADggEBAGBnKJRvDkhj6zHd6mcY
1Yl9PMWLSn/pvtsrF9+wX3N3KjITOYFnQoQj8kVnNeyIv/iPsGEMNKSuIEyExtv4
NeF22d+mQrvHRAiGfzZ0JFrabA0UWTW98kndth/Jsw1HKj2ZL7tcu7XUIOGZX1NG
Fdtom/DzMNU+MeKNhJ7jitralj41E6Vf8PlwUHBHQRFXGU7Aj64GxJUTFy8bJZ91
8rGOmaFvE7FBcf6IKshPECBV1/MUReXgRPTqh5Uykw7+U0b6LJ3/iyK5S9kJRaTe
pLiaWN0bfVKfjllDiIGknibVb63dDcY3fe0Dkhvld1927jyNxF1WW6LZZm6zNTfl
MrY=
-----END CERTIFICATE-----",
    "expiryDate": "2025-06-09T23:59:59Z"
}
```

