---
solution: Journey Optimizer
product: journey optimizer
title: Record DMARC
description: Scopri come impostare il record DMARC in Journey Optimizer
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: sottodominio, dominio, posta, dmarc, record
hide: true
hidefromtoc: true
source-git-commit: 5565c98e41e0abc9ae93f85cb12679e372e6d36f
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# Aggiornamento importante record DMARC{#dmarc-record}


>[!CAUTION]
>
>A seguito dei recenti annunci Gmail e Yahoo per mittenti in blocco, Journey Optimizer ora supporta la tecnologia di autenticazione DMARC.

Come parte delle procedure ottimali di settore, Google e Yahoo richiederanno entrambi di avere un record DMARC per qualsiasi dominio utilizzato per inviare loro e-mail. Questo nuovo requisito inizia il **1 febbraio 2024**.

Ulteriori informazioni sui requisiti di Google e Yahoo per il record DMARC in [questa sezione](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Ulteriori informazioni sulle modifiche annunciate in Google e Yahoo su [questa pagina](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/guidance-around-changes-to-google-and-yahoo.html?lang=en#dmarc%3A){target="_blank"}.

Ora avrai un&#39;azione o passaggi successivi per la sezione che ti indicherà:

Devi configurarlo per tutti i tuoi sottodomini
* Se hai delegato completamente il dominio a noi, allora hai due opzioni
   * Configurare DMARC sul dominio padre del dominio delegato nella soluzione di hosting, OPPURE
   * Configurare DMARC su un dominio delegato utilizzando la nostra prossima funzionalità nell’interfaccia di amministrazione senza ulteriori interventi sulla soluzione di hosting
* Se hai impostato il CNAME per i domini di invio, hai due opzioni
   * Configurare DMARC sul sottodominio O sul dominio principale del sottodominio nella soluzione di hosting, OPPURE
   * Configura il DMARC utilizzando la nostra prossima funzione nell’interfaccia di amministrazione. Tuttavia, richiederà non solo la nostra interfaccia utente, ma anche la voce nella soluzione di hosting.

Maggiori dettagli sulle prossime funzionalità saranno disponibili a breve.

Inoltre, se non impostato, l&#39;impatto può essere incluso copiando la sezione relativa al DMARC dalla sezione sottostante (copiata dal collegamento riportato sopra). Ora, o estraiamo solo elementi correlati al DMARC. In alternativa, è possibile indicare che l&#39;annuncio è per DMARC e l&#39;annullamento di un clic; qui è riportata la versione più recente della timeline per entrambe le funzioni.

Sono stati aggiornati i tempi rispetto all&#39;annuncio originale di ottobre.

Le timeline più recenti sono simili al seguente:

Gmail:

* Febbraio 2024 - Inizieranno i mancati recapiti temporanei progettati per fornire un avviso di non conformità. Le e-mail continueranno a essere consegnate come di consueto dopo un breve ritardo se non sei ancora in regola con le normative. Se sei pienamente conforme, non ci saranno mancati recapiti temporanei e non noterai nulla.
* Aprile 2024 - Inizieranno i blocchi per i mittenti che non sono conformi a tutto eccetto List-Unsubscribe 1-Click. Solo una parte delle e-mail non conformi verrà bloccata inizialmente, con % bloccato in aumento nel tempo.
* 1 giugno 2024 - Qualsiasi mittente non pienamente conforme, incluso List-Unsubscribe 1-Click, si troverà in stato di blocco.

Yahoo:

Non ha fornito date esatte, ma ha detto che &quot;l&#39;introduzione dell&#39;applicazione inizierà a febbraio 2024. L&#39;applicazione sarà introdotta gradualmente&quot;.
