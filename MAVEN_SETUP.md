# Q7 Training Application

A Java console application built with Maven and Java 17.

## Prerequisites

- Java 17 or higher installed
- Maven 3.6.0 or higher installed

## Project Structure

```
q7-training/
├── src/
│   ├── main/
│   │   ├── java/com/q7training/    # Source code
│   │   └── resources/               # Resource files
│   └── test/
│       ├── java/com/q7training/    # Test code
│       └── resources/               # Test resources
├── pom.xml                          # Maven configuration
└── README.md
```

## Building the Project

### Compile the code
```bash
mvn clean compile
```

### Run tests
```bash
mvn test
```

### Build a JAR file
```bash
mvn clean package
```

### Run the application
After building:
```bash
java -jar target/q7-training-app.jar
```

Or run directly without building a JAR:
```bash
mvn exec:java -Dexec.mainClass="com.q7training.Main"
```

## Project Configuration

- **Java Version**: 17
- **Build Tool**: Maven
- **Testing Framework**: JUnit 4
- **Packaging**: JAR with dependencies

## Adding Dependencies

Edit `pom.xml` to add new dependencies. For example:

```xml
<dependency>
    <groupId>org.slf4j</groupId>
    <artifactId>slf4j-api</artifactId>
    <version>2.0.9</version>
</dependency>
```

Then run:
```bash
mvn install
```

## Maven Commands Reference

| Command | Purpose |
|---------|---------|
| `mvn clean` | Remove build artifacts |
| `mvn compile` | Compile source code |
| `mvn test` | Run unit tests |
| `mvn package` | Create JAR file |
| `mvn install` | Install to local repository |
| `mvn clean package` | Clean and build |

## IntelliJ IDEA Setup

1. Open the project in IntelliJ
2. Maven should auto-detect the `pom.xml`
3. Right-click `pom.xml` → "Add as Maven Project" if needed
4. Project should compile and run automatically
