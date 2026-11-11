# Mappa di battaglia

Mappa tattica per le one-shot della Gilda di Boar Tail: il master apre la battaglia dallo schermo del master, i giocatori entrano dal telefono con il codice della stanza o il QR, muovono il proprio personaggio entro la sua velocità e vedono solo ciò che vede.

- `index.html`: tutta l'applicazione, nessuna dipendenza da installare.
- Le mappe sono nell'oggetto `MAPS` in cima allo script.
- I telefoni si collegano direttamente al dispositivo del master (WebRTC, tramite il servizio pubblico PeerJS): serve internet. Master e vista tavolo locale funzionano anche offline.
- La vista tavolo ha in alto il pulsante «QR per entrare»: i giocatori inquadrano il QR dal tavolo, senza guardare lo schermo del master.
- Se il master sparisce per un po' (per esempio l'iPad passa a un'altra scheda o app), telefoni e vista tavolo se ne accorgono entro 15 secondi e si ricollegano da soli quando torna.

## Punti di fuga (nodo 3)

Le caselle `X` sono buchi nel muro. Solo i nemici possono entrarci: chi ci arriva esce dalla mappa. Ogni nemico ha il suo numero di uscita (badge giallo, visibile solo al master). I giocatori non vedono i buchi finché il master non li rivela dal pannello «Punti di fuga» (per esempio dopo una prova di Saggezza (Percezione) CD 15). Sulle mappe buie c'è il pulsante «Torcia».

## Mappe incluse, divise per one-shot

Nella preparazione si sceglie prima la one-shot, poi la battaglia: i due menu leggono i gruppi. I gruppi sono nell'elenco `ONESHOTS`, subito dopo `MAPS`: per una one-shot nuova basta aggiungere un gruppo con gli id delle sue mappe. Le mappe che non stanno in nessun gruppo finiscono in «Altre mappe».

### Il Grande e Glorioso Me

- `n3` Nodo 3 · Gli schiavi in fuga (buia, punti di fuga)
- `n6` Nodo 6 · La galleria dei portatori
- `n7` Nodo 7 · Il magazzino del bottino (gabbia degli sciami)
- `n9` Nodo 9 · Il recinto dei prigionieri (sbarre, gabbia di Kem)
- `a3` Atto 3 · L'assalto alla Grotta della Gloria
- `a4` Atto 4 · Il Pozzo e la Macchina

### L'Esame di Rango C (Torre Sommersa di Verdaluce)

- `carovana` Atto 1 · La carovana (bosco, alleati da proteggere)
- `atrio` Atto 2 · L'Atrio degli Eroi (sala rotonda con le statue)
- `forzieri` Atto 2 · La Sala dei Forzieri (mimic sulla pedana)
- `ponte` Atto 2 · Il Ponte sull'Abisso (voragine)
- `nucleo` Atto 3 · Il Nucleo di Smeraldo (lago, Virydrax in riserva)
- `rovine` Atto 3 · Le rovine (variante se il dungeon esplode)

### Il Risveglio di Kem

- `campo` Scena 3 · L'assalto al campo (deserto di notte, sabbia, fuoco)
- `custodi` Scena 4 · La Sala dei Custodi (buia, sabbia e cornicioni)
- `sepolcreto` Scena 5 · L'imboscata nel sepolcreto (buia, sarcofagi, breccia)

### Altre mappe

- `vuota` Stanza vuota 20×14

Ogni mappa può definire `spawns` (posizioni di partenza per ruolo, in base al nome del nemico) e `marks` (etichette; quelle «solo master» sono viola).

## Caselle per esterni e voragini

Aggiunte per l'Esame, non cambiano le mappe precedenti: `q` erba, `f` sottobosco (terreno difficile), `A` albero (blocca passo e vista), `v` voragine (blocca il passo a PG e alleati; i nemici, che lì sono tutti volanti, possono sorvolarla), `N` gemma del Nucleo (blocca passo e vista).

## Caselle del deserto e delle tombe

Aggiunte per il Risveglio di Kem: `s` sabbia (terreno difficile), `Z` sarcofago (blocca il passo, non la vista), `F` fuoco da campo (blocca il passo, non la vista).
