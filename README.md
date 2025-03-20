# Hospital Management System - Backend

## Overview
This backend service is developed for a **Hospital Management System** using **Node.js, Express.js, MongoDB, and JWT authentication**. It provides role-based access for **Admin, Doctors, and Patients** with functionalities such as user authentication, doctor management, and appointment booking.

## Features
- **Admin**
  - Can register/login.
  - Can add new doctors.
  - Has full control over user management.
  
- **Doctors**
  - Can register/login.
  - Can manage their own profile and appointments.

- **Patients**
  - Can register/login.
  - Can book appointments with available doctors.
  - Cannot add doctors or other patients.

## Tech Stack
- **Backend**: Node.js, Express.js
- **Database**: MongoDB (Mongoose ORM)
- **Authentication**: JWT (JSON Web Token)
- **API Documentation**: Postman / Swagger (Optional)

## Installation

1. **Clone the repository**
   ```sh
   git clone https://github.com/your-repo/hospital-management.git
   cd hospital-management/backend
   ```

2. **Install dependencies**
   ```sh
   npm install
   ```

3. **Set up environment variables** (Create a `.env` file and add the following values)
   ```env
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_secret_key
   ```

4. **Run the server**
   ```sh
   npm start
   ```
   The backend will run on `http://localhost:5000`.

## API Endpoints

### Authentication
| Method | Endpoint       | Description          |
|--------|--------------|----------------------|
| POST   | /auth/register | Register a user (Admin/Doctor/Patient) |
| POST   | /auth/login    | Login a user |

### Admin
| Method | Endpoint       | Description          |
|--------|--------------|----------------------|
| POST   | /admin/add-doctor | Admin can add a new doctor |

### Doctor
| Method | Endpoint       | Description          |
|--------|--------------|----------------------|
| GET    | /doctor/profile | View doctor profile |

### Patient
| Method | Endpoint       | Description          |
|--------|--------------|----------------------|
| GET    | /patient/profile | View patient profile |
| POST   | /appointment/book | Book an appointment with a doctor |

## Security Measures
- JWT-based authentication for secure API access.
- Role-based authorization (Only admin can add doctors).
- Data validation and error handling.

## Contribution
Feel free to fork this project and contribute by submitting a pull request!

## License
This project is licensed under the **MIT License**.

---

Developed with ❤️ by **Ashirwad**

