Smart Bus Tracking & Overcrowding Detection System
1️⃣ System Overview

The Smart Bus Tracking & Overcrowding Detection System is an IoT-based real-time monitoring system that integrates GPS tracking, passenger counting sensors, AI detection models, cloud backend, and web applications to improve transport management and passenger safety.

The system consists of:

Bus Hardware Unit

Backend Server

Cloud Database

Admin Dashboard

Student Web Application

AI Processing Module

2️⃣ Hardware Specifications
2.1 Microcontroller Unit

Device: ESP32

Processor: Dual-core Tensilica LX6

Clock Speed: 240 MHz

WiFi: 802.11 b/g/n

Bluetooth: v4.2

Operating Voltage: 3.3V

GPIO Pins: 34

Purpose:

Collect GPS and sensor data

Send data to backend server

2.2 GPS Module

Model: NEO-6M

Interface: UART

Position Accuracy: 2.5 meters

Update Rate: 1Hz

Power: 3.3–5V

Purpose:

Provide real-time latitude and longitude

2.3 Passenger Detection Module
Option A – IR Sensor Based

Sensor Type: Infrared Obstacle Sensor

Detection Distance: 2–30 cm

Voltage: 3.3–5V

GPIO Interface

Placement:

Two sensors at bus door for entry/exit detection

Option B – AI Camera Based (Advanced)

Camera: ESP32-CAM or USB Camera

Resolution: 720p minimum

AI Model: YOLOv5 / YOLOv8

Framework: OpenCV + Python

Purpose:

Detect and count passengers automatically

2.4 Communication Module

Method: WiFi / GSM (SIM800L)

Protocol: HTTP/HTTPS

Data Format: JSON

2.5 Power Supply

Input: 5V–12V (Bus battery)

Voltage Regulator: 5V/3.3V regulated output

Backup: Optional battery backup

3️⃣ Software Specifications
3.1 Frontend Specification

Technology Stack:

React (Vite)

JavaScript

Tailwind CSS (optional)

Leaflet / Google Maps API

System Requirements:

Browser: Chrome, Edge, Firefox

Responsive Design (Mobile + Desktop)

REST API integration

Features:

Live map view

Passenger count display

Overcrowding alerts

Admin analytics dashboard

Student bus tracking page

3.2 Backend Specification

Technology Stack:

Node.js

Express.js

REST API Architecture

System Requirements:

Node.js v18+

npm / yarn

Cloud deployment (Render / Railway)

Core Responsibilities:

Receive GPS data

Receive passenger count

Store data in database

Perform overcrowding logic

Provide APIs to frontend

Trigger alerts

3.3 Database Specification

Database: Supabase (PostgreSQL)

Tables:

buses

id (Primary Key)

bus_number

capacity

route

bus_location

id

bus_id

latitude

longitude

timestamp

bus_status

bus_id

current_passengers

is_overcrowded

trip_history

trip_id

bus_id

start_time

end_time

3.4 AI Module Specification

Language: Python
Libraries:

OpenCV

YOLOv5 / YOLOv8

NumPy

Flask (API integration optional)

Functionality:

Detect persons in frame

Count detected persons

Send count to backend API

Improve accuracy over time

Performance Target:

Detection time ≤ 1 second per frame

Accuracy ≥ 90%

4️⃣ System Architecture Specification

Architecture Type:
Client-Server + IoT Architecture

Flow:

ESP32 collects GPS + passenger data

Data sent via HTTP POST to backend

Backend processes and stores in database

Frontend fetches data using GET APIs

Dashboard displays real-time updates

5️⃣ Functional Specification Summary

The system shall:

Track bus in real time

Update location every 5–10 seconds

Count passengers automatically

Detect overcrowding

Trigger alerts

Provide historical analytics

Predict arrival time

6️⃣ Non-Functional Specifications
Performance

API response time ≤ 2 seconds

Location update interval: 5 seconds

Support minimum 10 buses simultaneously

Security

Supabase Authentication

Role-based access control

HTTPS communication

Secure API keys

JWT-based session handling

Reliability

99% uptime

Automatic retry on connection failure

Cloud database backup

Scalability

Modular architecture

Easy addition of new buses

Supports scaling to city-level transport

Usability

User-friendly interface

Minimal training required

Mobile responsive

7️⃣ Deployment Specifications

Frontend Deployment:

Vercel

Backend Deployment:

Render / Railway

Database Hosting:

Supabase Cloud

AI Model Hosting:

Local system / Cloud VM

8️⃣ Operating Requirements

Minimum Requirements:

For Backend Server:

4GB RAM

2 Core CPU

20GB Storage

For AI Model:

8GB RAM recommended

GPU optional (for better performance)

9️⃣ Environmental Constraints

Requires stable internet

GPS signal must be available

Hardware must be properly mounted

Weather protection needed for components

🔟 Testing Specifications

Testing Types:

Unit Testing (API endpoints)

Integration Testing (Hardware + Backend)

System Testing

Field Testing (Real Bus Environment)

Load Testing (Multiple buses)

1️⃣1️⃣ Future Scalability Specification

Mobile App Development (Android/iOS)

Fuel Monitoring Integration

Smart Ticketing System

Route Optimization AI

Government Transport Integration

1️⃣2️⃣ Conclusion

The Smart Bus Tracking & Overcrowding Detection System is a scalable, secure, and real-time intelligent transport monitoring solution combining IoT hardware, cloud backend, AI processing, and web technologies.

The system is technically feasible, cost-effective, and suitable for real-world institutional deployment.
