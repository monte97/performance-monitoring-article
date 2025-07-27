---
title: "Introduzione all'analisi delle performance: dalla teoria alla pratica"
date: 2025-07-26T10:00:00+02:00
description: "Fondamenta teoriche e pratiche del performance testing: dalle metriche RED ai percentili, una guida completa per iniziare"
menu:
    sidebar:
        name: "Performance Testing Intro"
        identifier: "performance-testing-intro"
        weight: 10
tags: ["Performance Testing", "Monitoring", "SRE", "Metrics", "Observability"]
categories: ["Performance Engineering", "Software Testing"]
---

## Introduzione

__definizione__

- determinare responsivness, througput, reliability, scalability di un _sistema_ sotto un determinato workload
    - sistema == diversi componenti che devono interagire, non possiamo prendere solamente una parte isolata. a volte potrebbe semplicemente "risolvere" un problema spostando il blocco in un altro sistema

__perchè misuriamo?__

- le applicazioni non performanti generalmete non sono in grado di svolgere la funzione per cui erano state progettate/pensate

- passo aggiuntivo agli operational acceptance test. questi si fermano a dire se l'applicazine funziona oppure no

- cosa sono le performance? quando una applicazione è performante? Quando consente ad un utente di eseuguire un dato task senza _percepire_ delay o irritazione

- eserre certi di essere pronti alla release

- verificare adeguatezza dell'infrastruttura
    - abbiamo abbastanza risorse? il sistema rimane stabile?
    - valutare diverse modalità di deploy. siamo certi che quella configuraizone più costosa ne valga davvero la pena?

- circoscrivere le ottimizzazioni
    - non ha senso ottimizzare elementi che non incidono realmente sulle metriche di interesse

__Cosa possiamo misurare?__
- avaiability
- response time
- througput
- utilization
- scalability

__Perché i problemi di performance esistono?__

- più tardi il problema di performance emerge, maggiore è il costo per risolverlo -> come molti altri problemi! anche in questo caso è necessario uno shift-left nella risoluzione del problema, così come accade per la security o altro

- ma perché non si eseguono questi test __prima__?
    - problemi culturali
    - scarsa utilità percepita
    - brutta developer experience? strumenti complessi, difficili da configurare?

__quali attività comprende?__

1. identficare l'ambiente di test: con cosa dobbiamo lavorare?
2. determinare gli acceptance criteria: come faccamo a sapere che abbiamo fatto bene?
3. pianificare i test: quali sono gli scenari? assomigliano all'uso reale del prodotto? non ha senso eseguire test simulando milioni di utenti se abbiamo centinaia i utenti
4. setup ambiente
5.  implementazione dei test
6. esecuzione
7. analisi dei test


__Contesto di progetto__

di che cosa dobbiamo tenere conto quando definiamo dei test sulle performance? più che in altre tipologie di test il risultato non è bianco/nero ma deve essere inerpretato e il perimetro delineato. senza defnire il contesto del progetto è estremamene facile focalizzarsi su aree errate di analisi

- project vsion: la vision del progetto definisce il suo scopo ultimo, il suo stato desiderato futuro e consente di allineare le decisioni strategiche degli stakeholder

- scopo del sistema: se non sappiamo l'intento del sistema certamen non possiamo neanche ipotizzare le aree su cui mettere il focus

- aspettative degli utenti: mettersi nei panni degli utenti. la loro felicità non rispecchia per forza di cose dei requisiti scritti su un foglio da un manager

- obiettivi di business: come per ogni altro progetto, tenere rispettare tempi e budget

- motivo per cui vengono eseguiti i test: possono variare durante le fasi di sviluppo, importante sapre rimetterli in discussione

- valore che i test portano al progetto: sapere mappare i requisiti di business in appropriati test e determianre il valore che portano

- gestione di progetto: 

- processi:

- criteri di compliance

- schedule del progetto

__tipologia di test__

- performance: determinare valocità, scalabilità, stabilità di un sistema. importante capire tempi di risposta, througput, e utilizzo di risorse

- load: simulare un elevato carico sul sistema per vedere come si comporta rimanendo comunque nei limiti progettuali (sitme iniziali sull'utilizzo)

- stress testing: andre anche oltre alle condizioni progettuali. determinare cosa succede con poca memoria, paizo insufficiente, failure di server. L'importante è capire come e perché il sistema schiatta

__definizione di baseline__

definire una baseline significa determinare le condizioni "as-is" del sistema in modo da  o identificre regressioni futurepotere avere un confronto per i nostir miglioramenti

------
## I Pilastri della misurazione: Metodologia e Segnali Chiave

### Metodo RED

### Google Four Signals

## Tassonomia dei test



--- 

## Dall'intuizione alla scienza

### Il pericolo della media e l'importanza dei percentili

### Correlazione vs. Causa

---

## Developer Experience: La democratizzazione delle performane

---

## Observability-Driven Developement

### I tre pilastri

### debug multi layer


