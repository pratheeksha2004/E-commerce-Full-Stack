# E-commerce Full-Stack Application

This is a full-stack e-commerce application built with a modern tech stack. It showcases a user-friendly frontend experience with a robust and scalable backend architecture.

## Technologies Used

**Frontend:**

*   **React:** A JavaScript library for building user interfaces.
*   **Vite:** A fast, opinionated build tool that provides blazing-fast development experience.
*   **Tailwind CSS:** A utility-first CSS framework for rapidly building custom designs.

**Backend:**

*   **Spring Boot:** A Java-based framework for building microservices and web applications.
*   **PostgreSQL:** A powerful, open-source object-relational database system.

## Features

*   **User Authentication:** Secure user registration, login, and logout functionality.
*   **Product Catalog:** Browse and search through a wide variety of products.
*   **Shopping Cart:** Add, remove, and manage items in a shopping cart.
*   **Checkout Process:** Secure and seamless checkout experience with order placement.
*   **Responsive Design:** Optimized for viewing on various devices (desktops, tablets, and mobile phones).

## Setup Instructions

Follow these instructions to set up and run the application locally.

### Prerequisites

*   **Node.js:** (Version >= 16 recommended). Download from [https://nodejs.org/](https://nodejs.org/)
*   **npm or Yarn:** (Package manager for frontend dependencies).  npm comes with Node.js. Yarn: `npm install --global yarn`
*   **Java Development Kit (JDK):** (Version >= 11 recommended). Download from [https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html) (or a distribution like OpenJDK)
*   **PostgreSQL:** Download and install from [https://www.postgresql.org/download/](https://www.postgresql.org/download/)
*   **IntelliJ IDEA or Eclipse (Recommended):** For backend development (Spring Boot).

### Frontend Setup

1.  **Navigate to the frontend directory:**
    ```bash
    cd frontend
    ```

2.  **Install dependencies:**
    ```bash
    npm install   # or yarn install
    ```

3.  **Configure environment variables:**
    *   Create a `.env` file in the `frontend` directory.
    *   Add the necessary environment variables (e.g., API endpoint for the backend).  Example:
        ```
        VITE_API_BASE_URL=http://localhost:8080
        ```

4.  **Start the development server:**
    ```bash
    npm run dev   # or yarn dev
    ```

    The frontend application will be running at `http://localhost:3000` (or the port Vite assigns).

### Backend Setup

1.  **Navigate to the backend directory:**
    ```bash
    cd backend
    ```

2.  **Configure PostgreSQL:**
    *   Create a PostgreSQL database for your application.
    *   Update the `src/main/resources/application.properties` or `application.yml` file with your database credentials:

        ```properties
        spring.datasource.url=jdbc:postgresql://localhost:5432/your_database_name
        spring.datasource.username=your_username
        spring.datasource.password=your_password
        spring.jpa.hibernate.ddl-auto=update  # Use 'create' for the first run, then 'update' or 'none'
        ```
        (Adjust the properties based on your actual configuration file and database setup.)

3.  **Build and run the Spring Boot application:**

    *   **Using IntelliJ IDEA or Eclipse:** Import the `backend` directory as a Maven or Gradle project and run the main application class.
    *   **From the command line:**
        ```bash
        ./mvnw spring-boot:run  # If using Maven
        ./gradlew bootRun       # If using Gradle
        ```

    The backend application will be running at `http://localhost:8080` (or the port you configured).

## Environment Variables

*   **Frontend:**  Create a `.env` file in the `frontend` directory.  Common variables:
    *   `VITE_API_BASE_URL`: The URL of your backend API.
*   **Backend:**  Set environment variables or configure them in `application.properties` or `application.yml`.  Important variables:
    *   `spring.datasource.url`, `spring.datasource.username`, `spring.datasource.password`: Database connection details.
    *   (Any other API keys or secrets).  *Never commit these directly to your repository!*
