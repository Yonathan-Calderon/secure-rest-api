# Secure Rest API 

A custom-built REST API for production with protected routes. This API allows you to manage products and users with role-based access.

## Table of Contents

- [Description](#description)
- [Routes](#routes)
- [Postman Collection](#postman-collection)
- [Installation](#installation)
- [Usage](#usage)
- [Environment Variables](#environment-variables)
- [Dependencies](#dependencies)

## Description

This repository contains a detailed overview of a custom-built REST API named "Rest API Dev". The API includes authentication routes, product management, and user roles. Explore the features, capabilities, and how it can empower your applications.

## Routes

### Auth Routes

#### Sign Up
- Endpoint: `/api/auth/signup`
- Method: `POST`
- Create a new user account with roles.

#### Sign In
- Endpoint: `/api/auth/signin`
- Method: `POST`
- Authenticate and sign in a user.

### Index Route

#### API Overview
- Endpoint: `/api`
- Method: `GET`
- Retrieve information about the API.

### Products Routes

#### Get Products
- Endpoint: `/api/products`
- Method: `GET`
- Retrieve a list of products.

#### Get Product by ID
- Endpoint: `/api/products/:productId`
- Method: `GET`
- Retrieve a specific product by ID.

#### Create Product
- Endpoint: `/api/products`
- Method: `POST`
- Create a new product (requires moderator role).

#### Update Product by ID
- Endpoint: `/api/products/:productId`
- Method: `PUT`
- Update a product by ID (requires moderator role).

#### Delete Product by ID
- Endpoint: `/api/products/:productId`
- Method: `DELETE`
- Delete a product by ID (requires admin role).

### User Routes

#### Create User
- Endpoint: `/api/users`
- Method: `POST`
- Create a new user (requires admin role).

## Postman Collection

Explore the [Postman Collection](./postman_collection.json) for easy API testing.

## Installation

1. Clone the repository: `https://github.com/Yonathan-Calderon/secure-rest-api.git`
2. Install dependencies: `npm install`

## Usage

1. Run the development server: `npm run dev`
2. Access the API at `http://localhost:4000/api`

## Dependencies

1. bcryptjs: Password hashing.
2. cors: Cross-Origin Resource Sharing middleware.
3. dotenv: Environment variable management.
4. express: Web application framework.
5. helmet: Security middleware.
6. jsonwebtoken: JSON Web Token authentication.
7. mongoose: MongoDB object modeling.
8. morgan: HTTP request logger.

## Environment Variables

Create a `.env` file based on the provided `.env.example` to set up your environment variables.

```plaintext
MONGODB_URI=mongodb://127.0.0.1/apicompany
PORT=4000
SECRET=yoursecretkey
ADMIN_EMAIL=admin@localhost
ADMIN_USERNAME=admin
ADMIN_PASSWORD=admin

