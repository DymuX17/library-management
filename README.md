# Library Management System

## Overview

The **Library Management System** is a simple REST API application 
built with **Spring Boot** to manage a library's book collection. 
It allows users to perform basic operations such as adding books, 
retrieving a list of books, and borrowing books. 
The project is developed in 
Java and Spring Boot, focusing on modern technologies and 
best practices like dependency injection, RESTful APIs, 
and database integration.

This project demonstrates the following concepts:
- Building a REST API with Spring Boot.
- Using Spring Data JPA for database operations.
- Implementing a layered architecture (Model, Repository, Service, Controller).
- Configuring a PostgreSQL database with Docker.
- Managing sensitive configuration with a `.env` file.

## Features

- **Get All Books**: Retrieve a list of all books in the library (`GET /api/books`).
- **Add a Book**: Add a new book to the library (`POST /api/books`).
- **Borrow a Book**: Borrow a book by its ID, marking it as unavailable (`PUT /api/books/{id}/borrow`).
- **Database Integration**: Books are stored in a PostgreSQL database running in a Docker container.
- **Environment Configuration**: Sensitive data (e.g., database credentials) are stored in a `.env` file.

## Technologies Used

- **Java 17**: The programming language used for development.
- **Spring Boot 3.4.4**: Framework for building the REST API and managing dependencies.
- **Spring Data JPA**: For database operations and ORM (Object-Relational Mapping).
- **PostgreSQL**: Relational database to store book data.
- **Docker**: Used to run PostgreSQL in a containerized environment.
- **Lombok**: To reduce boilerplate code (e.g., getters, setters).
- **Maven**: Dependency management and build tool.
- **Spring Dotenv**: To load environment variables from a `.env` file.

## Project Structure

The project follows a layered architecture for better organization and maintainability:

- **Model (`com.example.librarymanagement.model`)**: Contains the `Book` entity class, which represents a book in the library.
- **Repository (`com.example.librarymanagement.repository`)**: Contains the `BookRepository` interface for database operations.
- **Service (`com.example.librarymanagement.service`)**: Contains the `BookService` class, which implements the business logic.
- **Controller (`com.example.librarymanagement.controller`)**: Contains the `BookController` class, which handles HTTP requests and responses.

## Prerequisites

Before running the project, ensure you have the following installed:

- **Java 17** (or higher): [Download JDK](https://adoptium.net/)
- **Docker Desktop**: [Download Docker](https://www.docker.com/products/docker-desktop/)
- **IntelliJ IDEA** (or another IDE): [Download IntelliJ](https://www.jetbrains.com/idea/download/)
- **Postman** (for testing the API): [Download Postman](https://www.postman.com/downloads/)
- **Maven**: Usually bundled with IntelliJ, but you can download it separately if needed.

## Setup and Installation

### 1. Clone the Repository
Clone this repository to your local machine:

```bash
git clone https://github.com/your-username/library-management.git
cd library-management