# Mappa di battaglia

Mappa tattica per le one-shot della Gilda di Boar Tail: il master apre la battaglia dallo schermo del master, i giocatori entrano dal telefono con il codice della stanza o il QR, muovono il proprio personaggio entro la sua velocità e vedono solo ciò che vede.

- `index.html`: tutta l'applicazione, nessuna dipendenza da installare.
- Le mappe sono nell'oggetto `MAPS` in cima allo script.
- I telefoni si collegano direttamente al dispositivo del master (WebRTC, tramite il servizio pubblico PeerJS): serve internet. Master e vista tavolo locale funzionano anche offline.
