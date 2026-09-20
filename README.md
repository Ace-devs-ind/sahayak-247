# SAHAYAK 24/7

**Smart Disaster Response Platform** — connecting citizens, rescue teams, and authorities during floods, earthquakes, fires, landslides, and building collapses.

> Built for **Smart India Hackathon 2026** | Problem Statement ID: **26206**

---

## 🎯 Problem

During disasters, people struggle to get quick emergency assistance. Rescue teams receive information late, exact locations are hard to find, and coordination between agencies breaks down. The result: delayed help, wasted resources, and preventable loss of life.

## 💡 Solution

SAHAYAK 24/7 is a serverless disaster response platform that lets citizens send **SOS alerts with live GPS location** in one tap. Authorities see every request on a **live command dashboard**, prioritized by severity and affected-zone intelligence from satellite data.

### Key Features
- 📍 One-tap SOS with automatic geolocation
- 🗺️ Live rescue dashboard with map view
- 🚨 Real-time alerts to responders
- 🧠 AI-based priority scoring
- 🛰️ Integration with ISRO/NRSC Earth-observation data (planned)
- 📱 Progressive Web App — works on low connectivity

---

## 🏗️ Architecture



### Tech Stack
| Layer | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript (PWA) |
| Maps | Leaflet.js |
| Database | Firebase Firestore |
| Hosting | Firebase Hosting |
| Alerts | Firebase Cloud Messaging *(planned)* |
| Satellite Data | ISRO / NRSC Earth Observation *(planned)* |

---

## 📅 Progress Log

### Day 1 — September 20, 2026
- ✅ Firebase project initialized (`resqtech-sahayak`)
- ✅ Firestore database configured (asia-south1 region)
- ✅ Citizen SOS interface built (`index.html`)
- ✅ Geolocation API integrated
- ✅ SOS data successfully written to Firestore

**Milestone:** End-to-end citizen → database pipeline working.

---

## 🚀 Getting Started

### Prerequisites
- A modern browser (Chrome/Edge)
- Python 3.x (for local development server)
- A Firebase account

### Run Locally
```bash
# Clone the repo
git clone https://github.com/<your-username>/sahayak-247.git
cd sahayak-247

# Start a local server
python -m http.server 8000