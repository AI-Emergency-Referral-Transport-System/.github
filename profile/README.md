<h1 align="center" style="font-size: 70px; font-weight:bold; color:#E53935;">
AI Emergency Referral and Transport System
</h1>

<h3 align="center">
A real-time AI-powered emergency healthcare coordination platform connecting patients, ambulances, and hospitals
</h3>

<p align="center">
<img src="https://readme-typing-svg.demolab.com?font=Arial+Black&size=30&duration=3500&pause=800&color=E53935&center=true&vCenter=true&width=1200&lines=Solving+Emergency+Response+Delays;AI-Powered+Medical+Dispatch+System;Real-Time+Life-Saving+Coordination;Smart+Hospital+Selection+Engine" />
</p>

<p align="center">
<img src="https://img.shields.io/badge/System-AI%20Healthcare-red">
<img src="https://img.shields.io/badge/Backend-Django-blue">
<img src="https://img.shields.io/badge/Frontend-Flutter-green">
<img src="https://img.shields.io/badge/Realtime-WebSocket-orange">
<img src="https://img.shields.io/badge/Architecture-Distributed-lightgrey">
</p>

---

# Problem Statement

Emergency healthcare systems in many regions suffer from:

- Delayed ambulance response times  
- Lack of real-time hospital coordination  
- Poor resource visibility (beds, ICU, oxygen)  
- No intelligent decision-making for hospital selection  
- Fragmented communication between patients, drivers, and hospitals  

These issues directly lead to preventable loss of lives.

---

# Solution

This system introduces an AI-driven emergency coordination platform that:

- Instantly analyzes emergency requests using AI  
- Finds the nearest available ambulance in real time  
- Recommends the best hospital based on:
  - Distance  
  - Specialization  
  - Resource availability  
  - Waiting time  
- Enables live tracking of ambulances  
- Allows hospitals to prepare resources before patient arrival  

---

# System Overview

The system operates as a unified ecosystem:

```
Patient → AI Analysis → Ambulance Dispatch → Hospital Recommendation → Real-Time Tracking → Treatment Completion
```

Each component communicates in real time using WebSockets and REST APIs.

---

# System Architecture

```
Mobile Application (Flutter)
  ├── Patient Module
  ├── Ambulance Driver Module
  ├── Hospital Module
  └── AI Assistant Interface
            ↓
Backend (Django REST Framework)
  ├── User Management
  ├── Emergency Engine
  ├── Hospital System
  ├── Ambulance System
  ├── AI Processing Engine
  ├── Tracking Service
            ↓
Infrastructure Layer
  ├── Database (SQLite/PostgreSQL)
  ├── Redis Cache
  └── WebSocket Server (Real-Time Communication)
```

---

# Core System Capabilities

| Capability | Description |
|------------|------------|
| Emergency Detection | AI understands medical emergencies from text |
| Smart Dispatch | Finds nearest available ambulance automatically |
| Hospital Ranking | AI scores hospitals for best match |
| Live Tracking | Real-time ambulance movement monitoring |
| Resource Monitoring | ICU beds, oxygen, ER status tracking |
| Multi-Role System | Separate flows for patient, driver, hospital |
| Fault Handling | Handles failures, delays, and unavailability |

---

# AI Intelligence Engine

The AI system performs:

### 1. Emergency Classification
Transforms raw input into structured medical data:

- Cardiac emergency  
- Trauma  
- Respiratory failure  
- Stroke  
- Other critical conditions  

---

### 2. Priority Scoring

```
Priority = Symptom Severity + Risk Level + Time Sensitivity
```

---

### 3. Hospital Recommendation Engine

Each hospital is scored based on:

- Distance from patient  
- Availability of ICU beds  
- Oxygen level status  
- Specialty availability  
- Estimated waiting time  

---

### 4. Smart Decision Logic

Handles:
- No available ambulances  
- Hospital rejection  
- Timeout fallback routing  
- Load balancing between hospitals  

---

# Emergency Lifecycle

```
1. Patient submits emergency request
2. AI analyzes symptoms and location
3. System finds nearest ambulance
4. AI ranks hospitals
5. Hospital receives alert and prepares resources
6. Ambulance is dispatched
7. Live tracking begins
8. Patient is picked up
9. Patient is delivered to hospital
10. Emergency is completed and logged
```

---

# Real-Time Communication System

```
Driver GPS → WebSocket Server → Patient + Hospital Dashboards
```

This enables:
- Live ambulance movement tracking  
- ETA updates in real time  
- Instant hospital notifications  

---

# Resource Management System

Hospitals manage:

- ICU beds  
- General beds  
- Oxygen levels  
- Emergency room availability  
- Surgical room availability  

### Safety Mechanism

```
Request → Lock Resource → Reserve → Assign → Release After Completion
```

Prevents:
- Double booking  
- Over-allocation  
- Resource conflicts  

---

# Authentication System

```
Phone Number → OTP Verification → Role Selection → Dashboard Access
```

Roles:
- Patient  
- Ambulance Driver  
- Hospital Admin  

---

# API System Overview

### Authentication
- /api/users/register/
- /api/users/verify-otp/
- /api/users/refresh-token/

### Emergency
- /api/emergencies/
- /api/emergencies/{id}/status/

### Ambulance
- /api/ambulances/find-nearest/
- /api/ambulances/{id}/location/

### Hospital
- /api/hospitals/suggest/
- /api/hospitals/{id}/resources/

### AI
- /api/ai/process-emergency/
- /api/ai/chat/

---

# Data Models

### User
- Phone number  
- Role  
- Medical history  

### Emergency Request
- Type  
- Priority  
- Status lifecycle  
- Location  

### Hospital
- Beds  
- ICU availability  
- Oxygen level  
- Specialties  

### Ambulance
- Location  
- Status  
- Driver assignment  

---

# Key Features

| Feature | Description |
|----------|------------|
| AI Emergency Detection | Understands symptoms automatically |
| Smart Hospital Selection | AI ranking system |
| Real-Time Tracking | Live ambulance movement |
| Resource Reservation | Prevents conflicts |
| Multi-Role Dashboards | Separate interfaces |
| Scalable Architecture | Ready for large systems |

---

# Installation

### Backend

```
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

### Mobile App

```
cd mobile
flutter pub get
flutter run
```

---

# Testing Flow

```
Register → OTP Verification → Emergency Request → AI Processing → Dispatch → Tracking → Completion
```

---

# Future Enhancements

| Feature | Description |
|--------|------------|
| Voice AI Assistant | Voice emergency reporting |
| Predictive Analytics | Forecast emergency demand |
| Wearable Integration | Smartwatch triggers |
| Offline Mode | Rural connectivity support |
| Advanced Routing | AI-powered GPS optimization |
| Cloud Scaling | Multi-region deployment |

---

# Project Impact

This system directly improves:

- Emergency response time  
- Hospital coordination efficiency  
- Resource utilization  
- Patient survival probability  

It transforms fragmented emergency systems into a unified intelligent network.

---

# License

MIT License

---

# Acknowledgements

- Django REST Framework  
- Flutter SDK  
- WebSocket Technology  
- AI APIs (OpenAI, Gemini, HuggingFace)  
- Medical emergency coordination standards  
