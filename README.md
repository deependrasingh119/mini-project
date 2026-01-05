# Full-Stack User Submission Application

This is a simple full-stack web application that allows users to submit their name and email, which are then stored and displayed in a list. The project demonstrates the end-to-end data flow between a React frontend and a Node.js/Express backend.

## Features

*   **User Submission Form:** A clean and simple form to submit user data (Name and Email).
*   **Client-Side Validation:** Basic required field validation on the frontend.
*   **Backend API:** A RESTful API built with Node.js and Express to handle data submission and retrieval.
*   **Server-Side Validation:** Ensures that name and email are valid before storing them.
*   **In-Memory Storage:** Uses a simple in-memory array on the backend for temporary data storage.
*   **Dynamic User List:** The list of submitted users updates in real-time after each submission.
*   **UI Feedback:** Provides users with loading, success, and error messages.

## Tech Stack

*   **Frontend:**
    *   [React.js](https://reactjs.org/)
    *   [Vite](https://vitejs.dev/)
    *   [Axios](https://axios-http.com/) for API requests
*   **Backend:**
    *   [Node.js](https://nodejs.org/)
    *   [Express.js](https://expressjs.com/)
    *   [CORS](https://expressjs.com/en/resources/middleware/cors.html)

## Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

*   [Node.js](https://nodejs.org/en/download/) (which includes npm) installed on your system.
*   A terminal or command-line interface.

### Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/deependrasingh119/mini-project.git
    cd mini-project
    ```

2.  **Set up the Backend:**
    Navigate to the backend directory and install the required npm packages.
    ```bash
    cd backend
    npm install
    ```

3.  **Set up the Frontend:**
    Navigate to the frontend directory and install the required npm packages.
    ```bash
    cd ../frontend/frontend
    npm install
    ```

### Running the Application

You will need to run the backend and frontend servers in two separate terminals.

1.  **Start the Backend Server:**
    In the `backend` directory, run:
    ```bash
    npm start
    ```
    The server will start on `http://localhost:5000`.

2.  **Start the Frontend Development Server:**
    In the `frontend/frontend` directory, run:
    ```bash
    npm run dev
    ```
    The application will be available at `http://localhost:5173` (or another port if 5173 is in use).

Open your browser and navigate to the frontend URL to use the application.

## API Endpoints

The backend server exposes the following REST API endpoints:

*   **`GET /api/users`**
    *   **Description:** Retrieves a list of all submitted users.
    *   **Response:** A JSON array of user objects.
    ```json
    [
      {
        "id": 1672939200000,
        "name": "John Doe",
        "email": "john.doe@example.com"
      }
    ]
    ```

*   **`POST /api/users`**
    *   **Description:** Creates and stores a new user.
    *   **Request Body:** A JSON object containing the user's name and email.
    ```json
    {
      "name": "Jane Doe",
      "email": "jane.doe@example.com"
    }
    ```
    *   **Success Response:** A JSON object of the newly created user with a status code of `201`.
    *   **Error Response:** A JSON object with an error message and a status code of `400` if validation fails.
