# MAD-II-Project

# QuizSphere (quiz-master-v2)

QuizSphere is a modern quiz application developed as part of the MAD II project. The platform offers a robust and interactive quiz experience, leveraging a Python backend, a modern JavaScript frontend, and supporting services for real-time and asynchronous operations.

---

## Features

- Interactive quiz platform
- Real-time feedback and scoring
- Email notifications (using MailHog)
- Asynchronous task handling (Celery & Redis)
- Modular frontend and backend architecture

---

## Getting Started

Follow the steps below to set up and run QuizSphere on your local machine.

### 1. Clone and Unzip the zip file

Unzip the project archive or clone the repository if available.

unzip QuizSphere.zip
cd QuizSphere


### 2. Install Python Dependencies

Open a terminal and install the required Python packages:

pip install -r requirements.txt


### 3. Start the Backend Server

python main.py


### 4. Set Up the Frontend

Open a second terminal, navigate to the `frontend` directory, and install dependencies:

cd frontend
npm install
npm run serve


### 5. Start Redis Server

Open a third terminal and run:

redis-server


### 6. Start Celery Worker

Open a fourth terminal and run:

celery -A main.celery_app worker --pool=solo -l info


### 7. Start MailHog (for Email Testing)

Open a fifth terminal and run:

~/go/bin/MailHog


### 8. Start Celery Beat Scheduler

Open a sixth terminal and run:

celery -A main:celery_app beat -l INFO


---

## Additional Notes

- Ensure all required services (Redis, MailHog, Celery) are running for full functionality.
- The application is designed for development and testing purposes.
- For any issues, please contact the project maintainer.
