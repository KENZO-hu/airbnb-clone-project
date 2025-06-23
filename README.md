Airbnb Clone Project

##  Project Overview

*StayEase* is a full-stack accommodation booking platform inspired by Airbnb. Developed as part of the *ALX Software Engineering Program (ProDev Back-End)*, it simulates real-world development by integrating backend logic, database design, authentication, and deployment practices.

This project showcases a robust system for property listings, user authentication, booking flow, and secure payments—built with scalability, maintainability, and teamwork in mind.

###  Project Goals

- Build a scalable and secure backend architecture  
- Design and manage a relational database for property booking  
- Implement RESTful APIs and JWT-based authentication  
- Enable a smooth and secure booking process  
- Integrate CI/CD workflows and containerization  
- Document the system and collaborate in a team-based setup  

---

##  Technology Stack

| Technology      | Purpose                                                                 |
|-----------------|-------------------------------------------------------------------------|
| *Django*      | High-level Python backend framework for building APIs and business logic |
| *PostgreSQL*  | Relational database for storing structured data                         |
| *GraphQL*     | API query language for flexible and efficient data fetching             |
| *React.js*    | Front-end library for building responsive UIs (for full-stack integration) |
| *JWT*         | Secure user authentication and authorization                            |
| *Stripe API*  | Payment gateway for booking transactions                                |
| *Docker*      | Containerization of the app for portability and consistency             |
| *GitHub Actions* | CI/CD pipeline for automated testing and deployment                  |

---

##  Team Roles

| Role                 | Responsibilities                                                                 |
|----------------------|----------------------------------------------------------------------------------|
| *Project Manager*  | Oversees project timeline and coordination                                       |
| *Backend Developer*| Develops APIs, handles logic, manages security and data layers                   |
| *Database Admin*   | Designs and maintains database schema and performance                            |
| *DevOps Engineer*  | Sets up deployment pipelines and configures Docker                               |
| *Frontend Developer*| (Optional) Builds user interfaces and connects to backend                       |
| *QA Tester*        | Tests API endpoints, reports bugs, ensures software reliability                  |
| *Product Owner*    | Prioritizes features and ensures the system aligns with user needs               |

---

##  Database Design

### Key Entities and Relationships

| Entity     | Key Fields                                                                 |
|------------|----------------------------------------------------------------------------|
| *User*   | id, email, password_hash, name, profile_picture, created_at                |
| *Property* | id, title, description, price, location, host_id, created_at             |
| *Booking* | id, user_id, property_id, check_in, check_out, total_price, status        |
| *Review*  | id, user_id, property_id, rating, comment, created_at                     |
| *Payment* | id, booking_id, amount, payment_method, status, transaction_id            |

### Relationships

- A user can host multiple properties  
- A user can book multiple properties  
- A booking links a guest to a property  
- A review belongs to one user and one property  
- A payment is tied to a booking

---

##  Feature Breakdown

| Feature               | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| *User Management*    | Registration, login/logout, profile management with secure authentication  |
| *Property Listings*  | Hosts can create, edit, and manage rental properties                        |
| *Booking System*     | Guests can reserve properties with date selection and conflict resolution   |
| *Review System*      | Users can leave reviews and ratings after booking                           |
| *Payment Integration*| Booking payments are processed securely via Stripe API                      |
| *Search & Filtering* | Users can filter listings by price, location, amenities, and availability   |

---

##  API Security

### Key Measures

| Security Area        | Explanation                                                                 |
|----------------------|------------------------------------------------------------------------------|
| *Authentication*   | JWT-based login system with sessionless tokens                              |
| *Authorization*    | Role-based access control (admin, guest, host)                              |
| *Rate Limiting*    | Prevents brute-force and abuse using request caps per IP                    |
| *Data Encryption*  | HTTPS/TLS for in-transit encryption, password hashing using bcrypt          |
| *Input Validation* | Prevents SQL injection and XSS with strict data sanitization                |

---

## 🔁 CI/CD Pipeline

| Tool              | Role                                                                         |
|-------------------|------------------------------------------------------------------------------|
| *GitHub Actions*| Triggers test and deploy workflows on code changes                           |
| *Docker*        | Ensures consistent environments from development to production               |
| *Heroku / Fly.io*| Optional backend deployment platforms                                       |
| *PostgreSQL Add-on*| Hosted database integration for deployed environments                     |

### Benefits of CI/CD

- Faster release cycles with automated workflows  
- Immediate feedback from test failures  
- Reliable and repeatable deployment with fewer bugs  
- Easier team collaboration and parallel development  

---

##  License

This project is licensed under the [MIT License](./LICENSE).
