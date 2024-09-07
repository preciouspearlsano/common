# Common Project

This repository contains the common dependencies and configurations for the `Common Project`. It is organized into modules to provide reusable components across multiple Spring Boot services.

## Project Structure

The project is organized into the following structure:

common-project/ ├── core/ │ ├── src/ │ │ ├── main/ │ │ │ ├── java/ │ │ │ └── resources/ │ │ └── test/ │ │ ├── java/ │ │ └── resources/ │ ├── pom.xml ├── pom.xml └── README.md


### Core Module

The `core` module is the heart of the `Common Project`. It includes:

- Common configurations
- Shared utilities and classes
- Reusable components

### Common Parent POM

The root `pom.xml` acts as a parent for the `core` module and provides shared configurations for dependencies, plugins, and properties.

## Getting Started

### Prerequisites

- Java 17
- Maven 3.8.1 or higher

### Building the Project

To build the project, navigate to the root directory and run:

```bash```
mvn clean install


This will compile the core module and install the artifacts in your local Maven repository.

```Running Tests```
To execute tests, run the following command in the root directory or in any specific module directory:

mvn test

Modules
Core Module
The core module includes common configurations and utilities. It is intended to be used as a dependency in other Spring Boot services.

Dependencies
Spring Boot 3.3.3
Java 17
Maven Dependency
To use the core module in another project, add the following dependency to your pom.xml:

<dependency>
    <groupId>com.company.common</groupId>
    <artifactId>core</artifactId>
    <version>1.0.0-SNAPSHOT</version>
</dependency>

Example Usage
Here’s an example of how to use the core module in your Spring Boot application:

package com.company.service;

import com.company.common.core.SomeCommonClass;
import org.springframework.stereotype.Service;

@Service
public class ExampleService {

    private final SomeCommonClass commonClass;

    public ExampleService(SomeCommonClass commonClass) {
        this.commonClass = commonClass;
    }

    public void performTask() {
        commonClass.doSomething();
    }
}

### License
This project is licensed under the MIT License - see the LICENSE file for details.

### Contributing
Contributions are welcome! Please see the CONTRIBUTING.md file for guidelines.

### Contact
For any inquiries or issues, please contact us at support@company.com.

### Resources

- [Boringblox Website](http://www.boringblox.com)
- [Spring Boot Documentation](https://spring.io/projects/spring-boot)
- [Maven Documentation](https://maven.apache.org/guides/index.html)


### Key Points:

- **Project Structure:** Describes the organization of the project files and directories.
- **Core Module:** Details about the core module, its purpose, dependencies, and how to use it.
- **Getting Started:** Instructions on building the project and running tests.
- **Example Usage:** A simple example of how to integrate and use the core module in another Spring Boot service.
- **Contact Information:** Provides a way to reach out for support.

This `README.md` is designed to give a clear understanding of the project and how to work with it. Adjust any sections as needed based on the specifics of your project.