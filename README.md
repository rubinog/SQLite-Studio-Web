# 🗄️ SQLite Studio Web

> Un explorer e visualizzatore per database **SQLite (`.db`, `.sqlite`, `.sqlite3`)** leggero, moderno e 100% client-side, eseguito direttamente nel browser grazie a **WebAssembly (`sql.js`)**. Nessun backend, nessun server e nessun dato inviato all'esterno.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![SQLite](https://img.shields.io/badge/SQLite-WebAssembly-orange.svg)](https://sql.js.org/)
[![TailwindCSS](https://img.shields.io/badge/TailwindCSS-v3-38bdf8.svg)](https://tailwindcss.com/)

---

## ✨ Funzionalità Principali

- 🔒 **100% Privacy & In-Memory:** I tuoi file `.db` non lasciano mai il dispositivo. L'elaborazione, le query e le modifiche avvengono interamente all'interno del browser.
- 📂 **Caricamento Semplice:**
  - Drag & Drop immediato di file `.db`, `.sqlite`, `.sqlite3`.
  - File picker tradizionale.
  - Creazione rapida di un nuovo database vuoto.
  - Generazione di un database dimostrativo ("Demo DB") con tabelle relazionate già popolate.
- 🧭 **Schema Explorer & Navigazione:**
  - Elenco automatico di tabelle e viste con conteggio righe in tempo reale.
  - Filtro di ricerca per navigare schemi complessi.
  - Visualizzatore delle istruzioni DDL (`CREATE TABLE ...`) con copia rapida negli appunti.
- 📊 **Visualizzazione & Manipolazione Dati (CRUD):**
  - Griglia dati con paginazione configurabile (25, 50, 100, 500 righe per pagina).
  - Ricerca istantanea su tutti i campi della tabella.
  - **Aggiunta e Modifica di Record** tramite form generati dinamicamente dai tipi colonna con supporto per valori `NULL` e chiavi autoincrementanti.
  - **Cancellazione righe** sicura tramite `rowid`.
  - **Creazione e Drop visuale delle tabelle** senza scrivere codice a mano.
- 💻 **SQL Console Avanzata:**
  - Esecutore di query arbitrarie (`SELECT`, `INSERT`, `UPDATE`, `ALTER`, `JOIN`, ecc.).
  - Esecuzione rapida con scorciatoia `Ctrl + Invio` (o `Cmd + Invio`).
  - Misurazione del tempo di esecuzione in millisecondi.
  - Cronologia delle ultime query eseguite.
- 💾 **Esportazione Completa:**
  - Esportazione del binario SQLite aggiornato (`.db`) pronto per essere riutilizzato su qualsiasi applicazione desktop, server o mobile.
  - Esportazione delle singole tabelle in formato **CSV** e **JSON**.
- 🎨 **Interfaccia Utente:**
  - Design curato con supporto per **Dark/Light Mode**.
  - Icone vettoriali [Lucide](https://lucide.dev/).
  - Feedback visivo tramite toast notification e dialog di conferma.

---

## 🛠️ Stack Tecnologico

- **[sql.js](https://sql.js.org/)**: Porting di SQLite in C compilato in WebAssembly (WASM).
- **HTML5 & Vanilla JavaScript**: Nessun framework pesante, massima reattività e zero overhead di build.
- **[Tailwind CSS](https://tailwindcss.com/)**: Styling e design responsivo.
- **[Lucide Icons](https://lucide.dev/)**: Set di icone pulito e scalabile.

---

## 🚀 Come Utilizzarlo

Poiché l'applicazione è contenuta in un singolo file HTML autonomo, non richiede installazioni, configurazioni complesse o Node.js.

### Opzione 1: Esecuzione Locale Diretta
1. Clona la repository:
   ```bash
   git clone https://github.com/tuo-username/sqlite-studio-web.git
   cd sqlite-studio-web
   ```
2. Apri direttamente il file `index.html` in un qualsiasi browser moderno:
   - Su macOS: `open index.html`
   - Su Linux: `xdg-open index.html`
   - Su Windows: fai doppio clic su `index.html` o usa `start index.html`

### Opzione 2: Con un semplice server locale (consigliato per WASM)
Sebbene `sql.js` funzioni via CDN, alcuni browser restringono determinate API sui file aperti tramite protocollo `file://`. Puoi avviare un server web locale con una sola riga:

- **Con Python 3:**
  ```bash
  python3 -m http.server 8080
  ```
- **Con Node (npx):**
  ```bash
  npx serve .
  ```
- **Con estensioni per editor:** Usa estensioni come *Live Server* su VS Code.

Apri quindi `http://localhost:8080` nel browser.

---

## 📖 Guida Rapida

1. **Aprire un database:** Trascina un file `.db` all'interno della finestra oppure clicca sul pulsante **"Apri DB"** nella barra superiore.
2. **Esplorare una tabella:** Clicca sul nome della tabella nella sidebar a sinistra.
3. **Modificare o aggiungere dati:** Usa il pulsante **"Nuovo Record"** in alto a destra oppure le icone di modifica (✏️) ed eliminazione (🗑️) presenti su ciascuna riga.
4. **Eseguire query SQL:** Clicca sulla scheda **"SQL Console"**, digita la query e premi `Ctrl + Invio`.
5. **Salvare le modifiche:** Fai clic sul pulsante verde **"Salva / Esporta DB"** per scaricare la versione aggiornata del file `.db` sul tuo disco locale.

---

## 📁 Struttura del Progetto

```text
sqlite-studio-web/
├── index.html       # Applicazione completa (UI, logica ed engine WASM)
├── README.md        # Documentazione del progetto
└── LICENSE          # Licenza open-source (MIT)
```

---

## 🤝 Contribuire

I contributi sono sempre benvenuti!
1. Fai un **Fork** del progetto.
2. Crea un branch per la tua feature (`git checkout -b feature/NuovaFunzionalita`).
3. Effettua un commit delle tue modifiche (`git commit -m 'Aggiunta nuova funzionalità'`).
4. Esegui il push sul tuo branch (`git push origin feature/NuovaFunzionalita`).
5. Apri una **Pull Request**.

---

## 📄 Licenza

Questo progetto è distribuito sotto licenza **MIT**. Consulta il file `LICENSE` per maggiori dettagli.