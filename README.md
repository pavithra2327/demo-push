# Autism Care System

A comprehensive autism screening and learning enhancement platform with ML-powered predictions.

## Features

- **User Authentication**: Secure login system
- **20-Question Screening**: Evidence-based autism screening questionnaire
- **ML Prediction**: Random Forest model for risk assessment
- **Diagnosis Dashboard**: Visual results and recommendations
- **Personalized Learning**: Adaptive educational games
- **Performance Tracking**: Monitor child's progress over time

## Tech Stack

- **Frontend**: React 18
- **Backend**: Spring Boot 3.2
- **Database**: MySQL
- **ML Model**: Python Flask + scikit-learn
- **API**: RESTful architecture

## Setup Instructions

### 1. Database Setup

```sql
mysql -u root -p
CREATE DATABASE autism_db;
USE autism_db;
SOURCE database/schema.sql;
```

### 2. ML Model Setup

```bash
cd ml-model
pip install -r requirements.txt
python train_model.py
python app.py
```

ML API runs on: http://localhost:5000

### 3. Backend Setup

```bash
cd backend
mvn clean install
mvn spring-boot:run
```

Backend API runs on: http://localhost:8080

### 4. Frontend Setup

```bash
cd frontend
npm install
npm start
```

Frontend runs on: http://localhost:3000

## API Endpoints

### Screening
- POST `/api/screening/submit` - Submit screening responses

### Learning Activities
- GET `/api/learning/activities` - Get all activities
- GET `/api/learning/recommended/{riskLevel}` - Get recommended activities

### Performance
- POST `/api/performance/save` - Save game performance
- GET `/api/performance/user/{userId}` - Get user performance history

## Workflow

1. User logs in
2. Completes 20-question screening
3. ML model predicts autism risk
4. Dashboard displays results and recommendations
5. User plays personalized learning games
6. System tracks and analyzes performance
7. Recommendations adapt based on progress

## Project Structure

```
autism/
├── backend/          # Spring Boot REST API
├── frontend/         # React UI
├── ml-model/         # Python ML model
└── database/         # SQL schema
```

## Future Enhancements

- Real-time progress analytics
- Parent/therapist dashboard
- Video-based emotion recognition games
- Multi-language support
- Mobile app version

## License

MIT License
