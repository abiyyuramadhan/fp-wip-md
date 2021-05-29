# {project-name} Backend Team B Homey
Hello there! Welcome to our playground. We're here for having fun.



## *Need to do*:
1. java openjdk version✔️
2. spring version✔️
3. gitignore inside
4. example of application.properties ✔️
5. folder purpose
6. design pattern what to choose?✔️
7. clean code especially naming conventions✔️
8. 1 class 1 method 1 purpose✔️
9. how auth will works?
10. getting started✔️
11. git flow✔️
12. credentials config✔️
13. database schema✔️ 
14. api docs✔️
15. docker command
16. project description✔️
17. folder structure ✔️
18. folder purpose
19. table of contents✔️
20. code style✔️

## What we're developing, {project-name}
description...

## Table of Contents
- [{project-name} Backend Team B Homey](#project-name-backend-team-b-homey)
  - [*Need to do*:](#need-to-do)
  - [What we're developing, {project-name}](#what-were-developing-project-name)
  - [Table of Contents](#table-of-contents)
  - [Tech Stack](#tech-stack)
  - [Git Work Flow](#git-work-flow)
    - [Clone Remote Repository](#clone-remote-repository)
    - [Create Branch](#create-branch)
    - [Add Changes](#add-changes)
    - [Commit Changes](#commit-changes)
    - [Read History](#read-history)
    - [Check Remote Repository](#check-remote-repository)
    - [Push Changes](#push-changes)
    - [Pull Changes](#pull-changes)
    - [Keep Up-to-date With Branch Develop](#keep-up-to-date-with-branch-develop)
    - [How to merge request](#how-to-merge-request)
  - [Code Style](#code-style)
  - [Credentials Configuration](#credentials-configuration)
    - [Inside application.properties](#inside-applicationproperties)
  - [Architecture Structure](#architecture-structure)
  - [Architecture Purpose](#architecture-purpose)
  - [Database Schema](#database-schema)
  - [API Documentation](#api-documentation)





## Tech Stack
- Java openjdk version 16, here for resources [Openjdk Archive](https://jdk.java.net/archive/)<br> Check if java version is openjdk:
```
java -version
```
- Spring version 2.5.0 with maven project
- Dependencies: 
   - Spring Web 
   - PostgreSQL
   - Spring Data JPA
   - Lombok 
   - Spring Security
   - JJWT
   - ModelMapper
   - Springfox Swagger


## Git Work Flow
### Clone Remote Repository
```bash
git clone {git-url}
```
### Create Branch
```bash
git checkout -b feature/{feature-name}
```
*Kindly remember to always create new feature and not making changes in branch develop*
### Add Changes
```bash
git add .
git add {file-name}
```
### Commit Changes
```bash
git commit -m "message"
```
### Read History
```bash
git log
```
### Check Remote Repository
```bash
git remote -v
```
### Push Changes
```bash
git push origin feature/{feature-name}
```
### Pull Changes
```bash
git pull develop
```
### Keep Up-to-date With Branch Develop
from branch feature:
```bash
git merge develop 
```
### How to merge request
- Create new merge request
- Select from `branch feature` into `branch develop`
- Fill title and description with meaningful explanation
- Select asignees as yours and reviewers as tech lead and backend facilitator
- Check mark✔️ *delete source branch when merge request is accepted*


## Code Style
We're free to code using clean architecture but kindly remember the code principles:<br>
- KISS (Keep It Simple Stupid) 
- DRY (Don't Repeat Yourself)
- Single Responsibility
- Separation of Concerns
- YAGNI (You Aren't Gonna Need It)
- Refactor


## Credentials Configuration
### Inside application.properties
File location: `src/main/resources/application.properties`
```properties
## Spring DATASOURCE (DataSourceAutoConfiguration & DataSourceProperties)
spring.datasource.url= jdbc:postgresql://localhost:5432/{database-name}
spring.datasource.username= {postgresql-username} 
spring.datasource.password= {postgresql-password}

# The SQL dialect makes Hibernate generate better SQL for the chosen database
spring.jpa.properties.hibernate.dialect = org.hibernate.dialect.PostgreSQLDialect

# Hibernate ddl auto (create, create-drop, validate, update)
spring.jpa.hibernate.ddl-auto= {create/create-drop/validate/update}

# JWT SECRET
jwt.secret= {jwt-secret}
```
*Kindly remember to add this to .gitignore, so it won't be push to our repository*


## Architecture Structure
```
├── .mvn/wrapper
├── src
|   ├── main
|   |   ├── java/com/projects
|   |   |   ├── controller
|   |   |   ├── model
|   |   |   ├── exception
|   |   |   ├── repository
|   |   |   ├── service
|   |   |   ├── util
|   |   ├── recources
|   |   |   ├── application.properties
|   ├── test/java/com/projects
```

## Architecture Purpose


## Database Schema
![](images/DB%20Banking%20Gamification.png)
For detail information, take a look at [Database Schema](https://dbdiagram.io/d/60a86e29b29a09603d16040e)


## API Documentation
We're using [Swagger For API Docs]({swagger-link}), look for further information



