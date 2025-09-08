# 🚀 MERN Booking App

A full-stack **MERN (MongoDB, Express.js, React, Node.js)** application for booking hotels.  
This guide will help you set up and run the app on your local machine.  

---

## 📌 Prerequisites
Before you begin, make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v16+ recommended)  
- [npm](https://www.npmjs.com/) (comes with Node.js)  

---

## 📂 Cloning the Repository
Clone the repository to your local machine:

```bash
git clone https://github.com/your-username/mern-booking-app.git
cd mern-booking-app
⚙️ Backend Configuration
1. Environment Files
Navigate to the backend folder and create two files: .env and .env.e2e.

Add the following contents to both:

plaintext
Copy code
MONGODB_CONNECTION_STRING=

JWT_SECRET_KEY=
FRONTEND_URL=

# Cloudinary Variables
CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=

# Stripe
STRIPE_API_KEY=
2. MongoDB Setup
Sign up at MongoDB Atlas.

Create a cluster and database.

Copy the connection string into MONGODB_CONNECTION_STRING.

3. Cloudinary Setup
Sign up at Cloudinary.

Copy your Cloud Name, API Key, and API Secret into the .env files.

4. Stripe Setup
Sign up at Stripe.

Copy your API key into STRIPE_API_KEY.

5. JWT Secret
Use any long, random string (e.g., generated via an online secret key generator).

6. Frontend URL
For local development, set it to:

plaintext
Copy code
FRONTEND_URL=http://localhost:3000
💻 Frontend Configuration
Navigate to the frontend folder.

Create a .env file with the following:

plaintext
Copy code
VITE_API_BASE_URL=
VITE_STRIPE_PUB_KEY=
Example for local dev:

plaintext
Copy code
VITE_API_BASE_URL=http://localhost:7000
▶️ Running the Application
Start Backend
bash
Copy code
cd backend
npm install
npm start
Start Frontend
bash
Copy code
cd frontend
npm install
npm run dev
🔗 The app should be running at: http://localhost:5173

🧪 Running Automated Tests
1. Test Database
Create a new MongoDB database for tests (to keep data separate).

Add its connection string to .env.e2e.

2. Import Test Data
Test data is in the data/ folder (test-users.json, test-hotel.json).

Import them into MongoDB via MongoDB Compass.

Test user login:

makefile
Copy code
email: 1@1.com
password: password123
3. Run Tests
Install the Playwright VS Code extension.

Start backend + frontend.

Run tests from the e2e-tests directory with:

bash
Copy code
cd e2e-tests
npm install
Then run tests using Playwright.

🛠️ Tech Stack
Frontend: React + Vite + TailwindCSS

Backend: Node.js + Express.js

Database: MongoDB (Atlas)

Authentication: JWT

Image Hosting: Cloudinary

Payments: Stripe

📜 License
This project is licensed under the MIT License.

✨ Built with ❤️ using the MERN stack.

yaml
Copy code
