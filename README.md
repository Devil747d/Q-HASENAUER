# 🎯 Matrice di Eisenhower - Web App

Web Application single-file moderna, responsive e interattiva basata sui 4 quadranti della **Matrice di Eisenhower**:
- **Q1 (Crisi)**: *Urgente & Importante* &rarr; **Fare Subito**
- **Q2 (Qualità)**: *Importante, Non Urgente* &rarr; **Pianificare**
- **Q3 (Inganno)**: *Urgente, Non Importante* &rarr; **Delegare**
- **Q4 (Spreco)**: *Né Urgente né Importante* &rarr; **Eliminare**

---

## 🚀 Guida di Configurazione Rapida (3 Passaggi)

### 1. Esegui lo script SQL nel tuo Database Supabase
1. Accedi alla dashboard del tuo progetto su [supabase.com](https://supabase.com).
2. Nel menu laterale sinistro, fai clic sull'icona **SQL Editor**.
3. Clicca sul pulsante **New query**.
4. Apri il file [`supabase_schema.sql`](file:///e:/PROGETTI%20AI/QUADRANTE%20OSENHAUER/supabase_schema.sql), copia tutto il suo contenuto e incollalo nell'editor di Supabase.
5. Clicca sul pulsante verde **Run** in basso a destra.
   > Questo creerà la tabella `tasks`, gli indici di ricerca e attiverà la **Row Level Security (RLS)** che isola in totale sicurezza i dati di ogni utente registrato.

---

### 2. Recupera le tue credenziali Supabase
Nella dashboard del tuo progetto Supabase:
1. Vai su **Project Settings** (icona ingranaggio in basso a sinistra).
2. Nella sezione laterale, clicca su **API**.
3. Copia i due valori:
   - **Project URL** (es: `https://abcdefghijkl.supabase.co`)
   - **Project API keys** &rarr; copia la chiave **`anon` `public`** (stringa che inizia solitamente con `eyJhbGciOi...`).

*(Puoi anche incollare questi dati nel file [`.env.example`](file:///e:/PROGETTI%20AI/QUADRANTE%20OSENHAUER/.env.example) e salvarlo come `.env` per tuo promemoria personale)*.

---

### 3. Avvia e Usa l'Applicazione
1. Apri direttamente il file [`index.html`](file:///e:/PROGETTI%20AI/QUADRANTE%20OSENHAUER/index.html) con un qualsiasi browser (Chrome, Edge, Safari, Firefox).
2. Al primo avvio comparirà la finestra di configurazione: incolla il tuo **Project URL** e la tua **Anon Public Key**, poi clicca su **Salva e Connetti**.
3. Seleziona la scheda **Crea Account** e inserisci la tua email e una password (minimo 6 caratteri).
4. Fatto! Sarai immediatamente all'interno della tua Matrice di Eisenhower.

---

## 💡 Caratteristiche dell'Applicazione

- **Single-File Portatile**: Nessuna installazione Node.js o pacchetti `npm` richiesti. Tutto il codice (HTML5, Tailwind CSS, JavaScript e icone Lucide) risiede in [`index.html`](file:///e:/PROGETTI%20AI/QUADRANTE%20OSENHAUER/index.html).
- **Drag & Drop Nativo su Desktop**: Trascina le card delle attività direttamente da un quadrante all'altro.
- **Ottimizzato per Smartphone / Mobile**: 
  - Selettore rapido a tendina su ogni card per spostare l'attività tra i quadranti con un tocco.
  - Filtro per visualizzare un singolo quadrante alla volta o tutti e 4 insieme.
  - Pulsante galleggiante (+) per aggiungere attività al volo.
- **Autenticazione Cloud**: Ogni utente accede solo ed esclusivamente alle proprie attività, sincronizzate in tempo reale sul cloud di Supabase.
- **Stato e Scadenze**: Spunta di completamento per sbarrare le attività svolte, selettore di data di scadenza, modifica ed eliminazione rapida.
