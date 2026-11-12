# Domanda 3 dell'AD · Entro marzo risponde l'AI a tutti, in tutte le lingue?
*Bozza approvata dal gruppo. Fonti: 02_caso_policy_richiamo_verso.md (P05, P06, P07, P10), 02_caso_Project_Work_L1-L14.md, 02_caso_Richieste_150_base.csv, 02_caso_L8_vincoli_comuni_e_carte.md.*

**In una frase:** entro marzo il sistema può rispondere da solo alle richieste semplici in italiano e tedesco, con le persone sulle eccezioni. «A tutti, in tutte le lingue, persone solo per i casi gravi» oggi non è dimostrabile.

## Cosa non torna con i documenti
- **«Tutte le lingue»:** il sistema e i dati del caso prevedono solo italiano e tedesco. Altre lingue non sono state testate.
- **«Persone solo per i casi gravi»:** la policy chiede una persona anche per rimborsi, richieste esplicite di un operatore, conflitti sui dati e officine che non accettano la prenotazione (P05, P06, P07). Nelle 150 richieste di prova circa 1 su 8 contiene parole che portano a una persona (conteggio per parole chiave, da confermare con la classificazione vera).
- **«A tutti»:** serve un seriale leggibile e un dato aggiornato; l'export ERP è notturno (vincolo C1).

## Cosa manca, in ordine di importanza
1. Passaggio a una persona con coda e riassunto del caso; il sistema non dice «operatore contattato» finché la coda non conferma (P07). Il supporto umano lavora lun-ven 9-18: serve una regola per notte e fine settimana.
2. Collegamento tra i due assistenti e invio della risposta (oggi non arriva a nessuno).
3. Prenotazione dell'officina (non costruita; per C4 l'officina conferma).
4. Misura degli errori: ci sono già 20 domande di valutazione e 50 richieste di stress.
5. Privacy: filtro dati personali troppo largo, verifica della DPO su dove vanno i dati, il cliente deve sapere di parlare con un'AI.
6. Tetto di spesa (oggi inesistente, memo del CFO).
7. Altre lingue, una per volta, ciascuna con il suo test.

## Cosa possiamo promettere a marzo (nostra valutazione, da confermare con i test)
Risposta automatica per richieste informative e verifica del richiamo in italiano e tedesco, con rimborsi, sicurezza e casi dubbi a una persona. Non possiamo promettere «assistenza quasi interamente automatizzata».

## Da verificare
La quota di richieste che finiscono a una persona, misurata con l'eval; i tempi per costruire i punti 1-4; la lingua delle richieste reali (nelle 150 di prova circa 16 in tedesco, nessuna in altre lingue).
