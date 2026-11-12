# L10 · Policy AI di Vèrso · traccia sulla ISO/IEC 42001 (SIM)

*Traccia di riferimento per l'esercizio «Dalla RACI alla policy» (prompt 6 di PROMPT_L10.md): Claude propone, il gruppo decide. Caso didattico Vèrso: dati simulati.*

**Scheletro senza certificazione.** La struttura segue le clausole 4-10 della ISO/IEC 42001 (sistema di gestione dell'AI), come tutte le norme di sistema di gestione: contesto, leadership, pianificazione, supporto, attività operative, valutazione, miglioramento. Si usa come scheletro: **nessun documento deve far intendere che Vèrso sia certificata**. Ciclo PDCA (pianificare, fare, verificare, correggere), compatibile con la ISO 9001. Principio di progetto: **corpo stabile, allegati che si aggiornano**.

**Postura:** abilitante governata. Sì per default sul verde, condizioni sul giallo, divieti solo sul rosso. "Una policy non serve a vietare. Serve a poter dire sì, sapendo a quali condizioni."

**Etichette di adozione** (da mettere su ogni riga; non sono i colori del semaforo):
- **DA VALIDARE**: fatto sull'organizzazione da confermare (ruoli, numeri, interlocutori, raccordi);
- **PROPOSTA**: scelta da prendere; si adotta, si adatta o si rinvia con una decisione registrata;
- **DAL GIORNO 0**: applicabile subito (metodo, formati, fatti verificati).

---

## Corrispondenza con le clausole (proposta di lavoro)
| Clausola 42001 | Capitoli della policy |
|---|---|
| 4 Contesto | 1 Scopo e campo · 2 Riferimenti e definizioni · 3 Ruolo e postura |
| 5 Leadership | 4 Principi · 5 Governance e ruoli |
| 6 Pianificazione | 7 Informazioni e semaforo (rischi) |
| 7 Supporto | 9 Formazione e consapevolezza |
| 8 Attività operative | 6 Strumenti ammessi e account · 8 Regole d'uso e decisioni non delegabili |
| 9 Valutazione delle prestazioni · 10 Miglioramento | 10 Incidenti, controllo e revisione |

## I dieci capitoli

**1. Scopo e campo di applicazione.** A chi si applica (personale, collaboratori, consulenti che lavorano con informazioni di Vèrso), su qualsiasi strumento. Organi tramite estratto (allegato E). [DA VALIDARE: perimetro, compresi i servizi di noleggio e sharing]

**2. Riferimenti e definizioni.** AI Act (Reg. UE 2024/1689), L. 132/2025, GDPR, ISO/IEC 42001, ISO 9001. Definizioni: sistema di AI, utilizzatore, piattaforma organizzativa, strumento governato, account personale, account aziendale, informazione verde/gialla/rossa, zona grigia, decisione non delegabile, punto di controllo. [DAL GIORNO 0 per le definizioni; testo vigente delle norme da riconfermare]

**3. Ruolo e postura.** Vèrso è utilizzatore (deployer) di sistemi di terzi; ruolo da rivalutare se offre a terzi un sistema a proprio nome. Postura abilitante governata. [PROPOSTA]

**4. Principi.** Sei principi, ciascuno con una regola verificabile. [PROPOSTA]
| Principio | Regola verificabile |
|---|---|
| Supervisione umana | L'AI propone, chi firma decide |
| Verifica | Fatti, numeri e fonti si controllano prima dell'uso |
| Riservatezza | Il semaforo decide dove va ogni informazione |
| Trasparenza | Si dichiara l'uso dell'AI a clienti e officine |
| Equità | Nessuna valutazione di persone affidata all'AI |
| Proporzionalità | Più rischio, più controlli; meno rischio, meno attrito |

**5. Governance e ruoli.** Owner (direzione); referente AI (porta unica, zone grigie entro tre giorni, aggiorna gli allegati, coordina IT, DPO, qualità); responsabili di area (definiscono che cosa fa l'AI e chi verifica nel proprio processo: la RACI); raccordi con DPO e IT. Ogni ruolo ha un vice. "Sono incarichi, non gradi"; "chi modifica non decide, chi decide non modifica". [DA VALIDARE: nomi e ore; non inventare nomi]

**6. Strumenti ammessi e account.** Tre livelli: piattaforma organizzativa, strumenti governati, strumenti personali. Elenco puntuale nell'allegato B. [PROPOSTA]
**Regola sugli account (proposta):**
- informazioni gialle e rosse **mai** in account personali; il verde sì, se l'account ha l'addestramento spento;
- un account per persona: **nessuna utenza condivisa** (altrimenti non si sa chi ha approvato);
- al primo accesso si apre la privacy e si spegne l'uso dei dati per l'addestramento; **un'istruzione nel project non basta**, conta l'impostazione;
- le impostazioni si verificano e si registrano con la data nell'allegato B, per piano e fornitore ("non addestra" non vuol dire "non conserva");
- chiavi API: una per uso o per persona, con un tetto di spesa; mai in chat, nei file o nelle istruzioni;
- chi oggi usa un abbonamento personale per lavoro lo segnala senza conseguenze: è un'informazione per scegliere lo strumento giusto (caso e non colpa).

**7. Informazioni e semaforo.** Verde, giallo, rosso, con le regole del semaforo; "nel dubbio, il colore più alto"; zone grigie decise entro tre giorni e trasformate in esempi. Allegato A per macro-processo. [PROPOSTA]

**8. Regole d'uso e decisioni non delegabili.** Regole d'uso valide su qualunque strumento. Decisioni non delegabili, ciascuna con un verificatore umano nella RACI: [PROPOSTA]
- rimborsi, risarcimenti, coupon;
- impegni con officine, Comuni e fornitori;
- comunicazioni pubbliche dopo un incidente;
- valutazione di persone (operatori, clienti, ciclisti);
- risposte al Garante e agli enti di controllo;
- modifiche alle istruzioni e al flusso dell'agente.

**9. Formazione e consapevolezza.** Modulo base prima dell'accesso; nuovi ingressi entro tre mesi; aggiornamento annuale; partecipazione registrata (evidenza dell'alfabetizzazione, AI Act art. 4). [PROPOSTA]

**10. Incidenti, controllo e revisione.** Segnalazione entro 24 ore (allegato C); la segnalazione in buona fede non si sanziona ("caso e non colpa"); indicatori in un cruscotto; revisione trimestrale nel primo anno, poi annuale e a ogni cambiamento significativo. [PROPOSTA]

## I cinque allegati
- **A · Semaforo per macro-processo** (assistenza, officine, noleggio, sharing, amministrazione). [DA VALIDARE]
- **B · Strumenti, piattaforme e account**: piattaforma · livello · informazioni ammesse · chi amministra · addestramento spento (sì/no, data della verifica) · conservazione · connettori ammessi · chiavi e tetti. [DA VALIDARE, aggiornare ogni mese]
- **C · Modulo di segnalazione** di un incidente. [DAL GIORNO 0]
- **D · Riferimenti interni**: codice etico, privacy, qualità, regolamento IT. [DA VALIDARE]
- **E · Estratto di una pagina** per gli organi e per l'esterno. [PROPOSTA]

## Controlli prima di chiudere la bozza
- [ ] Nessuna frase dichiara o lascia intendere una certificazione.
- [ ] Nessun nome di persona inventato: i ruoli restano DA VALIDARE.
- [ ] La postura non è restrittiva travestita.
- [ ] Ogni decisione non delegabile ha un verificatore nella RACI.
- [ ] C'è la regola su account personali e aziendali.
- [ ] Le righe DAL GIORNO 0 non nascondono decisioni.
