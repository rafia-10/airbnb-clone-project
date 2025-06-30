# Airbnb Clone Project

## Project Overview

The Airbnb Clone Project is a full-stack web application designed to simulate the core features of Airbnb, a popular property booking platform. This project focuses on backend development, database design, API security, and continuous integration/deployment (CI/CD) to build a scalable, secure, and maintainable system. The technology stack includes Django, MySQL, GraphQL, Docker, and GitHub Actions, aiming to equip learners with real-world software development skills.

---

## Team Roles

- **Backend Developer**: Responsible for designing and implementing the server-side application logic, APIs, and database interactions to ensure seamless data flow and business logic execution.
- **Database Administrator**: Designs, optimizes, and maintains the relational database system to ensure data integrity, performance, and scalability.
- **Frontend Developer**: Develops the user interface and client-side logic to provide an interactive and user-friendly experience (though not the main focus in this project).
- **DevOps Engineer**: Sets up and manages CI/CD pipelines, automates deployment, and maintains the development environment to support continuous delivery.
- **Project Manager**: Oversees project planning, progress tracking, team coordination, and communication to ensure timely delivery of project milestones.

---

## Technology Stack

- **Django**: A high-level Python web framework used for building robust backend APIs and handling application logic.
- **MySQL**: A relational database management system used to store and manage structured data such as users, properties, bookings, and payments.
- **GraphQL**: A flexible query language and runtime for APIs that allows clients to request exactly the data they need.
- **Docker**: A containerization platform used to package the application and its dependencies for consistent development, testing, and deployment environments.
- **GitHub Actions**: A CI/CD service that automates building, testing, and deploying the application to ensure faster and reliable releases.
- **Postman**: A tool used for testing and validating API endpoints to ensure they work as expected.

---

## Database Design

### Entities & Fields

- **User**
  - `id` (Primary Key)
  - `username`
  - `email`
  - `password_hash`
  - `profile_picture`

- **Property**
  - `id` (Primary Key)
  - `owner_id` (Foreign Key to User)
  - `title`
  - `description`
  - `location`
  - `price_per_night`

- **Booking**
  - `id` (Primary Key)
  - `user_id` (Foreign Key to User)
  - `property_id` (Foreign Key to Property)
  - `start_date`
  - `end_date`
  - `status`

- **Review**
  - `id` (Primary Key)
  - `user_id` (Foreign Key to User)
  - `property_id` (Foreign Key to Property)
  - `rating`
  - `comment`
  - `created_at`

- **Payment**
  - `id` (Primary Key)
  - `booking_id` (Foreign Key to Booking)
  - `amount`
  - `payment_date`
  - `payment_status`

### Relationships

- A **User** can own multiple **Properties** (one-to-many relationship).
- A **Booking** belongs to one **Property** and is made by one **User**.
- A **User** can leave multiple **Reviews** on different **Properties**.
- Each **Booking** has one associated **Payment** record.

---

## Feature Breakdown

- **User Management**: Enables users to register, authenticate, and manage their profiles securely.
- **Property Management**: Allows property owners to list, update, and delete properties.
- **Booking System**: Provides functionality for users to book properties for specific dates and manage their bookings.
- **Review System**: Lets users leave ratings and comments on properties they have stayed in to build community trust.
- **Payment Processing**: Handles secure payments linked to bookings, ensuring smooth transactions.
- **API Security**: Implements authentication, authorization, and input validation to protect data and prevent unauthorized access.
- **CI/CD Pipeline**: Automates testing, building, and deployment to improve efficiency and maintain code quality.

---

## API Security

The project employs several key security measures to safeguard the application:

- **Authentication**: Uses JSON Web Tokens (JWT) to verify user identity securely.
- **Authorization**: Role-based access control restricts user actions based on permissions.
- **Input Validation**: Validates all incoming data to prevent injection attacks and data corruption.
- **Rate Limiting**: Controls the number of requests a user can make in a given time to prevent abuse.
- **Secure Data Storage**: Passwords are hashed and sensitive data is encrypted.

---

## CI/CD Pipeline

Continuous Integration and Continuous Deployment (CI/CD) automate the development process by automatically testing, building, and deploying code changes. This speeds up releases, reduces manual errors, and improves software quality.

For this project:

- **GitHub Actions** automates workflows that run tests and build Docker images upon every commit.
- **Docker** containers ensure consistent environments across development, testing, and production.
- Automated deployment reduces downtime and allows for rapid iteration.

Using CI/CD pipelines fosters collaboration, maintains code integrity, and enables faster delivery of features.

---

*Developed by Rafia Kedir loper, Pro Dev Backend Cohort 2*

