# Portale Agenti UP Auto

## Struttura
```
portale-agenti/
├── index.html                  ← pagina principale
├── netlify.toml                ← configurazione Netlify
├── netlify/
│   └── functions/
│       └── chat.js             ← proxy API Anthropic
└── docs/                       ← metti qui tutti i PDF Ayvens
    ├── MLA_Consumer_Ayvens_2025.pdf
    ├── MLA_Business_Ayvens_2025.pdf
    ├── Informazioni_precontrattuali.pdf
    ├── Ayvens_Guidastatouso_Ayvens_Autoveicoli_2507.pdf
    ├── Ayvens_La_Limitazione_di_responsabilita_per_danni.pdf
    ├── Ayvens_Condizioni_Generali_Fuel_Card_02_2026.pdf
    ├── AYVENS_INFORMATIVA_SCORING_SIC.pdf
    ├── ALL_A_Designazione_resp_Cliente_Targa_2025.pdf
    ├── DPA_Pro_Controller_Ayvens_Fleet_Management_2025.pdf
    ├── Ayvens_Dichiarazione_Guida_Stato_DUso__2025_07_Ayvens.pdf
    ├── Mod_Serv_Agg.pdf
    └── Modulo_SEPA.pdf
```

## Deploy su Netlify

### 1. Crea il repo GitHub
- Crea nuovo repo privato su GitHub (es. `up-auto-portale-agenti`)
- Carica tutti i file mantenendo la struttura cartelle
- Metti i PDF nella cartella `docs/`

### 2. Connetti a Netlify
- Vai su app.netlify.com
- "Add new site" → "Import from Git" → seleziona il repo

### 3. Aggiungi la variabile d'ambiente
- In Netlify: Site Settings → Environment Variables
- Aggiungi: `ANTHROPIC_API_KEY` = la tua chiave API Anthropic

### 4. Deploy
- Netlify fa il deploy automatico
- Vai in Domain Settings e aggiungi il sottodominio `agenti.noleggioupauto.it`
- Su Internet.bs aggiungi CNAME: `agenti` → `[tuo-sito].netlify.app`

## PIN di accesso
`upauto` (modificabile nel file index.html)
