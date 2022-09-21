# spring-transaction-example

In this template we learn the simple example of flight-booking-service with Spring-boot transaction management 
with Spring data JPA and @Transactional annotation.

# Technology
 * Java 1.8 
 * Spring Boot 2.7.3 (with Spring Web MVC, Spring Data JPA, lombook and my-sql driver) 
 * MySQL
 * Maven 3.8.1 or above

# Create & Setup Spring Boot project
Use Spring web tool or your development tool (Spring Intializer.io, Spring Tool Suite, Eclipse, Intellij) to create a Spring Boot project.

Then open pom.xml and add these dependencies:

* spring-boot-starter-data-jpa
* spring-boot-starter-web
* mysql-connector-java
* org.projectlombok
* spring-boot-starter-test
* spring-boot-maven-plugin

# Configure Spring boot with Spring Data JPA
Under src/main/resources folder, open application.properties and add following lines.
<br />
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver <br />
spring.datasource.url = jdbc:mysql://localhost:3306/knoldus_db <br />
spring.datasource.username = root <br />
spring.datasource.password = root <br />
spring.jpa.show-sql = true <br />
spring.jpa.hibernate.ddl-auto = update <br />
spring.jpa.properties.hibernate.dialect = org.hibernate.dialect.MySQL8Dialect <br />
server.port=9090 <br />

# Run Spring Boot application

 mvn spring-boot:run or   <br />
 SpringApplication.run(FlightServiceExampleApplication.class, args)
 
# Result 

 Test 1 - If want to bookflight ticket and person account has insuffcient fund then it will 
 throw the exception of InsufficientAmountException and check the same message. <br />
 Test 2 - If want to book flight ticket and account has fund then it will book the ticket and 
 get the success message with full Passenger and Payment Info details.
 Check the DB for the entries and stored or not?