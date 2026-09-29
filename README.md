# Recall — Autonomous AI Procurement Agent

Recall is an AI-powered negotiation assistant that preserves institutional procurement knowledge across quarters using persistent agent memory.

Powered by [Hindsight](https://github.com/vectorize-io/hindsight) for long-term memory and Groq for high-speed LLM reasoning.

---

## Architecture & Features

- **Persistent Memory Bank:** Tracks vendor price shifts, delivery disputes, and counter-tactics over time via Hindsight retain/recall APIs.
- **Dual-Column Telemetry UI:** Displays tactical briefings side-by-side with the raw recalled memory records to verify provenance.
- **Grounded Playbooks:** Restricts inference strictly to verified historical vendor events to eliminate hallucinated concessions.

---

## Quick Start

### 1. Clone & install dependencies
```bash
git clone https://github.com/hardikraoaiare/procurement-memory.git
cd procurement-memory
pip install -r requirements.txt asgiref
```

### 2. Configure credentials
Create a `.env` file in the root directory:
```env
HINDSIGHT_API_KEY=your_hindsight_key
HINDSIGHT_BANK_ID=procurement-agent
GROQ_API_KEY=your_groq_key
```

### 3. Ingest vendor memory bank
```bash
python ingest_vendor_data.py
```

### 4. Launch the dashboard
```bash
python server.py
```
Open `http://127.0.0.1:5000` in your web browser.
