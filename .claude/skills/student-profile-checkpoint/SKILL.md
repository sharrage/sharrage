---
name: student-profile-checkpoint
description: Esegue un checkpoint evidence-based del percorso ITAPPT e aggiorna i file locali dello student profile (current-profile.md, progress-log.md, e final-learning-report.md per il checkpoint final). Da invocare manualmente dallo studente.
argument-hint: <checkpoint-id>
---

# Student Profile Checkpoint

Questa skill è pensata per l'invocazione MANUALE da parte dello studente, con:

`/student-profile-checkpoint <checkpoint-id>`

Non eseguirla di tua iniziativa e non proporre di eseguirla automaticamente. Usa l'argomento ricevuto (`$ARGUMENTS`) come `checkpoint_id`.

ID validi, e soli ammessi: `checkpoint-1`, `checkpoint-2`, `checkpoint-3`, `checkpoint-4`, `final`.

## 1. Validazione

Verifica che esistano tutti questi file:
- student-profile/baseline.md
- student-profile/current-profile.md
- student-profile/progress-log.md
- student-profile/checkpoint-plan.md

Verifica inoltre che `checkpoint_id` sia uno degli ID validi. Se manca un file o l'ID è assente o non valido, NON modificare nulla e spiega brevemente il problema.

## 2. Leggi lo stato attuale

Leggi baseline.md, current-profile.md, progress-log.md e la sezione di checkpoint-plan.md relativa a `checkpoint_id`.

- baseline.md è READ-ONLY: non modificarlo mai.
- progress-log.md è APPEND-ONLY: nessuna entry precedente può essere riscritta o cancellata.

Prima di procedere controlla in progress-log.md che `checkpoint_id` non sia già stato completato. Se esiste già una entry per quell'ID, NON creare una seconda entry: avvisa lo studente e chiedi se vuole rieseguire intenzionalmente il checkpoint. Procedi solo con conferma esplicita.

## 3. Cerca nuove evidenze

Analizza il progetto locale e cerca evidenze nuove, soprattutto rispetto al focus del checkpoint. Considera, quando presenti: workflow e automazioni; file e artefatti prodotti; prompt e istruzioni strutturate; integrazioni, API, webhook e JSON; data handling, fogli di calcolo e trasformazione dati; database, SQL e sistemi dati; RAG; debugging; error handling; eval e testing; guardrail e human-in-the-loop; documentazione; analisi di processo; scelte progettuali o architetturali; business case e materiali strategici; lavoro di gruppo e autonomia osservabile.

- Non valutare una competenza solo perché l'argomento è stato affrontato a lezione: valuta ciò che lo studente dimostra di saper fare.
- Non duplicare come nuova evidenza ciò che è già registrato nei checkpoint precedenti.
- Non inventare attività o competenze non supportate da file o risposte dello studente.

## 4. Domande mirate

Se le evidenze nel progetto non bastano per valutare un aspetto importante del checkpoint, fai al massimo 2 domande, UNA ALLA VOLTA, brevi e concrete. Non chiedere ciò che puoi ricavare dai file.

## 5. Valutazione

Usa ESATTAMENTE uno di questi livelli: Base, Intermedio, Avanzato, Non ancora osservato.
Usa ESATTAMENTE una di queste forze delle evidenze: Bassa, Media, Alta.

- Un livello può aumentare, restare invariato o essere rivalutato. Non aumentarlo automaticamente a ogni checkpoint: ogni variazione richiede nuove evidenze.
- Nessun qualificatore nella cella del livello: note e distinguo vanno nelle evidenze.
- Usa SEMPRE gli stessi nomi e lo stesso ordine delle aree di baseline.md in current-profile.md, progress-log.md e final-learning-report.md. Non abbreviare, aggregare o rinominare (es. "Data Handling / Spreadsheets", non "Data Handling").

## 6. Aggiorna current-profile.md

Aggiorna solo student-profile/current-profile.md: Current summary, Current competency map, Current strengths, Current growth areas, Current project roles, Current learning goals, Last updated, Last checkpoint.

Il file è la fotografia ATTUALE, non la cronologia. Se una nuova evidenza rende obsoleta o contraddittoria una frase del Current summary, riscrivila (niente "non ha mai usato X" dopo che X è stato usato). Per preservare il confronto temporale puoi scrivere "prima del master non aveva mai usato X; oggi…". Mantieni la regola di manutenzione in fondo al file.

## 7. Aggiorna progress-log.md

Aggiungi IN FONDO una nuova entry, senza modificare le precedenti, con questa struttura:

```
## [checkpoint-id] — [data]

### Focus
### Attività ed evidenze rilevanti
### Evoluzione delle competenze
(per ogni area rilevante: livello precedente → livello attuale, oppure livello invariato — nuove evidenze; indica la forza delle evidenze quando utile)
### Nuove capacità emerse
(max 5)
### Aree ancora da sviluppare
(max 5)
### Focus fino al prossimo checkpoint
(max 3)
```

## 8. Caso speciale: final

Se `checkpoint_id` = `final`: esegui prima il normale aggiornamento di current-profile.md e progress-log.md; poi confronta baseline.md, current-profile.md e tutte le evidenze del progress-log.md, e crea student-profile/final-learning-report.md con queste sezioni:

```
# Final Learning Report
## Executive summary            (max 8 righe)
## Baseline → Final             (tabella: Area | Livello iniziale | Livello finale | Forza evidenze finali | Evidenze principali dell'evoluzione — tutte le aree della baseline, stessi nomi e stesso ordine)
## Evoluzioni più significative (max 5)
## Cosa so fare oggi che non sapevo fare all'inizio   (elenco concreto, basato su evidenze)
## Evidenze principali          (progetti, workflow, artefatti, attività)
## Competenze consolidate
## Aree ancora da sviluppare
## Next steps                   (max 5 raccomandazioni concrete)
## Learning journey             (max 6 righe: partenza → passaggi di crescita → stato finale)
```

Il report deve essere comprensibile anche a un docente che non ha seguito le attività quotidiane. Includi, se supportate dalle evidenze di L19, la capacità di spiegare, difendere e trasferire il lavoro (pitch, peer teaching).

## 9. Output a schermo

Per i checkpoint normali mostra soltanto:

```
### Checkpoint completato
**Principali evoluzioni**            (max 3)
**Competenze aggiornate**            (solo quelle effettivamente cambiate)
**Focus fino al prossimo checkpoint** (max 3)
```

Per `final` mostra anche il percorso di final-learning-report.md.

## 10. Privacy

Tutti i file dello student profile restano locali al progetto. Non inviare, sincronizzare o pubblicare questi dati su servizi esterni. Non modificare file fuori da student-profile/ (salvo il file di questa skill).
