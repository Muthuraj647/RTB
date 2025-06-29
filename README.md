# 🚆 Railway Ticket Booking System (RTB)

A fullstack web application that allows users to search trains, book tickets, and manage bookings. Built using Spring Boot, React, and MySQL with CI/CD via Jenkins and deployed on Kubernetes hosted on AWS.

---

## 📋 Features

- User registration and login
- Train search by source, destination, and date
- Complex Availability check
- Ticket booking and cancellation
- View booking history
- Payment Gateway
- Admin portal to manage trains and stations
- Secure REST APIs (JWT based)
- Responsive frontend interface

---

## 🏗️ Tech Stack

| Layer        | Technology         |
|--------------|--------------------|
| Frontend     | React              |
| Backend      | Spring Boot (Java) |
| Database     | MySQL              |
| CI/CD        | Jenkins + GitHub   |
| Deployment   | Kubernetes         |

---

## Microservices

| # | Microservice                | Responsibility                                             |
| - | --------------------------- | ---------------------------------------------------------- |
| 1 | **User Service**            | Register, login, auth, roles                               |
| 2 | **Train Service**           | Trains, stations, routes, schedules                        |
| 3 | **Booking Service**         | Booking logic, interaction with Inventory, Payment, Ticket |
| 4 | **Ticket Service**          | Ticket generation, history, cancellation                   |
| 5 | **Inventory Service**       | Track real-time seat availability                          |
| 6 | **Payment Service**         | Process mock payments, confirm booking                     |
| 7 | **Notification Service**    | Send emails/SMS after booking/cancellation                 |
| 8 | **Auth Gateway (Optional)** | API Gateway or auth proxy (Spring Cloud Gateway or NGINX)  |

---

## 🧠 Project Design

- 📄 [Requirements](./docs/Requirements.md) 
- 📄 [High Level Design (HLD)](./docs/HLD.md)
- 📄 [Low Level Design (LLD)](./docs/LLD.md)
- 📄 [API Documentation (Swagger)](http://localhost:8080/swagger-ui.html)

---

## 🚀 Running the Project Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/railway-ticket-booking.git
