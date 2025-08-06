# Diary Queen
"DQ" is a personal diary management web application. It was built with with **Spring Boot** and **Maven** in class.
It provides RESTful APIs and an optional web interface for creating, viewing, updating, and deleting diary entries.

##  Tech Stack
- **Java 8+**
- **Spring Boot**
  - `spring-boot-starter-web` — MVC & routing
  - `spring-boot-starter-thymeleaf` — HTML templating
  - `spring-boot-devtools` — Hot reload for development
  - `spring-boot-starter-test` — Unit testing
- **Maven** — Build & dependency management


## Tech Stack

- **Language & Platform**  
  - Java 8  
  - Spring Boot 2.3.3.RELEASE  

- **Frameworks & Libraries**  
  - **Spring MVC** — Handles HTTP requests and routing  
  - **Thymeleaf** — Server-side HTML template engine for rendering dynamic pages  
  - **Spring Boot DevTools** — Hot reload for faster development  
  - **Spring Boot Starter Test** — JUnit 5 & Spring Test framework for unit/integration testing  

- **Build Tool & Dependency Management**  
  - **Maven** — Dependency management and project build (`pom.xml`)  

- **Packaging & Deployment**  
  - Spring Boot Maven Plugin — Packages the app as an executable JAR  
  - Embedded Tomcat — Built-in web server that runs automatically with Spring Boot  

##  How Spring Boot Powers Diary Queen

- **Spring Boot Starter Parent**  
  Provides dependency and plugin management for building the project without complex configuration.  
  In this project, it simplifies managing Spring MVC, Thymeleaf, and test dependencies.

- **Embedded Tomcat Server**  
  Eliminates the need for an external web server. When you run `mvn spring-boot:run`, Spring Boot automatically starts Tomcat and serves your application.

- **Convention over Configuration**  
  By following standard Maven and Spring Boot directory structures, minimal configuration is needed.  
  For example, placing `index.html` in `/templates` lets Thymeleaf find it automatically.

- **Dependency Injection (IoC)**  
  Spring Boot’s core feature, allowing the `DiaryQueenController` to be managed as a Spring bean so it can handle requests without manual object creation.

- **Auto-Configuration**  
  Detects `spring-boot-starter-thymeleaf` in the classpath and configures the template engine automatically.

##  Conclusion
Spring Boot makes it possible for Diary Queen to work as a complete web application without spending weeks setting up the basics. The project launches with an embedded Tomcat server, so there’s no need to download, configure, and deploy to an external server. In plain Java, that setup alone would involve installing Tomcat, packaging the application as a WAR file, and handling deployment manually.

Routing in Spring Boot is handled through simple annotations like @RequestMapping, which map browser requests directly to controller methods. Without it, you’d have to write and register servlets yourself, parse requests, and implement your own routing logic. The same goes for the front end: Thymeleaf is automatically integrated in Spring Boot, so placing an HTML file in the /templates directory is enough for it to be rendered with data from the backend. In plain Java, you’d spend extra time wiring a template engine like JSP or FreeMarker and configuring it to work with your servlets.

Configuration is equally streamlined. In Diary Queen, all settings live in a single application.properties file, which Spring Boot reads automatically. A plain Java setup would require custom code to read configuration files or, worse, hardcode values in the source. Testing benefits from the same simplicity, with Spring Boot bringing in JUnit and the Spring testing framework without any extra setup.

In short, Spring Boot handles the heavy lifting — server startup, dependency wiring, view rendering, and configuration — so the Diary Queen project can focus on its actual purpose: presenting and managing diary entries in a clean, functional interface.
  
##  Personal Understanding
Spring Boot is a convention-over-configuration framework designed to optimize Java web development. It minimizes manual configuration through:

* **Auto-configuration**: Intelligently defaults components based on classpath dependencies.

* **Starter POMs**: Pre-bundled dependencies (e.g., Spring Data, Security)sets for rapid setup.

* **Embedded Servers**: Self-contained deployment via Tomcat or others.

* **Production-Ready Features**: Actuator for monitoring, metrics, and health checks.

By abstracting infrastructure concerns, it allows developers to focus on business logic rather than framework setup. Its opinionated defaults and seamless third-party integration, spring boot has become the preffered choice for:

* Microservices (lightweight, cloud-native design)

* REST APIs (quick scaffolding via Spring Web)

* DevOps-friendly workflows (Docker compatibility).

Key Advantage: 
* Accelerated development lifecycle
* Redced confirguration overhead
* Maintains Spring's modularity and enterprise capabilities

**Other Similar Class Work Practices**
[git@github.com:Xiao0909/soit.git](https://github.com/Xiao0909/soit.git)
