# Computer Inventory Management System API Documentation

## Overview
The Computer Inventory Management System (CIMS) API allows users to manage computer inventory effectively. Users can add, update, delete, and view computer records.

## Base URL
```
https://api.example.com/v1
```

## Authentication
All requests to the API require authentication. Users must provide a valid API token in the `Authorization` header.

## Endpoints

### 1. Get All Computers
- **Endpoint:** `/computers`
- **Method:** `GET`
- **Description:** Retrieve a list of all computers in the inventory.
- **Response:**
  - 200 OK - Returns an array of computer objects.

### 2. Get Computer by ID
- **Endpoint:** `/computers/{id}`
- **Method:** `GET`
- **Description:** Retrieve a single computer by its ID.
- **Response:**
  - 200 OK - Returns a computer object.
  - 404 Not Found - If the specified ID does not exist.

### 3. Add a New Computer
- **Endpoint:** `/computers`
- **Method:** `POST`
- **Description:** Add a new computer to the inventory.
- **Request Body:**
  ```json
  {
    "name": "string",
    "brand": "string",
    "model": "string",
    "serial_number": "string"
  }
  ```
- **Response:**
  - 201 Created - Returns the created computer object.

### 4. Update Computer
- **Endpoint:** `/computers/{id}`
- **Method:** `PUT`
- **Description:** Update an existing computer's details.
- **Request Body:** (same structure as Add a New Computer)
- **Response:**
  - 200 OK - Returns the updated computer object.
  - 404 Not Found - If the specified ID does not exist.

### 5. Delete Computer
- **Endpoint:** `/computers/{id}`
- **Method:** `DELETE`
- **Description:** Deletes a computer from the inventory.
- **Response:**
  - 204 No Content - Successfully deleted.
  - 404 Not Found - If the specified ID does not exist.

## Error Handling
- The API returns standardized error messages. For example, a 400 Bad Request error will return:
  ```json
  {
    "error": "Invalid request"
  }
  ```

## Conclusion
This API provides a foundational approach to managing computer inventories programmatically. For further details, please refer to the specific endpoint documentation above.