# cse5_queue-management-for-parking
This project is a web-based Queue Management System designed to streamline the flow of vehicles in parking areas. It allows users to reserve parking spots, join entry queues, and complete payments—all through an intuitive interface.  The system aims to reduce wait times, prevent congestion, and ensure optimal use of parking spaces.
Based on the extracted and reviewed code from your **Queue Management for Parking** project, here's a **final explanation** of the system:

---

### 🔧 **Project Title**: Queue Management System for Parking

### 🌐 **Tech Stack**
- **Frontend**: HTML, CSS, JavaScript
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Payment Gateway**: Razorpay (test mode)
- **Middleware**: CORS, Body-parser

---

### 🧩 **System Overview**

This project is designed to efficiently manage vehicle parking with queue handling and integrated payment functionality.

---

### 🗂️ **Main Components**

#### 1. **Backend (Node.js with Express)**
- **Entry Point (`server.js`)**:
  - Connects to MongoDB using Mongoose.
  - Uses middleware (`cors`, `body-parser`) for request handling.
  - Serves frontend static files (like `payment.html`).
  - Integrates Razorpay for payments.
  - Routes are modularized (`/routes/api.js`, `/routes/userRoutes.js`).

- **Routes**:
  - `api.js`: Contains queue-related logic (like booking a spot or checking position).
  - `userRoutes.js`: Handles user operations (e.g., registration, login, user info).

#### 2. **Frontend**
- **HTML Pages**:
  - `payment.html`: Interface to enter amount and make payments using Razorpay.
  - Uses Razorpay Checkout API to initiate payments from the frontend.
  - After payment, a confirmation screen or redirection is handled.

#### 3. **Payment Integration**
- Uses **Razorpay test keys** to simulate transactions.
- Payment process:
  1. User enters amount → clicks "Pay".
  2. Razorpay Checkout form opens.
  3. Upon success, Razorpay returns a transaction ID.

#### 4. **MongoDB (Database)**
- Stores user information, queue positions, and possibly payment data.
- Collections could include:
  - `users`: User info and login data.
  - `queue`: Vehicles in the parking queue.
  - `transactions` (optional): Payment logs for each session.

---

### 🔄 **Flow of the System**

1. **User arrives** and gets added to the queue.
2. **Queue logic** determines their position and updates availability.
3. **When it's their turn**, they're prompted to make a payment.
4. **Payment is processed** via Razorpay, and the user is granted access.
5. **Queue updates** as cars leave/enter.

---

### ✅ **Key Features**
- Efficient queue management.
- Razorpay-based secure payment system.
- Real-time updates with backend integration.
- Simple and modular code structure.

