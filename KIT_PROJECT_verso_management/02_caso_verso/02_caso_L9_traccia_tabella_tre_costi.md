# Tabella dei tre costi · TRACCIA

*La versione con le formule è `Tabella_tre_costi_TRACCIA.xlsx` (file Excel, si apre sul computer: è con le schede da compilare): compilate solo le celle gialle, il resto si calcola. Questa pagina serve a chi lavora su carta, in un Project o in chat. Un esempio compilato su un caso diverso è in `02_caso_L9_tabella_tre_costi_ESEMPIO_consegne.md`.*

**Processo:** [ ]
**I vincoli comuni che pesano sui costi:** [ ]
**Estensione (se l'avete presa):** [ ]
**Prezzi usati (fonte e data):** [es. listino OpenRouter al gg/mm/aaaa, da riverificare]
**Volumi a regime:** [ ] richieste a settimana × [52] settimane = [ ] richieste l'anno
**Costo pieno di un'ora di lavoro:** [28 €/h nel caso Vèrso]

## 1. Il costo tecnico, passo per passo
Una riga per ogni passo che chiama un modello. Un passo fatto da una regola o da uno script costa zero: scrivetelo comunque, è una contromisura.

| Passo | Quota di richieste che passano qui | Chiamate per richiesta (giri × tentativi) | Token entrata per chiamata | di cui dalla cache | Token uscita | Token ragionamento | $ entrata / M | $ cache / M | $ uscita / M | € per richiesta |
|---|---|---|---|---|---|---|---|---|---|---|
| | | | | | | | | | | |

Formula: € per richiesta = quota × chiamate × (entrata non in cache × prezzo entrata + entrata in cache × prezzo cache + (uscita + ragionamento) × prezzo uscita) / 1.000.000 / cambio. Più gli eventuali costi fissi a settimana divisi per le richieste.

## 2. La tabella
| Costo | Prima: per richiesta | Prima: annuo | Dopo: per richiesta | Dopo: annuo | Fonte (M = misurato, S = stimato) |
|---|---|---|---|---|---|
| **Tecnico** (token, ragionamento, caching) | | | | | |
| **Umano di gestione** (minuti × costo orario ÷ 60) | | | | | |
| **Controllo** (minuti di verifica × quota verificata × costo orario ÷ 60) | | | | | |
| **Totale** | | | | | |
| Riferimento: tutto a mano | | | | | |

## 3. Economia di pensiero
Quanto vale da sola l'ottimizzazione dei file e del contesto (meno token letti a ogni chiamata, a parità di modello):
token risparmiati per chiamata [ ] × chiamate per richiesta [ ] × prezzo di entrata [ ] $ / M = [ ] € per richiesta, [ ] € l'anno.
Effetti non in euro (meno errori, meno rilettura, risposte più precise): [ ]

## 4. Come lo teniamo sotto controllo
- **Contromisure** (almeno tre), compatibili con i vincoli comuni: [ ]
- **Tetto di spesa**: quanto, su quale chiave, chi lo controlla, ogni quanto: [ ]
- **Soglia decisa prima** per la prova di quattro settimane: [ ]
- **Rischio delle contromisure** (per esempio un modello più piccolo che sbaglia sposta il costo nel controllo): [ ]

Il board chiede: questi numeri sono **misurati o a occhio?**
