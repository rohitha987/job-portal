

### Dummy Data for Endpoints

#### 1. **Register User Endpoint**
- **Endpoint**: `POST /register`
- **Description**: Registers a new user.
- **Sample Request Body**:
  ```json
  {
    "username": "john_doe",
    "email": "john@example.com",
    "password": "securePassword123"
  }
  ```
- **Sample Response**:
  ```json
  {
    "_id": "60c72b2f5f1b2c001c123456",
    "username": "john_doe",
    "email": "john@example.com",
    "appliedJobs": [],
    "createdAt": "2023-01-01T00:00:00.000Z",
    "updatedAt": "2023-01-01T00:00:00.000Z"
  }
  ```

#### 2. **Apply for Job Endpoint**
- **Endpoint**: `POST /:userId/apply`
- **Description**: Allows a user to apply for a job.
- **Sample Request Body**:
  ```json
  {
    "jobId": 12345
  }
  ```
- **Sample Response**:
  ```json
  {
    "_id": "60c72b2f5f1b2c001c123456",
    "username": "john_doe",
    "email": "john@example.com",
    "appliedJobs": [
      {
        "jobId": 12345,
        "appliedAt": "2023-01-01T00:00:00.000Z"
      }
    ],
    "createdAt": "2023-01-01T00:00:00.000Z",
    "updatedAt": "2023-01-01T00:00:00.000Z"
  }
  ```

#### 3. **Get User Applications Endpoint**
- **Endpoint**: `GET /:userId/applications`
- **Description**: Retrieves a list of jobs the user has applied for.
- **Sample Response**:
  ```json
  [
    {
      "jobId": 12345,
      "appliedAt": "2023-01-01T00:00:00.000Z"
    }
  ]
  ```

