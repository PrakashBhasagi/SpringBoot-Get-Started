# `Getting Started with Spring-Boot`
This Guide helps you for getting started with springboot
- [`Getting Started with Spring-Boot`](#getting-started-with-spring-boot)
  - [`What You Will build`](#what-you-will-build)
  - [`What You Need`](#what-you-need)
  - [Generating Spring Boot Project](#generating-spring-boot-project)
    - [`Visit spring initializr`](#visit-spring-initializr)
    - [`Run Spring Boot Application`](#run-spring-boot-application)
    - [`Click to see project structure`](#click-to-see-project-structure)
## `What You Will build`
You will build a simple web application with Spring Boot and add some useful dependencies and services to it.

## `What You Need`

- About 15 minutes
  
- A favorite text editor or IDE
  
- [JDK 1.8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) or later
  
- [Maven 3.2+](https://maven.apache.org/download.cgi)(used for this guide)

- You can also import the code straight into your IDE:

    - [Spring Tool Suite (STS)](https://spring.io/guides/gs/sts)

    - [IntelliJ IDEA](https://spring.io/guides/gs/intellij-idea/)

## Generating Spring Boot Project
Like most Spring Getting Started guides, you can start from scratch and complete each step or you can bypass basic setup steps that are already familiar to you. Either way, you end up with working code.


### [`Visit spring initializr`](https://start.spring.io/)

![spring initializr image](spring%20initializr.PNG)

**Enter Following Deatils:**  
These are the details prefered for his guide.

- Project: `Maven`
- Langage: `Java`
- Spring Boot : `2.5.3`(as per latest stable)
- Project Metadata:
  - Group: `com.example`
  - Artifact: `spring-boot`
  - Name: `spring-boot-demo` 
  - Description: `Demo project for Spring Boot`
  - Package name: `com.example.spring-boot`
  - Packaging: `Jar/War`
  - Java: `16/ 11/ 8`

[**Dependencies**](#Dependencies)
- Click on ADD Dependencies and add dependncies as required for your projects   
- But as of now no need to add any dependencies

**Explore**  
Click on Explore, so that you can see the project structre and all files    
![project structure image](project%20structure.PNG)

`pom.xml`
```xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>
  <parent>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-parent</artifactId>
    <version>2.5.3</version>
    <relativePath/> <!-- lookup parent from repository -->
  </parent>
  <groupId>com.example</groupId>
  <artifactId>spring-boot</artifactId>
  <version>0.0.1-SNAPSHOT</version>
  <name>spring-boot-demo</name>
  <description>Demo project for Spring Boot</description>
  <properties>
    <java.version>1.8</java.version>
  </properties>
  <dependencies>
    <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter</artifactId>
    </dependency>

    <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-test</artifactId>
      <scope>test</scope>
    </dependency>
  </dependencies>

  <build>
    <plugins>
      <plugin>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-maven-plugin</artifactId>
      </plugin>
    </plugins>
  </build>

</project>
```
`SpringBootDemoApplication.java`
```java
package com.example.springboot;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class SpringBootDemoApplication {
    public static void main(String[] args) {
        SpringApplication.run(SpringBootDemoApplication.class, args);
  }
}
```

**Share**   
Click on Share to share your configuration URL to others

**Generate**
- Click on generate 

- A Zip file will be downloaded
  
- Exract the Zip file to your workspace

### `Run Spring Boot Application`
- Open you IDE

- Open/ Import your project

- Build project

- On successfull build - Run as Spring Boot Application


### [`Click to see project structure`](spring-boot)