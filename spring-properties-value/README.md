# Properties @Value

copiado do artigo no site: https://www.baeldung.com/spring-value-annotation


## Properties File
Properties files are used to keep ‘N’ number of properties in a single file to run the application in a different environment. In Spring Boot, properties are kept in the application.properties file under the classpath.

The application.properties file is located in the src/main/resources directory. The code for sample application.properties file is given below −

server.port = 9090
spring.application.name = demoservice
Note that in the code shown above the Spring Boot application demoservice starts on the port 9090.

## YAML File
Spring Boot supports YAML based properties configurations to run the application. Instead of application.properties, we can use application.yml file. This YAML file also should be kept inside the classpath. The sample application.yml file is given below −

spring:
   application:
      name: demoservice
   server:
port: 9090

## Externalized Properties
Instead of keeping the properties file under classpath, we can keep the properties in different location or path. While running the JAR file, we can specify the properties file path. You can use the following command to specify the location of properties file while running the JAR −

-Dspring.config.location = C:\application.properties
Externalized Properties
Use of @Value Annotation
The @Value annotation is used to read the environment or application property value in Java code. The syntax to read the property value is shown below −

@Value("${property_key_name}")
Look at the following example that shows the syntax to read the spring.application.name property value in Java variable by using @Value annotation.

@Value("${spring.application.name}")