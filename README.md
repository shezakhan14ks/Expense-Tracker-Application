<<<<<<< HEAD
# Expensify---Finance-Tracker
=======
# Expensify - Expense Tracker Application

Expensify is a comprehensive expense tracking application that helps users manage their finances, track expenses, set up recurring bills, and get insights through data visualization and machine learning predictions.

> **Note:** This application consists of a Node.js backend, a web frontend, and a Python-based machine learning service.

## Features

- ✅ User authentication and account management
- ✅ Expense tracking with categories and notes
- ✅ Recurring bills management
- ✅ Data visualization with charts
- ✅ Machine learning for expense predictions
- ✅ Push notifications for bill reminders
- ✅ Responsive design for mobile and desktop

## Prerequisites

Before you begin, ensure you have the following installed:

- Node.js (v14 or higher)
- npm (v6 or higher)
- Python (v3.8 or higher) for the ML service
- PostgreSQL database

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/sandipan-das-sd/Final-Expense.git
cd Final-Expense
```

### 2. Install Node.js dependencies

```bash
npm install
```

### 3. Install Python dependencies for the ML service

```bash
pip install -r public/requirements.txt
```

### 4. Set up the PostgreSQL database with Neon DB

This project uses [Neon DB](https://neon.tech/) as the cloud PostgreSQL service instead of a local PostgreSQL server:

1. Sign up at https://neon.tech/
2. Create a new project
3. Create a new database
4. Copy the connection details for use in your `.env` file
5. Use the Neon PostgreSQL Editor to run the PostgreSQL commands from `command.sql` to set up the required tables

### 5. Configure environment variables

Create a `.env` file in the root directory with the following variables:

```
# Server Configuration
PORT=3000
NODE_ENV=development

# Database Configuration (Neon DB)
DB_USER=your_neon_db_username
DB_PASSWORD=your_neon_db_password
DB_HOST=your_neon_db_host.neon.tech
DB_PORT=5432
DB_NAME=your_neon_db_name
DB_SSL=require

# JWT Configuration
JWT_SECRET=your_jwt_secret_key

# ML Service Configuration
ML_SERVICE_URL=http://localhost:5000

# Firebase Configuration (for push notifications)
FIREBASE_PROJECT_ID=expensify-401ce
FIREBASE_CLIENT_EMAIL=firebase-adminsdk-fbsvc@expensify-401ce.iam.gserviceaccount.com
FIREBASE_PRIVATE_KEY="your-private-key-here"

# AWS Configuration (optional, for SMS notifications)
AWS_ACCESS_KEY=your_aws_access_key
AWS_SECRET_KEY=your_aws_secret_key
```

## Running the Application

### Development Mode

Start the Node.js server and ML service concurrently:

```bash
npm run dev-all
```

This will start both the Node.js server and the Python ML service using nodemon for auto-reloading.

### Production Mode

1. Start the Node.js server:

```bash
npm start
```

2. Start the ML service separately:

```bash
npm run start-ml
```

3. Alternatively, use PM2 for process management:

```bash
pm2 start ecosystem.config.js
```

## Accessing the Application

Once the server is running, you can access the application at:

```
http://localhost:3000
```

## API Endpoints

| Endpoint        | Description                             |
| --------------- | --------------------------------------- |
| /api/auth       | Authentication routes (login, register) |
| /api/expenses   | Expense management                      |
| /api/bills      | Recurring bills management              |
| /api/users      | User profile management                 |
| /api/categories | Expense categories                      |
| /api/ml         | Machine learning predictions            |

## Project Structure

```
expensify/
├── public/               # Static files and frontend
│   ├── index.html        # Main dashboard
│   ├── expenses-list.html # Expenses list page
│   ├── add-expense.html  # Add expense page
│   ├── bills.html        # Bills management page
│   ├── expense-chart.html # Charts and visualizations
│   ├── login.html        # Login page
│   ├── register.html     # Registration page
│   ├── style.css         # Main stylesheet
│   ├── mobile.css        # Mobile-specific styles
│   └── requirements.txt  # Python dependencies
├── routes/               # API routes
├── db/                   # Database connection
├── middleware/           # Express middleware
├── utils/                # Utility functions
├── ml_service.py         # Python ML service
├── start_ml_service.js   # Script to start ML service
├── server.js             # Main Express server
├── command.sql           # Database schema
└── package.json          # Node.js dependencies
```

## Troubleshooting

**Database Connection Issues:**
If you encounter database connection issues, ensure your Neon DB connection details are correct in your .env file and that your project is active. Check the Neon DB dashboard to verify your database status.

**ML Service Not Starting:**
If the ML service fails to start, check that Python is installed correctly and all dependencies are installed. Check the ml_service.log file for errors.

## License

This project is licensed under the ISC License.
>>>>>>> 78ce048 (Hosting the app)
#   E x p e n s i f y - F i n a n c e - T r a c k e r - m a i n _ s h e z a  
 #   E x p e n s e - T r a c k e r -  
 