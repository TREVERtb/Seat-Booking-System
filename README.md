# Seat Booking System 🎟️

A premium, full-stack seat booking application that demonstrates real-world booking scenarios with backend validation and concurrent request handling.

## ✨ Features

- **Atomic Transactions**: Prevents double-booking using SQLite transactions.
- **Single Source of Truth**: The database is the final authority on seat availability.
- **Premium UI**: Modern dark theme with glassmorphism and real-time status updates.
- **Real-time Feedback**: Instant success/error notifications for booking actions.
- **Adaptive Layout**: Responsive grid that scales to 50 seats (A1-E10).

## 🚀 Getting Started

### Prerequisites

- Node.js (v18+)
- npm

### Installation

1. **Clone the repository** (or just navigate to the folder).
2. **Install Server Dependencies**:
   ```bash
   cd server
   npm install
   ```
3. **Install Client Dependencies**:
   ```bash
   cd client
   npm install
   ```

### Running the Application

1. **Start the Backend Server**:
   ```bash
   cd server
   npm run dev
   ```
   The server will run on `http://localhost:5000`.

2. **Start the Frontend Client**:
   ```bash
   cd client
   npm run dev
   ```
   The client will typically run on `http://localhost:5173`.

## 🛠️ Tech Stack

- **Frontend**: React, Vite, Vanilla CSS
- **Backend**: Express.js, better-sqlite3
- **Database**: SQLite (local `booking.db`)

## 🔒 Security & Data Integrity

- The system uses **Database Transactions** to ensure that checking a seat's status and updating it happens atomically.
- If two users try to book the same seat at the exact same millisecond, only one will succeed; the other will receive a "Seat already booked" error message.
