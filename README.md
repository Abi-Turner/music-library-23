# Music Library Project

This project is a music library application that allows you to perform CRUD (Create, Read, Update, Delete) operations on artists and albums stored in a PostgreSQL database. It provides a set of functionalities to manage and organize music data.

## Installation

To use this project, follow the instructions below:

1. Clone the repository from [GitHub](https://github.com/your-repo-link).
2. Navigate to the project directory: `cd music-library-23`.
3. Install the dependencies by running `npm install`.

## Configuration

Before running the application, you need to configure the PostgreSQL database connection. Follow the steps below:

1. Create a `.env` file in the project's root directory.
2. Specify the database connection details in the `.env` file. Example:
   ```
   DB_HOST=localhost
   DB_PORT=5432
   DB_NAME=music_library
   DB_USER=your_username
   DB_PASSWORD=your_password
   ```

## Docker Setup

This project uses Docker to run the PostgreSQL database. Make sure you have Docker installed on your machine before proceeding with the steps below:

1. Build the Docker container by running the following command in the project's root directory:
   ```
   docker build -t music-library-23 .
   ```
2. Run the Docker container with the following command:
   ```
   docker run -p 5432:5432 -e POSTGRES_DB=music_library -e POSTGRES_USER=your_username -e POSTGRES_PASSWORD=your_password -d postgres
   ```
   Replace `your_username` and `your_password` with your desired credentials.

## Database Setup

Once the Docker container is running, you can set up the database by running the following command:

```
npm run migrate
```

This command will create the necessary tables in the PostgreSQL database.

## Usage

To start the application, run the following command:

```
npm start
```

The application will be accessible at `http://localhost:3000`.

## API Endpoints

The following API endpoints are available for performing CRUD operations on the music library:

- `GET /artists`: Retrieves a list of all artists.
- `GET /artists/:id`: Retrieves an artist by ID.
- `POST /artists`: Creates a new artist.
- `PUT /artists/:id`: Updates an existing artist.
- `DELETE /artists/:id`: Deletes an artist by ID.

- `GET /albums`: Retrieves a list of all albums.
- `GET /albums/:id`: Retrieves an album by ID.
- `POST /albums`: Creates a new album.
- `PUT /albums/:id`: Updates an existing album.
- `DELETE /albums/:id`: Deletes an album by ID.

## Testing

This project includes unit tests to ensure the correctness of the implemented CRUD functionality. To run the tests, use the following command:

```
npm test
```

## Dependencies

The project uses the following dependencies:

- [Express](https://www.npmjs.com/package/express): A fast and minimalist web framework for Node.js.
- [pg](https://www.npmjs.com/package/pg): A PostgreSQL client for Node.js.
- [postgres-migrations](https://www.npmjs.com/package/postgres-migrations): A module for running database migrations for PostgreSQL.
- [chai](https://www.npmjs.com/package/chai): A BDD/TDD assertion library for Node.js.
- [dotenv](https://www.npmjs.com/package/dotenv): A zero-dependency module to load environment variables from a `.env` file.
- [eslint](https://www.npmjs.com/package/eslint): A tool for identifying and reporting on patterns found in ECMAScript/JavaScript code.
- [mocha](https://www.npmjs.com/package/mocha): A feature-rich JavaScript test framework.
- [nodemon](https://www.npmjs.com/package/nodemon): A utility that automatically restarts the Node.js application when file changes are detected.
- [supertest](https://www.npmjs.com/package/supertest): A library for testing HTTP servers.

## License

This project is licensed under the ISC License.
