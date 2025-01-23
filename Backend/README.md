# API Documentation

## User Registration Endpoint

### `POST /users/register`

Register a new user in the system.

### Request Body

```json
{
    "username": "string",
    "email": "string",
    "password": "string",
    "phone": "string"
}
```

### Required Fields

- `username`: User's display name (3-30 characters)
- `email`: Valid email address
- `password`: Password (minimum 6 characters)
- `phone`: Valid phone number

### Response Status Codes

- `201 Created`: User successfully registered
- `400 Bad Request`: Invalid input data
- `409 Conflict`: Email already exists
- `500 Internal Server Error`: Server error

### Example Response (Success)

```json
{
    "status": "success",
    "message": "User registered successfully",
    "data": {
        "id": "uuid",
        "username": "example_user",
        "email": "user@example.com"
    }
}
```

### Example Response (Error)

```json
{
    "status": "error",
    "message": "Email already exists"
}
```
