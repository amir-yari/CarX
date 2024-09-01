
# CarX - Car Rental API

## Overview

CarX is a car-sharing API designed to function like Turo, offering a seamless platform for users to find, book, and manage car rentals. With CarX, users can browse a wide range of available vehicles, select their desired car, and book it for their next trip. Each reservation is tracked as a trip within the system, allowing users to manage their rentals efficiently. The API integrates with Stripe for secure and reliable payment processing, ensuring a smooth checkout experience for all transactions.

> This project demonstrates my capability to develop a sophisticated application from scratch and integrate it with other services, such as Stripe. I have standardized the API to help developers and clients by using consistent formats for data, such as dates and country codes. Through this project, I have also honed my skills in collaborating on design, effectively communicating deadlines, and managing the end-to-end development process.

## Features

- **Car Listings**: Retrieve a list of available cars based on filters such as availability dates, location, and price range.
- **Car Details**: Get detailed information about specific cars.
- **User Authentication**: Sign up, log in, and manage user sessions.
- **User Accounts**: Update and retrieve user profile information.
- **Trip Management**: Book, manage, and view trips.
- **Payment Processing**: Create and manage Stripe checkout sessions, view payment history.

**API Documentation: [API Docs](https://carx.hassan-attar.com/api/v1/docs)**

## Development

### Team

- **Hassan Attar**: Backend & DevOps Engineer
    - Developed the backend API, database, and business logic.
    - Created and managed the development environment with containers simulating the production environment.
    - Containerized and deployed the application to its own cluster on AWS.

- **Amir**: Frontend Engineer
    - Developed the UI and web app.
    - Integrated and served the API to the end user.


### Development Setup

*The code changes will reflect instantly on both frontend and backend code since volumes are mounted correctly to reflect the latest source code in the containers. React Hot Module Replacement (HMR) and sockets are set up and configured in Nginx and Vite, making development in this environment a breeze.*

To run the project locally, follow these steps:

1. **Ensure Docker is Installed**

   Make sure you have Docker installed on your machine. If not, you can download and install Docker from the [official Docker website](https://www.docker.com/).

2. **Clone the Repository**

   Clone the repository and fetch all submodules:

   ```bash
   git clone --recurse-submodules https://github.com/hassan-attar/CarX
   ```

3. **Build and Start the Project**

   Navigate to the project directory and build the containers:

   ```bash
   cd CarX
   npm run build-start
   ```

   This command will build the Docker containers and start them in detached mode using the `dev.docker-compose.yml` configuration.

4. **Running Commands**

    - **Start Containers**: If you have already built the containers, you can start them with:

      ```bash
      npm start
      ```

    - **Stop Containers**: To stop the running containers, use:

      ```bash
      npm run stop
      ```

    - **Destroy and Stop Containers**: To stop and remove the containers:

      ```bash
      npm run destroy-stop
      ```

    - **Clean Database (App)**: To clean the app database:

      ```bash
      npm run clean-db:app
      ```

    - **Clean Database with Data (App)**: To clean the app database and load sample data:

      ```bash
      npm run clean-db-with-data:app
      ```

    - **Clean Database (Auth)**: To clean the auth database:

      ```bash
      npm run clean-db:auth
      ```

    - **Clean Database with Data (Auth)**: To clean the auth database and load sample data:

      ```bash
      npm run clean-db-with-data:auth
      ```

## License

CarX is licensed under the [MIT License](LICENSE).
