---
solution: Journey Optimizer
product: journey optimizer
title: Chiavi gestite dal cliente
description: Scopri come configurare e gestire le chiavi del cliente per Adobe Journey Optimizer.
feature: Privacy, Monitoring
role: Developer, User, Admin, Leader
level: Intermediate
exl-id: f0985d1f-0bcf-452f-bd46-dfeca0424f01
TQID: https://experienceleague.adobe.com/yCl5CISD1-Xx6gfcK2sWdFWAeE0LicO-3r3YndB2cVQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2:
  - id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56
  - id: f365ec33-2b99-4b7f-b4ee-c743dd7f615f
  - id: c8d5f2ce-ba44-43e9-a2bf-94a3d7d85ec3
source-git-commit: 4e89993a998268ae2810c949d0669bf6dc458dd6
workflow-type: tm+mt
source-wordcount: 312
ht-degree: 89%

---

# Configurare e gestire le chiavi gestite dal cliente {#cmk}

>[!BEGINSHADEBOX]

**In questa pagina:** configurare e gestire le chiavi gestite dal cliente (CMK) in modo da poter crittografare i dati Adobe Journey Optimizer con le proprie chiavi e mantenerli protetti in transito e a riposo.

>[!ENDSHADEBOX]

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
