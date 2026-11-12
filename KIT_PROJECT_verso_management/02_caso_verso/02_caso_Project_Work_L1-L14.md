# Project Work L1-L14 · il caso e la sfida
*Versione ottimizzata in Markdown del PDF `Project_Work_L1-L14.pdf`: stesso testo, senza impaginazione, piè di pagina e immagini. In caso di dubbio vale il PDF originale (in 04_files_non_ottimizzati).*

**Project Work​**
**Materiale per i partecipanti · AI Management &**
**Prompt engineering**
Tutto ciò che segue è fittizio: azienda, persone, numeri e documenti esistono solo dentro al corso. I dati non provengono da nessuna azienda reale e non vanno usati fuori dall'aula.

## Parte 1 • Il case

**L'azienda**
Vèrso è un brand italiano di e-bike di design. Nasce a Bergamo nel 2019 come startup e oggi è una scale-up da 140 persone e circa 38 milioni di fatturato. Vende online direttamente al cliente finale, senza negozi propri. L'assistenza dopo l'acquisto passa da una rete di 250 officine partner tra Italia, Germania e Austria: il cliente prenota, porta la bici, l'officina ripara e fattura a Vèrso. A Milano e Torino Vèrso gestisce anche due servizi diretti: e-bike in abbonamento mensile e un servizio di bike sharing in concessione con i due Comuni, circa 1.200 bici prenotabili da app. Il posizionamento è premium: la bici costa più della media, e il cliente si aspetta che qualcuno risponda quando qualcosa non va. L'assistenza clienti è però rimasta piccola, due persone più un responsabile, perché finora il volume lo permetteva.

**La crisi**
Il fornitore delle batterie segnala un difetto su un lotto di celle: in condizioni di ricarica prolungata la batteria può surriscaldarsi. Vèrso richiama il lotto B-2404, circa 4.200 batterie montate su bici vendute tra marzo e dicembre 2025.

Il richiamo viene annunciato il 12 gennaio. Quello che succede nelle due settimane successive: ●​ I contatti dei clienti passano da circa 350 a circa 600 a settimana, +70%. Le due persone dell'assistenza non reggono: l'arretrato arriva a 1.400 richieste e il tempo medio di risposta passa da un giorno a cinque. ●​ Le officine partner sono sommerse. Molte accettano le prenotazioni per telefono e non aggiornano il gestionale, così Vèrso non sa più dove sia la capacità libera. ●​ Sui social il caso esplode. Un video che mostra una batteria fumante fa 300.000 visualizzazioni in due giorni. Nei commenti si mescolano clienti davvero coinvolti dal richiamo e clienti che hanno un guasto qualsiasi e si spaventano. ●​ Arrivano richieste in italiano e in tedesco, spesso senza il numero seriale o con un seriale trascritto male. Il mandato. L'AD concede 90 giorni e un budget pilota. Vuole una soluzione AI che funzioni davvero, non una demo, e la vuole vedere presentata al CdA alla fine del periodo. Se funziona, il pilota diventa strutturale; se non funziona, si torna ad assumere persone a tempo.

**I numeri chiave**
Sono le cifre da usare in tutte le esercitazioni. Quando serve un numero che qui non c'è, il gruppo lo stima e dichiara l'ipotesi.

**Voce**
**Valore**
**Dipendenti Vèrso**
**Fatturato annuo**
**~38 milioni di euro**
**Officine partner**
**250 (Italia, Germania, Austria)**
**Bici in bike sharing**
**~1.200, di cui ~300 con batterie del lotto**
**Batterie richiamate (lotto B-2404)**
**~4.200**
**Richieste clienti prima del richiamo**
**~350 a settimana**
**Richieste clienti dopo il richiamo**
**~600 a settimana (+70%)**
**Arretrato accumulato**
**~1.400 richieste**
**Tempo medio di risposta prima / dopo**
**1 giorno / 5 giorni**
**Persone in assistenza clienti**
**2, più un responsabile**
**Costo pieno di un'ora di assistenza**
**28 euro**
**Tempo medio di lavorazione di una richiesta**
**9 minuti**
**Tempo concesso dall'AD**
**90 giorni**
**Quota di richieste che riguarda davvero il richiamo**
**circa 4 su 10**
L'ultima riga è la più importante per il business case: oggi le due persone dell'assistenza leggono tutto, e sei richieste su dieci non c'entrano con il richiamo.

**Le persone**
**Persona**
**Ruolo**
**Cosa vuole**
**Cosa teme**
**Elena Rizzi**
**AD**
**Risultati visibili, in fretta**
**Che il caso continui a bruciare**
**reputazione**
**Marco Sala**
**CFO**
**Sapere quanto costa ogni**
**Una spesa che cresce senza un tetto**
**richiesta gestita**
**Luca**
**IT manager**
**Invernizzi**
**Avv. Giulia**
**DPO**
**Mori**
**Nessun impatto sui sistemi in**
**Dare accessi che non sa come**
**produzione**
**revocare**
**Sapere dove finiscono i dati e**
**Un reclamo al Garante o un cliente**
**chi risponde**
**che non sa di parlare con un'AI**
**Franco**
**Capo officina**
**Che le officine non ricevano**
**Che un software decida al posto di**
**Pagani**
**storico**
**prenotazioni sbagliate**
**chi conosce le bici**
Franco Pagani è lo scettico del gruppo, ed è anche l'unico che conosce davvero i casi limite: quali seriali sono stati trascritti male negli anni, quali modelli hanno il vano batteria diverso, quali officine non useranno mai un sistema nuovo. Vale la pena ascoltarlo prima di contraddirlo.

**I sistemi e i dati**
Questo è il paesaggio tecnico in cui l'agente deve inserirsi.

**Sistema**
**Cosa contiene**
Casella assistenza Le richieste dei clienti, via mail e form del sito

**ERP**
**Ordini, numeri seriali, lotti delle batterie**
**Come ci si accede**
**Lettura diretta**
**Export notturno in CSV, non in**
**tempo reale**
**Gestionale officine**
**Documentazione**
Anagrafica delle 250 officine, CAP serviti,

**API di prenotazione, a volte**
**disponibilità dichiarata**
**lenta**
**Manuale e-bike, policy di richiamo**
**PDF**
Due cose da sapere. L'export dell'ERP gira di notte: una verifica fatta alle 18 vede i dati di stamattina. E la disponibilità delle officine è quella che l'officina ha dichiarato, non quella reale, perché molte prenotano ancora per telefono.

## Parte 2 • La scheda sfida

**L'incarico**
Tutti i gruppi ricevono lo stesso incarico: costruire l'agente che gestisce le richieste dei clienti legate al richiamo batterie, e poi dimostrare che può entrare davvero in Vèrso. L'agente deve fare cinque cose: 1.​ Leggere e classificare ogni richiesta in arrivo: interessato dal richiamo, guasto diverso, richiesta di informazioni, cliente arrabbiato. 2.​ Verificare se numero seriale e lotto rientrano nel richiamo. 3.​ Rispondere in modo corretto, usando il manuale e la policy di richiamo, non quello che il modello crede di sapere. 4.​ Agire: prenotare la sostituzione nell'officina più vicina al cliente. 5.​ Passare a una persona i casi che non può decidere da solo: rimborsi, reclami gravi, qualunque cosa che impegni Vèrso al di fuori della policy. I cinque compiti non si costruiscono tutti insieme. Si aggiungono una sessione alla volta, così che a ogni passaggio l'agente sappia fare una cosa in più di quella precedente.

**L'output atteso**
Alla fine della Sfida 1 il gruppo ha un agente che gira da solo: riceve una richiesta, la classifica, verifica il seriale, risponde citando i documenti, prenota l'officina, passa a una persona i casi che non gli competono. Regge gli imprevisti senza bloccarsi. E il gruppo sa dire quanto sbaglia, perché l'ha misurato. Alla fine della Sfida 2 il gruppo ha la presentazione per il CdA: sette slide, sei delle quali nascono una per sessione.

**Slide**
**Contenuto**
**Nasce in**
**Il problema e la soluzione**
**Fase 1**
**I vincoli e come li superiamo**
**L8**
**Quanto costa farla girare e come lo teniamo sotto controllo**
**L9**
**Chi governa la soluzione**
**L10**
**Conformità e rischi**
**L11**
**Roadmap**
**L12**
**La richiesta al board: budget, decisione, tempi**
**L13**
Ogni slide nasce da una pagina prodotta in sessione. Non si scrive la presentazione alla fine: si monta.

**I criteri di successo**
Vince il gruppo che porta in azienda la soluzione più credibile. Non vince l'agente più potente, ma quello che il board riterrebbe più realistico da mettere in esercizio lunedì mattina.

**Criterio**
**La domanda a cui rispondere**
**Solidità dei numeri**
Costi, tempo risparmiato, errori evitati: sono misurati o stimati a occhio?

**Affidabilità dimostrata**
**Quanto sbaglia l'agente, e come lo sapete?**
**Governance**
Chi controlla cosa, ed è sostenibile con le persone che ci sono?

**Rischio residuo**
**Che cosa resta scoperto, e come viene gestito?**
**Piano di rollout**
**Tempi, fasi, e come si convincono le officine**
Tutti i gruppi partono dalle stesse condizioni e affrontano gli stessi ostacoli. Quindi la differenza non la fa il problema che vi è capitato: la fa come l'avete risolto.
