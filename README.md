# JwtAuth

# JwtAuth

Welcome to JwtAuth! This repository provides a simple implementation of JSON Web Token (JWT) authentication in a web application based on Spring Boot.

## Installation

To get started with JwtAuth, follow these steps:

1. Clone the repository: `https://github.com/DCCXVII/JwtAuth.git`
2. Navigate to the project directory: `cd JwtAuth`
3. Install the dependencies: `mvn install`
4. Configure the environment variables: Create an `application.properties` file and set the following variables:

   - `spring.application.name`:
   - `spring.main.allow-circular-references`: true
   - `spring.datasource.driver-class-name`: com.mysql.cj.jdbc.Driver
   - `spring.datasource.url`: jdbc:mysql://localhost:3306/your-db-name
   - `spring.datasource.username`:
   - `spring.datasource.password`:
   - `spring.jpa.properties.hibernate.dialect`: org.hibernate.dialect.MySQLDialect
   - `spring.jpa.hibernate.naming.physical-strategy`: org.hibernate.boot.model.naming.PhysicalNamingStrategyStandardImpl
   - `spring.jpa.hibernate.ddl-auto`: update
   - `spring.jpa.show-sql`: true
   - `JWT_SECRET`: Secret key for JWT encryption
   - `DB_URL`: URL of your MongoDB database

5. Start the server: ` mvn spring-boot:run`

## Usage

Once the server is running, you can use the following endpoints:

## Endpoints

The following endpoints are available in JwtAuth:

- `GET /auth/welcome`: This endpoint is not secure and returns a welcome message.
- `POST /auth/addNewUser`: This endpoint is used to add a new user. It expects a JSON payload containing user information.
- `GET /auth/user/userProfile`: This endpoint is accessible only to users with the ROLE_USER authority. It returns a message for the user profile.
- `GET /auth/user/adminProfile`: This endpoint is accessible only to users with the ROLE_ADMIN authority. It returns a message for the admin profile.
- `POST /auth/generateToken`: This endpoint is used to authenticate a user and generate a JWT token. It expects a JSON payload containing the username and password.

Please note that the paths are relative to the base URL of your application.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.
