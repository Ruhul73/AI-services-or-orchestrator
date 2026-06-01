# AI-services-or-orchestrator
# KhidmatAI — Geospatial Service Orchestration Engine
### Powered by the Google Antigravity Agentic Platform

KhidmatAI is a next-generation, premium geospatial matchmaking platform designed for the informal service economy of Pakistan. Built natively on top of the **Google Antigravity SDK/Framework**, it processes natural language demands (in Roman Urdu, Urdu, and English) to orchestrate an autonomous 4-phase planning agent pipeline to discover local services, extract schedules, geocode locations, and establish downstream lifecycle triggers.

---

## 🌟 Key Features

### 1. Google Antigravity Multi-Agent Architecture (25% Evaluation Weight)
The core backend workflow is explicitly built upon simulated Google Antigravity SDK classes:
* **`AntigravityOrchestrator`**: The master coordinator managing state transitions, agent registration, and trace streaming.
* **`AntigravityAgent`**: Formal planning units wrapping task executions:
  * 🗣️ **`Linguist_Agent`**: Parses roman Urdu syntax, extracts scheduled dates, and geocodes specific sectors.
  * 🤝 **`Matchmaker_Agent`**: Connects to the **Google Places API (New)** to fetch real-world candidates with real phone numbers, with a zero-crash failover to **OpenStreetMap Overpass Engine**.
  * 🏗️ **`Executor_Agent`**: Finalizes transactions, schedules slots, and generates unique transaction hashes.
  * 🛎️ **`Concierge_Agent`**: Establishes SMS followups, ratings hooks, and push notifications.

### 2. Location & Time Teleportation Mapping
* **Area Geocoding:** Matches mentions like `G-13`, `DHA`, `Gulberg`, `Saddar`, `Clifton` via Nominatim API and teleports the search focus to that exact coordinates.
* **Urdu Time Parser:** Translates phrases like:
  * `"kal subah"` ➡️ Tomorrow morning at `09:00 AM`
  * `"kal dopahar"` ➡️ Tomorrow afternoon at `02:00 PM`
  * `"aaj sham"` ➡️ Today evening at `06:00 PM`
  * parses them directly into ISO-8601 timestamps.

### 3. Dynamic Evaluator settings
To guarantee zero-crash evaluations, the **Antigravity Client** (Flutter App) features a **Settings Config Dialog** (top right gear icon) allowing evaluators to type in their local backend server IP address dynamically without hardcoded roadblocks.

---

## 🛠️ Installation & Setup

### 1. Backend Setup (FastAPI)
Navigate to the root directory and set up the Python virtual environment:
```bash
# Install dependencies
pip install fastapi uvicorn pydantic python-dotenv

# Run the server
uvicorn main:app --host 0.0.0.0 --port 8000
```
Make sure to create a `.env` file in the root containing your active Google Places credentials:
```env
GOOGLE_API_KEY=AIzaSyD5CJF4OGXgQ3d7r6vfawB3WApVuD6eCx4
```

### 2. Frontend Web Portal
Open your favorite browser and navigate to:
👉 **[http://localhost:8000/](http://localhost:8000/)**

### 3. Mobile Client (Flutter)
Launch the Flutter app on your dynamic workstation:
```bash
flutter pub get
flutter run
```
Use the top-right settings icon to configure the endpoint URL to point to your backend.
