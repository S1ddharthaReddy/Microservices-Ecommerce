# Full-Stack E-Commerce Application with Microservices Architecture

A robust, full-stack e-commerce platform built using a **Microservices Architecture**. This project is designed to demonstrate modern distributed system patterns, inter-service communication, and asynchronous event-driven architecture.


## Tech Stack

Backend: Node.js / Express

Databases: MongoDB, PostgreSQL

Message Broker / Event Bus: Apache Kafka

Frontend: React.js / Next.js / Tailwind CSS

## Architecture & Services

The application is broken down into multiple independent microservices, ensuring high scalability, fault tolerance, and clear separation of concerns:
```
                  ┌────────────────────────┐
                  │      API Gateway       │
                  └───────────┬────────────┘
                              │
         ┌────────────────────┼────────────────────┐
         │                    │                    │
         ▼                    ▼                    ▼
┌─────────────────┐  ┌─────────────────┐  ┌─────────────────┐
│  Auth Service   │  │ Product Service │  │  Order Service  │
└─────────────────┘  └─────────────────┘  └─────────────────┘
         │                    │                    │
         └────────────────────┼────────────────────┘
                              ▼
                  ┌───────────────────────┐
                  │ Event Bus / Broker    │
                  └───────────────────────┘
