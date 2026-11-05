# Mappa di battaglia

Mappa tattica per le one-shot della Gilda di Boar Tail: il master apre la battaglia dallo schermo del master, i giocatori entrano dal telefono con il codice della stanza o il QR, muovono il proprio personaggio entro la sua velocità e vedono solo ciò che vede.

- `index.html`: tutta l'applicazione, nessuna dipendenza da installare.
- Le mappe sono nell'oggetto `MAPS` in cima allo script.
- I telefoni si collegano direttamente al dispositivo del master (WebRTC, tramite il servizio pubblico PeerJS): serve internet. Master e vista tavolo locale funzionano anche offline.

## Punti di fuga (nodo 3)

Le caselle `X` sono buchi nel muro. Solo i nemici possono entrarci: chi ci arriva esce dalla mappa. Ogni nemico ha il suo numero di uscita (badge giallo, visibile solo al master). I giocatori non vedono i buchi finché il master non li rivela dal pannello «Punti di fuga» (per esempio dopo una prova di Saggezza (Percezione) CD 15). Sulle mappe buie c'è il pulsante «Torcia».
