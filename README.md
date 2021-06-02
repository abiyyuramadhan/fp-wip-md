# Monola Backend Team B Homey
Hello there! Welcome to our playground. We're here for having fun.




## What we're developing, Monola
Description loading...

## Table of Contents
- [Monola Backend Team B Homey](#monola-backend-team-b-homey)
  - [What we're developing, Monola](#what-were-developing-monola)
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
    - [Integrate Changes Between Branches](#integrate-changes-between-branches)
    - [How to Merge Request](#how-to-merge-request)
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
For branch feature: `feature/{feature-name}`<br>
For branch fixing: `fixing/{fixing-name}`<br>
```bash
git checkout -b feature/{feature-name}
```
or
```bash
git branch fixing/{fixing-name}
git checkout fixing/{fixing-name}
```
*Kindly remember to always create new feature and not making changes in branch develop and master*
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
### Integrate Changes Between Branches
Making branch feature keep up-to-date with commits from branch develop<br>
Preventing merge conflict when merge request<br>
From branch feature:
```bash
git merge develop 
```
### How to Merge Request
- Create new merge request
- Select from `branch feature` into `branch develop`
- Fill title and description with meaningful explanation
- Select asignees as yours and reviewers as tech lead


## Code Style
With **Clean Architecture** as a design pattern, we're free to code but kindly remember the code principles:<br>
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
spring.datasource.url= jdbc:postgresql://localhost:5432/{database-name}
spring.datasource.username= {postgresql-username} 
spring.datasource.password= {postgresql-password}


spring.jpa.properties.hibernate.dialect= org.hibernate.dialect.PostgreSQLDialect
spring.jpa.properties.hibernate.format_sql= true
spring.jpa.hibernate.ddl-auto= {create/create-drop/validate/update}
spring.jpa.show-sql= true

jwt.secret= {jwt-secret}
```
*Kindly remember to add this to .gitignore, so it won't be push to our repository*


## Architecture Structure
```
├── .mvn/wrapper
├── src
|   ├── main
|   |   ├── java/com/projects
|   |   |   ├── auth
|   |   |   ├── configuration
|   |   |   ├── controller
|   |   |   ├── dto
|   |   |   ├── exception
|   |   |   ├── model
|   |   |   ├── repository
|   |   |   ├── service
|   |   |   |   ├── impl
|   |   |   ├── util
|   |   ├── recources
|   |   |   ├── application.properties
|   ├── test/java/com/projects
```

## Architecture Purpose
- `main`
  - `java/com/projects`
    -  `auth` represents as a place for all auth of the applications.
    -  `configuration` represents as a configuration needed as necessary need.
    -  `controller` represents as a place for interaction between applications and we're defining endpoint to provide client side.
    -  `dto` represents as a place that defining customization of attribute of entity for response needed.
    -  `exception` represents as a place that all custom handling errors we made to prevent unwanted things.
    -  `model` represents as a place to define databases info. For example table, column, relations.
    -  `repository` represents as a place for modifying databases with query for example searching queries.
    -  `service` represents as a place for business logic for our applications, makes our controller cleaner.
        -  `impl` represents as a implementation of service interface.
    -  `util` represents as a place for helpers. Simplify and prevent calling a class repeatedly.
  - `resources` usually represents as a place for database info credentials like `application.properties`
- `test/java/com/projects` represents as a place for all testing we're gonna do. For example like unit testing, functional testing.


## Database Schema
![](images/DB%20Banking%20Gamification.png)
For detail information, take a look at [Database Schema](https://dbdiagram.io/d/60a86e29b29a09603d16040e)


## API Documentation
We're using [Swagger For API Docs]({swagger-link}), look for further information



