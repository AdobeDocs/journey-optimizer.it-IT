---
solution: Journey Optimizer
product: journey optimizer
title: Elenco esclusioni
description: Ulteriori informazioni sulle esclusioni che si verificano durante l’invio
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: a34ba1a8-87d5-4f9c-a181-2f49e74e8f09
source-git-commit: 853e87cdd69a3fc180dcb1aa38b4b67f27977939
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 8%

---

# Motivi di esclusione {#exclusion-list}

## Conteggio delle esclusioni nei rapporti delle campagne

Quando visualizzi i rapporti sulle campagne, tieni presente che la metrica *Esclusioni* viene calcolata come segue:

**Esclusioni = Esclusioni univoche + Eventi di esclusione duplicati**

Ciò significa che se un profilo viene escluso più volte (ad esempio, a causa di più eventi di esclusione per lo stesso profilo), ogni evento viene conteggiato nel totale Esclusioni. Di conseguenza, la somma di *Delivered* e *Exclusions* potrebbe superare le dimensioni del pubblico di destinazione originale. Questo comportamento è previsto e riflette il modo in cui gli eventi di esclusione vengono tracciati nel sistema.

**Esempio:**

- Pubblico di destinazione: 94.000 profili
- Consegnato: 69.000
- Esclusioni: 37.000 (include eventi di esclusione duplicati)
- Totale (Consegne + Esclusioni): 106.000

Il totale supera il pubblico di destinazione perché nel conteggio delle esclusioni sono inclusi eventi di esclusione duplicati.

Per ulteriori dettagli sui motivi specifici di esclusione, consulta la tabella seguente.

## Elenco motivi di esclusione

| Motivo di esclusione | Codice errore | Canale | Spiegazione |
|-|-|-|-|
| RuntimeDispatchError | 050301 | Tutti i canali | Evento di esclusione generico per qualsiasi errore di invio runtime. |
| RuntimeRenderingError | 050302 | Tutti i canali | Evento di esclusione generico per qualsiasi errore di rendering Runtime. |
| NamespaceErrorForExperimentation | 050017 | Tutti i canali | Un evento di esclusione viene generato quando Namespace in Experiment è diverso dallo spazio dei nomi del profilo. |
| SperimentazioneEsclusioneDiRitenzione | 050018 | Tutti i canali | Questo evento di esclusione viene generato quando il trattamento qualificato per un esperimento è &quot;Holdout&quot;. |
| ExcludedForControlRules | 050002 | Tutti i canali | Questo evento di esclusione viene generato quando la consegna del messaggio corrente comporta la violazione delle regole di controllo, ad esempio il numero di e-mail consentite in un mese. |
| DirectMailNoVariantDefined | 050062 | DirectMail | Un evento di esclusione viene generato quando nella variante direct mailing non è definita. |
| DirectMailNoMessageFoundForTreatment | 050061 | DirectMail | Un evento di esclusione viene generato quando l’esperimento è abilitato per il messaggio e non viene trovato alcun messaggio per il trattamento qualificato. |
| EmailNoConsent | 050101 | E-mail | Un evento di esclusione viene generato quando l’utente rinuncia alla ricezione di e-mail di marketing. |
| Soppresso | 050107 | E-mail | Esclusione a causa di uno dei motivi di soppressione. |
| E-mail soppressa | 050102 | E-mail | Quando l’e-mail di destinazione viene soppressa, viene generato un evento di esclusione. |
| DomainSuppressed | 050105 | E-mail | Quando il dominio dell’e-mail di destinazione viene eliminato, viene generato un evento di esclusione. |
| NotAllowed | 050108 | E-mail | Un evento di esclusione viene generato quando l’elenco Consentiti è abilitato e l’e-mail di destinazione viene esclusa dall’elenco Consentiti. |
| EmailNotAllowed | 050103 | E-mail | Un evento di esclusione viene generato quando l’elenco Consentiti è abilitato e l’e-mail di destinazione viene esclusa dall’elenco Consentiti. |
| DomainNotAllowed | 050106 | E-mail | Un evento di esclusione viene generato quando l’elenco Consentiti è abilitato e il dominio dell’e-mail di destinazione è escluso dall’elenco Consentiti. |
| EmailNoSubscriberIdFoundInProfile | 050025 | E-mail | Un evento di esclusione viene generato quando subscriberId non viene trovato nel profilo di un’e-mail di abbonamento. |
| EmailNoAddressFoundInProfile | 050020 | E-mail | Un evento di esclusione viene generato quando l’indirizzo e-mail non è presente nell’indirizzo di esecuzione. |
| EmailNoAddressDefinedInPreset | 050021 | E-mail | Un evento di esclusione viene generato quando l’indirizzo di esecuzione non è definito nella configurazione. |
| EmailNoVariantDefined | 050026 | E-mail | Un evento di esclusione viene generato quando nel messaggio e-mail non è definita alcuna variante. |
| EmailNoMessageFoundForTreatment | 050027 | E-mail | Un evento di esclusione viene generato quando l’esperimento è abilitato per il messaggio e non viene trovato alcun messaggio per il trattamento qualificato. |
| EmailMalformedAddress | 050024 | E-mail | Se l’e-mail contiene un indirizzo non valido, viene generato un evento di esclusione. |
| InAppNoVariantDefined | 050041 | InApp | Un evento di esclusione viene generato quando non è definita alcuna variante per il messaggio InApp. |
| InAppNoMessageFoundForTreatment | 050042 | InApp | Un evento di esclusione viene generato quando l’esperimento è abilitato per il messaggio e non viene trovato alcun messaggio per il trattamento qualificato. |
| PushNoTokenFoundInProfile | 050030 | Push | Quando il profilo non dispone di token push, viene generato un evento di esclusione. |
| PushNoValidTokenFoundForApps | 050031 | Push | Quando non viene trovato alcun token valido per le app di destinazione nella configurazione, viene generato un evento di esclusione. |
| PushMalformedProfile | 050034 | Push | Quando il formato di pushNotificationDetails nel profilo non è corretto, viene generato un evento di esclusione. |
| PushNoConsent | 050111 | Push | Un evento di esclusione viene generato quando l’utente ha rinunciato alle notifiche push di marketing. |
| PushNoApplicationDefinedInPreset | 050033 | Push | Un evento di esclusione viene generato quando la configurazione non contiene alcuna applicazione di destinazione. |
| PushNoVariantDefined | 050035 | Push | Quando non è definita alcuna variante, viene generato un evento di esclusione. |
| PushNoMessageFoundForTreatment | 050036 | Push | Un evento di esclusione viene generato quando l’esperimento è abilitato per il messaggio e non viene trovato alcun messaggio per il trattamento qualificato. |
| SMSNoConsent | 050104 | SMS | Un evento di esclusione viene generato quando l’utente ha rinunciato al marketing degli SMS. |
| SMSFromNumberNotDefinedInPreset | 050152 | SMS | Un evento di esclusione viene generato quando &quot;FromNumber&quot; non è definito nella configurazione. |
| SMSNoToNumberDefinedInProfile | 050153 | SMS | Un evento di esclusione viene generato quando &quot;ToNumber&quot; non è definito nella configurazione. |
| SMSNoVariantDefined | 050154 | SMS | Quando non è definita alcuna variante, viene generato un evento di esclusione. |
| SMSNoMessageFoundForTreatment | 050155 | SMS | Un evento di esclusione viene generato quando l’esperimento è abilitato per il messaggio e non viene trovato alcun messaggio per il trattamento qualificato. |
| WebNoVariantDefined | 050041 | Web | Un evento di esclusione viene generato quando non è definita alcuna variante per un messaggio web. |
| WebNoMessageFoundForTreatment | 050042 | Web | Un evento di esclusione viene generato quando l’esperimento è abilitato per il messaggio e non viene trovato alcun messaggio per il trattamento qualificato. |
