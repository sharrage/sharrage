# Il Mazzo Vincolo · quattro vincoli comuni e due carte di estensione

*Le carte riprendono le proposte del documento docenti del programma (Mazzo Vincolo, L8). Dalla v4 (2/11/2026) le esercitazioni sono identiche per tutti i gruppi: quattro delle sei carte sono i **vincoli comuni C1-C4**, uguali per tutti, fino al board. Le altre due sono l'**estensione per chi finisce prima**: il gruppo ne sceglie una, oppure propone un quinto vincolo plausibile, e ne valuta l'impatto. L'estensione è facoltativa e non entra nel confronto al board. Niente sorteggio. Caso didattico Vèrso, fittizio.*

**Vincoli flessibili.** Vincoli comuni ed estensione sono limiti flessibili: ci sono, ma si possono discutere. **Non si aggirano, si negoziano con argomenti**: chi vuole spostare un limite lo dichiara, dice con chi negoziarlo, con quale argomento (euro, rischi, tempi) e a quale prezzo. Lo stesso vale per le regole della policy del caso.

I fatti del caso (veri per tutti, ricavati dai documenti; non sono vincoli comuni, ma i vincoli li portano all'estremo):
- **Dati in ritardo**: ERP esportato di notte; disponibilità delle officine dichiarata, non reale.
- **Dati personali minimi**: nome, email, indirizzo e telefono fuori dai log tecnici del pilota (policy v2.1, P08).
- **Persone poche**: due persone in assistenza più un responsabile, nei giorni feriali.
- **Tempo e soldi con un tetto**: 90 giorni, un budget pilota, il CdA alla fine.

---

## I quattro vincoli comuni (uguali per tutti i gruppi)

## C1 · ERP solo di notte
- **Che cosa impone:** l'IT concede solo un export notturno, niente verifiche in tempo reale.
- **Come cambia l'agente:** verifica del lotto in batch, risposte in due tempi.
- **Estremizza:** i dati in ritardo. **Pesa di più in:** L8.
- **Argomento per il board:** nessun impatto sui sistemi aziendali.
- **Domanda guida:** che cosa dite al cliente oggi, e che cosa domattina?
- **Aggiramento da evitare:** chiedere comunque un'API in tempo reale.
- **Si può negoziare con:** l'IT, per esempio un secondo export a mezzogiorno, con il suo costo e il suo rischio.

## C2 · Niente nomi salvati
- **Che cosa impone:** nessun dato personale può essere conservato nei componenti AI.
- **Come cambia l'agente:** anonimizzazione spinta, audit trail senza dati personali, collegamento alla persona solo nel sistema autorizzato.
- **Estremizza:** i dati personali minimi. **Pesa di più in:** L11.
- **Argomento per il board:** privacy by design.
- **Domanda guida:** come richiamate un cliente se l'agente non sa chi è?
- **Aggiramento da evitare:** chiamare "anonimo" un dato in cui avete solo tolto il nome (un seriale resta collegabile).
- **Si può negoziare con:** la DPO, su che cosa resta nel sistema autorizzato e per quanto tempo.

## C3 · Budget dimezzato
- **Che cosa impone:** il pilota ha la metà del budget chiesto.
- **Come cambia l'agente:** più filtri prima dell'AI, modello leggero quasi ovunque, meno risposte automatiche.
- **Estremizza:** tempo e soldi con un tetto. **Pesa di più in:** L9.
- **Argomento per il board:** il costo per richiesta più basso.
- **Domanda guida:** quali richieste non devono nemmeno arrivare al modello?
- **Aggiramento da evitare:** spostare il costo sulle persone senza dirlo.
- **Si può negoziare con:** il CFO, con il costo per richiesta e il costo di non farlo (role play E7).

## C4 · Officine diffidenti
- **Che cosa impone:** le officine non accettano prenotazioni automatiche.
- **Come cambia l'agente:** l'agente propone, l'officina conferma; comunicazione e adozione diventano centrali.
- **Estremizza:** le persone poche (quelle della rete). **Pesa di più in:** L10 e L12.
- **Argomento per il board:** una soluzione che la rete accetta davvero.
- **Domanda guida:** che cosa deve vedere Franco per fidarsi?
- **Aggiramento da evitare:** prenotare comunque e avvisare l'officina dopo.
- **Si può negoziare con:** il capo officina, su un pilota con poche officine volontarie.

---

## Estensione per chi finisce prima (facoltativa, fuori dal confronto al board)

Il gruppo sceglie una delle due carte, oppure propone un quinto vincolo plausibile per Vèrso, e ne valuta l'impatto: che cosa impone, come cambia la soluzione, con chi si negozia.

## Estensione · Solo dati in UE
- **Che cosa impone:** nessun dato può uscire dall'Unione Europea.
- **Come cambia l'agente:** modello o fornitore diverso, magari meno capace; prompt da ricalibrare; ogni servizio della catena va controllato.
- **Estremizza:** C2. **Pesa di più in:** L11.
- **Argomento per il board:** massima tutela legale.
- **Domanda guida:** quali anelli della vostra catena oggi portano dati fuori dall'UE, e come lo sapete?
- **Aggiramento da evitare:** "tanto anonimizziamo e poi mandiamo dove vogliamo".
- **Si può negoziare con:** la DPO e l'IT, per esempio su quali dati possono uscire se resi non identificabili, con prova.

## Estensione · Due soli operatori
- **Che cosa impone:** ogni promessa al cliente va approvata da una persona, ma il team è di due.
- **Come cambia l'agente:** soglie di confidenza, approvazione solo sui casi a rischio, priorità.
- **Estremizza:** le persone poche. **Pesa di più in:** L10.
- **Argomento per il board:** controllo umano reale e sostenibile.
- **Domanda guida:** quante approvazioni al giorno reggono due persone nel picco?
- **Aggiramento da evitare:** far approvare tutto a mano (o niente).
- **Si può negoziare con:** il responsabile assistenza e il CFO, su quante approvazioni al giorno sono sostenibili.

## Estensione · Un quinto vincolo vostro
Un limite plausibile per Vèrso che le carte non coprono. Scrivetelo con le stesse voci: che cosa impone, come cambia l'agente, aggiramento da evitare, con chi si negozia.
