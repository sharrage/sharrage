# Tabella dei tre costi · ESEMPIO compilato (caso diverso, SIM)

*Esempio di fantasia, a scopo didattico: "RapidoCasa", un servizio di consegne a domicilio che risponde con l'AI ai messaggi dei clienti su ordini e consegne. Non è il caso Vèrso: serve a vedere come si compila la traccia. Prezzi: listino OpenRouter al 30/10/2026, da riverificare. Cambio 1 € = 1,16 $. Versione con formule: `Tabella_tre_costi_ESEMPIO_consegne.xlsx` (file Excel, si apre sul computer: è con le schede da compilare).*

**Processo:** risposte ai messaggi dei clienti su ordini e consegne. **Vincolo che pesa sui costi (esempio):** budget dimezzato.
**Volumi:** 2.000 messaggi a settimana × 52 = 104.000 l'anno. **Costo orario:** 24 € (SIM). **A mano:** 4 minuti a messaggio.

## Il costo tecnico
**Prima:** un agente unico su un modello medio (Sonnet 5.5, 2/10 $), con catalogo e condizioni interi in ogni chiamata (14.000 token), 2 giri, il 20% con un tentativo in più (2,4 chiamate), 250 token di risposta e 800 di ragionamento. **0,080 € a messaggio.**
**Dopo:**
| Passo | Quota | Chiamate | Entrata | Cache | Uscita + ragionamento | Modello | € per richiesta |
|---|---|---|---|---|---|---|---|
| Regola: "dov'è il mio ordine?" risposto dallo script con lo stato della consegna | 60% | 1 | 0 | | | nessuno | 0 |
| Smistamento | 40% | 1 | 900 | | 50 | Haiku 5.5 | 0,00004 |
| Agente per reclami e casi aperti, cache sul prefisso | 25% | 2 | 4.000 | 80% | 250 + 600 | Sonnet 5.5 | 0,0045 |
| Escalation per rimborsi e danni | 3% | 2 | 4.000 | 80% | 300 + 1.500 | Opus 5.5 | 0,0021 |
Più 2 $ a settimana di scritture in cache. **0,0075 € a messaggio.**

## La tabella
| Costo | Prima: per richiesta | Prima: annuo | Dopo: per richiesta | Dopo: annuo | Fonte |
|---|---|---|---|---|---|
| Tecnico | 0,080 € | 8.284 € | 0,0075 € | 775 € | S: token stimati, da sostituire con le ricevute di una settimana |
| Umano di gestione | 1,5 min = 0,60 € | 62.400 € | 1,2 min = 0,48 € | 49.920 € | S: stima del responsabile, da misurare su 50 richieste |
| Controllo | 1 min sul 100% = 0,40 € | 41.600 € | 0,5 min sul 40% = 0,08 € | 8.320 € | S: verifica a campione con soglia decisa prima |
| **Totale** | **1,08 €** | **112.284 €** | **0,57 €** | **59.015 €** | |
| Riferimento: tutto a mano | 4 min = 1,60 € | 166.400 € | | | |

**Che cosa si legge:** prima delle contromisure il controllo costava 5 volte il modello. Il risparmio più grande non è nei token (7.500 € l'anno) ma nel controllo (33.300 €) e nella gestione (12.500 €). Il costo tecnico scende del 91%, il totale del 47%.

## Economia di pensiero
Le schede prodotto pertinenti al posto del catalogo intero tolgono 10.000 token di entrata a chiamata: 10.000 × 2,4 × 2 $ / M = **0,041 € a messaggio, circa 4.300 € l'anno** sul modello di partenza. Effetti non in euro: risposte più corte, meno errori sui tempi di consegna (da misurare).

## Come lo teniamo sotto controllo
- **Contromisure:** regola prima dell'AI per lo stato dell'ordine; taglia giusta (S per smistare, M per i reclami, L solo per rimborsi e danni); cache sul prefisso; tetto a un tentativo in più; catalogo sostituito dalle schede pertinenti.
- **Tetto di spesa:** mini-chiave del pilota con tetto di 60 $ al mese; la responsabile del servizio guarda la pagina delle attività ogni lunedì.
- **Soglia decisa prima:** dopo quattro settimane si resta sul nuovo flusso se il costo totale per messaggio scende almeno del 30% e la quota di risposte corrette resta almeno al 95%.
- **Rischio:** se lo smistamento su modello piccolo sbaglia più del previsto, il costo si sposta nel controllo. Si misura nella prima settimana.
