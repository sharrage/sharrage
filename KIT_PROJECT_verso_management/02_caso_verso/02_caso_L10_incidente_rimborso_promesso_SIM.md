# L10 · L'incidente del rimborso promesso (SIM)

*Caso didattico Vèrso: azienda, persone, orari, testi e numeri sono simulati. È l'evento di L10: l'assistente promette un rimborso non dovuto e il cliente lo pubblica sui social. Succede nella settimana di picco del richiamo, dopo l'arrivo di Dracula Ventures. Si usa nel Laboratorio 2 e nella risposta all'AD.*

## 1. I due post
Un cliente del lotto B-2404, la sera di un martedì di picco del richiamo (19:35), pubblica lo screenshot di una risposta firmata "Assistenza Vèrso":

> «L'assistente di Vèrso mi ha scritto: provvederemo al rimborso completo della bici. Finalmente! Screenshot salvato, così non cambiano idea.»

Mercoledì alle 9:40, dopo la risposta "era un errore", pubblica le due risposte una accanto all'altra:

> «Ieri il rimborso completo, oggi "era un errore". Ecco le due risposte.»

Nella notte il post viene condiviso in un gruppo locale e ripreso da alcuni video brevi. Mercoledì mattina ha centinaia di condivisioni e decine di commenti di altri clienti: "allora lo chiedo anch'io". Alle 10:30 lo vede l'AD.

## 2. Il messaggio del cliente (pratica SIM-PR-0417)
> «Ho la bici del richiamo, seriale VS-004417. Sono stanco di aspettare: mi rimborsate la bici e chiudiamo qui? Ho speso 2.400 euro.»

## 3. La bozza dell'assistente (inviata)
> «Gentile cliente, ci dispiace molto per il disagio. Comprendiamo la sua frustrazione e provvederemo al rimborso completo della bici, come previsto nei casi valutati dal nostro team. Nel frattempo la invitiamo a non utilizzare né ricaricare la batteria.»

## 4. Cronologia

| Quando | Che cosa succede | Chi | Versione o stato |
|---|---|---|---|
| Lunedì della settimana prima | Per smaltire l'arretrato viene attivato nel flusso il pulsante "approva e invia tutto", che manda ai clienti in un colpo tutte le bozze selezionate | un consulente esterno, su richiesta a voce | nessuna richiesta scritta, nessuna approvazione registrata |
| Lunedì della settimana prima | Nella conoscenza dell'assistente viene caricata la policy v2.1, senza togliere la v2.0 | chi aggiornava i documenti | v2.0 (15/01) e v2.1 (26/01) presenti insieme |
| Martedì, 16:41 | Arriva il messaggio del cliente | casella assistenza | |
| 16:42 | L'assistente classifica "cliente arrabbiato · richiamo" e prepara la bozza | assistente | istruzioni del flusso v7 |
| 16:42 | La bozza entra nella coda "da approvare" con altre 21 | flusso | |
| 17:52 | L'operatore di turno apre la coda: 22 bozze | Operatore 2 | |
| 17:52-17:58 | Le 22 bozze vengono selezionate e approvate con "approva e invia tutto" | Operatore 2 | sei minuti per 22 bozze |
| 17:58 | Le 22 risposte partono | flusso | |
| 19:35 | Il cliente pubblica lo screenshot | cliente | |
| Mercoledì, 9:10 | Il responsabile assistenza scrive al cliente che si è trattato di un errore | Responsabile assistenza | |
| 9:40 | Il cliente pubblica la seconda risposta accanto alla prima | cliente | |
| 10:30 | L'AD vede il post e scrive ai gruppi (vedi `dal_management`) | AD, tramite la segreteria | |

## 5. I documenti, così come erano nel contesto dell'assistente
- **Policy del richiamo v2.0 (15/01), P06:** «Eventuali rimborsi sono valutati dal team caso per caso.»
- **Policy del richiamo v2.1 (26/01), P06:** «Rimborso del prezzo bici, taxi, corriere scelto dal cliente, mancato lavoro, danni a persone o beni, coupon e risarcimenti sono decisioni umane. L'agente raccoglie la richiesta e la trasferisce senza accettare, respingere in modo definitivo o fissare un importo.» La v2.1 dichiara non operative le versioni precedenti.
- **Istruzioni del flusso v7, riga 31:** «Non promettere rimborsi.» È scritta come istruzione nel testo del prompt; sullo strumento non c'è nessun controllo.
- **Orario del supporto umano:** lunedì-venerdì, 9:00-18:00.

## 6. Che cosa dicono le persone (raccolto mercoledì)
- **Operatore 2:** «Alle sei meno dieci avevo ventidue bozze. Le prime le ho lette, poi sembravano tutte uguali. Erano scritte bene.»
- **Operatore 1:** «Il pulsante "invia tutto" l'hanno messo per l'arretrato. Nessuno ci ha detto quando usarlo.»
- **Responsabile assistenza:** «L'operatore doveva leggere meglio.»
- **IT ad interim (Luca Invernizzi):** «Del pulsante non sapevo niente. Non è passato da noi.»
- **DPO ad interim:** «Nel post si vede il seriale del cliente. Va valutato se c'è un problema di dati.»
- **CFO ad interim (Marco Sala):** «Se diventa un precedente, quanti rimborsi ci chiederanno? E chi li firma?»

## 7. Domande guida
1. Chi aveva le chiavi? Chi poteva far uscire una promessa di denaro senza una firma?
2. Per ogni passaggio: c'era una A, cioè una persona che ne risponde? C'era un punto di fermata?
3. Che cosa ha visto davvero chi ha approvato?
4. Quali falle sarebbero rimaste uguali con un altro modello?
5. Quali tre modifiche chiudono la porta al ritorno, senza cercare un colpevole?
