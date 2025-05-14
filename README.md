# 🏥 Clinic Booking System Database

## 📌 Description
A complete relational database for managing clinic operations including patient appointments, doctor schedules, medical records, billing, and inventory. This database supports all core functions needed for a modern healthcare clinic management system.

**Key Features:**
- Patient registration and management
- Doctor scheduling with availability tracking
- Appointment booking system
- Medical services catalog
- Electronic medical records
- Billing and payment tracking
- Inventory management
- User authentication and notifications

## 🛠️ Database Setup

### Prerequisites
- MySQL Server (8.0+ recommended)
- MySQL Workbench or similar database management tool

### Installation
1. **Create the database:**
   ```sql
   CREATE DATABASE clinic_booking_system;
   USE clinic_booking_system;

🗃️ Database Structure
   📂 clinic_booking_system
├── 📄 clinics
├── 📄 specialties
├── 📄 doctors
├── 📄 doctor_specialties (junction table)
├── 📄 doctor_schedules
├── 📄 doctor_unavailable_times
├── 📄 patients
├── 📄 medical_services
├── 📄 appointments
├── 📄 medical_records
├── 📄 bills
├── 📄 bill_items
├── 📄 users
├── 📄 notifications
├── 📄 feedback
├── 📄 inventory
└── 📄 inventory_usage


🔗 Entity Relationships
erDiagram
    clinics ||--o{ doctors : "1:N"
    doctors }o--o{ specialties : "M:N"
    doctors ||--o{ appointments : "1:N"
    patients ||--o{ appointments : "1:N"
    appointments ||--|{ medical_records : "1:1"
    appointments ||--o{ bills : "1:1"
    bills ||--o{ bill_items : "1:N"
