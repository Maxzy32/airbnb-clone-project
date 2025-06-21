# airbnb-clone-project

## 📌 Overview

The **AirBnB Clone Project** is a full-stack web application that replicates key features of the AirBnB platform. It is intended for learning purposes and demonstrates knowledge of web development, backend services, UI/UX design, and database integration.

## 🎯 Project Goals

- Recreate the core functionality of the AirBnB website
- Implement user authentication and profile management
- Build listing pages for hosts and browsing pages for guests
- Allow users to book, manage, and review stays
- Practice version control and collaborative development

## 🛠️ Tech Stack

- **Frontend:** HTML5, CSS3, JavaScript (React.js recommended)
- **Backend:** Python (Flask or Django) / Node.js (Express)
- **Database:** MySQL / PostgreSQL / MongoDB
- **Version Control:** Git and GitHub
- **Deployment:** GitHub Pages / Heroku / Render / Vercel



## 👥 Team Roles

In a real-world software development project like the AirBnB Clone, each team member plays a critical role in ensuring the project's success. Below are the key roles and their responsibilities:

### 🔧 Backend Developer
Responsible for building the server-side logic, APIs, and handling authentication, user sessions, data processing, and integration with the database.

### 🎨 Frontend Developer
Designs and implements the user interface of the application using technologies like HTML, CSS, JavaScript, and frameworks such as React.js. Ensures the app is responsive and user-friendly.

### 🛢️ Database Administrator (DBA)
Designs and manages the database structure, ensures data integrity, optimizes queries, and handles data backup and recovery processes.

### 📦 DevOps Engineer
Manages deployment, CI/CD pipelines, and cloud infrastructure. Ensures that the application runs smoothly in staging and production environments.

### 🔍 QA Engineer / Tester
Creates test cases and runs manual or automated tests to identify bugs. Ensures the application meets quality standards before deployment.

### 🧠 Project Manager
Coordinates the team, manages timelines, ensures everyone is aligned with the project goals, and communicates progress with stakeholders.

### 🎯 UI/UX Designer
Creates wireframes, prototypes, and user journey maps. Ensures that the design is both visually appealing and easy to use.


## 🧰 Technology Stack

Below is a list of technologies used in the AirBnB Clone Project along with their purposes:

### 🐍 Django
A high-level Python web framework that simplifies the process of building secure and maintainable backends. It is used to create RESTful APIs and manage server-side logic.

### 🐘 PostgreSQL
An advanced open-source relational database system. It stores user data, property listings, bookings, reviews, and more.

### ⚛️ React.js
A JavaScript library for building fast and interactive user interfaces. It manages the frontend components and handles routing, forms, and state management.

### 🎨 Tailwind CSS
A utility-first CSS framework that helps in designing modern and responsive interfaces quickly with pre-built utility classes.

### 🔁 GraphQL
An API query language used to request only the needed data from the server, improving performance and flexibility compared to traditional REST APIs.

### 🐙 Git & GitHub
Version control and collaboration tools used to manage source code changes, coordinate teamwork, and store the project repository.

### 🚀 Vercel / Heroku / Render
Cloud platforms used to deploy and host the frontend and backend services, making the project accessible online.


## 🗃️ Database Design

The database schema for the AirBnB Clone Project is designed to support user interaction, property listings, and transactions. Below are the key entities and their fields:

### 👤 Users
Stores information about all registered users.

- `id` (Primary Key)
- `name`
- `email`
- `password_hash`
- `role` (host or guest)

### 🏠 Properties
Stores details about properties listed by hosts.

- `id` (Primary Key)
- `user_id` (Foreign Key referencing Users)
- `title`
- `description`
- `location`
- `price_per_night`

### 📅 Bookings
Tracks reservations made by guests.

- `id` (Primary Key)
- `user_id` (Foreign Key referencing Users)
- `property_id` (Foreign Key referencing Properties)
- `check_in_date`
- `check_out_date`
- `total_price`

### 💬 Reviews
Allows guests to leave feedback on properties they have booked.

- `id` (Primary Key)
- `user_id` (Foreign Key referencing Users)
- `property_id` (Foreign Key referencing Properties)
- `rating` (1 to 5)
- `comment`

### 💳 Payments
Records payment transactions for bookings.

- `id` (Primary Key)
- `booking_id` (Foreign Key referencing Bookings)
- `payment_date`
- `amount`
- `payment_method` (e.g., card, PayPal)

### 🔗 Entity Relationships

- A **User** can be a **host** (who owns properties) or a **guest** (who makes bookings).
- A **User** can have many **Bookings** and **Reviews**.
- A **Property** belongs to one **User** (the host), but can have many **Bookings** and **Reviews**.
- A **Booking** belongs to one **User** and one **Property**.
- A **Payment** is linked to a **Booking**.

