---
solution: Journey Optimizer
product: journey optimizer
title: Creare un piano di preparazione IP
description: Scopri come creare un piano di riscaldamento IP in Journey Optimizer
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, gruppo, sottodomini, recapito messaggi
exl-id: c2434086-2ed4-4cd0-aecd-2eea8f0a55f6
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '1760'
ht-degree: 6%

---

# Creare un piano di preparazione IP {#ip-warmup}

Dopo aver creato una o più [campagne di riscaldamento IP](ip-warmup-campaign.md) con una configurazione dedicata e l&#39;opzione corrispondente abilitata, puoi iniziare a creare il piano di riscaldamento IP.

Per accedere, creare, modificare ed eliminare i piani di riscaldamento IP, è necessario disporre delle autorizzazioni relative al ruolo **[!UICONTROL Consulente per il recapito messaggi]** o ai piani di riscaldamento IP.

+++Scopri come assegnare il ruolo di Consulente del recapito messaggi o le autorizzazioni relative ai piani di riscaldamento IP

Il controllo dell&#39;accesso a livello di oggetto consente di proteggere i dati e concedere un accesso specifico per visualizzare e gestire i piani. Se al piano di riscaldamento IP non viene assegnata alcuna etichetta, verrà aperto per la visualizzazione e la modifica da parte di tutti gli utenti.

La concessione dell&#39;autorizzazione **[!UICONTROL Visualizza piani di riscaldamento IP]** limita l&#39;accesso alla sola visualizzazione e pubblicazione, mentre l&#39;assegnazione dell&#39;autorizzazione **[!UICONTROL Gestisci piani di riscaldamento IP]** consente agli utenti di visualizzare e modificare il piano.

Per assegnare l&#39;autorizzazione corrispondente a un **[!UICONTROL Ruolo]** specifico:

1. Dal prodotto [!DNL Permissions], passare al menu **[!UICONTROL Ruoli]** e selezionare il ruolo da aggiornare con le nuove autorizzazioni **[!UICONTROL Configurazioni di riscaldamento IP]**.

1. Dal dashboard **[!UICONTROL Ruolo]**, fai clic su **[!UICONTROL Modifica]**.

   ![](assets/ip_permissions_1.png)

1. Trascina e rilascia la risorsa **[!UICONTROL Configurazioni di riscaldamento IP]** per assegnare le autorizzazioni.

1. Dall&#39;elenco a discesa delle risorse **[!UICONTROL Configurazioni di riscaldamento IP]**, selezionare le autorizzazioni necessarie per l&#39;utente: **[!UICONTROL Visualizza piani di riscaldamento IP]**, **[!UICONTROL Gestisci piani di riscaldamento IP]** e/o **[!UICONTROL Visualizza rapporti di riscaldamento IP]**. Se necessario, puoi selezionarli tutti contemporaneamente.

   ![](assets/ip_permissions_2.png)

1. Fai clic su **[!UICONTROL Salva]**.

Per assegnare il ruolo corrispondente a un **[!UICONTROL utente]**:

1. Dal prodotto [!DNL Permissions], passare al menu **[!UICONTROL Ruoli]** e selezionare il ruolo predefinito **[!UICONTROL Consulente recapito messaggi]**.

1. Dal dashboard **[!UICONTROL Ruolo]**, accedi alla scheda **[!UICONTROL Utenti]**.

   ![](assets/ip_permissions_3.png)

1. Fai clic su **[!UICONTROL Aggiungi utente]** per assegnare il ruolo predefinito **[!UICONTROL Consulente recapito messaggi]**.

   ![](assets/ip_permissions_4.png)

1. Seleziona il tuo **[!UICONTROL utente]** e fai clic su **[!UICONTROL Salva]**.

   ![](assets/ip_permissions_5.png)

+++

## Preparare il file del piano di preparazione IP {#prepare-file}

Il riscaldamento dell’IP è un’attività che consiste nell’aumentare gradualmente il volume di e-mail che escono dagli IP e dal dominio verso i principali provider di servizi Internet (ISP) - al fine di stabilire la tua reputazione di mittente legittimo.

Questa attività viene generalmente eseguita con l’aiuto di un esperto di recapito messaggi che aiuta a preparare un piano ben concepito basato sui domini di settore, i casi di utilizzo, le aree geografiche, gli ISP e vari altri fattori.

<!--When working with the [!DNL Journey Optimizer] IP warmup feature, this plan takes the form of an Excel file that must contain a number of predefined columns.-->

Prima di poter creare un piano di riscaldamento IP nell&#39;interfaccia [!DNL Journey Optimizer], è necessario compilare un modello di Excel con tutti i dati che alimenteranno il piano.

* Dall&#39;interfaccia utente è possibile scaricare il modello di [piano di riscaldamento IP di Excel](assets/IPWarmupPlan-Template.xlsx) vuoto da compilare.

* Puoi anche scaricare un [piano di riscaldamento dell&#39;IP di esempio](assets/IPWarmupPlan-Sample.xlsx) già compilato con alcuni dati che puoi utilizzare come esempio.

<!--
* From the user interface you can download the blank Excel IP warmup plan template to fill in.

* You can also download a sample IP warmup plan already filled in with some data you can use as an example.
-->

>[!CAUTION]
>
>Rivolgiti al tuo consulente di recapito messaggi per assicurarti che il file del piano di riscaldamento IP sia configurato correttamente.
>
>Assicurati di utilizzare il formato fornito nel modello.

Di seguito è riportato un esempio di file contenente un piano di riscaldamento IP.

![](assets/ip-warmup-sample-file.png)

### Scheda Piano di riscaldamento {#ip-warmup-plan-tab}

Per creare il piano di riscaldamento IP, compila la prima scheda con i dati necessari per alimentare il piano.

* Nell&#39;esempio precedente, è stato preparato un piano che si estende su 17 giorni (denominato &#39;**esecuzioni**&#39;) per raggiungere un volume di destinazione di oltre un milione di profili.

* Questa operazione pianificata viene eseguita in sei **fasi**, ognuna delle quali contiene almeno una esecuzione.

* Puoi avere fino a 6 colonne (4 colonne per i gruppi di dominio, una per la colonna **Altri** e una per la colonna **Giorni di coinvolgimento**). In questo esempio, il piano è diviso in sei colonne:

   * Tre di questi corrispondono a **gruppi di dominio predefiniti** da utilizzare nel piano (Gmail, Yahoo e Microsoft). I gruppi di dominio predefiniti sono tutti elencati nella scheda [Gruppi di dominio OOTB](#ootb-domain-groups-tab).
   * Una colonna corrisponde a un gruppo di dominio personalizzato (che è necessario aggiungere utilizzando la scheda [Gruppo di dominio personalizzato](#custom-domain-group-tab)).
   * La quinta colonna, **Altri**, contiene tutti gli indirizzi rimanenti di altri domini non inclusi esplicitamente nel piano. Questa colonna è facoltativa: se omessa, le e-mail verranno inviate solo ai domini specificati.
   * L&#39;ultima colonna, **Giorni di coinvolgimento**, consente di specificare il numero di giorni in cui il coinvolgimento deve essere tracciato o valutato.

L’idea è quella di aumentare progressivamente il numero di indirizzi target in ogni esecuzione, riducendo al contempo il numero di esecuzioni per ogni fase.

### Scheda Gruppo di dominio personalizzato {#custom-domain-group-tab}

Puoi anche aggiungere più colonne al piano includendo gruppi di dominio personalizzati.

Utilizzare la scheda **[!UICONTROL Gruppo di dominio personalizzato]** per definire un nuovo gruppo di dominio. Per ogni dominio, puoi aggiungere tutti i sottodomini coperti.

>[!IMPORTANT]
>
>Assicurati che ogni dominio sia univoco per il relativo gruppo di dominio e non si sovrapponga ad altri gruppi di dominio o [gruppi di dominio predefiniti](#ootb-domain-groups-tab).

Ad esempio, se aggiungi il dominio personalizzato Roadrunner, vuoi includere i seguenti sottodomini, come nell’esempio seguente: roadrunner.com, nc.rr.com, tampabay.rr.com, rochester.rr.com, ecc.

![](assets/ip-warmup-sample-file-custom.png)

>[!NOTE]
>
>Se non sono necessari domini personalizzati, lasciare vuota la scheda **[!UICONTROL Gruppo di dominio personalizzato]**.

### Scheda Gruppi di dominio preconfigurati {#ootb-domain-groups-tab}

La scheda **Gruppi di dominio OOTB** del modello di piano di riscaldamento IP contiene tutti i gruppi di dominio principali predefiniti che è possibile aggiungere al piano.

![](assets/ip-warmup-sample-file-ootb.png)

>[!NOTE]
>
>Se un gruppo di dominio non è elencato in questa scheda, è necessario creare un gruppo di dominio personalizzato nella scheda corrispondente. [Ulteriori informazioni](#custom-domain-group-tab)

Di seguito sono elencati anche i gruppi di dominio principali predefiniti:

+++ Gmail
gmail.com;google.com;googlemail.com;googlemail.co.uk
+++

+++Microsoft
hotmail.com.tr;live.de;live.ru;live.nl;windowslive.com;live.jp;mts.net;xbox.com;hotmail.fr;hotmail.cl;hotmail.jp;live.cl;live.at;live.com.au;hotmail.co.th;live.hk;hotmail.com.au;hotmail.com;live.com.my;hotmail.co.kr;live.ie;outlook.com.br;hotmail.co.il;hotmail.dk;live.co.kr;live.co.uk;live.com.mx;outlook.ie;live.cn;hotmail.co.uk;live.com.sg;hotmail.es;live.fr;live.no;live.dk;hotmail.it;msn.com;live.se;hotmail.co.jp;live.be;live.co.za;live.in;hotmail.htmail.live.com.pt;hotmail.ch;outlook.com;live.com;hotmail.gr;live.it;live.com.ar;hotmail.ca;hotmail.com.br;hotmail.com.ar;live.ca;hotmail.de
+++

+++Yahoo
aol.fi;games.com;cs.com;yahoo.com.in;y7mail.com;yahoo.co.uk;yahoo.hu;yahoo.co.hu;yahoo.cn;yahoogroups.com.sg;yahoogroups.com.au;aol.es;yahoo.com.au;yahoo.com.vn;yahoo.ca;aol.hk;aol.co.nz;yahoo.com.br;aolpoland.pl;aolnorge.no;yahoo.ne.jp;yahoo.fi;ymail.com;netscape.com;yahoo.com.pe;yahoo.hr;aol.cz;yahoo.ee;aol.be;aolcom.tr;yahoo.si;yahoo.co.id;aol.it;citlink.net;yahoo.es yahoo.dk;yahoogroups.ca;wmconnect.com;yahoo.com.jp;aol.kr;yahoo.ie;aol.jp;yahoo.com.hk;yahoo.lt;aol.com.br;aol.nl;yahoo.co.kr;yahoo.bg;yahoo.com.ar;ygm.com;aol.se;yahoo.co.nz;yahoo.de;aol.com;goowy.com;rocketmail.com;frontiernet.net;yahoo.nl;aim.com;aol.dk;yahoogroups.co.in;aol.cl;netscape.net;yahoo.no;luckymail.com;yahoo.cz;yahoo.co.jp;yahoo.sk;yahoo.com.kr yahoogroups.de;yahoo.gr;yahoo.co.za;verizon.net;yahoo.ro;aol.com.ve;yahoo.at;aol.com.ar;aol.com.co;wild4music.com;aol.fr;yahoo.in;aol.in;yahoogroups.com.cn;yahoo.rs;aol.de;yahoo.com.co;wow.com;yahoo.com;yahooxtra.co.nz;yahoo.com.mx;yahoo.com.ph;sky.com;aol.com.mx;yahoo.se;myaol.jp;aol.com.au;yahoo.pt;aolchina.com;yahoo.com.net;yahoo.dk;yahoo.fr;yahoo.com.tw;aol.pl;talk21.com;compuserve.com;aol.aol.aol yahoo.it;yahoo.com.sg;yahoogroups.com.tw;aolpolcka.pl;frontier.com;yahoo.co.in;yahoogruppi.it;yahoo.co.il;yahoo.cl;verizon.net.in;yahoo.com.tr;yahoogroups.com.hk;yahoogroups.co.uk;yahoo.be;yahoo.com.biz;yahoo.com.hr;aol.tw;aol.co.uk;ybb.ne.jp;yahoogroups.co.kr;yahoo.com.my;rogers.com;gte.net;yahoogroups.com;yahoo.co.th;yahoo.com.cn;love.com;bellatlantic.net;aol.ru;yahoo.com.ve;yahoo.com.ua;yahoo.lv;aolpolska.pl;aol.at;yahoo.pl
+++

+++Apple
mac.com;icloud.com;apple.com;me.com
+++

+++Comcast
comcast.net
+++

+++Arancione
voila.com;francetelecom.com;orange.com;orange.fr;wanadoo.fr;voila.fr
+++

+++La Poste
laposte.net
+++

+++Italia Online
inwind.it;blu.it;virgilio.it;giallo.it;iol.it;libero.it
+++

+++WP
wp.pl;o2.pl
+++

+++United Internet
gmx.de;1and1.com;gmx.fr;mail.com;1und1.de;gmx.com;gmx.net;gmx.at;web.de;gmx.ch
+++

+++Bigpond
bigpond.com;bigpond.com.au;bigpond.net;telstra.com;bigpond.net.au
+++

+++Docomo
docomo.ne.jp
+++

+++Softbank
c.vodafone.ne.jp;jp-h.ne.jp;k.vodafone.ne.jp;jp-d.ne.jp;jp-c.ne.jp;t.vodafone.ne.jp;h.vodafone.ne.jp;r.vodafone.ne.jp;q.vodafone.ne.jp;jp-t.ne.jp;jp-q.ne.jp;s.vodafone.ne.jp;jp-s.ne.jp;jp-r.ne.jp;jp-k.ne.jp;n.vodafone.ne.jp;d.vodafone.ne.jp;softbank.ne.jp;jp-n.ne.jp
+++

+++KDDI
au.com;ezweb.ne.jp;uqmobile.jp
+++

### Esempio {#example}

Supponiamo che tu voglia disporre di due gruppi di dominio personalizzati:

* Uno solo per i domini Hotmail.
* Uno per tutti gli altri domini del gruppo di dominio Microsoft (escludendo quindi tutti i domini Hotmail).

I domini esterni a Hotmail e dal gruppo di domini Microsoft verranno raccolti nella colonna **[!UICONTROL Altri]**.

1. Nella scheda **[!UICONTROL Gruppo di dominio personalizzato]**, crea il gruppo di dominio **Hotmail**.

1. Aggiungi tutti i domini Hotmail sulla stessa riga.

   È possibile [copiare e incollare](#copy-paste) tutti i domini di Hotmail elencati nella sezione [scheda Gruppi di domini OOTB](#ootb-domain-groups-tab).

1. Aggiungi un&#39;altra riga.

1. Crea il gruppo di dominio **Microsoft_X**.

1. Aggiungi tutti i domini Microsoft che non sono Hotmail sulla stessa riga. Allo stesso modo, puoi [copiarli e incollarli](#copy-paste) dall&#39;elenco precedente.

1. Torna alla scheda **[!UICONTROL Piano di riscaldamento IP]**.

1. Creare tre colonne: una per **Hotmail**, una per **Microsoft_X** e una per **Altri**.

1. Compila le colonne in base alle tue esigenze.

<!--Only the domain groups listed in the **[!UICONTROL IP Warmup Plan]** tab will be taken into account.-->

### Copiare e incollare i domini predefiniti {#copy-paste}

Se ad esempio si desidera creare un gruppo di dominio personalizzato contenente tutti i domini di Hotmail, è possibile copiare e incollare i domini dalla scheda **Gruppi di dominio OOTB** del [modello di piano di riscaldamento IP](assets/IPWarmupPlan-Template.xlsx) o dall&#39;elenco fornito [sopra](#ip-warmup-plan-tab).

Quindi utilizzare lo strumento di conversione Excel per convertire il testo in colonne:

1. Seleziona **[!UICONTROL Dati]** > **[!UICONTROL Testo in colonne...]**, scegli **[!UICONTROL Delimitati]** e seleziona **[!UICONTROL Successivo]**.

1. Seleziona **[!UICONTROL Punto e virgola]**, fai clic su **[!UICONTROL Avanti]** e **[!UICONTROL Fine]**.

Ogni dominio ora viene visualizzato in una colonna diversa sulla stessa riga.

## Accesso e gestione dei piani di riscaldamento IP {#manage-ip-warmup-plans}

1. Accedi al menu **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni e-mail]** > **[!UICONTROL Piani di riscaldamento IP]**. Vengono visualizzati tutti i piani di riscaldamento IP creati finora.

   ![](assets/ip-warmup-filter-list.png)

1. Puoi filtrare in base allo stato. I diversi stati sono:

   * **Non avviato**: nessuna esecuzione è stata ancora attivata. [Ulteriori informazioni](ip-warmup-execution.md#define-runs)
   * **Live**: il piano passa a questo stato non appena la prima esecuzione nella prima fase è stata attivata correttamente. [Ulteriori informazioni](ip-warmup-execution.md#define-runs)
   * **Completato**: il piano è stato contrassegnato come completato. <!--This option is only available if all the runs in the plan are in **[!UICONTROL Completed]** or **[!UICONTROL Draft]** status (no run can be **[!UICONTROL Live]**).--> [Ulteriori informazioni](ip-warmup-execution.md#mark-as-completed)
     <!--* **Paused**: to check (user action)-->

1. Per eliminare un piano di riscaldamento IP, selezionare l&#39;icona **[!UICONTROL Elimina]** accanto al nome di un piano e confermare l&#39;eliminazione.

   >[!NOTE]
   >
   >È possibile eliminare solo i piani con stato **Non avviato**.

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >Il piano di riscaldamento IP selezionato verrà eliminato definitivamente.

## Creare un piano di preparazione IP {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="Specificare il piano di preparazione IP"
>abstract="Compila il modello Excel con tutti i dati che alimenteranno il tuo piano, ad esempio le fasi di preparazione IP e il numero di profili di destinazione, e caricalo qui."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/implement-ip-warmup-plan/ip-warmup-plan.html?lang=it#prepare-file" text="Preparare il file del piano di preparazione IP"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="Selezionare una configurazione di marketing"
>abstract="Devi selezionare la stessa configurazione di quella selezionata nella campagna da associare al piano di preparazione IP."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=it" text="Impostare le configurazioni dei canali"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=it" text="Creare campagne di preparazione IP"

Per creare un piano di riscaldamento IP, attenersi alla procedura descritta di seguito.

1. Accedi al menu **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni e-mail]**> **[!UICONTROL Piani di riscaldamento IP]**, quindi fai clic su **[!UICONTROL Crea piano di riscaldamento IP]**.

   ![](assets/ip-warmup-create-plan.png)

1. Compila i dettagli del piano di riscaldamento IP: fornisci un nome e una descrizione.

   ![](assets/ip-warmup-plan-details.png)

1. Selezionare la [configurazione](channel-surfaces.md) che si desidera riscaldare. Solo le configurazioni di marketing sono disponibili per la selezione. [Ulteriori informazioni sul tipo di e-mail](../email/email-settings.md#email-type)

   >[!NOTE]
   >
   >Le campagne da associare al piano di riscaldamento IP devono utilizzare la stessa configurazione. [Scopri come creare una campagna di riscaldamento IP](ip-warmup-campaign.md)

1. Carica il file Excel contenente il piano di riscaldamento IP. [Ulteriori informazioni](#prepare-file)

   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

   >[!NOTE]
   >
   >Se il caricamento non riesce, assicurati di utilizzare la formattazione e il formato di file corretti (xls o xlsx). Utilizza il [modello](assets/IPWarmupPlan-Template.xlsx) fornito da Adobe.

1. Fai clic su **[!UICONTROL Crea]**. Tutte le fasi, le esecuzioni, le colonne e il relativo contenuto definito nel file caricato vengono visualizzati automaticamente nell&#39;interfaccia [!DNL Journey Optimizer].

   ![](assets/ip-warmup-plan-uploaded.png)

   >[!NOTE]
   >
   >La colonna **[!UICONTROL Target]** mostra la somma di tutti i profili target per ogni esecuzione, ovvero tutti i profili di ogni gruppo di dominio definito, inclusa l&#39;eventuale colonna **Altri**.

Ora puoi eseguire il piano di riscaldamento IP. [Ulteriori informazioni](ip-warmup-execution.md)
