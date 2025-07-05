# eDoc Doctor Appointment System

## Overview

eDoc is a web-based Doctor Appointment System designed to streamline the process of booking, managing, and tracking doctor appointments for patients, doctors, and administrators. The system provides a user-friendly interface for all users and supports role-based access for patients, doctors, and admins.

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

## Folder Structure

```
admin/      # Admin dashboard and management pages
css/        # Stylesheets
img/        # Images and icons
patient/    # Patient dashboard and features
doctor/     # Doctor dashboard and features
```

## Database Setup

1. Create a MySQL database named `edoc`.
2. Import the provided `SQL_Database_edoc.sql` file to set up the required tables and sample data.
3. The main tables include:
   - `webuser`: Stores all user emails and their roles (admin, doctor, patient)
   - `admin`: Admin credentials
   - `doctor`: Doctor profiles and specialties
   - `patient`: Patient profiles
   - `appointment`: Appointment records
   - `schedule`: Doctor session schedules
   - `specialties`: List of medical specialties

## Installation & Setup

1. Clone or download this repository to your web server directory.
2. Ensure you have PHP and MySQL installed (tested with PHP 7.3+ and MySQL 5.7+).
3. Update the database connection settings in `connection.php` if needed:
   ```php
   $database = new mysqli("localhost", "root", "", "edoc");
   ```
4. Import the SQL file into your MySQL server:
   ```sh
   mysql -u root -p edoc < SQL_Database_edoc.sql
   ```
5. Access the application via your browser (e.g., http://localhost/edoc-doctor-appointment-system-main/).

## Usage

- **Patients** can sign up, log in, search for doctors, book appointments, and manage their bookings.
- **Doctors** can log in, view their appointments, manage their sessions, and update their profile.
- **Admins** can log in, manage doctors, patients, schedules, and appointments.

## Default Admin Credentials
- Email: `admin@dhfzk.in`
- Password: `123`

## Screenshots
Screenshots of the application are available in the `Screenshots/` folder.

## License
This project is for educational purposes.
