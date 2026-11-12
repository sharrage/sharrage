# Lista flotta sharing · versione compatta
*Ottimizzata da `Lista Flotta.xlsx` (1200 bici, 6 colonne). Tutte le righe seguono le regole qui sotto, verificate riga per riga il 10/11/2026. L'originale è in 04_files_non_ottimizzati.*

| Campo | Regola |
|---|---|
| Bici | da BK-0001 a BK-1200 |
| Batteria montata | da BK-0001 a BK-0300: seriale VS-(3900 + numero bici), cioè da VS-003901 a VS-004200. Da BK-0301 a BK-1200: seriale VS-(4800 + numero bici), cioè da VS-005101 a VS-006000. |
| Lotto | quello del seriale: le bici da BK-0001 a BK-0300 hanno batterie **B-2404, nel richiamo** (300 bici). Le altre 900: B-2403 o B-2405. |
| Modello | quello del seriale (si ripete ogni tre: Cargo, Urban, Linea) |
| Zona | Z1-Z8: numero bici ÷ 8, resto + 1 (BK-0001 → Z2, BK-0008 → Z1) |
| Stato batteria | IN_USO per tutte le 1.200 bici |

**Conteggi di controllo:** 150 bici per zona; B-2404 300, B-2403 450, B-2405 450.
