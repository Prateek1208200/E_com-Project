🛒 Ecom-Proj — Spring Boot E-Commerce API

A simple backend API for managing products in an e-commerce application. Built with Spring Boot 3.3.0, Java 21, and H2 in-memory database.

🚀 Features

Add, update, delete products with image upload

Fetch all products or a single product by ID

Serve product images via endpoint

Search products by keyword

Cross-origin support for frontend integration

📦 Tech Stack

Layer

Technology

Backend

Spring Boot 3.3.0

Language

Java 21

Database

H2 (in-memory)

ORM

Spring Data JPA

File Upload

MultipartFile support

Dev Tools

Spring Boot DevTools

Testing

Spring Boot Starter Test

📁 Project Structure

com.telusko.ecom_proj
├── controller
│   └── ProductController.java
├── service
│   └── ProductService.java
├── model
│   └── Product.java
├── repo
│   └── ProductRepo.java
└── EcomProjApplication.java

🔧 API Endpoints

Product Operations

Method

Endpoint

Description

GET

/api/products

Get all products

GET

/api/product/{id}

Get product by ID

POST

/api/product

Add new product with image

PUT

/api/product/{id}

Update product and image

DELETE

/api/product/{id}

Delete product by ID

GET

/api/product/{id}/image

Get image of product by ID

GET

/api/products/search?keyword=...

Search products by keyword

🖼️ Image Handling

Images are uploaded via MultipartFile and stored as byte arrays in the database.

Image metadata includes name and MIME type.

Served via /api/product/{id}/image with correct content type.

🧪 Run Locally

Prerequisites

Java 21+

Maven

Steps

Access API at: http://localhost:8080/api

🧰 Useful Maven Commands

mvn clean install       # Build the project
mvn spring-boot:run     # Run the application
mvn test                # Run tests

📝 Notes

Uses H2 database for development. Switch to MySQL/PostgreSQL for production.

Enable CORS for frontend integration.

Lombok is included for cleaner model code (optional).

