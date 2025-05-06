# JSON Server Backend

This is a simple JSON Server backend for a book library application, built using Node.js and the `json-server` package.

## Features

- Serves data from a `db.json` file.
- Includes middleware to disable CORS, allowing requests from any origin.
- Uses `morgan` for request logging.
- Configurable port via `.env` file or defaults to 5005.

## Setup

1.  **Install dependencies:**

    ```bash
    npm install json-server morgan dotenv
    ```

2.  **Create a `.env` file** (optional) to configure the port:

    ```
    PORT=5005
    ```

3.  **Create a `db.json` file** with your data. Example:

    ```json
    {
      "books": [
        { "id": 1, "title": "The Great Gatsby", "author": "F. Scott Fitzgerald" },
        { "id": 2, "title": "To Kill a Mockingbird", "author": "Harper Lee" }
      ]
    }
    ```

## Usage

1.  **Start the server:**

    ```bash
    node app.js
    ```

    or

    ```bash
    npm start
    ```

2.  **Access the data** via the following endpoints:

    -   `GET /books` - Get all books
    -   `GET /books/:id` - Get a specific book by ID
    -   `POST /books` - Create a new book
    -   `PUT /books/:id` - Update an existing book
    -   `DELETE /books/:id` - Delete a book

## Dependencies

-   `json-server`: For creating a REST API from a JSON file.
-   `morgan`: For request logging.
-   `dotenv`: For loading environment variables from a `.env` file.
