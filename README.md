# TodoApp with Express.js and MongoDB

A simple TodoApp built with Express.js and MongoDB, providing basic CRUD operations (Create, Read, Update, Delete) for managing tasks.

## Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/)
- [MongoDB](https://www.mongodb.com/)

## Getting Started

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd TodoApp-Express-MongoDB
   ```

2. **Install Dependencies**

   ```bash
   npm install
   ```

3. **Configure MongoDB**

   - Make sure your MongoDB server is up and running.
   - Update the MongoDB connection URL in `config.js` file if necessary.

4. **Start the Application**

   ```bash
   npm start
   ```

   The app will be running at `http://localhost:3000`.

## API Endpoints

### 1. **Get All Todos**

- **Endpoint:** `GET /todos`
- **Response:** Array of all todos.

### 2. **Get Todo by ID**

- **Endpoint:** `GET /todos/:id`
- **Response:** Todo with the specified ID.

### 3. **Create a Todo**

- **Endpoint:** `POST /todos`
- **Request Body:**
  ```json
  {
    "title": "Todo Title",
    "description": "Todo Description"
  }
  ```
- **Response:** Created Todo object.

### 4. **Update Todo**

- **Endpoint:** `PUT /todos/:id`
- **Request Body:**
  ```json
  {
    "title": "Updated Todo Title",
    "description": "Updated Todo Description"
  }
  ```
- **Response:** Updated Todo object.

### 5. **Delete Todo**

- **Endpoint:** `DELETE /todos/:id`
- **Response:** Success message.

## Sample Request (using cURL)

1. **Get All Todos:**

   ```bash
   curl http://localhost:3000/todos
   ```

2. **Get Todo by ID:**

   ```bash
   curl http://localhost:3000/todos/:id
   ```

3. **Create Todo:**

   ```bash
   curl -X POST -H "Content-Type: application/json" -d '{"title": "New Todo", "description": "Todo Description"}' http://localhost:3000/todos
   ```

4. **Update Todo:**

   ```bash
   curl -X PUT -H "Content-Type: application/json" -d '{"title": "Updated Todo", "description": "Updated Description"}' http://localhost:3000/todos/:id
   ```

5. **Delete Todo:**

   ```bash
   curl -X DELETE http://localhost:3000/todos/:id
   ```

## Technologies Used

- **Express.js:** Web framework for Node.js.
- **MongoDB:** NoSQL database for storing todo data.
- **Mongoose:** MongoDB object modeling for Node.js.
- **Body-parser:** Node.js body parsing middleware.
- **Nodemon:** Development utility that automatically restarts the server.
- **dotenv:** Loads environment variables from a `.env` file.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
