Piattaforma Torrent – README
📌 Descrizione del progetto

La piattaforma permette agli utenti di condividere e scaricare file torrent. Ogni torrent può avere titolo, descrizione, dimensione, categorie, immagini e commenti con valutazioni.

Gli utenti registrati possono caricare torrent, scaricare file, lasciare commenti e valutazioni. I moderatori e amministratori hanno permessi avanzati per gestire contenuti e utenti.

⚙️ Tecnologie utilizzate

Backend: Node.js, Express, MongoDB, Mongoose, JWT, bcryptjs

Frontend: HTML, CSS, JavaScript

Gestione pacchetti: npm

Database: MongoDB Atlas o locale

Autenticazione: JSON Web Token (JWT)

🗂 Struttura progetto
torrent-platform/
├── backend/
│   ├── app.js                  # Server principale
│   ├── config/
│   │   └── db.js               # Connessione MongoDB
│   ├── models/
│   │   ├── User.js
│   │   ├── Torrent.js
│   │   └── Download.js
│   ├── routes/
│   │   ├── users.js
│   │   ├── torrents.js
│   │   ├── reviews.js
│   │   └── downloads.js
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
├── package.json
└── .env

⚡ Funzionalità principali
Backend

API REST per:

Registrazione e login utenti

Upload e gestione torrent

Aggiunta/modifica/cancellazione commenti

Registrazione download

Autenticazione JWT per utenti registrati

Ruoli: user, moderator, admin

Frontend

Interfaccia web con:

Registrazione e login

Ricerca torrent per titolo o descrizione

Visualizzazione dettagli torrent

Inserimento commenti e valutazioni

Scaricamento torrent

🗃 Database

MongoDB con le seguenti collezioni:

Collezione	Contenuto
users	Dati utenti (username, email, password hash, ruolo)
torrents	Dati torrent (titolo, descrizione, dimensione, categorie, immagini, commenti, numero download)
downloads	Record download per utente e torrent

Connessione configurata in backend/config/db.js tramite .env:

MONGO_URI=<MongoDB connection string>
JWT_SECRET=<chiave segreta JWT>
PORT=5000

🚀 Avvio progetto
Backend

Apri terminale in backend/

Installa dipendenze:

npm install


Avvia server:

node app.js


Backend disponibile su http://localhost:5000/

Frontend

Apri frontend/index.html in un browser

Oppure servi tramite live-server o VSCode Live Preview

📄 Note progettuali

Backend e frontend sono separati per una struttura modulare.

JWT viene utilizzato per autenticazione e autorizzazione.

Tutti i nomi delle collezioni sono centralizzati in app.config (Node.js: file .env e modelli Mongoose).

I commenti e i download sono collegati ai rispettivi torrent e utenti tramite ID.

Frontend semplice per prototipo, ma facilmente estendibile con filtri avanzati, categorie multiple e ordinamento.
