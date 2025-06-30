# Project Overview
The Airbnb Clone Project is a full-stack application that mimics the core functionalities of Airbnb — a popular booking platform. This project focuses on backend development, database design, API security, and continuous deployment workflows. It’s designed to give hands-on experience with building scalable, secure, and maintainable software systems, using Django, MySQL, and GraphQL among other modern tools.

Team Roles
Backend Developer: Designs and implements the server-side logic, APIs, and database interactions to ensure smooth and secure data flow.

Database Administrator: Manages the database design, optimization, and maintenance to ensure data integrity and performance.

Frontend Developer: (Though not in scope here) Builds the user interface and client-side logic to interact with backend services.

DevOps Engineer: Sets up CI/CD pipelines and deployment processes to automate testing and deployment.

Project Manager: Oversees the project progress, manages timelines, and facilitates communication between team members.

Technology Stack
Django: Web framework used for building the backend APIs and managing application logic.

MySQL: Relational database system used to store and organize user data, properties, bookings, and reviews.

GraphQL: API query language that allows clients to request exactly the data they need.

Docker: Containerization tool to package the application and its dependencies for consistent deployment.

GitHub Actions: CI/CD platform to automate testing, building, and deployment processes.

Postman: Tool used for API testing and validation.

Database Design
Entities & Fields:
User: id, username, email, password_hash, profile_picture

Property: id, owner_id (User), title, description, location, price_per_night

Booking: id, user_id (User), property_id (Property), start_date, end_date, status

Review: id, user_id (User), property_id (Property), rating, comment, created_at

Payment: id, booking_id (Booking), amount, payment_date, payment_status

Relationships:
A User can own multiple Properties.

A Booking belongs to one Property and is made by one User.

A User can leave multiple Reviews on different Properties.

Each Booking has one associated Payment record.

Feature Breakdown
User Management: Allows users to register, log in, and manage their profiles securely.

Property Management: Enables property owners to list, update, and remove properties.

Booking System: Lets users book properties for specified dates and manage their bookings.

Review System: Users can leave feedback and rate properties they stayed in, enhancing community trust.

Payment Processing: Handles secure payment transactions linked to bookings.

API Security: Implements authentication, authorization, and input validation to protect user data.

CI/CD Pipeline: Automates testing and deployment to maintain code quality and speed up releases.
