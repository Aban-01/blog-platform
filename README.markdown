# Simple Blogging Platform Backend

A backend for a simple blogging platform built as part of the "Backend Beginner Level Assignment No. 1" for Bridge Engineers. This project uses Node.js, Express.js, and MongoDB to create a REST API for managing users and blog posts, with JWT-based authentication and role-based permissions.

## Table of Contents
- [Overview](#overview)
- [Tech Stack](#tech-stack)
- [Setup Instructions](#setup-instructions)
- [API Endpoints](#api-endpoints)
- [Features](#features)
- [User Roles and Permissions](#user-roles-and-permissions)
- [Testing](#testing)
- [Troubleshooting](#troubleshooting)

## Overview
This project is a backend for a blogging platform where users can register, log in, and perform CRUD operations (create, read, update, delete) on blog posts. It includes user authentication using JSON Web Tokens (JWT) and enforces role-based permissions (e.g., users can only edit/delete their own posts unless they are admins).

## Tech Stack
- **Node.js**: JavaScript runtime for server-side development.
- **Express.js**: Web framework for building the REST API.
- **MongoDB**: NoSQL database for storing users and posts.
- **Mongoose**: ODM library for MongoDB to define schemas and interact with the database.
- **jsonwebtoken**: For user authentication and authorization.
- **bcryptjs**: For hashing passwords.
- **dotenv**: For managing environment variables.
- **cors**: To enable cross-origin requests.

## Setup Instructions
Follow these steps to set up and run the project locally.

### Prerequisites
- Node.js (v22.14.0 or later)
- npm (v11.3.0 or later)
- MongoDB (v8.0 or later)

### Installation
1. **Clone the Repository** (if applicable):
   ```bash
   git clone <repository-url>
   cd blog-platform
   ```
   Alternatively, if you have the project files locally, navigate to the project directory:
   ```bash
   cd C:\path\to\blog-platform
   ```

2. **Install Dependencies**:
   ```bash
   npm install
   ```

3. **Set Up MongoDB**:
   - Ensure MongoDB is installed and running on your machine.
   - On Windows, if installed as a service, start it:
     ```bash
     net start MongoDB
     ```
     (Run this in a Command Prompt with administrator privileges.)
   - Verify MongoDB is running on the default port `27017`:
     ```bash
     mongosh
     show dbs
     ```

4. **Configure Environment Variables**:
   - Create a `.env` file in the project root:
     ```bash
     echo > .env
     ```
   - Add the following environment variables to `.env`:
     ```
     PORT=3000
     MONGO_URI=mongodb://localhost:27017/blog