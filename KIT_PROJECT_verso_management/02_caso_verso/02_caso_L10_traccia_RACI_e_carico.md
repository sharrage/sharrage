# L10 · Traccia per la RACI e per il carico di controllo (SIM)

*Caso Vèrso, dati fittizi. Serve a preparare le due slide L10 del deck del gruppo. I passaggi sono gli stessi della slide "L10 · La matrice RACI".*

**Legenda.** R fa · A risponde (una sola per riga, sempre una persona) · C va sentito prima · I va informato dopo.

## 1. La matrice RACI · traccia compilata in fretta da correggere
*Qualcuno l'ha compilata di corsa: ci sono almeno tre errori. Correggetela riga per riga, poi completatela per il vostro flusso.*

| Passaggio | Agente | Operatori | Resp. assistenza | Officina | IT | DPO | CFO |
|---|---|---|---|---|---|---|---|
| Classificare | A | I | | | C | | |
| Verificare seriale e lotto | R | | A | | C | | |
| Rispondere al cliente | R | | | | | | |
| Prenotare l'officina | R | I | | | | | |
| Rimborsi ed eccezioni | R | A | A | | | | C |
| Reclamo grave o post pubblico | R | | | | | C | |

## 2. Le cinque regole (checklist)
- [ ] Una sola A per riga, ed è una persona, con un vice.
- [ ] L'agente può essere R, mai A: si delega il compito, non la responsabilità.
- [ ] Chi modifica non decide, e chi decide non modifica: sui gesti irreversibili R e A sono persone diverse.
- [ ] Sono incarichi, non gradi: la A è chi ha il tempo e il nome.
- [ ] Poche C (ognuna rallenta), tutte le I (una I mancante è una sorpresa).

**Una riga che manca nella traccia:** chi cambia il flusso o le istruzioni dell'agente? È la riga che avrebbe fermato "approva e invia tutto".

## 3. I punti di controllo
Per ogni gesto irreversibile: chi firma (e il vice), che cosa vede (il delta: importo, slot, seriale, non tutto il testo), la soglia (sempre, a campione o mai, scritta sui fatti), che cosa succede se nessuno firma (la bozza resta bozza).

## 4. Il carico di controllo: i conti del picco
| Ipotesi | Valore | Fonte |
|---|---|---|
| Richieste a settimana nel picco | 600 (erano circa 350) | Project Work |
| Persone che controllano | 2, più un responsabile | Project Work |
| Ore di presenza a testa a settimana | circa 40 (feriali 9-18) | policy v2.1 e stima |
| Costo pieno di un'ora | 28 € | Project Work |

| Scenario | Ore di gestione a settimana | Ore di controllo a settimana |
|---|---|---|
| Tutto a mano (9 minuti a richiesta) | 90 | 0 |
| Pilota, tutto approvato (3 minuti di controllo a bozza) | 40 | 30 |
| Pilota, con soglie (1 minuto sul 40% richiamo, mezzo minuto sul 50% informative) | 30 | 6,5 |

*Le ore di presenza delle due persone sono circa 80 a settimana. Approvare tutto vuol dire circa 60 approvazioni a testa al giorno.*

## 5. La regola che protegge chi controlla
- **Tetto:** ___ approvazioni a testa al giorno; oltre, piano B: ___
- **Pause:** approvazioni a blocchi di ___; mai in blocco a fine turno.
- **Rotazione:** chi approva oggi, domani gestisce le eccezioni.
- **Vice:** ___ sostituisce ___.
