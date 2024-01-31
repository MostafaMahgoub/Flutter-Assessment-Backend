# Strapi API for Flutter - Assessment

## Overview

This outlines the setup and usage of the Strapi API locally for the Frontend Assessment. The API includes various endpoints for managing user data and content.

## Setup and Running Strapi API Locally

### Prerequisites

- Node.js (Refer to the [Node.js website](https://nodejs.org/) for installation)
- npm (Usually comes with Node.js installation)
- Strapi (Install Strapi globally for this project)

### Installation

1. **Clone the repository:**
   ```
   git clone https://github.com/DigiFly-Development/Flutter-Assessment-Backend.git
   ```
2. **Navigate to the project directory:**
   ```
   cd Flutter-Assessment-Backend
   ```
3. **Install Strapi globally (if not installed):**
   ```
   npm install strapi -g
   ```
4. **Install project dependencies:**
   ```
   npm install
   ```
5. **Start the Strapi server in development mode:**
   ```
   strapi start
   ```

**Important Note:** If you face an issue while using `npm install` and receive a network error, you might need to delete the existing `node_modules` folder and rerun the `npm install` command.

## API Endpoints

### Content Management

- **`/data` (GET)**
  Retrieves content data.

  ```
  GET http://localhost:1337/data
  ```

- **`/data` (POST)**
  Submits new content data.
  ```
  POST http://localhost:1337/data
  ```
  **Request Body Format:**
  ```
  {
    "Title": "YourTitle",
    "Subtitle": "YourSubTitle"
  }
  ```

### Authentication

- **`/auth/local/register` (POST)**
  Registers a new user.

  ```
  POST http://localhost:1337/auth/local/register
  ```

  **Request Body Format:**

  ```
  {
    "username": "test",
    "email": "test@email.com",
    "password": "test"
  }
  ```

- **`/auth/local` (POST)**
  Authenticates a user and returns a JWT token.
  ```
  POST http://localhost:1337/auth/local
  ```
  **Request Body Format:**
  ```
  {
    "identifier": "email@email.com",
    "password": "YourPassword"
  }
  ```

## Testing the API

Use tools like Postman for making HTTP requests to the API endpoints.
