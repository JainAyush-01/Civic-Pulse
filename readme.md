# AI City Scanner: Cascading Risk Ontology Engine

> **"India does not have a data shortage. It has a data blindness problem."**

The **Cascading Risk Ontology Engine** is an enterprise-grade AI and Knowledge Graph platform built to eliminate governance blind spots. It ingests disconnected public datasets (Health, Environment, Infrastructure) and unstructured live news, mapping the "domino effect" of local crises before they happen.

---

## The Problem: Data Blindness
India's public datasets hold every signal needed to predict a crisis, yet policymakers often act only after the catastrophe has arrived. The compounding failures are:
1. **No Integration:** Datasets (Health, Weather, Crime) never communicate across departments.
2. **False Averages:** State-level statistics mask district-level collapse. A failing region looks "stable" on a state dashboard.
3. **Deceptive Metrics:** Governments count physical hospital buildings, not working doctors. A district with 10 hospitals may still have a lethal 1-to-25,000 doctor-to-patient ratio.

*Example:* Water quality deteriorates -> Diarrhea cases rise -> Hospitals get overwhelmed due to a hidden lack of pediatricians -> Public panic ensues. 

---

## Our Solution: Precision Policy in One Click
We replace stale bureaucratic reporting with a **Predictive Spatiotemporal Architecture**.

* **Predictive AI Engine (XGBoost):** A custom Machine Learning model trained on 15 years of historical EpiClim data. It mathematically forecasts disease volume based on live weather, water toxicity, and immunization shields.
* **Causal Knowledge Graph (Neo4j):** We cross-link datasets to map the "domino effect." It connects environmental triggers (AQI/Rain) to health outcomes and infrastructure limits.
* **Deceptive Surplus Elimination:** We run "Real-Time Load Analytics." We evaluate the WHO Standard (1 Doctor per 1,000 people) against predicted outbreak surges to expose hidden critical manpower shortages.
* **Real-Time NLP Radar (spaCy):** We use Natural Language Processing to scan local news and unstructured public panic, converting them into structured Government Alerts.
* **Geospatial Spillover:** If a district's healthcare system collapses, the AI calculates the GPS distance to the nearest city and simulates the patient overflow (The Domino Effect).

---

## Tech Stack
* **Frontend:** React.js, Tailwind CSS (MERN Stack Architecture)
* **AI/ML API:** FastAPI, Python, Uvicorn
* **Machine Learning:** XGBoost, Scikit-Learn, Pandas
* **NLP (Natural Language Processing):** spaCy, NewsAPI
* **Ontology/Database:** Neo4j AuraDB (Graph Database)

---

## Project Structure
```text
Inovate_Hackathon/
├── ai_engine/                 # Python/FastAPI Microservice
│   ├── data/                  # Synthesized & Cleaned CSV Datasets
│   ├── models/                # Serialized XGBoost Brain (.json) & Encoders
│   ├── main.py                # FastAPI Gateway
│   ├── logic_engine.py        # ML Prediction & Geospatial Spillover Logic
│   ├── nlp_scanner.py         # Real-time News Scraping & NLP extraction
│   └── graph_db.py            # Neo4j Cypher Query Manager
├── client/                    # React Frontend
└── README.md
```

---

## How to Run the AI Backend Locally

**1. Install Dependencies**
Navigate to the `ai_engine` directory and install the required Python libraries:
```bash
cd ai_engine
pip install fastapi uvicorn pandas numpy scikit-learn xgboost fuzzywuzzy python-Levenshtein spacy requests neo4j python-dotenv
python -m spacy download en_core_web_sm
```

**2. Environment Variables**
Create a `.env` file inside the `ai_engine` folder and add your credentials:
```ini
NEO4J_URI=neo4j+s://<your-instance>.databases.neo4j.io
NEO4J_USER=neo4j
NEO4J_PASSWORD=<your_neo4j_password>
NEWS_API_KEY=<your_newsapi_key>
```

**3. Start the FastAPI Server**
```bash
uvicorn main:app --host 0.0.0.0 --port 8001 --reload
```
*The AI Engine will now be running at http://localhost:8001.*

---

## API Documentation

### 1. GET /news/{district}
Scans the live internet for news regarding the district, extracts entities, and maps them to our Knowledge Graph Ontology.
* **Response:** JSON containing scanned articles, trending topics, and hidden problems detected.

### 2. POST /predict
Runs the Omega ML Simulation. Ingests weather conditions, predicts the exact case volume of a disease, calculates hospital bed deficit, and checks for "Deceptive Surplus" manpower failure.
* **Payload:** `{"district": "Leh", "month": 7, "rain": 50.0, "temp": 18.0, "lai": 0.5, "disease": "Acute Diarrhoeal Disease"}`
* **Response:** JSON containing infection rates, capacity status, AI X-Ray reasoning, and GPS spillover targets.

### 3. GET /dashboard/{district}
The "One-Click" endpoint for the React Map. Fetches the completely unified Graph Ontology directly from Neo4j (Combining NLP + ML + Infrastructure).