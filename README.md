# 🎬 CineMatch – Motore di Raccomandazione ML per Film nei Cinema Locali

**CineMatch** è un sistema di raccomandazione basato su machine learning progettato per suggerire agli utenti i film più adatti in programmazione nei cinema vicini. Integra un modello di regressione per stimare la percentuale di match utente-film e un classificatore multilabel per consigliare i film migliori in base alle preferenze.

## 🚀 Caratteristiche
- 📊 Raccolta e parsing dei dataset IMDb ufficiali.
- 🧠 Regressione per il calcolo del match film-utente.
- 🎯 Classificazione multilabel per raccomandazioni personalizzate.
- 🌍 Integrazione con un sito web per mostrare suggerimenti in tempo reale.
- 🔌 API REST per predizione e raccomandazione film.

## 🛠 Setup rapido
1. Clona il progetto:
```bash
git clone https://github.com/Calisti-Daniele/CineMatch.git
cd CineMatch
````

2. Installa le dipendenze:

```bash
pip install -r requirements.txt
```

3. Scarica i dataset IMDb da [qui](https://datasets.imdbws.com/) e decomprimili nella cartella del progetto.

4. Genera `movies.csv`:

```bash
python build_movies_dataset.py
```

## 🧠 Modelli ML

* **Regressore** (XGBoost / MLP): predice la compatibilità utente-film.
* **Classificatore** (XGBoost / Neural Net): suggerisce top-N film.

## 📡 API REST (in arrivo)

* `GET /recommend?user_id=123`
* `GET /predict_match?user_id=123&movie_id=456`

## 📁 Struttura del progetto

```
CineMatch/
├── data/
│   └── [file IMDb decompressi]
├── build_movies_dataset.py
├── models/
│   └── train_model.py
├── api/
│   └── app.py
├── movies.csv
└── README.md
```

## 📄 Licenza

MIT – libero utilizzo per progetti personali o accademici. Per uso commerciale, contattare l’autore.

---

✨ *Creato con amore per gli amanti del cinema e del machine learning.*

