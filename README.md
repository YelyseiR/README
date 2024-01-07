
# Java Quick Link App ![Java](https://cdn3.emoji.gg/emojis/java.png)
## Table of contents
* [About the project](#about-the-project)
* [Project requirements](#project-requirements)
* [How to start the project](#how-to-start-the-project)
* [About team](#about-team)

## About the project
This REST API project is implemented for educational purposes in GoIT school were we learning on how to work in team, how to build a whole project from zero using java and related development environment in order to build this project, such as: IntelijIdea, PostgreSQL, Docker, GitHub, etc. 
#### The main functions of the project:
-  Create a URL for your valid settlement.
- Edit/submit individual URLs.
- Ability to obtain conversion statistics for high-speed URLs.
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
