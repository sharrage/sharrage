# L9 · I numeri dei costi · caso Vèrso (SIM)
*Versione 10/11/2026 · dati simulati del caso, dalla lezione L9 "Costi e sostenibilità". Prezzi dei modelli: listino OpenRouter al 30/10/2026, da riverificare. Cambio usato negli esempi: 1 € = 1,16 $. L'esempio del docente serve da riferimento: ogni gruppo usa le proprie stime e lo dichiara.*

## 1. La fattura del picco (dal memo del CFO ad interim)
| Voce | Valore |
|---|---|
| Richieste nella settimana di picco | 600 (prima del richiamo circa 350) |
| Spesa per le chiamate al modello | 311 € a settimana, circa 1.350 € al mese |
| Budget approvato per le API del pilota | 400 € al mese |
| Tetti di spesa sulle chiavi | nessuno |

## 2. Il costo umano, tutto a mano
- 9 minuti a richiesta × 28 € l'ora = **4,20 € a richiesta** (dati del Project Work).
- A 600 richieste a settimana per 52 settimane (31.200 richieste, ipotesi di picco da dichiarare): **131.040 € l'anno**.

## 3. I tre costi di una richiesta (esempio del docente)
| Per richiesta | Pilota, prima | Pilota, dopo le contromisure | Misurato o stimato |
|---|---|---|---|
| Costo tecnico (token) | 0,52 € | 0,02 € | stimato sulle ipotesi del punto 4 |
| Costo umano di gestione | 1,87 € (4 min) | 1,40 € (3 min) | stimato: forchetta 3-5 min prima, 2,5-3,5 dopo |
| Costo di controllo | 1,40 € (3 min) | 0,30 € | stimato: forchetta 2-4 min prima, 0,20-0,45 € dopo |
| **Totale** | **3,79 €** | **1,72 €** | |
| Annuo a regime (31.200 richieste) | circa 118.000 € | circa 53.700 € | stima |
| Tutto a mano | 4,20 € | | 9 minuti a 28 € l'ora |

**La lettura:** anche se il modello fosse gratis, il pilota "prima" risparmierebbe solo il 14% rispetto al lavoro a mano. L'obiettivo -30% dell'AD arriva dal processo, non dal listino.

## 4. Dentro il costo tecnico "prima" (0,52 € a richiesta)
Ipotesi: Claude Opus 5.5 (4 $ entrata, 20 $ uscita per milione di token); 3 giri per richiesta; ogni giro rilegge istruzioni (5.000 token), manuale (9.000) e policy (7.000), più la domanda (300); risposta visibile 300 token e ragionamento 1.500 per giro; il 15% delle richieste riparte quattro volte, senza tetto.

| Voce | € per richiesta |
|---|---|
| Tentativi in più (nessun tetto) | 0,188 |
| Manuale e policy riletti a ogni giro | 0,166 |
| Ragionamento nascosto | 0,078 |
| Istruzioni rilette a ogni giro | 0,052 |
| Export ERP notturno | 0,017 |
| Risposta visibile | 0,016 |
| Domanda del cliente | 0,003 |

## 5. Contromisure e ordini di grandezza
- **Filtro prima dell'AI:** cortesie, formato del seriale, ricerca nel registro si fanno con regole o script, senza modello.
- **La taglia giusta:** modello piccolo per smistare, medio per le risposte, grande solo per i casi difficili.
- **Caching del prefisso:** su un prefisso di 12.750 token con Sonnet 5.5, a settimana 39,57 € senza cache, 7,80 € con cache di 5 minuti (-80%), 2,41 € con cache di 1 ora (-94%).
- **Tetti:** un tetto per chiave e per gruppo (nel corso 5 $ per gruppo); un tetto ai tentativi (al secondo errore di formato, passa a una persona).
- **Documenti leggeri:** il riassunto e le versioni in Markdown al posto dei PDF e dei fogli interi.
- **Il ragionamento si paga:** 1.000 domande "rispondi solo con la parola pronto" costano 0,73 $ con ragionamento lungo e 0,014 $ con ragionamento breve.

## 6. Le regole per la tabella
- Il costo per richiesta si divide per le richieste, non per le righe di un estratto.
- I prezzi hanno una data.
- Ogni cella dice se il numero è misurato o stimato, e da dove viene.
