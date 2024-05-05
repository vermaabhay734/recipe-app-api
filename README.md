# Recipe API

This project implements a robust REST API for managing recipes using Django and Django REST Framework. It includes features for user authentication, CRUD operations for recipes, image uploading, and advanced filtering/search capabilities.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project serves as a virtual recipe box where users can create, store, and manage their favorite recipes. The API allows users to perform CRUD operations on recipes, upload images, and apply filters to search for specific recipes based on various criteria.

## Features

- User authentication and authorization (register, login, logout)
- Create, read, update, delete (CRUD) operations for recipes
- Image upload functionality for recipe images
- Filtering and searching recipes by title, ingredients, tags, etc.

## Technologies Used

- Python
- Django (3.2)
- Django REST Framework (3.12)
- Docker
- PostgreSQL

## Getting Started

### Prerequisites

Make sure you have the following prerequisites installed on your local machine:

- Python (version 3.6 or higher)
- Docker
- PostgreSQL

### Installation

1. Clone the repository:

   ```
   git clone https://github.com/your_username/recipe-api.git
   ```

2. Navigate to the project directory:

   ```
   cd recipe-api
   ```

3. Set up a virtual environment (optional but recommended):

   ```
   python -m venv venv
   source venv/bin/activate  # Activate the virtual environment (Linux/macOS)
   ```

4. Install dependencies:

   ```
   pip install -r requirements.txt
   ```

5. Set up environment variables:

   Create a `.env` file in the root directory and add the following:

   ```
   SECRET_KEY=your_secret_key_here
   DEBUG=True
   ```

6. Apply database migrations:

   ```
   python manage.py migrate
   ```

7. Run the development server:

   ```
   python manage.py runserver
   ```

## Usage

Once the server is running locally, you can interact with the API using tools like `curl`, `Postman`, or `httpie`. Refer to the [API Endpoints](#api-endpoints) section below for details on available endpoints and how to use them.

## API Endpoints

- **POST /api/auth/register/**: Register a new user
- **POST /api/auth/login/**: Obtain an authentication token (JWT) by providing credentials
- **POST /api/auth/logout/**: Invalidate the authentication token
- **GET /api/recipes/**: Retrieve a list of recipes
- **POST /api/recipes/**: Create a new recipe
- **GET /api/recipes/{id}/**: Retrieve details of a specific recipe
- **PUT /api/recipes/{id}/**: Update a recipe
- **DELETE /api/recipes/{id}/**: Delete a recipe
- **GET /api/recipes/search/**: Search recipes by title, ingredients, or tags

Refer to the Django REST Framework browsable API interface (`/api/`) for more details and interactive exploration of endpoints.

## Testing

To run tests for the project, use the following command:

```
python manage.py test
```

## Contributing

Contributions are welcome! Please follow the [contribution guidelines](CONTRIBUTING.md) for this project.

## License

This project is licensed under the [MIT License](LICENSE).
```
