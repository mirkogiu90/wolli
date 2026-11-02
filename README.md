# WOLLI 0.1.0 — PWA locale

Versione iniziale funzionante: archivio documenti e allegati (immagini/PDF), cartelle, ricerca, preferiti, scadenze all'apertura (scaduti ed entro 30 giorni), visualizzazione, condivisione file, backup JSON completo e ripristino, uso offline dopo prima visita.

## Installazione su iPhone
1. Pubblicare **tutti** i file di questa cartella su un hosting statico HTTPS (per esempio GitHub Pages).
2. Aprire l'indirizzo in Safari su iPhone.
3. Condividi → Aggiungi alla schermata Home → WOLLI.

## Prova da PC
Da questa cartella eseguire `python -m http.server 8000`, quindi aprire `http://localhost:8000`.

## Limiti importanti
- I documenti sono salvati in IndexedDB **senza cifratura applicativa**. Non inserire documenti sensibili prima di valutare il rischio; il blocco del dispositivo resta essenziale.
- Il backup JSON contiene i documenti **in chiaro**: conservarlo solo in posizione protetta. Non inviarlo a terzi.
- Se iOS elimina i dati del sito o l'utente rimuove la web app, i documenti locali possono andare persi.
- Nessuna sincronizzazione, Face ID, notifiche push o server per documenti.
- Stampa: aprire/condividere il singolo allegato e usare la stampa di iOS; non è presente una stampa multipagina aggregata.
- Non sono ancora implementati scanner con ritaglio prospettico, OCR, codici a barre, sottocartelle, cestino o PDF multipagina generato nell'app. Previsti per versioni successive.
- Nessun test reale su iPhone è stato effettuato in questo ambiente.
