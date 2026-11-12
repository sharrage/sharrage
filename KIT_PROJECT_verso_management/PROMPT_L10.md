# PROMPT · L10 · Controllo umano e RACI

*Questo file è nella cartella 01_Files_per_tutti dello zip: si apre e si copia, non si carica nello spazio. I prompt valgono su tutti e tre i percorsi. **Claude Code:** nell'app, sessione aperta sulla cartella dello spazio, modalità Plan. **Project (anche LIGHT):** una chat nuova nel Project, dopo aver caricato i file di L10 nella conoscenza. Nel Project Claude non salva: prepara il documento e lo salvate voi.*

---

## 0 · Che cosa c'è di nuovo (all'inizio)
```
Ho aggiunto i file di L10 allo spazio. Elencali e dimmi in tre righe che cosa cambiano per il nostro lavoro con il management. Non modificare e non creare nulla.
```

## 1 · Le schede L8 e L9 (Laboratorio 1)
Partite dalla scheda che vi manca. La versione lunga, con gli esempi di domande, è in `PROMPT_slide_L8_L9.md`.

**1a · La scheda L8**
```
Dobbiamo compilare la scheda L8 del nostro deck: "I vincoli e come li superiamo" e "Tre decisioni, e la frase per il board". Usa le informazioni che hai e le richieste del management. Prima fammi al massimo 3 domande di chiarimento, una alla volta, solo su ciò che non trovi nei documenti. Poi prepara le tabelle con le stesse colonne della scheda L8 in 05_schede_da_compilare. Al massimo 12 parole per cella.
```

**1b · La scheda L9**
```
Dobbiamo compilare la scheda L9 del nostro deck: "Quanto costa una richiesta, prima e dopo" e "Dove si spreca e che cosa cambiamo". Usa le informazioni che hai e le richieste del management. Prima fammi al massimo 3 domande di chiarimento, una alla volta, solo su ciò che non trovi nei documenti. Poi prepara le tabelle con le stesse colonne della scheda L9 in 05_schede_da_compilare. Al massimo 12 parole per cella.
```

## 2 · La scheda L10: matrice RACI e punti di controllo (Laboratorio 2)
```
Dobbiamo compilare la scheda L10 del nostro deck: la matrice RACI con i punti di controllo umano. Usa il riassunto del caso, la policy del richiamo v2.1, l'incidente del rimborso promesso, la traccia RACI e carico, il nostro flusso n8n e le schede L8 e L9 se le abbiamo.
Prima fammi al massimo 5 domande di chiarimento, una alla volta, solo su ciò che non trovi nei documenti.
Poi prepara due tabelle con le stesse colonne della scheda in 05_schede_da_compilare:
1) la matrice RACI sui sei passaggi (Agente, Operatori, Resp., Officina, IT, DPO, CFO), con una sola A per riga, sempre una persona, mai l'agente;
2) i punti di controllo per i gesti irreversibili: chi firma e vice, che cosa vede, soglia (sempre, a campione o mai, scritta sui fatti), se nessuno firma; più il carico a testa e la regola di tutela.
Al massimo 12 parole per cella. Sotto le tabelle, controlla le cinque regole della RACI e dimmi quali righe non le rispettano.
```

## 3 · La risposta all'AD (Laboratorio 2)
```
Leggi il messaggio dell'AD dopo il post, in dal_management. Prepara la risposta del gruppo, in una pagina, senza gergo tecnico:
1) dove si è rotta la catena, in sei passaggi, cercando il caso e non la colpa;
2) tre modifiche che chiudono la porta al ritorno (sullo strumento, sul processo, sulle persone);
3) chi firma che cosa: le righe della nostra RACI con i gesti irreversibili;
4) che cosa costa il controllo in ore, nel picco, con e senza soglie.
Verifica con i documenti le due affermazioni dell'AD: assistenza solo AI a marzo, e controlli che rallentano e basta. Ogni numero ha la fonte.
Code: salva in 03_intercambio_management/al_management/ con data e ora nel nome, dopo il mio sì.
Project: prepara il testo; lo salviamo noi nella cartella del gruppo su Drive.
```

## 4 · I dieci gesti (se il gruppo vuole rifarli con calma)
```
Leggi i dieci gesti del flusso di Vèrso. Per ognuno dimmi: dentro, sopra o fuori dal ciclo; il livello (informa, propone, prepara, agisce); il fatto che decide; se è irreversibile. Poi confronta con il nostro flusso: quale gesto del nostro n8n somiglia di più al numero 10?
```

## 5 · Il prezzo della delega (esercizio, in coppia o in stanza)
```
Leggi L10_esercizio_prezzo_della_delega. Aiutaci a compilare la tabella per tre gesti che scegliamo noi. Prima chiedici quali gesti, uno alla volta. Per ogni gesto proponi la chiave (piccola, media, grande) con il motivo, stima che cosa guadagniamo in minuti a settimana con i numeri del caso, e chiedici che cosa non vogliamo smettere di saper fare: quella colonna la decidiamo noi, non tu. Alla fine proponi una frase per l'AD su quanta libertà cediamo e in cambio di che cosa.
```

## 6 · Dalla RACI alla policy (esercizio, in stanza, dopo la scheda L10)
```
Leggi L10_esercizio_dalla_RACI_alla_policy e L10_policy_42001_traccia_breve. Prendi i gesti irreversibili della nostra scheda L10 e per ognuno proponi una regola di policy verificabile, il capitolo, la clausola della ISO/IEC 42001 usata come scheletro, la A dalla nostra RACI e l'etichetta (DA VALIDARE, PROPOSTA, DAL GIORNO 0). Non scrivere mai che Vèrso è certificata. Se una regola non è verificabile, dimmelo e proponine una versione che lo sia.
```

---

## Per chi finisce prima
**A · I quattro messaggi difficili**
```
Leggi i quattro messaggi difficili. Per ognuno: chi risponde, entro quando, a quale livello, la frase da non scrivere mai, la prima frase corretta, la riga della nostra RACI e la sua A. Il messaggio RQ2-110 cita l'AD: spiega perché un nome importante non è un'autorizzazione (policy v2.1, P06).
```

**B · La mappa di residenza della vostra catena**
```
Usa L10_estensione_mappa_residenza_TRACCIA. Per ognuno dei sette anelli del nostro flusso n8n (interfaccia e memoria, modello, strumenti, server MCP, fonti collegate, servizi esterni, log) dimmi dove restano i dati a riposo, dove avviene il calcolo e chi ne risponde. Segna in grigio gli anelli di cui non sappiamo la risposta, con chi verifica. Non inventare: se un dato non è nei documenti, scrivi "da verificare".
```

**C · La traccia compilata in fretta**
```
Leggi L10_traccia_RACI_e_carico. Nella matrice compilata in fretta ci sono almeno tre errori: trovali, dimmi quale delle cinque regole viola ciascuno e proponi la correzione. Poi dimmi quale riga manca, e perché è quella dell'incidente.
```
