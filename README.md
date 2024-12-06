# Activity Tracker
## WORK IN PROGRESS
This repo contains our group project - Activity Tracker. A workout generating and tracking app.

#### Frontend
JavaScript, React, CSS, Bootstrap  
[![My Skills](https://skillicons.dev/icons?i=js,react,css,bootstrap)](https://skillicons.dev)

#### Backend
Python, Flask, PostgresSQL  
[![My Skills](https://skillicons.dev/icons?i=python,flask,postgres)](https://skillicons.dev)

#### Current functionality:
- A user can signup and create an account.
- A user can login and log out.
- A user can update their weight.
- A user can generate exercises based on a chosen muscle group.
- A user can log generated exercises along with loading and reps to create a workout plan.
- A user can enter their closest city or town and see the weather.
- A chart that displays the users weight updates.
- A gauge that displays someones weight.
- A user can favourite (and unfavourite) a generated exercise and then see a list of favourited exercises on the dashboard.

#### Currently scope of update:
- Review frontend testing.
- Review UI experience.
- Review API keys and requirements.



#### Prerequisites
You will need to: 
- Generate a free API key from [Api Ninjas](https://api-ninjas.com) and add this to your backend `.env` file.
- Generate a free API key from [Open Weather](https://openweathermap.org/api) and add this to your backend `.env` file.

#### Installation
Instructions for how to install the project:

### 1. Clone the repository
```
# Clone the repository:
git clone https://github.com/cajcrook/activity_tracker

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
(backend-venv); brew install postgresql@15
(backend-venv); createdb Activity_Tracker
(backend-venv); createdb Activity_Tracker_TEST

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

### 4. Testing

The React Testing Library is used to test the Frontend.  
Pytest is used to test the Backend.  

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
