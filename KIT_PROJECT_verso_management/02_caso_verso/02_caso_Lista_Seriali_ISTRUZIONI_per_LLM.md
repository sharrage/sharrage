# Istruzioni per leggere la lista seriali
*Da leggere prima di rispondere a qualsiasi domanda su un seriale. Valgono per `Lista_Seriali_compatta.md`.*

## Che cosa contiene
L'export notturno dell'ERP con le batterie Vèrso: per ogni seriale il lotto, il modello, lo stato, la destinazione (vendita diretta o sharing) e l'eventuale seriale sostitutivo. È aggiornato alla notte precedente: una sostituzione fatta oggi non c'è ancora.

## Come rispondere a «il seriale X è nel richiamo?»
1. **Controlla il formato:** VS- seguito da sei cifre (es. VS-004047). Non correggere mai un seriale: niente O al posto di 0, niente I al posto di 1, niente cifre aggiunte o tolte. Se il formato non torna, chiedi al cliente di ricontrollarlo.
2. **Controlla l'intervallo:** se il numero è sotto 000001 o sopra 006000, il seriale non è nel registro. Secondo la policy l'esito è DA_VERIFICARE, non "non richiamato".
3. **Applica la regola del lotto:** fino a VS-004200 è B-2404, cioè **nel richiamo**. Oltre, non è nel lotto richiamato.
4. **Guarda le eccezioni:** se il seriale è nella tabella delle eccezioni, lo stato è quello indicato (SOSTITUITA con il seriale nuovo, o BLOCCATA). Altrimenti lo stato è IN_USO.
5. **Rispondi con la formula della policy** (P02), citando il registro e la data dell'export.

## Errori da evitare
- Un seriale NEW-xxxxxx è una batteria sostitutiva: non è nel lotto richiamato.
- Un codice BK-xxxx è una bici dello sharing, non una batteria: per trovare la batteria usa la lista flotta.
- Il modello e la data d'acquisto non dicono il lotto: conta solo il seriale.
- Non dire "sicura" a una batteria: si dice solo se il seriale risulta o non risulta nel lotto B-2404.

## Se le regole non bastano
Per una verifica puntuale (per esempio prima di un rimborso) si consulta il file originale nell'archivio `04_files_non_ottimizzati`: in Claude Code con una ricerca sul seriale, senza leggere tutto il file.
