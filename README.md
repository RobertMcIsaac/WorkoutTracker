# WeatherOrNot

A **Workout Generator and Tracker** web application that helps users create personalised workouts, log their exercises, and track weight progress—all while providing local weather insights.

## Table of Contents
- [WeatherOrNot](#weatherornot)
  - [Table of Contents](#table-of-contents)
  - [Overview](#overview)
  - [Features](#features)
  - [Structure](#structure)
    - [Frontend](#frontend)
    - [Backend](#backend)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
    - [1. Clone the Repository](#1-clone-the-repository)
    - [2. Set Up the Backend](#2-set-up-the-backend)
    - [3. Set Up the Frontend](#3-set-up-the-frontend)
    - [4. Run the Tests](#4-run-the-tests)
  - [Other Authors \& Acknowledgments](#other-authors--acknowledgments)
- [WeatherOrNot](#weatherornot-1)
  - [Table of Contents](#table-of-contents-1)
  - [Features](#features-1)
  - [Structure](#structure-1)
      - [Frontend](#frontend-1)
      - [Backend](#backend-1)
      - [Testing](#testing)
  - [Prerequisites](#prerequisites-1)
  - [Installation](#installation-1)
    - [1. Clone the repository](#1-clone-the-repository-1)
    - [2. Setup the Backend](#2-setup-the-backend)
    - [3. Setup the frontend](#3-setup-the-frontend)
    - [4. Run the Tests](#4-run-the-tests-1)
      - [Backend tests](#backend-tests)
      - [Frontend tests](#frontend-tests)

---

## Overview
**WeatherOrNot** is designed to help users create and manage their workout plans with dynamically generated exercises. Users can track changes in their weight over time through a chart and gauge, and even check the local weather to plan outdoor workouts. The app started out life as a weather-based activity recommendation app but our team pivotted away from basing recommendations on local weather and focussed more closely on generating and tracking workouts. 

---

## Features
- **User Authentication**  
  - Sign up for a new account  
  - Log in and log out securely  

- **Weight Management**  
  - Update and track weight changes  
  - View weight history on a chart and gauge  

- **Exercise Generation**  
  - Choose a muscle group to generate exercises  
  - Log exercises with details (loading, reps) to create a workout plan  

- **Favorites & Dashboard**  
  - “Favorite” a generated exercise and easily access it on your dashboard  
  - Unfavorite exercises when they’re no longer needed  

- **Weather Insights**  
  - Enter your location to see local weather conditions  

---

## Structure

### Frontend
- **Technologies**: JavaScript, React, CSS, Bootstrap  
- **Testing**: React Testing Library  
- **Icons**:  
  [![My Skills](https://skillicons.dev/icons?i=js,react,css,bootstrap)](https://skillicons.dev)

### Backend
- **Technologies**: Python, Flask, PostgreSQL  
- **Testing**: Pytest  
- **Icons**:  
  [![My Skills](https://skillicons.dev/icons?i=python,flask,postgres)](https://skillicons.dev)

---

## Prerequisites
You will need to:
- **Generate a free API key** from [API Ninjas](https://api-ninjas.com) and add it to your backend `.env` file.  
- **Generate a free API key** from [OpenWeather](https://openweathermap.org/api) and add it to your backend `.env` file.  
- Ensure you have **Python**, **Node.js**, and **PostgreSQL** installed on your system.

---

## Installation

### 1. Clone the Repository
```shell
# Clone the repository
git clone https://github.com/Dewi-Afoko/WeatherOrNot.git ProjectName

# Change directory to the cloned repository
cd ProjectName
```
### 2. Set Up the Backend
```shell
# Change directory to the backend folder
cd backend

# Set up the virtual environment
python -m venv backend-venv

# Activate the virtual environment (Mac/Linux)
source backend-venv/bin/activate

# (On Windows)
backend-venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Create a test and development database
createdb Activity_Tracker_TEST
createdb Activity_Tracker_TEST_tEst

# Optional: Open lib/database_connection.py to confirm or adjust database names
open lib/database_connection.py

# Create a .env file in the backend folder
touch .env

#Add the following to the .env file (adjust as needed):
API_KEY="your_api_ninjas_key_here"
OPENWEATHER_API_KEY="your_openweather_key_here"
JWT_SECRET="your_secret_key"

# Seed the SQL files into the database
python seed_database.py

# Run the app
python app.py

# Open your browser and visit:
# http://localhost:5000/index
```

### 3. Set Up the Frontend
```shell
# Move back to the project root, then to the frontend folder
cd ../frontend

# Create an .env file in the frontend
touch .env

# Add the backend URL to your .env file
echo 'VITE_BACKEND_URL="http://localhost:5000"' >> .env

# Install frontend packages
npm install

# Run the frontend
npm run dev

# In your browser, visit:
# http://localhost:5173/
```

### 4. Run the Tests
Backend Tests:
```shell
# From your project's root directory, navigate to backend
cd backend

# Activate the virtual environment if needed
source backend-venv/bin/activate

# Run tests (with extra logging)
pytest -sv
```
Frontend Tests:
```shell
# From your project's root directory, navigate to frontend
cd frontend

# Run the frontend tests
npm test
```
## Other Authors & Acknowledgments

This project was originally created as WeatherOrNot by a team during the Makers Software Development bootcamp. Special thanks to my original team members for their contributions:

- **Chris Crook** ([@cajcrook](https://github.com/cajcrook))  

- **Dewi Afoko** ([@Dewi-Afoko](https://github.com/Dewi-Afoko))  

- **Edgar Valero** ([@edgarvalero23](https://github.com/edgarvalero23))

- **Rebecca Clarke** ([Rclarkeweb](https://github.com/Rclarkeweb))

---

**Current Maintenance**:  
Following the initial development, I ( [**@RobertMcIsaac**](https://github.com/RobertMcIsaac) ) am continuing to edit, fine-tune, add new features in a new repository: **ActiviTips**! If you have any questions or ideas, feel free to open an issue or submit a pull request!




<!-- 

# WeatherOrNot

A full-stack web application that generates exercise recommendations based on user preferences, tracks users’ workouts, and monitors health metrics.

## Table of Contents

- [Features](#features)
- [Structure](#structure)
- [Prerequisites](#prerequisites)
- [Installation](#installation)

## Features
- A user can signup and create an account
- A user can login and log out 
- A user can update their weight
- A user can generate exercises based on a chosen muscle group
- A user can log generated exercises along with loading and reps to create a workout plan
- A user can enter their closest city or town and see the weather
- A chart that displays the users weight updates
- A gauge that displays someones weight
- A user can favourite (and unfavourite) a generated exercise and then see a list of favourited exercises on the dashboard

## Structure
Our web application consists of:

#### Frontend
JavaScript, React, CSS, Bootstrap  
  
[![My Skills](https://skillicons.dev/icons?i=js,react,css,bootstrap)](https://skillicons.dev)

#### Backend
Python, Flask, PostgresSQL  
  
[![My Skills](https://skillicons.dev/icons?i=python,flask,postgres)](https://skillicons.dev)

#### Testing

The React Testing Library is used to test the Frontend.  
Pytest is used to test the Backend.

## Prerequisites

You will need to: 
- Generate a free API key from [Api Ninjas](https://api-ninjas.com) and add this to your backend `.env` file.
- Generate a free API key from [Open Weather](https://openweathermap.org/api) and add this to your backend `.env` file.

## Installation

Instructions for how to install the project:

### 1. Clone the repository
```
# Clone the repository:
git clone https://github.com/Dewi-Afoko/WeatherOrNot.git ProjectName

# Change directory to the cloned repository
cd ProjectName
```

### 2. Setup the Backend
```
# Change directory to the backend folder
cd backend

# Set up the virtual environment
python -m venv backend-venv

# Activate the virtual environment
source backend-venv/bin/activate

# Install dependencies
(backend-venv); pip install -r requirements.txt

# Create a test and development database
(backend-venv); createdb Activity_Tracker_TEST
(backend-venv); createdb Activity_Tracker_TEST_tEst

# Open lib/database_connection.py and change the database names to match the above (if changed)
(backend-venv); open lib/database_connection.py

# Create .env file in backend folder
.env

# Add this to the .env file 
API_KEY = 'your api ninjas key here'
JWT_SECRET= your_secret_key

# Run seed_database to seed the sql files into database 
(backend-venv); python seed_database.py

# Run the app
(backend-venv); python app.py

# Now visit http://localhost:5000/index in your browser
```

### 3. Setup the frontend

```
# Change directory to the frontend folder
cd ../
cd frontend

# Create an .env file in frontend
.env

# Add this line to your .env file
VITE_BACKEND_URL="http://localhost:5000"

# Install the frontend packages
npm install 

# Run the app
npm run dev

# Visit the url http://localhost:5173/ in your browser
```

### 4. Run the Tests
  
#### Backend tests
```
# Run the backend tests
cd backend

# Run the tests (with extra logging)
(backend-venv); pytest -sv
```
  
#### Frontend tests
```
cd frontend

# Run the tests
npm test
```
