<h1 align="center" style="font-size: 70px; font-weight:800; color:#E53935;">
AI Emergency Referral and Transport System
</h1>

<h3 align="center">
A real-time AI-powered emergency healthcare platform connecting patients, ambulances, and hospitals through intelligent coordination and automation
</h3>

<p align="center">
<img src="https://readme-typing-svg.demolab.com?font=Arial+Black&size=28&duration=3500&pause=800&color=E53935&center=true&vCenter=true&width=1200&lines=AI+Driven+Emergency+Healthcare+System;Real-Time+Ambulance+Dispatch+Platform;Smart+Hospital+Recommendation+Engine;Unified+Medical+Coordination+Network" />
</p>

<p align="center">
<img src="https://img.shields.io/badge/Frontend-Flutter-green">
<img src="https://img.shields.io/badge/Backend-Django-blue">
<img src="https://img.shields.io/badge/Realtime-WebSocket-orange">
<img src="https://img.shields.io/badge/AI-Integrated-red">
<img src="https://img.shields.io/badge/Architecture-Distributed-lightgrey">
<img src="https://img.shields.io/badge/License-MIT-lightgrey">
</p>

---

# System Vision

Emergency healthcare systems often fail due to fragmented communication, delayed decision-making, and lack of real-time coordination between patients, ambulances, and hospitals.

This system introduces a unified intelligent emergency network where AI and real-time data ensure every second is optimized to save lives.

---

# Problem Statement

Traditional emergency systems suffer from:

- Delayed ambulance dispatch  
- No real-time hospital availability tracking  
- Manual coordination between entities  
- Lack of intelligent hospital selection  
- Poor resource visibility (beds, ICU, oxygen)  
- Inefficient emergency routing  

These inefficiencies directly contribute to preventable loss of lives.

---

# Solution Overview

This system solves these problems by introducing an AI-powered emergency coordination platform that:

- Understands emergency requests using AI  
- Automatically dispatches the nearest available ambulance  
- Recommends optimal hospitals based on real-time conditions  
- Tracks ambulances live using GPS  
- Prepares hospitals before patient arrival  
- Manages hospital resources dynamically and safely  

---

# System Architecture

```
Flutter Mobile Application (Frontend)
        ⇄ REST API ⇄
Django Backend System
        ⇄
AI Processing Engine
        ⇄
WebSocket Real-Time Layer
        ⇄
Database + Redis
```

---

# Technology Stack

## Frontend
- Flutter (Mobile Application)
- Dart
- Real-time UI with WebSocket integration

## Backend
- Django (REST Framework)
- Python
- Django Channels (WebSockets)

## Database
- SQLite (development)
- PostgreSQL (production-ready)

## Real-Time Layer
- WebSocket (live tracking & notifications)
- Redis (caching & performance optimization)

## AI Layer
- Emergency classification engine
- Hospital recommendation system
- Rule-based + LLM-based decision support

---

# Why Django + Flutter?

## Django
- Robust backend framework
- Fast API development
- Secure authentication system
- Strong ORM for database management
- Easy AI and WebSocket integration

## Flutter
- Cross-platform mobile development
- High-performance UI
- Smooth animations for real-time updates
- Single codebase for Android and iOS

---

# Core System Capabilities

| Capability | Description |
|------------|------------|
| AI Emergency Detection | Converts symptoms into structured medical data |
| Smart Ambulance Dispatch | Finds nearest available ambulance automatically |
| Hospital Ranking Engine | AI-based hospital scoring system |
| Real-Time Tracking | Live ambulance GPS monitoring |
| Resource Management | ICU beds, oxygen, emergency rooms |
| Multi-Role System | Patient, Driver, Hospital workflows |
| Fault Tolerance | Handles failures and fallback routing |
| Scalable Architecture | Designed for large-scale deployment |

---

# AI Intelligence Engine

## Emergency Classification
Transforms user input into structured emergency types:
- Cardiac emergency  
- Trauma  
- Stroke  
- Respiratory failure  
- Other critical conditions  

---

## Priority Calculation

```
Priority Score =
  Symptom Severity +
  Time Sensitivity +
  Risk Level
```

---

## Hospital Recommendation Engine

Hospitals are ranked using:

- Distance from patient  
- Medical specialty match  
- ICU and bed availability  
- Oxygen level status  
- Estimated waiting time  

---

## Smart Dispatch Logic

Handles real-world complexity:
- No ambulance availability fallback  
- Hospital rejection rerouting  
- Timeout-based reassignment  
- Load balancing across hospitals  

---

# Emergency Lifecycle

```
1. Patient submits emergency request
2. AI analyzes symptoms and location
3. System finds nearest ambulance
4. AI ranks hospitals
5. Hospital receives pre-arrival alert
6. Ambulance is dispatched
7. Real-time tracking begins
8. Patient is picked up
9. Patient is delivered to hospital
10. Emergency is completed and logged
```

---

# Real-Time System

```
Ambulance GPS → WebSocket Server → Patient + Hospital Dashboards
```

Enables:
- Live ambulance tracking  
- ETA updates in real time  
- Instant hospital notifications  

---

# Hospital Resource Management

Hospitals manage:

- ICU beds  
- General beds  
- Oxygen supply  
- Emergency rooms  
- Surgical units  

## Resource Safety Model

```
Request → Lock → Reserve → Assign → Release
```

Ensures:
- No double booking  
- No resource conflicts  
- Safe concurrent operations  

---

# Authentication Flow

```
Phone Number → OTP Verification → Role Selection → Dashboard Access
```

Roles:
- Patient  
- Ambulance Driver  
- Hospital Admin  

---

# API Structure

## Authentication
- /api/users/register/
- /api/users/verify-otp/
- /api/users/refresh-token/

## Emergency System
- /api/emergencies/
- /api/emergencies/{id}/status/

## Ambulance System
- /api/ambulances/find-nearest/
- /api/ambulances/{id}/location/

## Hospital System
- /api/hospitals/suggest/
- /api/hospitals/{id}/resources/

## AI System
- /api/ai/process-emergency/
- /api/ai/chat/

---

# Data Models

## User
- Phone number  
- Role  
- Medical history  
- Emergency contacts  

## Emergency Request
- Type  
- Priority  
- Status lifecycle  
- Location data  

## Hospital
- Bed capacity  
- ICU availability  
- Oxygen level  
- Specialties  

## Ambulance
- GPS location  
- Status  
- Driver assignment  

---

# Key Features

| Feature | Description |
|----------|------------|
| AI Emergency Detection | Intelligent symptom understanding |
| Smart Hospital Matching | AI-based ranking system |
| Live Tracking | Real-time ambulance movement |
| Resource Reservation | Prevents hospital overbooking |
| Multi-Role System | Separate dashboards per user type |
| Scalable Backend | Production-ready architecture |

---

# System Impact

This system improves healthcare systems by:

- Reducing emergency response time  
- Improving hospital coordination  
- Increasing survival probability  
- Automating critical decision-making  
- Connecting fragmented healthcare systems into one unified network  

---

# Installation

## Backend Setup
```
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

## Mobile Setup
```
cd mobile
flutter pub get
flutter run
```

---

# Testing Flow

```
Register → OTP → Emergency Request → AI Processing → Dispatch → Tracking → Hospital Arrival → Completion
```

---

# Future Enhancements

- Voice-based emergency reporting system  
- Predictive emergency analytics  
- Wearable device integration  
- Offline emergency support for rural areas  
- AI-based route optimization  
- Cloud-scale deployment  
- National-level emergency integration  

---

# Project Vision

This organization aims to build a unified AI-powered healthcare emergency infrastructure that connects patients, ambulances, and hospitals into a single intelligent system capable of saving lives through real-time coordination and automated decision-making.

---

# License

MIT License

---

# Acknowledgements

- Django REST Framework  
- Flutter SDK  
- WebSocket Technology  
- AI APIs (OpenAI, Gemini, HuggingFace)  
- Healthcare system design principles  
