---
solution: Journey Optimizer
product: journey optimizer
title: Chiavi gestite dal cliente
description: Scopri come configurare e gestire le chiavi del cliente per Adobe Journey Optimizer.
feature: Privacy, Monitoring
role: Developer, User, Admin, Leader
level: Intermediate
exl-id: f0985d1f-0bcf-452f-bd46-dfeca0424f01
source-git-commit: f9e1ae68fcfb9ecc12e0b80a067ca29186fc01f7
workflow-type: ht
source-wordcount: '223'
ht-degree: 100%

---

# Configurazione e gestione delle chiavi gestite dal cliente {#cmk}

>[!AVAILABILITY]
>
>La funzionalità [!DNL Customer Managed Keys] è attualmente disponibile solo per le organizzazioni che hanno acquistato le offerte aggiuntive [Healthcare Shield o Privacy &amp; Security Shield](https://experienceleague.adobe.com/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield.html?lang=it){target="_blank"}.

Con Adobe Journey Optimizer, i clienti di [Healthcare Shield](https://www.adobe.com/trust/compliance/hipaa-ready.html){target="_blank"} e Privacy &amp; Security Shield hanno la possibilità di fruttare le chiavi gestite dal cliente Azure (CMK) e applicarle ai propri dati.

Il processo di configurazione di Journey Optimizer prevede due parti che sfruttano la tecnologia di Adobe Experience Platform e Customer Journey Analytics (CJA):

* Segui i passaggi descritti nella documentazione [Chiavi gestite dal cliente in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys.html?lang=it){target="_blank"}.
* Segui i passaggi descritti nella documentazione [Chiavi gestite dal cliente in Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-privacy/cmk.html?lang=it){target="_blank"}.

  È necessario completare questa procedura di configurazione anche se Customer Journey Analytics (CJA) non è stato acquistato, in quanto alcuni componenti di CJA vengono utilizzati in background.

Per completare il processo di configurazione, consulta le istruzioni dettagliate riportate nella documentazione [Chiavi gestite dal cliente in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/encryption.html?lang=it){target="_blank"}.

Sia Adobe Experience Platform che le chiavi gestite dal cliente garantiscono la sicurezza dei dati crittografandoli in transito e a riposo. I dati rimangono protetti, indipendentemente dal fatto che si utilizzino o meno le chiavi gestite dal cliente.

Per ulteriori informazioni sulla crittografia dei dati in Adobe Experience Platform, consulta la [documentazione](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/encryption.html?lang=it){target="_blank"} sulla crittografia dei dati.
