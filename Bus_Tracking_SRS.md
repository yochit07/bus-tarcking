🚌 SOFTWARE REQUIREMENTS SPECIFICATION (SRS)
Project Title:

Smart Bus Tracking & Overcrowding Detection System Using IoT and AI

1. Introduction
1.1 Purpose

This document specifies the functional and non-functional requirements of the Smart Bus Tracking & Overcrowding Detection System. The system aims to provide real-time bus location tracking, passenger counting, overcrowding alerts, and transport analytics using IoT devices and AI technologies.

This SRS serves as a reference for:

Developers

Project evaluators

Transport administrators

End users (students)

1.2 Scope

The proposed system will:

Track bus location in real-time using GPS

Monitor passenger count using sensors/AI

Detect overcrowding conditions

Provide live dashboards for administrators

Allow students to view bus status and arrival time

Store historical transport data

Provide predictive analytics

The system includes:

IoT hardware inside bus

Backend server

Cloud database

Admin dashboard

Student web application

1.3 Definitions, Acronyms and Abbreviations
Term	Meaning
IoT	Internet of Things
GPS	Global Positioning System
AI	Artificial Intelligence
ETA	Estimated Time of Arrival
ESP32	Microcontroller with WiFi capability
YOLO	You Only Look Once (Object Detection Model)
2. Overall Description
2.1 Product Perspective

The system consists of:

Hardware Unit (Installed in Bus)

Backend Server

Cloud Database

Admin Dashboard

Student Application

It is a real-time client-server architecture system.

2.2 Product Functions

The system shall:

Collect real-time GPS coordinates

Count passengers entering and exiting

Calculate current occupancy

Detect overcrowding

Generate alerts

Display live bus location on map

Provide ETA prediction

Store and retrieve historical data

Provide analytics dashboard

2.3 User Classes and Characteristics
1. Transport Administrator

Technical knowledge: Basic

Access: Full system access

Responsibilities: Monitor buses, manage routes

2. Students/Passengers

Technical knowledge: Basic

Access: View-only

Responsibilities: Check bus location and availability

3. System Administrator

Technical knowledge: Advanced

Access: System configuration and maintenance

2.4 Operating Environment

Hardware Environment:

ESP32 Microcontroller

GPS Module

IR Sensors / Camera

GSM/WiFi Module

Software Environment:

Frontend: React + Vite

Backend: Node.js + Express

Database: Supabase

AI Module: Python + OpenCV + YOLO

Deployment: Cloud (Vercel / Render / Railway)

2.5 Design Constraints

Internet connectivity required

GPS accuracy limitations

Sensor placement affects accuracy

Budget constraints for hardware

Limited processing power on microcontroller

2.6 Assumptions and Dependencies

Each bus has stable network connectivity

Sensors are properly installed

Cloud server is continuously available

Map API service is operational

3. Specific Requirements
3.1 Functional Requirements
3.1.1 Bus Tracking Module

FR1: The system shall collect latitude and longitude using GPS.
FR2: The system shall update location every 5–10 seconds.
FR3: The system shall store location data in the database.
FR4: The system shall display live bus movement on a map.

3.1.2 Passenger Counting Module

FR5: The system shall detect passenger entry.
FR6: The system shall detect passenger exit.
FR7: The system shall maintain real-time passenger count.
FR8: The system shall update passenger count in the database.

3.1.3 Overcrowding Detection Module

FR9: The system shall compare passenger count with bus capacity.
FR10: The system shall mark bus as overcrowded if capacity exceeded.
FR11: The system shall trigger alert notifications.
FR12: The system shall display overcrowding warning in dashboard.

3.1.4 Admin Dashboard

FR13: Admin shall view all buses on live map.
FR14: Admin shall view current passenger count.
FR15: Admin shall view overcrowding alerts.
FR16: Admin shall access historical trip data.
FR17: Admin shall generate analytics reports.

3.1.5 Student Application

FR18: Students shall view live bus location.
FR19: Students shall view available seats.
FR20: Students shall receive overcrowding alerts.
FR21: Students shall view estimated arrival time (ETA).

3.1.6 AI Prediction Module

FR22: The system shall analyze historical data.
FR23: The system shall predict arrival time.
FR24: The system shall improve prediction accuracy over time.

3.2 Non-Functional Requirements
3.2.1 Performance Requirements

Location update latency ≤ 5 seconds

Dashboard loading time ≤ 3 seconds

System shall support multiple buses simultaneously

3.2.2 Security Requirements

User authentication via Supabase Auth

Role-based access control

Secure API endpoints

HTTPS communication

Encrypted database connections

3.2.3 Reliability Requirements

99% system uptime

Automatic reconnection if network fails

Backup of historical data

3.2.4 Usability Requirements

Simple and intuitive UI

Mobile-responsive design

Clear alert indicators

Minimal training required

3.2.5 Scalability Requirements

System shall support adding new buses

System shall handle increasing user load

Modular architecture for future expansion

3.2.6 Maintainability Requirements

Modular code structure

Well-documented APIs

Easy hardware replacement

Version control support

4. External Interface Requirements
4.1 Hardware Interfaces

GPS connected to ESP32 via UART

IR Sensors connected via GPIO

Camera connected via USB or onboard module

GSM module via serial communication

4.2 Software Interfaces

REST API between hardware and backend

Backend to Supabase database

Frontend to backend via HTTP requests

Map API integration

4.3 Communication Interfaces

WiFi / GSM network

HTTP/HTTPS protocol

JSON data format

5. System Models
5.1 Data Flow (High Level)

Bus collects GPS and passenger data

ESP32 sends data to backend

Backend processes and stores data

Dashboard fetches and displays updates

Alerts generated if needed

6. Future Enhancements

Mobile app (Android/iOS)

Face recognition for attendance

Fuel monitoring system

Route optimization AI

SMS-based notification system

Integration with smart city infrastructure

7. Conclusion

The Smart Bus Tracking & Overcrowding Detection System is a real-time IoT-based transport monitoring solution designed to improve passenger safety, reduce waiting time, and optimize transport management through AI-driven analytics.

It is scalable, reliable, and suitable for institutional and public transport systems.
