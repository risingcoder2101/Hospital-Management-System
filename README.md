# Hospital Management System

## Overview

This Hospital Management System (HMS) is a comprehensive web-based platform designed to streamline the management of hospital operations, including patient registration, doctor and staff management, appointment scheduling, and administrative tasks. The system provides a user-friendly interface for all users and supports role-based access for patients, doctors, administrators, and other hospital staff.

## Features

### For Patients
- Register and manage personal account
- Search for doctors by name or specialty
- View available sessions and book appointments
- View and manage their bookings
- View all doctors and their details
- Edit profile and change password
- Delete account

### For Doctors
- Login and manage their profile
- View and manage their appointments
- View and manage their sessions (availability)
- View list of their patients
- Edit profile and change password
- Delete account

### For Admins
- Login to admin dashboard
- Manage doctors (add, edit, delete)
- Manage patients (view, search)
- Manage schedules/sessions (add, delete)
- Manage appointments (view, delete)
- View dashboard statistics
- Manage hospital staff and departments

## Folder Structure

```
admin/      # Admin dashboard and management pages
css/        # Stylesheets
img/        # Images and icons
patient/    # Patient dashboard and features
doctor/     # Doctor dashboard and features
```

## Database Setup

1. Create a MySQL database named `hospital`.
2. Import the provided `SQL_Database_edoc.sql` file to set up the required tables and sample data (rename as needed for HMS).
3. The main tables include:
   - `webuser`: Stores all user emails and their roles (admin, doctor, patient, staff)
   - `admin`: Admin credentials
   - `doctor`: Doctor profiles and specialties
   - `patient`: Patient profiles
   - `appointment`: Appointment records
   - `schedule`: Doctor session schedules
   - `specialties`: List of medical specialties
   - `staff`: Hospital staff profiles (if implemented)
   - `department`: Hospital departments (if implemented)

## Installation & Setup

1. Clone or download this repository to your web server directory.
2. Ensure you have PHP and MySQL installed (tested with PHP 7.3+ and MySQL 5.7+).
3. Update the database connection settings in `connection.php` if needed:
   ```php
   $database = new mysqli("localhost", "root", "", "hospital");
   ```
4. Import the SQL file into your MySQL server:
   ```sh
   mysql -u root -p hospital < SQL_Database_edoc.sql
   ```
5. Access the application via your browser (e.g., http://localhost/hospital-management-system/).

## Usage

- **Patients** can sign up, log in, search for doctors, book appointments, and manage their bookings.
- **Doctors** can log in, view their appointments, manage their sessions, and update their profile.
- **Admins** can log in, manage doctors, patients, schedules, appointments, staff, and departments.

## Default Admin Credentials
- Email: `admin@dhfzk.in`
- Password: `123`

## Screenshots

## License
This project is for educational purposes.
