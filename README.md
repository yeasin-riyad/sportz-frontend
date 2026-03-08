# 🏟️ Sportz App

**Sportz** is a real-time sports management and tracking application built with **React (Vite)** for the frontend and **Express + Node.js** for the backend. It provides live match updates, commentary, team management, and seamless WebSocket integration for real-time notifications. The app also uses **ArcJet** for security and bot protection.

---

## 🚀 Features

### 🔹 Real-time Live Commentary
- View minute-by-minute commentary of ongoing matches.
- Subscribe/unsubscribe to specific matches using WebSocket connections.
- Automatic updates with WebSocket reconnect and exponential backoff.

### 🔹 Match Management
- HR managers can add, update, and manage matches.
- Track match scores, periods, and events.

### 🔹 Team Management
- Create and manage teams.
- Add or remove team members dynamically.

### 🔹 Asset & Request Management
- Employees can request sports assets (e.g., jerseys, equipment).
- HR managers can approve/reject requests and view limited stock items.
- Dashboard with top requested and returnable/non-returnable items.

### 🔹 Security & Bot Protection
- **ArcJet** integration protects the API and WebSocket from bots and abusive requests.
- Rate limiting, threat detection, and automatic blocking of suspicious traffic.
- Ensures only legitimate users can access sensitive match data and live commentary.

### 🔹 Notifications & Alerts
- Live updates for match commentary.
- Alerts for pending requests or changes in asset availability.

### 🔹 Responsive & Dark Mode Support
- Mobile, tablet, and desktop support.
- Beautiful UI with light and dark mode options.

---

## 🛠️ Tech Stack

| Layer        | Technology                                                                 |
| ------------ | -------------------------------------------------------------------------- |
| Frontend     | React + Vite, Tailwind CSS, TypeScript                                     |
| Backend      | Node.js, Express, WebSocket (ws), ArcJet Security                          |
| Database     | PostgreSQL, Drizzle ORM                                                    |
| Deployment   | Vercel (Frontend), Railway (Backend)                                       |
| Real-time    | WebSocket (Subscribe to match updates and commentary)                      |
| Monitoring   | Site24x7 / AppMon for APM monitoring                                       |

---

## 🔐 ArcJet Integration

### Backend
- Protect REST API endpoints using **ArcJet** middleware:

```js
import { securityMiddleware } from './arcjet.js';
app.use(securityMiddleware());