---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Funzioni supportate nell’editor di personalizzazione
description: Scopri quali funzioni dell’editor di personalizzazione sono supportate durante la personalizzazione del contenuto delle offerte in Gestione delle decisioni (Offer Decisioning).
badge: label="Legacy" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
exl-id: c4df41a2-d740-437c-acc3-957508c4a1c0
source-git-commit: c15bae97ea52243d65aa59fdd4e924dc4e1852d8
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 15%

---

# Funzioni supportate nell’editor di personalizzazione {#personalization-editor-supported-functions}

Nella gestione delle decisioni, puoi utilizzare l&#39;**editor di personalizzazione** quando [aggiungi rappresentazioni](add-representations.md) e personalizzi il contenuto delle **offerte** (immagini, testo, collegamenti nelle offerte).

Il backend di Offer Decisioning supporta solo un **sottoinsieme** delle funzioni disponibili nell&#39;editor di personalizzazione durante la personalizzazione del contenuto. Questa pagina elenca tutte le funzioni che puoi utilizzare nell’editor per il contenuto delle offerte. Espandi ogni sezione per visualizzare gli operatori, gli helper e le funzioni supportati.

>[!NOTE]
>
>Questo elenco di funzioni si applica **solo alla personalizzazione del contenuto delle offerte** (rappresentazioni). Le regole di decisione e le formule di classificazione utilizzano editor diversi e non sono limitate a questo sottoinsieme.

## Elenco delle funzioni supportate {#supported-functions-list}

+++ Operatori

* Aritmetica: `+` `-` `*` `/` `%`
* Logico: `and` `or` `!`
* Confronto: `=` `!=` `>` `>=` `<` `<=`

+++

+++ Helper

* Ogni
* Con
* Se
* A meno che
* Let
* Valore di fallback predefinito
* frammento
* datasetLookup
* externalDataLookup (Alpha)
* In linea
* Url
* Metadati di esecuzione
* valueAtPath

+++

+++ Funzioni stringa

| Nome visualizzato | Nome interno |
|--------------|---------------|
| Minuscolo | lowerCase |
| Maiuscolo | upperCase |
| Borsa Camel | CamelCase |
| Tutte iniziali maiuscole | titleCase |
| Taglia | trim |
| Taglia a sinistra | leftTrim |
| Taglia a destra | rightTrim |
| È vuoto | IsEmpty |
| Ignora maiuscole/minuscole uguale a | equalsIgnoreCase |
| Non uguale con ignora maiuscole/minuscole | notEqualWithIgnoreCase |
| Sostituisci | replace |
| Sostituisci tutto | replaceAll |
| Concat | concatena |
| Dividi | split |
| Encode64 | encode64 |
| Lunghezza | lunghezza |
| MD5 | md5 |
| SHA256 | sha256 |
| Simile a | simile a |
| Inizia con | startsWith |
| Non inizia con | doesNotStartWith |
| Termina con | endsWith |
| Non termina con | doesNotEndWith |
| Contiene | contiene |
| Non contiene | doesNotContain |
| È uguale a | uguale a |
| Non uguale a | notEqualTo |
| Corrisponde a | matches |
| Gruppo di espressioni regolari | regexGroup |
| Stringa a numero | stringToNumber |
| Stringa a data | stringToDate |
| A Data/Ora | toDateTime |
| Solo a data/ora | toDateTimeOnly |
| Estrai dominio e-mail | extractEmailDomain |
| Estrai nome utente e-mail | extractEmailUsername |
| Non è vuoto | isNotEmpty |
| Indice di | indexOf |
| Ultimo indice di | lastIndexOf |
| Sottostringa | substr |
| To Bool | toBool |
| Stringa a numero intero | string_to_intero |
| Maschera | maschera |
| Ottieni valuta formato | formatCurrency |
| Ottieni il valore Unicode del carattere | charCodeAt |
| Ottieni codice Qr per qualsiasi testo | qrCode |

+++

+++ Funzioni array, elenca e imposta

| Nome visualizzato | Nome interno |
|--------------|---------------|
| Distinct | distinct |
| In entrata | in |
| Non in | notIn |
| Intersects | interseca |
| Sottoinsieme di | subsetOf |
| Soprainsieme di | supersetOf |
| Include | include |
| Ordinare e ottenere il primo N nell’array | topN |
| Ordina e ottieni l’ultimo N nell’array | bottomN |
| Primo elemento | testa |
| Count | conteggio |
| Sum | sum |
| Medio | media |
| Minimo | min |
| Massimo | max |

+++

+++ Funzioni di mappatura

| Nome visualizzato | Nome interno |
|--------------|---------------|
| Ottenere | get |
| Chiavi | tasti |
| Valori | valori |

+++

+++ Funzioni oggetto

| Nome visualizzato | Nome interno |
|--------------|---------------|
| È nullo | isNull |
| Non è nullo | isNotNull |

+++

+++ Funzioni matematiche

| Nome visualizzato | Nome interno |
|--------------|---------------|
| A percentuale | toPercentage |
| Arrotonda per eccesso | roundUp |
| Arrotonda per difetto | roundDown |
| Alla precisione | toPrecision |
| Assoluto | assoluto |
| Casuale | random |
| A esadecimale | toHexString |
| Ottieni numero per lingua | formatNumber |
| A stringa | toString |
| A Intero | toInt |
| A lungo | toLong |

+++

+++ Funzioni data/ora

| Nome visualizzato | Nome interno |
|--------------|---------------|
| Ora | now |
| Ottieni CurrentZonedDateTime | getCurrentZonedDateTime |
| Data - A | toDate |
| All&#39;ora | toTime |
| A Data/Ora | toDateTime |
| Solo a data/ora | toDateTimeOnly |
| Solo data - A | toDateOnly |
| Solo all&#39;ora | toTimeOnly |
| Al fuso orario | toTimeZone |
| Formato data | formatDate |
| Formato data e ora | formatDateTime |
| Formato ora | formatTime |
| Analizza data | parseDate |
| Analizza data e ora | parseDateTime |
| Tempo di analisi | parseTime |
| Aggiungi giorni | addDays |
| Aggiungi mesi | addMonths |
| Aggiungi anni | addYears |
| Aggiungi ore | addHours |
| Aggiungi minuti | addMinutes |
| Aggiungi secondi | addSeconds |
| Sottrai giorni | subtractDays |
| Sottrai mesi | subtractMonths |
| Sottrai anni | subtractYears |
| Sottrai ore | subtractHours |
| Sottrai minuti | subtractMinutes |
| Sottrai secondi | subtractSeconds |
| Differenza in giorni | diffDays |
| Differenza in mesi | diffMonths |
| Differenza negli anni | diffYears |
| Differenza in ore | diffHours |
| Differenza in minuti | diffMinutes |
| Differenza in secondi | diffSeconds |
| Inizio del giorno | startOfDay |
| Fine del giorno | endOfDay |
| È prima di | isBefore |
| È dopo | isAfter |

+++

+++ Funzioni URL

| Nome visualizzato | Nome interno |
|--------------|---------------|
| Codifica URL | encodeUrl |
| Decodifica URL | decodeUrl |
| Ottieni parametro di query URL | getUrlQueryParam |
| Ottieni protocollo URL | getUrlProtocol |
| Ottieni host URL | getUrlHost |

+++

>[!NOTE]
>
>Se utilizzi una funzione non inclusa nell’elenco precedente durante la personalizzazione del contenuto dell’offerta, l’espressione potrebbe non riuscire in fase di esecuzione o produrre risultati imprevisti. Per l&#39;insieme completo delle funzioni disponibili nella personalizzazione [!DNL Journey Optimizer], vedere [Elenco delle funzioni di supporto](../../personalization/functions/functions.md). Per la personalizzazione dei contenuti in Offer Decisioning è supportato solo il sottoinsieme documentato in questa pagina.
