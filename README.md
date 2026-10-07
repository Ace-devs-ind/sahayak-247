# SAHAYAK 24/7

Smart Disaster Response Platform - connecting citizens, rescue teams, and authorities during floods, earthquakes, fires, landslides, and building collapses.

Built for Smart India Hackathon 2026
Problem Statement ID: 26206
Theme: Disaster Management

---

## Live Demo

| Page | Link |
|---|---|
| Citizen SOS | https://resqtech-sahayak.web.app |
| Rescue Dashboard | https://resqtech-sahayak.web.app/dashboard.html |

Open both links. Send an SOS from your phone, watch responders dispatch on the dashboard in real time.

---

## The Problem

During disasters like floods, earthquakes, fires, landslides, and building collapses, people struggle to get help fast. Rescue teams receive information late, exact locations are unclear, and agencies fail to coordinate. The result is delayed response, wasted resources, and preventable loss of life.

## Our Solution

SAHAYAK 24/7 is a serverless, real-time disaster response platform. Citizens press one button to send an SOS with GPS location. Authorities see every request on a live command dashboard, prioritized by urgency, with automatic dispatch of the nearest responders.

---

## Key Features

- One-Tap SOS: Citizen sends location and disaster type in a single tap
- Live Dashboard: Real-time map updates as new SOS requests arrive
- Priority Scoring: Automatic urgency score based on severity, wait time, and status
- Multi-Responder Dispatch: Nearest ambulance, police, and fire truck dispatched simultaneously
- Road-Following Routes: Rescue vehicles follow actual roads, not straight lines
- 1km Affected Zone: Visual overlay around each SOS for situational awareness
- Audio Alerts: Command center beeps when a new SOS arrives
- Dispatch / Resolve Workflow: Track rescue lifecycle end to end
- Cross-Device: Works on phone and desktop, syncs instantly via Firestore

---

## System Architecture

Citizen (Web)  ---SOS--->  Firestore  ---live--->  Rescue Dashboard
                                |
                                +--> Priority Score
                                +--> Auto-Dispatch Nearest Responders
                                +--> Live Tracking with OSRM Routes

### Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML, CSS, vanilla JavaScript (ES modules) |
| Maps | Leaflet.js + OpenStreetMap tiles |
| Routing | OSRM (Open Source Routing Machine) |
| Database | Firebase Firestore (real-time listeners) |
| Hosting | Firebase Hosting |
| Alerts | Web Audio API |
| Satellite Data | ISRO / NRSC integration (planned) |

---

## Project Structure

sahayak-247/
  public/
    index.html          - Citizen SOS page
    dashboard.html      - Rescue command dashboard
    404.html            - Firebase default
  firebase.json         - Hosting config
  .firebaserc           - Project alias
  README.md

---

## Run Locally

Prerequisites:
- Python 3.x or Node.js
- A modern browser (Chrome or Edge)
- Internet connection for Firebase and map tiles

Steps:

    git clone https://github.com/Ace-devs-ind/sahayak-247.git
    cd sahayak-247
    python -m http.server 8000

Open in your browser:
- Citizen page: http://localhost:8000/index.html
- Dashboard: http://localhost:8000/dashboard.html

---

## Development Log

### Day 1 - September 20, 2026

- Firebase project initialized (resqtech-sahayak)
- Firestore database configured (asia-south1 region)
- Citizen SOS page with disaster-type selector and geolocation
- End-to-end pipeline: citizen to Firestore verified

### Day 2 - September 21 and October 7, 2026

- Live rescue dashboard built with Leaflet and real-time Firestore listener
- Priority scoring algorithm (severity x 10 + age x 5 + status x 5)
- Color-coded pins: red critical / orange medium / green low
- Dispatch and Resolve workflow with Firestore updates
- Audio alert on new SOS
- Auto-dispatch of nearest responders (ambulance, police, fire)
- Road-following routes via OSRM with dashed-line fallback
- 1km x 1km affected-zone overlay with dashed border and fill
- Emergency infrastructure seeded across 10 major Indian cities
- Deployed to Firebase Hosting with public live URL

---

## Roadmap

Completed:
- Citizen SOS with geolocation
- Firestore real-time backend
- Live rescue dashboard
- Priority scoring
- Multi-responder auto-dispatch
- Road-following routes (OSRM)
- 1km affected-zone overlay
- Firebase Hosting deployment

Planned:
- ISRO / NRSC satellite data integration
- SMS fallback for offline scenarios
- PWA with offline caching
- Multi-language support (Hindi, Tamil, Bengali)
- Role-based auth for responders

---

## Current Limitations

- Station data is seeded: 31 emergency facilities across 10 Indian cities are hardcoded for the prototype. Production will integrate live municipal databases.
- Real satellite overlays pending: ISRO/NRSC integration requires authorized data access.
- No authentication yet: required before any real-world deployment.
- Firestore rules are open: acceptable for hackathon demo only.

---

## Team ResQTech

Name: Abhinav
Role: Full-stack development

Team ID: (to be assigned)

---

## License

This project is built for Smart India Hackathon 2026. All rights reserved by Team ResQTech.