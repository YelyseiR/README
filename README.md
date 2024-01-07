# Java Quick Link App ![Java](https://cdn3.emoji.gg/emojis/java.png)
## Table of contents
* [About the project](#about-the-project)
* [Project requirements](#project-requirements)
* [How to start the project](#how-to-start-the-project)
* [About the team members](#about-the-team-members)

## About the project
This REST API project is being implemented for educational purposes at GoIT school, where we are learning how to work collaboratively in a team. We're building the entire project from scratch using Java and related development environments, including IntelliJ IDEA, PostgreSQL, Docker, GitHub, and more.
#### The main functions of the project:
-  Create a URL for your valid settlement.
- Edit/submit individual URLs.
- Ability to obtain conversion statistics for shorted URLs.
#### Technologies used:
- Spring Boot
- Spring Data
- PostgreSQL
- JWT
- FlyWay
- Swagger
- OpenApi 3.0
- Mockito
- CI pipeline (GitHub actions)
- Docker
- Docker-compose

## Project requirements
- There should be two launch profiles, default and prod https://www.baeldung.com/spring-profiles
- The default profile is set to run locally.
- Prod for the remote server (if available)
- The application must have a Dockerfile, and the local application startup (application + database) must be described in docker-compose.yml
- Database for tests should be run using https://java.testcontainers.org/
- All private information, such as login and password, to the database must be in the form of environment variables: ${DB_USERNAME}
 - Environment variables must be described in the README.md file
1. Registration and authentication of users

Registration:
- Verification of the uniqueness of the username.
- Password must contain at least 8 characters, including numbers, uppercase and lowercase letters.
- Storage of passwords in encrypted form.
 
Authentication:
- Checking the entered data for compliance with the data in the database.
- Upon successful authorization, return JWT (JSON Web Token), which will be used for further authentication.
 
2. Short reference
- It must contain a short link, the original one, the date of creation, the number of clicks on it and the user who created it.
- The link must have an expiration date.
 
3. Creating a short link
- Only a registered user can create a short link.
- The original link must be valid.
- The system should generate a new short link (6-8 random letters/numbers).
- Short and original link should be stored in the database according to the user.
4. User capabilities
- The user has the opportunity to view all created active links and their statistics.
- User can create new / delete existing link.


5. Follow the link
- Even a non-registered user can follow the shortened link.
- Statistics of transitions should be updated.
- The response must be cached.

## How to start the project
As it mentioned earlier, we use an environment variables in this project. So, before start the project be sure that you have build the project, set up the environment variables and created the variables.env file with all the necessary requirements.
`variables.env`



    DB_URL=your_custom_db_url
    DB_USERNAME=your_custom_username
    DB_PASSWORD=your_custom_password

Also, in order to start the project you need to generate `docker-image`

     docker build -t your-app-image .
     docker run --env-file=variables.env -p 9999:9999 your-app-image

## About the team members
### Andrii Protas 
- __[LinkedIn](https://www.linkedin.com/in/andriiiiiko/)__
- __[GitHub](https://github.com/andriiiiiko)__

### Vladyslav Malovanyi
- __[LinkedIn](https://www.linkedin.com/in/vladyslav-malovanyi-b1040b27b/)__
- __[GitHub](https://github.com/vldMlvn)__

### Diana Paievska
- __[LinkedIn]()__
- __[GitHub](https://github.com/paievska)__

### Yelysei Rodionov 
- __[LinkedIn](https://www.linkedin.com/in/yelysei-rodionov/)__
- __[GitHub](https://github.com/YelyseiR)__

### Team member
- __[LinkedIn]()__
- __[GitHub]()__

### Team member
- __[LinkedIn]()__
- __[GitHub]()__
### Team member
- __[LinkedIn]()__
- __[GitHub]()__
### Team member
- __[LinkedIn]()__
- __[GitHub]()__
