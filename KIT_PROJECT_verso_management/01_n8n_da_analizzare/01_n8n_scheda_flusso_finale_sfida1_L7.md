# Scheda del flusso n8n di esempio · "Versione finale" della Sfida 1 (L7)
*Una pagina al posto del file JSON (circa 34.000 caratteri). Descrive com'è costruito il flusso, senza giudicarlo: le migliorie le trovate voi. Nella stessa cartella c'è il JSON alleggerito per la lettura; l'originale da importare in n8n è in 04_files_non_ottimizzati (kit Code e Project).*

## Che cosa fa, in cinque righe
1. Riceve la richiesta di un cliente da un modulo web (form).
2. Un filtro di sicurezza (Guardrails) controlla il testo prima che arrivi all'agente.
3. Un primo agente, il **classificatore**, legge la richiesta e restituisce una scheda strutturata: categoria, livello di gravità, lingua, riassunto.
4. Per farlo può usare due strumenti: la **ricerca del seriale** nel database (un sottoflusso separato) e la **ricerca nei documenti** (manuale e policy, indicizzati con un flusso a parte).
5. Un secondo agente, il **risponditore**, prepara la risposta al cliente usando la policy.

## I pezzi del flusso (17 nodi)
| Pezzo | A che cosa serve | Note per il management |
|---|---|---|
| Moduli di ingresso (2) | ricevono la richiesta | uno dei due è disattivato |
| Guardrails | filtro di sicurezza prima del modello | ha un'uscita per i messaggi bloccati |
| Agente classificatore | categoria, gravità, lingua, riassunto | usa Claude (Anthropic) |
| Formato della risposta | obbliga il classificatore a rispondere sempre con gli stessi campi | categorie: interessato_richiamo, guasto_diverso, informazioni, cliente_arrabbiato; gravità: BASSO, MEDIO, ALTO, CRITICO; lingue: IT, DE |
| Ricerca seriale | interroga la tabella dei seriali tramite un sottoflusso | si usa solo se il seriale è nel formato giusto (es. VS-004047) |
| Ricerca nei documenti (RAG) | trova i passaggi pertinenti di manuale e policy | i documenti stanno in memoria: vanno ricaricati con il flusso di indicizzazione |
| Memorie (2) | ricordano i messaggi precedenti | |
| Agente risponditore | scrive la risposta al cliente | usa Claude e la ricerca nella policy |
| Embeddings (2) | trasformano i testi per la ricerca | usano un servizio OpenAI |

## I servizi esterni coinvolti
- Anthropic (Claude) per i due agenti e per il filtro di sicurezza.
- OpenAI per la ricerca nei documenti.
- Una tabella dati di n8n per i seriali.

## Che cosa guardare, se siete il management
- Che cosa succede a una richiesta dall'ingresso all'uscita: dove arriva la risposta?
- Che cosa succede ai messaggi bloccati dal filtro?
- Quante volte il flusso chiama il modello per una sola richiesta?
- Quali dati del cliente passano ai servizi esterni?
- Come sappiamo quanto sbaglia: c'è una misura?
