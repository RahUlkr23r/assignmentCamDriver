# 🚗 Fleet Monitoring Dashboard

A **real-time fleet monitoring dashboard** that simulates dashcam events (speeding, harsh braking, drowsiness) and displays live data on an interactive dashboard. Built with **Node.js**, **Express**, **Socket.IO**, **MySQL**, and vanilla **HTML/CSS/JavaScript**.

---

## 📌 Features

- 🚘 **Real-time vehicle monitoring** – Live updates via WebSockets
- 📹 **Dashcam event simulation** – Automatic event generation every 3 seconds
- 🔌 **WebSocket communication** – Instant data push to dashboard
- 📊 **Interactive dashboard UI** – Stats cards, alerts, charts, and events table
- ⚡ **Backend API** – REST endpoints for data ingestion and retrieval
- 🎨 **Clean, responsive design** – Glass-morphism UI with smooth animations

---

## 🛠 Tech Stack

### Frontend
| Technology | Purpose |
|------------|---------|
| HTML5 | Structure |
| CSS3 | Styling & animations |
| JavaScript (ES6) | Interactivity |
| Socket.IO Client | Real-time communication |
| Chart.js | Data visualization |
| Font Awesome | Icons |

### Backend
| Technology | Purpose |
|------------|---------|
| Node.js | Runtime environment |
| Express.js | REST API framework |
| Socket.IO | WebSocket server |
| MySQL | Database |
| Sequelize | ORM for MySQL |
| Axios | HTTP client for simulator |

---

## 🎥 Demo Video

### Watch the live demo:





---

## 📂 Project Structure
fleet-monitoring_assignment/
│
├── backend/
│ ├── config/
│ │ └── db.js # Database connection
│ ├── models/
│ │ ├── Trip.js # Trip model
│ │ └── Event.js # Event model
│ ├── routes/
│ │ └── api.js # REST API endpoints
│ ├── sockets/
│ │ └── socketHandler.js # WebSocket handlers
│ ├── simulator/
│ │ └── eventSimulator.js # Event generator
│ ├── server.js # Main server file
│ ├── package.json
│ └── .env # Environment variables
│
├── frontend/
│ ├── css/
│ │ └── style.css # All styles
│ ├── js/
│ │ └── dashboard.js # Frontend logic
│ ├── index.html # Main dashboard
│ └── dashcam.mp4 # Sample video (optional)
│
├── demo.mp4 # Demo video recording
└── README.md # This file

text

---

## ⚙ Installation

### Prerequisites
- [Node.js](https://nodejs.org/) (v16 or later)
- [MySQL](https://dev.mysql.com/downloads/) (v8 or later)
- Git (optional)

### Step 1: Clone the Repository
```bash
git clone https://github.com/RahUlkr23r/assignmentCamDriver.git
cd fleet-monitoring_assignment
Step 2: Set Up the Database
Open MySQL and create a database:

sql
CREATE DATABASE fleet_monitoring;
Step 3: Configure Environment Variables
Create a .env file inside the backend folder:

ini
PORT=5000
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=yourpassword
DB_NAME=fleet_monitoring
Step 4: Install Backend Dependencies
bash
cd backend
npm install
Step 5: Start the Backend Server
bash
node server.js
Expected output:

text
✅ Database synced
✅ Server running on port 5000
✅ Event simulation started (every 3s)
Step 6: Serve the Frontend
Open a new terminal and run:

bash
cd frontend
npx live-server .
The dashboard will open at http://localhost:8080.

📊 Simulation Logic
Event generation: Every 3 seconds

Event types: speeding, harsh_braking, drowsiness

Speeding range: 60–110 km/h

Risk score calculation:

Base increase: +5 per violation

Extra +10 for speeding >80 km/h

Red alert: Triggered when speed exceeds 80 km/h

📡 API Documentation
Base URL: http://localhost:5000/api

Method	Endpoint	Description	Request Body	Response
GET	/stats	Get current stats	–	{ totalTrips, liveDrivers, violationCount, avgRiskScore }
GET	/events/recent	Get last 10 events	–	Array of event objects
POST	/events	Ingest new event	{ type, speed, details }	Created event
🧪 Testing the Application
Backend: Visit http://localhost:5000/api/stats in browser

Frontend: Open http://localhost:8080

Real-time updates: Watch alerts appear every 3 seconds

Database: Check MySQL tables trips and events

🎥 Demo Video Recording
I've included a demo video (demo.mp4) in this repository showing:

Starting the backend server

Launching the frontend dashboard

Real-time events appearing (alerts, stats, charts updating)

Red alert for speeding >80 km/h

Risk score increasing after multiple violations

📝 License
This project is for demonstration purposes only, created as part of a technical assignment.

👨‍💻 Author
Rahul Kumar Singh

GitHub: @RahUlkr23r
