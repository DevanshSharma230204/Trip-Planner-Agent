# 🌍 Pathfinder: AI Multi-Agent Trip Planner

## 📖 Overview
Pathfinder is a Multi-Agent System designed to solve the fatigue of travel planning. By coordinating specialized agents (Hotels, Activities, Routing), it builds personalized itineraries using **Google Gemini 2.0** for reasoning and **Google Maps/Places API** for factual data.

## 🏗️ Architecture
This solution implements an **Orchestrator-Workers** pattern:
1.  **TripPlannerOrchestrator:** The main controller that manages user session state and delegates tasks.
2.  **HotelsAgent:** Uses `google_places_search` to find accommodation matching user budget and style.
3.  **ActivitiesAgent:** Generates day-by-day plans based on user interest tags (e.g., "nightlife", "history").
4.  **RoutingAgent:** Reviews the itinerary to ensure logistical flow.

## 🔑 Key Features
* **Grounded Reality:** Uses Google Places API tools so it doesn't hallucinate fake hotels.
* **Contextual Memory:** Remembers user preferences (Budget, Pace, Interests) explicitly via `TripSessionState`.
* **Structured Output:** Returns clean Markdown itineraries.

## 🚀 How to Run
1.  **Secrets:** Ensure you have a valid `GOOGLE_API_KEY` stored in Kaggle Secrets (Add-ons -> Secrets).
2.  **Install:** Run Cell 1 to install `google-genai`.
3.  **Run All:** Execute all cells to initialize the agents.
4.  **Interact:** Scroll to the final cell (`chat_loop_simple`) to plan your trip interactively!
