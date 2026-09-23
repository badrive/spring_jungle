# Spring Boot Learning Roadmap

**Goal:** independently build, test, and deploy a complete Spring Boot backend.

**Estimated time:** 10–12 weeks at 15–20 hours per week. This is an estimate for practical competence, not mastery or a guaranteed internship.

## Understanding the stack

- **Java:** the programming language.
- **Spring:** the framework that provides features such as dependency injection and HTTP request handling.
- **Spring Boot:** simplifies setting up and running Spring applications through automatic configuration and integrated tooling.

## Roadmap overview

| Period | Focus | Deliverable |
| --- | --- | --- |
| Weeks 1–2 | Java essentials and Maven | A command-line task manager |
| Week 3 | Spring fundamentals and Spring Boot | A small API; explain how Spring creates and connects its objects |
| Weeks 4–5 | REST API development | CRUD endpoints, validation, and consistent error responses |
| Weeks 6–7 | SQL and Spring Data JPA | PostgreSQL persistence, relationships, transactions, and pagination |
| Week 8 | Spring Security | Login, password hashing, roles, and ownership checks |
| Weeks 9–10 | Testing and debugging | Tests for business rules, endpoints, and database behavior |
| Weeks 11–12 | Finish and deploy | Docker Compose setup, documentation, and a running application |

Start writing small tests early. Weeks 9–10 are for making the application dependable.

## Weeks 1–2: Java essentials and Maven

Move quickly through variables, loops, and basic classes. Focus on the differences from C++ and the tools used in Java projects.

- [ ] Understand Java references, garbage collection, and pass-by-value.
- [ ] Practice interfaces, inheritance, and composition.
- [ ] Use `List`, `Set`, `Map`, and generics.
- [ ] Handle exceptions and use try-with-resources.
- [ ] Explain `equals()` versus `==` and the relationship between `equals()` and `hashCode()`.
- [ ] Practice lambdas and basic streams.
- [ ] Understand records and annotations.
- [ ] Use Maven: dependencies, `pom.xml`, building, and running tests.

**Resource:** [Dev.java — Learn Java](https://dev.java/learn/)

Read the relevant sections while coding. You do not need to finish the entire website before starting Spring.

**Checkpoint:** build a command-line task manager that adds, updates, searches, and removes tasks using collections, with file persistence.

## Week 3: Spring fundamentals and Spring Boot

Understand these concepts before memorizing annotations:

| Concept | Meaning |
| --- | --- |
| Bean | An object managed by Spring |
| Dependency injection | Spring supplies the objects a class needs, preferably through its constructor |
| Controller | Handles HTTP requests and responses |
| Service | Implements business rules |
| Repository | Handles data access |
| Auto-configuration | Spring Boot supplies configuration based on dependencies and settings |

- [ ] Create a project with [Spring Initializr](https://start.spring.io/).
- [ ] Select Java, Maven, and a stable Spring Boot release.
- [ ] Use Java 21 as a starting choice, checking compatibility with your selected Spring Boot version.
- [ ] Add Spring Web and create your first endpoint returning JSON.
- [ ] Connect a controller and service using constructor injection.
- [ ] Explain how a request reaches your controller and produces a response.

**Resource:** [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)

Keep tutorial and project versions aligned, especially for security configuration.

## Weeks 4–5: REST API development

- [ ] Implement create, read, update, and delete operations.
- [ ] Use HTTP methods and status codes appropriately.
- [ ] Handle path variables, query parameters, and JSON request bodies.
- [ ] Validate incoming data.
- [ ] Return consistent error responses.
- [ ] Separate HTTP handling from business rules.
- [ ] Test endpoints using `curl` or Postman.

**Resource:** [Building REST Services with Spring](https://spring.io/guides/tutorials/rest/)

**Checkpoint:** implement an issue-tracking API with clear endpoints and useful error messages.

## Weeks 6–7: SQL and Spring Data JPA

Learn SQL directly alongside JPA. Understand what your application asks the database to do.

- [ ] Practice SQL queries and joins.
- [ ] Understand primary keys, foreign keys, and constraints.
- [ ] Understand the purpose of indexes.
- [ ] Understand transactions.
- [ ] Connect the application to PostgreSQL.
- [ ] Map entities and relationships with JPA.
- [ ] Use repositories to store and retrieve data.
- [ ] Add pagination and filtering.

**Resource:** [Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)

**Checkpoint:** application data survives restarts, relationships are correct, and you can explain the main database queries.

## Week 8: Spring Security

- [ ] Explain authentication versus authorization.
- [ ] Implement session-based login.
- [ ] Store passwords using an appropriate password encoder.
- [ ] Restrict actions by role.
- [ ] Check project membership and resource ownership.
- [ ] Verify that unauthorized users cannot access protected resources.

**Resource:** [Hello Spring Security](https://docs.spring.io/spring-security/reference/servlet/getting-started.html)

Learn session-based login first. Add JWT later if the application needs it.

## Weeks 9–10: Testing and debugging

- [ ] Test business rules independently.
- [ ] Test successful and invalid API requests.
- [ ] Test database behavior.
- [ ] Test permissions and ownership rules.
- [ ] Read logs and debug failures.
- [ ] Run the test suite through Maven.

**Checkpoint:** tests catch meaningful failures, such as a user accessing another team's project or an invalid issue being accepted.

## Weeks 11–12: Finish and deploy

- [ ] Run the Spring Boot application in Docker.
- [ ] Run the application and PostgreSQL with Docker Compose.
- [ ] Configure the application for its deployment environment.
- [ ] Document setup instructions and API usage.
- [ ] Deploy and verify the main workflows.
- [ ] Explain the application architecture and important design decisions.

**Checkpoint:** another developer can follow your documentation, run the application, and test its main features.

## Main project: Team issue tracker

Build one project throughout the roadmap.

- [ ] Users can create projects and assign issues.
- [ ] Issues have statuses, priorities, and comments.
- [ ] Users can only access projects they belong to.
- [ ] Administrators can manage membership.
- [ ] Lists support filtering and pagination.
- [ ] PostgreSQL stores the data.
- [ ] Automated tests verify permissions and business rules.
- [ ] Docker Compose runs the application and database.

## Study routine

For a three-hour session:

| Time | Activity |
| --- | --- |
| 45 minutes | Study one concept |
| 2 hours | Implement it and debug it |
| 15 minutes | Explain what you built without looking at the tutorial |

Complete a tutorial example, close it, and implement a similar feature yourself.

Delay microservices, Kubernetes, Kafka, and reactive programming until you can independently build, test, and deploy one application.

## First step

Start the Java task manager. After roughly two weeks, begin Spring while continuing to improve your Java.

## Resource list

1. [Dev.java — Learn Java](https://dev.java/learn/)
2. [Spring Initializr](https://start.spring.io/)
3. [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)
4. [Building REST Services with Spring](https://spring.io/guides/tutorials/rest/)
5. [Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)
6. [Hello Spring Security](https://docs.spring.io/spring-security/reference/servlet/getting-started.html)
7. [Spring Boot overview](https://spring.io/projects/spring-boot)
8. [Spring Boot system requirements](https://docs.spring.io/spring-boot/system-requirements.html)
