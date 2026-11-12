# Tre migliorie al flusso di assistenza
*Bozza approvata dal gruppo. Il flusso non è stato modificato. Stime dichiarate: i numeri di partenza vengono da 02_caso_L9_numeri_dei_costi_SIM.md (esempio del docente), non da misure sul flusso. Ordine: dalla più utile alla meno utile per il nuovo AD.*

## 1. Collegare i due assistenti e passare i casi gravi a una persona (vincolo C4)
- **Per il cliente:** risposta adatta al suo caso; chi è arrabbiato o ha un caso critico o un rimborso viene preso in carico da una persona, non riceve una risposta automatica.
- **Costo o risparmio:** sviluppo basso (stima: un paio di giorni, ipotesi da validare con l'IT). Il risparmio non è calcolabile oggi: non si misura quanti casi gravi sbagli.
- **Rischio ridotto:** promesse non autorizzate (rimborsi), reclami gravi senza risposta.
- **Tempo:** 1-2 settimane, compreso il test sui casi critici.

## 2. Filtri prima dell'AI e tetto di spesa (vincolo C3)
- **Per il cliente:** nulla di visibile; risposte più rapide sui casi semplici.
- **Costo o risparmio:** dall'esempio del docente (L9 §3-4, stime) il costo tecnico scende da 0,52 € a 0,02 € a richiesta e il totale da 3,79 € a 1,72 €. Su 31.200 richieste l'anno (ipotesi di picco) sono circa 64.000 € l'anno in meno. Oggi la spesa è 311 € a settimana (misurata, memo CFO) contro un budget di 400 € al mese, e non c'è alcun tetto sulle chiavi.
- **Rischio ridotto:** una spesa che cresce senza controllo.
- **Tempo:** tetto in pochi giorni; filtri e contromisure 3-4 settimane.

## 3. Misurare gli errori con un test fisso (vincoli C1 e C2)
- **Per il cliente:** risposte più affidabili col tempo.
- **Costo o risparmio:** costo basso (il kit ha già 20 domande di valutazione e 50 richieste di stress). Nessun risparmio diretto: serve a dire all'AD quanto sbaglia prima di parlare di automazione quasi totale entro marzo. Include i messaggi bloccati dal filtro e l'effetto dei dati notturni sul seriale.
- **Rischio ridotto:** decidere sulla base di una sensazione.
- **Tempo:** 1 settimana per il primo test, poi a ogni modifica.

## Fonti
02_caso_L8_vincoli_comuni_e_carte.md, 02_caso_L9_numeri_dei_costi_SIM.md, 01_n8n_esempio_flusso_finale_sfida1_L7_alleggerito.json.

## Da verificare
Tempi e costi di sviluppo (non presenti nel kit); se il flusso del nostro gruppo ha gli stessi difetti.
