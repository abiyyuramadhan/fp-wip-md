# {project-name} Backend Team B Homey
Hello there! Welcome to our playground. We're here for having fun.
## *Need to do*:
1. java openjdk version✔️
2. spring version✔️
3. gitignore inside
4. example of application.properties
5. folder purpose
6. design pattern what to choose?
7. clean code especially naming conventions
8. 1 class 1 method 1 purpose
9. how auth will works?
10. getting started
11. git flow✔️
12. credentials config✔️
13. database schema✔️ 
14. api docs✔️
15. docker command
16. project description✔️
17. folder structure
18. folder purpose
19. table of contents
## What we're developing <br>{project-name}
descripton...
## What tech stack we're using
1. Java openjdk version 16, here for resources [Openjdk Archive](https://jdk.java.net/archive/)<br> Check if java version is openjdk:
```
java -version
```
2. Spring version 2.4.5 with maven project
3. Dependencies: 
   - Spring Web 
   - PostgreSQL
   - Spring Data JPA
   - Lombok 
   - Spring Security
   - JJWT
   - ModelMapper
   - Springfox Swagger
## Git Work Flow
### 1. How to clone our remote repository
```bash
git clone {git-url}
```
### 2. How to create branch feature and checkout from branch develop
```bash
git checkout -b feature/{feature-name}
```
*Kindly remember to always create new feature and not making changes in branch develop*
### 3. How to add changes to staging area
```bash
git add .
git add {file-name}
```
### 4. How to save changes from staging area
```bash
git commit -m "message"
```
### 5. How to check previous changes
```bash
git log
```
### 6. How to check list of remote repositories
```bash
git remote -v
```
### 7. How to push feature to remote repository
```bash
git push origin feature/{feature-name}
```
### 8. How to update from remote repostiory into local repository
```bash
git pull develop
```
### 9. How to keep changes up-to-date with branch develop into branch feature
from branch feature:
```bash
git merge develop 
```
### 10. How to merge request
1. Create new merge request
2. Select from `branch feature` into `branch develop`
3. Fill title and description with meaningful explanation
4. Select asignees as yours and reviewers as tech lead and backend facilitator
5. Check mark✔️ *delete source branch when merge request is accepted*
## Credentials Configuration
### 1. Inside application.properties
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
## Folder Structure
## Folder Purpose
## Database Schema
![]({image-db-schema-link})
For detail information, take a look at [Database Schema]({db-schema-link})
## API Documentation
We're using [Swagger For API Docs]({swagger-link}), look for further information



