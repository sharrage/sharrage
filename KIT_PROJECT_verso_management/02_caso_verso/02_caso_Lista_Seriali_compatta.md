# Lista seriali · versione compatta
*Ottimizzata dall'export ERP `Lista Seriali.xlsx` (6.000 righe, 6 colonne). Le 6.000 righe seguono quattro regole: qui ci sono le regole e le sole 21 righe che fanno eccezione. Ogni regola è stata verificata riga per riga sul file originale il 10/11/2026. L'originale è in 04_files_non_ottimizzati.*

## Le regole (valgono per tutti i seriali da VS-000001 a VS-006000)
| Campo | Regola |
|---|---|
| Esistenza | Esistono solo i seriali da VS-000001 a VS-006000. Fuori da questo intervallo il seriale **non è nel registro**. |
| Lotto | da VS-000001 a VS-004200: **B-2404** (il lotto richiamato). Da VS-004201 a VS-006000: numero dispari B-2403, numero pari B-2405. |
| Modello | si ripete ogni tre: numero ÷ 3 con resto 1 = Cargo, resto 2 = Urban, resto 0 = Linea. Esempio: VS-000184 → resto 1 → Cargo. |
| Destinazione | da VS-003901 a VS-004200 e da VS-005101 a VS-006000: **SHARING**. Tutti gli altri: D2C (vendita diretta). |
| Stato | **IN_USO** per tutti, tranne le eccezioni sotto. Seriale sostitutivo: vuoto, tranne le eccezioni. |

## Le eccezioni (21 righe)
| seriale | stato | seriale_sostitutivo |
|---|---|---|
| VS-000001 | SOSTITUITA | NEW-000001 |
| VS-000002 | SOSTITUITA | NEW-000002 |
| VS-000003 | SOSTITUITA | NEW-000003 |
| VS-000004 | SOSTITUITA | NEW-000004 |
| VS-000005 | SOSTITUITA | NEW-000005 |
| VS-000006 | SOSTITUITA | NEW-000006 |
| VS-000007 | SOSTITUITA | NEW-000007 |
| VS-000008 | SOSTITUITA | NEW-000008 |
| VS-000009 | SOSTITUITA | NEW-000009 |
| VS-000010 | SOSTITUITA | NEW-000010 |
| VS-000011 | SOSTITUITA | NEW-000011 |
| VS-000012 | SOSTITUITA | NEW-000012 |
| VS-000013 | SOSTITUITA | NEW-000013 |
| VS-000014 | SOSTITUITA | NEW-000014 |
| VS-000015 | SOSTITUITA | NEW-000015 |
| VS-000016 | SOSTITUITA | NEW-000016 |
| VS-000017 | SOSTITUITA | NEW-000017 |
| VS-000018 | SOSTITUITA | NEW-000018 |
| VS-000019 | SOSTITUITA | NEW-000019 |
| VS-000020 | SOSTITUITA | NEW-000020 |
| VS-000031 | BLOCCATA | - |

## Conteggi di controllo
B-2404: 4.200 (di cui 300 nello sharing) · B-2403: 900 · B-2405: 900 · sharing: 1.200 · D2C: 4.800 · Cargo, Urban, Linea: 2.000 ciascuno.
