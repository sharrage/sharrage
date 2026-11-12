# Il caso Vèrso · riassunto strutturato
*Versione 10/11/2026 · TAG APPT Fall 2026 · tutto è fittizio: azienda, persone, numeri e documenti esistono solo dentro il corso.*
*Fonti: "Project Work L1-L14" (materiale per i partecipanti) e i tre articoli del 5/11/2026 sull'acquisizione. Quando una versione più recente di questo file è nella cartella, vale quella.*

## 1. L'azienda in cinque righe
- **Chi è:** brand italiano di e-bike di design, nato a Bergamo nel 2019. Scale-up da 140 persone, circa 38 milioni di euro di fatturato.
- **Come vende:** online, diretto al cliente finale, senza negozi propri.
- **Assistenza dopo l'acquisto:** una rete di 250 officine partner in Italia, Germania e Austria. Il cliente prenota, porta la bici, l'officina ripara e fattura a Vèrso.
- **Servizi diretti a Milano e Torino:** e-bike in abbonamento mensile e bike sharing in concessione con i due Comuni (circa 1.200 bici prenotabili da app).
- **Posizionamento premium:** il cliente si aspetta che qualcuno risponda. L'assistenza clienti è piccola: due persone più un responsabile.

## 2. La crisi: il richiamo delle batterie
- Il fornitore segnala un difetto su un lotto di celle: con ricarica prolungata la batteria può surriscaldarsi.
- Vèrso richiama il **lotto B-2404**: circa **4.200 batterie** su bici vendute tra marzo e dicembre 2025. Annuncio: 12 gennaio.
- Nelle due settimane successive:
  - contatti da circa 350 a circa 600 a settimana (+70%); arretrato di circa 1.400 richieste; tempo medio di risposta da 1 a 5 giorni;
  - officine sommerse: molte prenotano per telefono e non aggiornano il gestionale, Vèrso non sa dove sia la capacità libera;
  - un video di una batteria fumante fa 300.000 visualizzazioni in due giorni; nei commenti si mescolano clienti coinvolti e clienti spaventati da guasti qualsiasi;
  - richieste in italiano e in tedesco, spesso senza seriale o con il seriale trascritto male.
- **Il mandato iniziale:** 90 giorni e un budget pilota per una soluzione AI che funzioni davvero, da presentare al CdA.

## 3. I numeri chiave (dal Project Work)
| Voce | Valore |
|---|---|
| Dipendenti | 140 |
| Fatturato annuo | circa 38 milioni di euro |
| Officine partner | 250 (Italia, Germania, Austria) |
| Bici in bike sharing | circa 1.200, di cui circa 300 con batterie del lotto |
| Batterie richiamate (lotto B-2404) | circa 4.200 |
| Richieste prima / dopo il richiamo | circa 350 / circa 600 a settimana (+70%) |
| Arretrato accumulato | circa 1.400 richieste |
| Tempo medio di risposta prima / dopo | 1 giorno / 5 giorni |
| Persone in assistenza | 2, più un responsabile |
| Costo pieno di un'ora di assistenza | 28 euro |
| Tempo medio di lavorazione di una richiesta | 9 minuti |
| Richieste che riguardano davvero il richiamo | circa 4 su 10 |

Quando serve un numero che qui non c'è, si stima e si dichiara l'ipotesi.

## 4. I sistemi e i dati
| Sistema | Che cosa contiene | Come ci si accede |
|---|---|---|
| Casella assistenza | richieste dei clienti, via mail e form del sito | lettura diretta |
| ERP | ordini, numeri seriali, lotti delle batterie | export notturno in CSV, non in tempo reale |
| Gestionale officine | anagrafica delle 250 officine, CAP serviti, disponibilità dichiarata | API di prenotazione, a volte lenta |
| Documentazione | manuale e-bike, policy di richiamo | PDF |

Due attenzioni: una verifica fatta alle 18 vede i dati di stamattina; la disponibilità delle officine è quella dichiarata, non quella reale.

## 5. Che cosa hanno costruito i gruppi in n8n (fase 1, L1-L7)
L'incarico, uguale per tutti: un agente per le richieste legate al richiamo, costruito una funzione per volta.
1. Leggere e classificare ogni richiesta (interessato dal richiamo, guasto diverso, informazioni, cliente arrabbiato).
2. Verificare se seriale e lotto rientrano nel richiamo.
3. Rispondere usando manuale e policy, non quello che il modello crede di sapere.
4. Agire: prenotare la sostituzione nell'officina più vicina.
5. Passare a una persona i casi che non può decidere: rimborsi, reclami gravi, impegni fuori policy.

Nella cartella dei flussi trovate gli esempi del docente e, se li aggiungete, i vostri. Ogni gruppo è arrivato a un punto diverso: è normale.

## 6. Lo scenario dal 5/11/2026: arriva Dracula Ventures
- Il fondo di private equity **Dracula Ventures** (Lussemburgo) acquisisce Vèrso con un'operazione ostile e azzera il vertice: l'AD Elena Rizzi lascia.
- **CFO, IT e DPO restano ad interim** e rispondono al nuovo AD.
- **Il nuovo AD** (interpretato dal docente):
  - conosce poco il business e niente di tecnologia; ha poco tempo; vuole risposte in una frase, in euro;
  - va dritto al punto anche con numeri sbagliati: "qualche centinaio di bici" (sono circa 4.200 batterie), "lo sharing è metà del business";
  - il suo Slack lo gestisce la segretaria; usa Claude per tutto e tiene copie dei file su Google Drive.
- **Il suo piano:** costi operativi -30% in sei mesi; bike sharing in almeno dieci città; assistenza clienti "quasi interamente automatizzata entro marzo".
- **Chi è preoccupato:** l'assistenza (l'ha saputo dai giornali), le officine ("noi abbiamo clienti, non slot"), i Comuni dello sharing (obblighi su sicurezza e dati).

## 7. Le persone
| Ruolo | Che cosa vuole | Che cosa teme |
|---|---|---|
| Nuovo AD (Dracula Ventures) | tagliare costi, sharing in dieci città, AI entro marzo | progetti che non dicono quanto costano e quanto rendono |
| CFO (ad interim) | sapere quanto costa ogni richiesta gestita | una spesa che cresce senza un tetto |
| IT manager (ad interim) | nessun impatto sui sistemi in produzione | dare accessi che non sa come revocare |
| DPO (ad interim) | sapere dove finiscono i dati e chi risponde | un reclamo al Garante, un cliente che non sa di parlare con un'AI |
| Capo officina storico | officine senza prenotazioni sbagliate | che un software decida al posto di chi conosce le bici |

## 8. I quattro vincoli comuni (L8)
1. L'export dall'ERP arriva solo di notte.
2. Il budget è dimezzato.
3. Nessun dato personale può essere conservato.
4. Le officine rifiutano le prenotazioni automatiche.

Per chi finisce prima c'è un'estensione facoltativa: una carta tra "Solo dati in UE" e "Due soli operatori", oppure un quinto vincolo proposto dal gruppo. Ogni gruppo cerca anche il proprio **vincolo nascosto**: quello che nessuno nomina. Il dettaglio è in `L8_vincoli_comuni_e_carte.md`. Un vincolo non si aggira: si rispetta o si negozia, con argomenti in euro, rischi e tempi.

## 9. Dove si va: la presentazione al board
Sette slide, una per sessione: 1 problema e soluzione (fase 1) · 2 vincoli (L8) · 3 costi e controllo (L9) · 4 governo della soluzione (L10) · 5 conformità e rischi (L11) · 6 roadmap (L12) · 7 la richiesta al board (L13). Non si scrive alla fine: si monta.

## 10. Che cosa non sappiamo ancora
- Quanto costa davvero una richiesta gestita dal flusso, voce per voce.
- Quante bici dello sharing hanno batterie del lotto, città per città.
- Se il dato "lo sharing è metà del business" ha una fonte. Fino a prova contraria è un'opinione dell'AD.
