
# Telecom App

A cross-platform telecom app that allows users to manage and monitor airtime and data balances, purchase airtime, view usage history, and receive notifications for multiple SIM cards. The app is designed to work on both mobile (React Native) and desktop with a robust backend powered by Flask.

## Features

- **Account Management:** Add and switch between multiple SIM cards from different carriers.
- **Airtime and Data Balance:** View real-time airtime and data balances.
- **Purchase Options:** Purchase airtime and data packages via linked payment methods.
- **Usage Tracking:** Access usage history and summaries by day, week, or month.
- **Notifications and Alerts:** Low balance notifications and data expiry reminders.
- **Cross-Platform Access:** Synchronize data across devices with cloud support.
- **Recharge Reminders:** Set periodic recharge reminders.
- **User Settings:** Customize themes, set data limits, and adjust notification preferences.

---

## Technology Stack

### Frontend
- **React Native:** Mobile app for iOS and Android
- **Axios:** For making API requests

### Backend
- **Flask:** REST API framework in Python
- **PostgreSQL:** Relational database for structured data
- **MongoDB:** NoSQL database for unstructured data
- **Firebase:** For real-time features and notifications

### Additional Tools and Services
- **AWS (EC2, RDS, S3):** Cloud infrastructure
- **Kubernetes and Docker:** For container orchestration
- **Auth0/Firebase Authentication:** User authentication
- **Stripe:** Payment processing
- **Firebase Cloud Messaging (FCM) / OneSignal:** Push notifications
- **Jenkins/GitLab CI:** CI/CD for automated builds and deployments
- **Datadog:** Monitoring and performance tracking
- **Sentry:** Error tracking

---

## Setup and Installation

### Prerequisites

Ensure you have the following installed:
- Node.js and npm
- Python 3.x and pip
- PostgreSQL and MongoDB databases
- Docker and Docker Compose (for containerization)

### Frontend Setup (React Native)

1. Clone the repository and navigate to the frontend directory:
   ```bash
   git clone https://github.com/Karabosithole/telecom-app.git
   cd telecom-app/frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Configure API URL in `frontend/src/services/api.js`:
   ```javascript
   const API_URL = "http://localhost:5000/api";
   ```

4. Start the React Native development server:
   ```bash
   npx react-native run-android # For Android
   npx react-native run-ios     # For iOS
   ```

### Backend Setup (Flask)

1. Navigate to the backend directory:
   ```bash
   cd ../backend
   ```

2. Create a virtual environment and activate it:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Install required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

4. Configure the database in `app/config.py` (update with your PostgreSQL and MongoDB credentials).

5. Run the Flask server:
   ```bash
   flask run
   ```

### Docker Setup (Optional)

To run the app using Docker:

1. Build and run the services using Docker Compose:
   ```bash
   docker-compose up --build
   ```

2. Access the app at `http://localhost:3000` for the frontend and `http://localhost:5000/api` for the backend.

---

## Usage

### 1. Add a New SIM Card

- Navigate to the account management section and add SIM card details (carrier, number, etc.).

### 2. View Balance and Data

- Go to the balance screen to view real-time data and airtime balances for your SIMs.

### 3. Purchase Airtime/Data

- Use the purchase option to add funds to your SIM card via Stripe-integrated payment methods.

### 4. Notifications

- Set thresholds for low balance alerts and expiration reminders in the settings section.

### 5. Accessing Usage History

- Access usage history for airtime, data, and SMS in the usage tracking section with daily, weekly, and monthly summaries.

---

## CI/CD Pipeline

This project uses **Jenkins/GitLab CI** for automated builds and deployment.

1. Set up Jenkins or GitLab CI for automated testing, builds, and deployment to AWS.
2. Use **Kubernetes** and **Docker** for containerized deployment on AWS or other cloud providers.

---


