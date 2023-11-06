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

### 1. **Get All Todos:**

- **Method:** GET
- **URL:** `http://localhost:3000/ap1/v1/getTodos`

### 2. **Get Todo by ID:**

- **Method:** GET
- **URL:** `http://localhost:3000/ap1/v1/getTodos:id`

### 3. **Create Todo:**

- **Method:** POST
- **URL:** `http://localhost:3000/ap1/v1/createTodo`
- **Body:**
  ```json
  {
    "title": "New Todo",
    "description": "Todo Description"
  }
  ```
- **Headers:**
  - `Content-Type: application/json`

### 4. **Update Todo:**

- **Method:** PUT
- **URL:** `http://localhost:3000/api/v1/updateTodo/:id`
- **Body:**
  ```json
  {
    "title": "Updated Todo",
    "description": "Updated Description"
  }
  ```
- **Headers:**
  - `Content-Type: application/json`

### 5. **Delete Todo:**

- **Method:** DELETE
- **URL:** `http://localhost:3000/api/v1/deleteTodo/:id`

In Postman, you can select the appropriate HTTP method from the dropdown menu, enter the URL, set the request body and headers accordingly, and then click "Send" to make the request.

## Technologies Used

- **Express.js:** Web framework for Node.js.
- **MongoDB:** NoSQL database for storing todo data.
- **Mongoose:** MongoDB object modeling for Node.js.
- **Body-parser:** Node.js body parsing middleware.
- **Nodemon:** Development utility that automatically restarts the server.
- **dotenv:** Loads environment variables from a `.env` file.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
