# 🚀 Autism Care System - Complete Startup Guide

## Prerequisites
- MySQL installed and running
- Python 3.x installed
- Node.js and npm installed
- Java JDK 17+ installed
- Maven installed

## Step-by-Step Startup

### 1️⃣ Database Setup (One-time)
```bash
# Open MySQL Command Line or MySQL Workbench
mysql -u root -p

# Enter your password: Renuka@2005

# Run these commands:
CREATE DATABASE autism_db;
USE autism_db;
SOURCE c:/Users/Admin/Desktop/autism/database/schema.sql;
exit;
```

### 2️⃣ Start ML Model (Terminal 1)
```bash
cd c:\Users\Admin\Desktop\autism\ml-model
pip install -r requirements.txt
python train_model.py
python app.py
```
✅ ML API running on: http://localhost:5000

### 3️⃣ Start Backend (Terminal 2)
```bash
cd c:\Users\Admin\Desktop\autism\backend
$env:Path += ";C:\Users\Admin\Downloads\apache-maven-3.9.12-bin\apache-maven-3.9.12\bin"
mvn spring-boot:run
```
✅ Backend API running on: http://localhost:8080

### 4️⃣ Start Frontend (Terminal 3)
```bash
cd c:\Users\Admin\Desktop\autism\frontend
npm install
npm start
```
✅ Frontend running on: http://localhost:3000

## 🎯 How to Use

1. **Visit**: http://localhost:3000
2. **Register**: Click Login → Register tab → Create account
3. **Login**: Enter credentials
4. **Screening**: Complete 20-question assessment
5. **Dashboard**: View results and recommendations
6. **Games**: Play learning activities
7. **Progress**: Track performance over time

## 📊 Data Storage

All data is automatically saved to MySQL database:
- ✅ User accounts (encrypted passwords)
- ✅ Screening responses (all 20 answers)
- ✅ ML predictions (risk levels & scores)
- ✅ Game performance (scores, time, accuracy)
- ✅ Learning activities

## 🔐 Authentication Features

- ✅ User registration with email validation
- ✅ Secure password encryption (BCrypt)
- ✅ Login/Logout functionality
- ✅ Session management
- ✅ User-specific data isolation

## 🎨 UI Features

- ✅ Modern landing page
- ✅ Responsive design (mobile + desktop)
- ✅ Soft pastel medical theme
- ✅ Smooth animations
- ✅ Interactive components

## ⚠️ Troubleshooting

**Backend won't start?**
- Check MySQL is running
- Verify password in application.properties
- Ensure port 8080 is free

**ML Model error?**
- Run `python train_model.py` first
- Check port 5000 is free

**Frontend issues?**
- Run `npm install` again
- Clear browser cache
- Check port 3000 is free

## 📝 Quick Commands

**Stop services**: Press `Ctrl+C` in each terminal

**Restart backend**: 
```bash
cd backend
mvn spring-boot:run
```

**Restart frontend**:
```bash
cd frontend
npm start
```

## ✅ System Status Check

All 3 services must be running:
- [ ] ML Model (port 5000)
- [ ] Backend (port 8080)
- [ ] Frontend (port 3000)

When all are running, open: http://localhost:3000
