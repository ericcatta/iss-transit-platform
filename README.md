# 🚀 ISS Transit Platform

Trova automaticamente i transiti della **Stazione Spaziale Internazionale (ISS)** davanti al **Sole ☀️** o alla **Luna 🌙** vicino alla tua posizione e ricevi tutto direttamente su **Telegram**.

---

## 🧠 Cos'è

ISS Transit Platform è un sistema automatico che:

- usa GitHub Actions
- esegue calcoli astronomici con Python
- analizza ISS, Sole e Luna
- cerca transiti reali su un’area (fino a 40 km)
- invia notifiche su Telegram

---

## 🍴 Usa il progetto (fork)

Per usare questo bot devi prima copiarlo nel tuo account GitHub.

### Metodo consigliato

1. Clicca su **Fork** in alto a destra  
2. Seleziona il tuo account  
3. Attendi la creazione del repository  

👉 Ora hai una copia tua del progetto.

---

## ✨ Funzionalità

- 📡 Calcolo posizione ISS, Sole e Luna
- 🎯 Ricerca transiti reali (non solo passaggi)
- 🌍 Analisi su area (non solo punto singolo)
- ⏱ Precisione fino al secondo
- 📏 Durata del transito
- 🧭 Traiettoria sul disco (centro / interno / bordo)
- 📬 Notifica automatica su Telegram
- 📱 Web app con mappa e GPS

---

## 📁 Struttura

```
iss-transit-platform
├─ send_telegram.py
├─ config.json
├─ app/
│  └─ index.html
└─ .github/workflows/
   └─ daily.yml
```

---

## ⚙️ Setup (5 minuti)

### 1. 🤖 Crea bot Telegram

Su Telegram cerca:

`@BotFather`

Poi esegui:

`/newbot`

Salva il token → sarà `TELEGRAM_BOT_TOKEN`

---

### 2. 🆔 Ottieni chat ID

Apri nel browser:

`https://api.telegram.org/botTUO_TOKEN/getUpdates`

Cerca:

```json
"chat": {
  "id": 123456789
}
```

👉 quello è il tuo `TELEGRAM_CHAT_ID`

---

### 3. 🔐 GitHub Secrets

Nel tuo repository vai su:

**Settings → Secrets → Actions**

Aggiungi:

- `TELEGRAM_BOT_TOKEN`
- `TELEGRAM_CHAT_ID`

---

### 4. 📍 Configura posizione

Apri la web app:

`app/index.html`

Oppure tramite GitHub Pages.

Poi:

1. clicca sulla mappa o usa GPS  
2. premi **Genera config**  
3. premi **Copia**  
4. apri `config.json` su GitHub  
5. incolla  
6. commit  

---

## 🔧 config.json

Esempio:

```json
{
  "users": [
    {
      "lat": 46.2465,
      "lon": 9.0245,
      "radius_km": 40,
      "grid_step_km": 5,
      "search_hours": 24
    }
  ]
}
```

---

## ▶️ Avvio

### Manuale

Vai su:

**Actions → Run workflow**

---

### Automatico

Il bot parte ogni giorno:

```
cron: "0 5 * * *"
```

👉 circa:
- 07:00 estate  
- 06:00 inverno  

---

## 📬 Output Telegram

Riceverai ogni giorno:

- ✔ messaggio anche senza eventi  
- ✔ dettagli completi se ci sono transiti  

Esempio:

```
🔹 Evento
Oggetto: Sole
Tipo: centrale
Durata: 0.8 s
Distanza: 12 km
Mappa: link
```

---

## 🧭 Web App

Include:

- mappa interattiva  
- GPS automatico  
- copia config  
- download config.json  
- link diretto a GitHub  

---

## 🔐 Sicurezza

- nessun token nel codice  
- uso GitHub Secrets  
- nessun server  
- tutto gira su GitHub  

---

## 🧠 Note

- I transiti ISS sono rari  
- È normale ricevere “nessun evento”  
- Il sistema analizza una zona, non un punto  
- Precisione dipende dai dati TLE  

---

## 🚀 Roadmap

- miglioramento UI web app  
- visualizzazione area su mappa  
- multi-utente  
- app Mac  

---

## 🧾 In breve

> Un sistema automatico che trova transiti ISS reali  
> e li invia su Telegram  
> senza server e senza costi.

---

## 📜 Licenza

Progetto personale / astronomia amatorial
