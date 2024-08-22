---
title: Configurazione del canale web
description: Creare la configurazione del canale web
feature: Web Channel, Channel Configuration
topic: Content Management
role: Admin
level: Experienced
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 1%

---

# Creare la configurazione del canale web {#web-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_page_rule"
>title="Regola di corrispondenza delle pagine"
>abstract="Per gestire e indirizzare in modo efficiente un gruppo di URL che condividono gli stessi criteri, crea una regola di corrispondenza Pagine. Questa regola ti consente di consolidare più URL in un’unica linea guida, semplificando l’applicazione di impostazioni e azioni coerenti in queste pagine."

>[!CONTEXTUALHELP]
>id="ajo_admin_default_url"
>title="URL predefinito per authoring e anteprima"
>abstract="Questo campo assicura che le pagine generate o associate dalla regola abbiano un URL designato, essenziale sia per la creazione che per l’anteprima efficace del contenuto."

Una configurazione web è una proprietà web identificata da un URL in cui il contenuto verrà recapitato. Può corrispondere a un singolo URL di pagina o a più pagine, consentendoti di apportare modifiche in una o più pagine web.

1. Accedi al menu **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni generali]** > **[!UICONTROL Configurazioni canale]**, quindi fai clic su **[!UICONTROL Crea configurazione canale]**.

   ![](assets/web_config_1.png)

1. Immetti un nome e una descrizione (facoltativa) per la configurazione.

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare i caratteri di sottolineatura `_`, punto`.` e trattino `-`.

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base alla configurazione, è possibile selezionare **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni sul controllo degli accessi a livello di oggetto](../administration/object-based-access.md).

1. Seleziona il canale **Web**.

   ![](assets/web_config_2.png)

1. Seleziona **[!UICONTROL Azione di marketing]** per associare i criteri di consenso ai messaggi utilizzando questa configurazione. Tutti i criteri di consenso associati all’azione di marketing vengono utilizzati per rispettare le preferenze dei clienti. [Ulteriori informazioni](../action/consent.md#surface-marketing-actions)

1. È possibile immettere un **[!UICONTROL URL pagina]** se si desidera applicare le modifiche solo a una singola pagina.

1. Oppure puoi creare una **[!UICONTROL regola di corrispondenza pagine]** per eseguire il targeting di più URL che corrispondono alla stessa regola, ad esempio, se desideri applicare le modifiche a un banner principale in un intero sito Web o aggiungere un&#39;immagine superiore che viene visualizzata in tutte le pagine di prodotto di un sito Web.

   A tale scopo, selezionare **[!UICONTROL Pagine corrispondenti alla regola]**.

1. Definisci i criteri per i campi **[!UICONTROL Dominio]** e **[!UICONTROL Pagina]**.

   Ad esempio, se desideri modificare gli elementi visualizzati in tutte le pagine del sito Web Luma relative alle donne, seleziona **[!UICONTROL Dominio]** > **[!UICONTROL Inizia con]** > `luma` e **[!UICONTROL Pagina]** > **[!UICONTROL Contiene]** > `women`.

   ![](assets/web_config_3.png)

1. Se hai creato una **[!UICONTROL regola di corrispondenza delle pagine]**, devi immettere l&#39;URL **Predefinito** per l&#39;authoring e l&#39;anteprima. Questo passaggio assicura che le pagine generate o associate dalla regola abbiano un URL designato sia per la creazione di contenuti che per l’anteprima. Ulteriori informazioni sulla regola di corrispondenza delle pagine nella [sezione seguente](#web-page-matching-rule).

1. Salva le modifiche.

Ora puoi selezionare la tua configurazione quando utilizzi il canale web in campagne o percorsi.

## Regola di corrispondenza pagina {#web-page-matching-rule}

Quando crei una regola che corrisponde a più pagine in modo da poter applicare le stesse modifiche al contenuto in più pagine contemporaneamente, puoi utilizzare operatori diversi nel **Dominio** e nelle sezioni **Percorso** per generare la regola desiderata. Controlla gli operatori disponibili di seguito.

Operatori disponibili per la creazione di regole di corrispondenza delle pagine:

* **Dominio**

  | Operatore  | Descrizione  | Esempi  |
  |---|---|---|
  | Uguale a  | Corrispondenza esatta del dominio.  |
  | Inizia con  | Corrisponde a tutti i domini (inclusi i sottodomini) che iniziano con la stringa immessa.  | Esempio: &quot;Starts with: dev&quot; -> rileva tutti i domini e i sottodomini che iniziano con &quot;dev&quot;, come: dev.example.com, dev.products.example.com, developer.example.com  |
  | Termina con  | Corrisponde a tutti i domini (inclusi i sottodomini) che terminano con la stringa immessa.  | Esempio: &quot;Ends with: example.com&quot; -> rileva tutti i domini e i sottodomini che terminano con &quot;example.com&quot;, come: stage.example.com, prod.example.com, myexample.com  |
  | Corrispondenza con caratteri jolly  | L’operatore &quot;Wildcard matching&quot; (Corrispondenza caratteri jolly) consente di definire una corrispondenza con caratteri jolly al centro della stringa, ad esempio &quot;dev.*.example.com&quot; Le regole di convalida prevedono che il valore debba contenere un solo carattere jolly (asterisco) quando l’operatore è &quot;corrispondenza con caratteri jolly&quot;.  | Esempio: &quot;Abbinamento con caratteri jolly: dev.*.example.com&quot; -> corrisponde a domini come: dev.products.example.com, dev.mytest.products.example.com, dev.blog.example.com  |
  | Qualsiasi  | Corrisponde a tutti i domini: utile quando si esegue il test di un percorso particolare tra più domini  |


* **Percorso**

  | | | |
  |-|-|-|
  | Operatore  | Descrizione  | Esempi  |
  | Uguale a  | Corrispondenza esatta del percorso.  |    |
  | Inizia con  | Corrisponde a tutti i percorsi (inclusi i percorsi secondari) che iniziano con la stringa immessa.  |    |
  | Termina con  | Corrisponde a tutti i percorsi (inclusi i percorsi secondari) che terminano con la stringa immessa.  |    |
  | Qualsiasi  | Corrisponde a tutti i percorsi: utile quando si esegue il targeting di tutti i percorsi sotto uno o più domini.  |    |
  | Corrispondenza con caratteri jolly  | L&#39;operatore &quot;Corrispondenza caratteri jolly&quot; consente all&#39;utente di definire un carattere jolly interno nel percorso, ad esempio &quot;/products/*/detail&quot;.  Il carattere jolly * nel componente ** percorso corrisponde a qualsiasi sequenza di caratteri fino a quando non viene rilevato il primo carattere /.  /*/ corrisponde a qualsiasi sequenza di caratteri (inclusi i percorsi secondari)  | Esempio: &quot;Corrispondenza con caratteri jolly: /products/*/detail&quot;, corrisponde a tutti i percorsi come:  example.com/products/yoga/detail  example.com/products/surf/detail  example.com/products/tennis/detail  example.com/products/yoga/pants/detail   Esempio: &quot;Corrisponde a: /prod*/detail, corrisponde a tutti i percorsi come:  example.com/products/detail  example.com/production/detail   non corrisponde a percorsi come:  example.com/products/yoga/detail  |
  | Contiene  | &quot;contains&quot; viene tradotto in un carattere jolly come &quot;mystring&quot; e corrisponde a tutti i percorsi che contengono questa sequenza di caratteri.  | Esempio: &quot;Contains: product&quot; (Contiene: prodotto), corrisponde a tutti i percorsi che contengono la stringa di prodotto, come: example.com/products, example.com/yoga/perfproduct, example.com/surf/productdescription, example.com/home/product/page  |


Se il caso d’uso non può essere modellato utilizzando una regola, puoi aggiungere più regole di pagina e utilizzare gli operatori &quot;Or&quot; o &quot;Exclude&quot; tra di esse. &#39;Escludi&#39; è utile quando una delle pagine che corrispondono alla regola definita non deve essere mirata: ad esempio, tutte le pagine &quot;example.com&quot; che contengono &quot;product&quot;, esclusa la pagina seguente: `https://example.com/blogs/productinfo`.