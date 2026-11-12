# Domanda 1 dell'AD · Che cosa fa il vostro sistema?
*Bozza approvata dal gruppo. Fonti: 02_caso_policy_richiamo_verso.md (P04, P06, P07, P10), 01_n8n_esempio_flusso_finale_sfida1_L7_alleggerito.json, al_management_flusso_spiegato_12112026_2005.md.*

**In breve:** il sistema legge le richieste dei clienti sul richiamo delle batterie e prepara una risposta. Quando serve una decisione che spetta a una persona, deve passare il caso a un operatore. Oggi il primo passo funziona e il secondo non è ancora collegato.

## Come lo spiegheremmo a un cliente
1. Lei ci scrive, in italiano o in tedesco, e il sistema legge la sua richiesta.
2. Controlla il numero di serie della sua batteria e verifica se rientra nel richiamo del lotto B-2404.
3. Le risponde sulla base del nostro manuale e della nostra policy, non di quello che il modello "crede di sapere".
4. Se la sua batteria è coinvolta, le spiega di non usarla né caricarla e che la sostituzione è gratuita.
5. Se chiede un rimborso, un risarcimento o parlare con una persona, o c'è un pericolo, la richiesta va a un operatore del supporto. Il sistema non decide e non promette soldi.

## Cosa fa davvero oggi
- Riceve, classifica (richiamo, guasto diverso, informazioni, cliente arrabbiato), controlla il seriale e scrive la risposta.
- Il passaggio a una persona (riga 5) è previsto dalla policy (P06, P07) ma nel flusso non è ancora costruito (miglioria 1).
- Non prenota ancora la sostituzione in officina: la policy prevede che l'agente proponga e l'officina confermi (vincolo C4).
- Non sappiamo quanto sbaglia: non c'è una misura (miglioria 3).

## Da tenere presente
Le cinque righe descrivono il sistema come progettato dalla policy. Per un cliente reale va chiuso prima il punto 5, altrimenti il sistema potrebbe rispondere a un rimborso come a una domanda qualsiasi.

## Da verificare
Se il flusso del nostro gruppo ha già il passaggio a una persona; se il lotto B-2404 coinvolge anche le bici dello sharing (domanda 4).
