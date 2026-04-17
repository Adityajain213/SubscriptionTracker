# 📊 Subscription Tracker API

A production-ready backend system for managing and tracking user subscriptions, built with a focus on scalability, security, and real-world automation.

---

## 🚀 Features

*  JWT-based Authentication & Authorization
*  User Registration, Login & Logout
*  Subscription Lifecycle Management (CRUD)
*  Auto-calculation of renewal dates
*  Automated Email Reminders before renewal
*  Email notifications using NodeMailer
*  Rate Limiting & Bot Protection (ArcJet)
*  Workflow automation using Upstash

---

## 🛠️ Tech Stack

* **Backend:** Node.js, Express.js
* **Database:** MongoDB Atlas (Mongoose ORM)
* **Authentication:** JWT, bcrypt
* **Security:** ArcJet (Rate limiting & bot protection)
* **Automation:** Upstash Workflows
* **Email Service:** NodeMailer (Gmail SMTP)
* **Utilities:** date-fns
* **Dev Tools:** nodemon, ESLint

---

## 📁 Project Structure

```bash
subscription-tracker/
├── src/
│   ├── controllers/      # Business logic
│   ├── models/           # Database schemas
│   ├── routes/           # API endpoints
│   ├── middleware/       # Auth & security
│   ├── services/         # Core services (email, workflows)
│   └── config/           # DB & environment config
│
├── server.js             # Entry point
├── package.json
└── README.md
```

---

## ⚙️ Installation & Setup

```bash
# Clone repository
git clone https://github.com/Adityajain213/SubscriptionTracker.git

# Navigate to project
cd SubscriptionTracker

# Install dependencies
npm install

# Start server
npm start
```

---

## 🔑 Environment Variables

Create a `.env` file:

```env
PORT=5000
MONGO_URI=your_mongodb_connection
JWT_SECRET=your_secret_key
EMAIL_USER=your_email
EMAIL_PASS=your_password
ARCJET_KEY=your_arcjet_key
UPSTASH_URL=your_upstash_url
UPSTASH_TOKEN=your_upstash_token
```

---

##  Authentication & Security

* Passwords are securely hashed using **bcrypt**
* JWT tokens used for stateless authentication
* Middleware validates tokens and protects routes
* **ArcJet** enforces:

  * Rate limiting (token bucket algorithm)
  * Bot detection & blocking

---

##  Subscription Management

* Create, update, delete subscriptions
* Track:

  * Name, price, frequency, category
  * Payment method & status
  * Start date & renewal date
* Renewal date is **automatically calculated**
* Fetch all subscriptions per user
* Identify upcoming renewals

---

##  Automation & Workflows

* Integrated **Upstash workflows** for scheduling tasks
* Automatically triggers:

  * Subscription checks
  * Renewal reminders
* Sends email alerts at:

  * 7, 5, 2, and 1 day before renewal

---

## 📧 Email System

* Built using **NodeMailer + Gmail SMTP**
* Uses HTML templates for:

  * Personalized subscription reminders
* Ensures timely user notifications

---

##  Database Design

### User Model

* Name, email (validated), password (hashed)

### Subscription Model

* Name, price, currency
* Frequency (monthly/yearly)
* Category, payment method
* Status (active/cancelled)
* Start date, renewal date
* Linked to user

---

## 🧠 Key Highlights

* Follows **modular architecture** (routes, controllers, services)
* Implements **real-world backend patterns**
* Combines:

  * Authentication
  * Security
  * Automation
  * Deployment
* Demonstrates **production-level backend design**

---


