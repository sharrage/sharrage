# Mappa di residenza della catena · TRACCIA

*Gruppo: ___ · Progetto: ___ · Vincoli comuni che pesano sulla mappa: ___ · Data: ___*
*Il vostro progetto vero, qualunque strumento usiate. Si compila a mano o con il prompt B di `PROMPT_L10.md`. Nessun dato personale in questo file.*

**Regola del blocco:** un agente vale quanto il suo anello meno residente. **Tre domande per ogni componente:** dove restano i dati a riposo, dove avviene il calcolo, chi ne risponde (e dove sta scritto).

**Colori:** VIOLA = in UE, verificato su contratto o impostazioni · CORALLO = fuori UE · GRIGIO = non lo sappiamo ancora (con chi verifica ed entro quando).

| # | Anello | Componente del vostro progetto | A riposo (dove) | Calcolo (dove) | Account (personale / aziendale / di gruppo) | Chi lo amministra | Addestramento sui dati spento? Verificato dove e quando | Prova (contratto, impostazione, documento con data) | Colore | Chi verifica il grigio, entro quando |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | Interfaccia e memoria (chat, project, memoria) | | | | | | | | | |
| 2 | Modello (dove gira l'inferenza) | | | | | | | | | |
| 3 | Strumenti (codice, sandbox, file creati) | | | | | | | | | |
| 4 | Server MCP (chi li ospita, dove) | | | | | | | | | |
| 5 | Fonti collegate (posta, fogli, gestionali, embedding) | | | | | | | | | |
| 6 | Servizi esterni (ricerca web, API di terzi, app dello sharing) | | | | | | | | | |
| 7 | Log e sicurezza (copie, monitoraggio, telemetria) | | | | | | | | | |

*Aggiungete righe: un anello può contenere più componenti (per esempio due fogli di calcolo di fornitori diversi).*

## Lettura
- **L'anello meno residente è:** ___
- **Gli anelli su account personali sono:** ___ (regola di policy: il giallo mai negli account personali)
- **Che cosa dicono i vincoli comuni (e l'eventuale estensione) su questa mappa:** ___
- **Le tre domande da fare al fornitore, per iscritto:** ___

## Promemoria
- La residenza si legge nel contratto e nelle impostazioni, non nella pagina commerciale.
- La cifratura protegge il transito e il riposo, non il calcolo.
- Residenza UE non è sovranità: conta anche la legge a cui è soggetto il fornitore.
- "Non addestra" non vuol dire "non conserva". Un'istruzione nel project non impedisce l'addestramento: lo fa solo l'impostazione.
- I fornitori stessi escludono di solito le integrazioni (app, connettori, server MCP, ricerca web) dalla residenza: verificate con la data (documentazione consultata a ottobre 2026, da ricontrollare l'11/11).
