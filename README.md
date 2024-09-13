
# CarX - Car Rental API

## Links:
- [Website](https://carxapp.org/)
- [API Docs](https://carxapp.org/api/v1/docs)
- [Frontend Repo](https://github.com/amir-yari/CarX-frontend)
- [Backend Repo](https://github.com/hassan-attar/CarX-API)

## Overview

CarX is a car-sharing Platform designed to function like Turo, offering a seamless platform for users to find, book, and manage car rentals. With CarX, users can browse a wide range of available vehicles, select their desired car, and book it for their next trip. Each reservation is tracked as a trip within the system, allowing users to manage their rentals efficiently. The App integrates with Stripe for secure and reliable payment processing, ensuring a smooth checkout experience for all transactions.

## Features

- **Car Listings**: Retrieve a list of available cars based on filters such as availability dates, location, and price range.
- **Car Details**: Get detailed information about specific cars.
- **User Authentication**: Sign up, log in, and manage user sessions.
- **User Accounts**: Update and retrieve user profile information.
- **Trip Management**: Book, manage, and view trips.
- **Payment Processing**: Create and manage Stripe checkout sessions, and view payment history.

## Development

### Team

- **Hassan Attar**: Backend & DevOps Engineer
    - Developed the backend API, database, and business logic.
    - Created and managed the development environment with containers simulating the production environment.
    - Containerized and deployed the application to its own cluster on AWS.

- **Amir**: Frontend Engineer
    - Developed a responsive and user-friendly UI ensuring smooth navigation and interaction for car owners and renters, while maintaining consistency across various devices and screen sizes.
    - Collaborated closely with the backend team to integrate the API, handling real-time data fetching for car listings, booking, and user management.
    - Implemented a seamless booking flow, enhancing the user experience with features like trip tracking, reservation management, and intuitive search functionality.


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
