# Il flusso di assistenza spiegato in cinque righe
*Bozza approvata dal gruppo. Fonti: 01_n8n_esempio_flusso_finale_sfida1_L7_alleggerito.json, 01_n8n_scheda_flusso_finale_sfida1_L7.md, 02_caso_00_RIASSUNTO_caso_Verso.md.*

## Il flusso in cinque righe
1. **Cosa riceve:** il testo che il cliente scrive in un modulo web dell'assistenza, in italiano o in tedesco.
2. **Primo controllo:** un filtro di sicurezza blocca tentativi di manipolazione, contenuti inadatti e richieste fuori tema.
3. **Cosa decide:** un primo assistente AI (agente) classifica la richiesta in una di quattro categorie (interessato al richiamo, guasto diverso, informazioni, cliente arrabbiato), assegna gravità (da bassa a critica) e lingua. Se c'è un seriale, controlla se rientra nel richiamo e consulta la policy.
4. **Cosa risponde:** un secondo assistente scrive la risposta al cliente.
5. **Quando passa a una persona:** oggi non succede. La scheda del classificatore è pensata per gli operatori, ma nessun passaggio la manda a qualcuno.

## Punti deboli che un cliente potrebbe notare
- **Nessuno riceve la risposta:** il flusso finisce con il testo prodotto, senza invio al cliente né assegnazione a un operatore.
- **Il filtro blocca in silenzio:** l'uscita "messaggio bloccato" non è collegata a nulla, quindi il cliente non sa di non essere stato letto. Il filtro cerca qualsiasi dato personale, e chi scrive per il richiamo lascia quasi sempre nome, mail o telefono. Quanti messaggi blocchi non è misurato (da verificare).
- **Il secondo assistente non usa il lavoro del primo:** riceve solo il testo originale. Categoria, gravità ed esito del seriale non gli arrivano, quindi un cliente arrabbiato o un caso critico riceve lo stesso trattamento di una domanda semplice, e rimborsi e reclami gravi non vengono fermati.
- **Legge dal modulo sbagliato:** prende il testo da un modulo che nel file risulta spento, non da quello in uso. Può lavorare su un testo vuoto.
- **Non ricorda niente:** l'identificativo della conversazione è l'ora esatta, quindi ogni richiesta parte da zero.
- **I documenti si perdono:** manuale e policy stanno in una memoria temporanea e vanno ricaricati a mano dopo ogni riavvio.
- **Non prenota nulla:** la sostituzione in officina non è costruita.
- **Dati dei clienti a servizi esterni:** il testo passa ad Anthropic e a OpenAI. Rilevante per il vincolo 3 e per la DPO; qui non lo valutiamo.
- **Nessuna misura degli errori:** non sappiamo quanto sbaglia.
- **Dati in ritardo:** i seriali vengono dall'export notturno dell'ERP (riassunto del caso, §4): una verifica alle 18 vede i dati della mattina.

## Da verificare
- Se il modulo spento è un errore o una scelta di test.
- Quanti messaggi bloccherebbe il filtro sul CSV delle richieste.
- Se il flusso del nostro gruppo ha gli stessi difetti.
