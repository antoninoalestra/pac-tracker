# 📈 Trade Republic PAC Tracker Pro

Una web dashboard moderna, reattiva e minimale progettata in stile **Fintech Premium** (ispirata alla UI/UX di *Trade Republic*) per monitorare, analizzare e tracciare la crescita del proprio Piano di Accumulo Capitale (PAC) ed ETF in tempo reale.

![License](https://img.shields.io/badge/license-MIT-green.svg)
![Vanilla JS](https://img.shields.io/badge/JavaScript-ES6+-yellow.svg)
![HTML5](https://img.shields.io/badge/HTML5-CSS3-blue.svg)
![Firebase](https://img.shields.io/badge/Firebase-RealtimeDB-orange.svg)
![Chart.js](https://img.shields.io/badge/Chart.js-v4.0-ff6384.svg)

---

## 🌟 Caratteristiche Principali

- 📱 **Design UI/UX Stile Trade Republic:** Tema scuro profondo (`#000000`), contrasti ad elevata leggibilità, card con angoli arrotondati, barra di navigazione fluttuante per mobile e layout desktop fluido.
- 📥 **Importazione CSV Trade Republic:** Parser integrato per importare direttamente l'estratto conto esportato da Trade Republic (estrazione automatica di acquisti/vendite, frazioni di quote, date, importi e mappatura ISIN).
- 🔄 **Prezzi di Mercato Live (Sincronizzazione Automatica):**
  - Integrazione nativa **Twelve Data API** con supporto CORS per GitHub Pages.
  - Ridondanza e fallback automatico tramite **Yahoo Finance / Stooq JSON Proxy**.
  - Sincronizzazione in background ogni **5 minuti** (modificabile).
- 🎯 **Allineamento Perfetto P&L Trade Republic:**
  - Possibilità di impostare il prezzo **Denaro (Bid) / Trade Republic** manualmente o per singolo asset.
  - Calcolo del *Totale Investito* basato esclusivamente sugli **asset attivi** in portafoglio, escludendo le posizioni chiuse per evitare distorsioni sul Profit/Loss globale.
- ☁️ **Sincronizzazione Ibrida (Cloud + Offline):**
  - **Firebase Realtime Database:** mantiene i dati sincronizzati su tutti i tuoi dispositivi (PC, Smartphone, Tablet).
  - **LocalStorage Fallback:** garantisce il funzionamento continuo e immediato anche in assenza di connessione internet.
- 📊 **Grafici Interattivi Avanzati (Chart.js):**
  - **Asset Allocation (%):** Grafico a ciambella con percentuali in evidenza.
  - **Andamento Mensile (€):** Grafico a barre con i versamenti suddivisi per mese.
  - **Profit / Loss per Asset (€):** Rendimento netto in euro generato da ciascuna posizione.
- 🛡️ **Zero Dipendenze di Build:** Realizzato interamente in **Vanilla JavaScript, HTML5 e CSS3**. Nessun passaggio di compilazione (`Node.js`, `npm` o `Webpack`) necessario.

---

## 🚀 Demo Live

Puoi testare l'applicazione direttamente online tramite GitHub Pages:

👉 **[Trade Republic PAC Tracker Pro Live](https://antoninoalestra.github.io/pac-tracker/)**

---

## 🛠️ Stack Tecnologico

- **Frontend:** HTML5, CSS3 Custom Properties (Flexbox/CSS Grid), ES6+ Vanilla JavaScript.
- **Grafici:** [Chart.js](https://www.chartjs.org/) + `chartjs-plugin-datalabels`.
- **Database Cloud:** [Firebase Realtime Database](https://firebase.google.com/).
- **API Finanziarie:** [Twelve Data API](https://twelvedata.com/) & [Yahoo Finance API via Proxy].
- **Hosting:** GitHub Pages.

---

## 💻 Installazione e Configurazione Locale

Poiché la dashboard è un'applicazione web lato client puramente statica, non richiede alcuna installazione di pacchetti.

### 1. Clona la repository
```bash
git clone [https://github.com/antoninoalestra/pac-tracker.git](https://github.com/antoninoalestra/pac-tracker.git)
cd pac-tracker
