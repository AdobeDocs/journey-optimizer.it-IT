---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Funzioni supportate nell’editor di espressioni
description: Scopri quali funzioni dell’editor di personalizzazione sono supportate nella gestione delle decisioni (Offer Decisioning).
badge: label="Legacy" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
exl-id: c4df41a2-d740-437c-acc3-957508c4a1c0
source-git-commit: b90e3af955496d4fcae54b109cb1e86a8a21be43
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 16%

---

# Funzioni supportate nell’editor di espressioni {#personalization-editor-supported-functions}

Nella gestione delle decisioni, puoi creare espressioni utilizzando l’editor di personalizzazione. Utilizza questo editor in particolare quando:

* **Definizione del contenuto dell&#39;offerta** - quando [aggiungi rappresentazioni](offer-library/add-representations.md) e personalizzi il contenuto dell&#39;offerta (immagini, testo, collegamenti)
* **Creazione di regole di decisione** - quando [definisci l&#39;idoneità](offer-library/creating-decision-rules.md) per le offerte
* **Creazione di formule di classificazione** - quando [crei formule di classificazione](ranking/create-ranking-formulas.md) per ordinare le offerte

Il backend di Offer Decisioning supporta solo un **sottoinsieme** delle funzioni disponibili nell&#39;editor di personalizzazione. In questa pagina sono elencate tutte le funzioni che è possibile utilizzare in modo sicuro. Espandi ogni sezione per visualizzare gli operatori, gli helper e le funzioni supportati.

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
>Se utilizzi una funzione non inclusa nell’elenco precedente, l’espressione potrebbe non riuscire in fase di esecuzione o produrre risultati imprevisti. Per l&#39;insieme completo delle funzioni disponibili nella personalizzazione [!DNL Journey Optimizer], vedere [Elenco delle funzioni di supporto](../personalization/functions/functions.md). In Offer Decisioning è supportato solo il sottoinsieme documentato in questa pagina.
