# Employee Management Service

## Overview
As part of my recent completion of **Hewlett Packard Enterprise's Software Engineering simulation on Forage**, I developed the **Employee Management Service**, a robust and scalable RESTful web service designed using **Java Spring Boot**. This powerful framework streamlines the creation of stand-alone applications and microservices. The service is hosted on the **Hewlett Packard Enterprise (HPE) GreenLake Cloud Platform**, a modern cloud solution that offers flexible data storage and computing resources tailored for enterprises.

The primary goal of the Employee Management Service is to simplify the management of employee records for organizations. I designed a solution that enables users to efficiently perform critical operations on employee data, including creating, retrieving, updating, and deleting employee records. By adhering to RESTful principles, the service supports intuitive HTTP requests, making it accessible for various clients, such as web applications, mobile apps, and other backend services.

### Key Features
- **Comprehensive Employee Management**: The service manages essential employee details, including `first_name`, `last_name`, `employee_id`, `email`, and `title`, ensuring organizations maintain accurate and up-to-date records.
  
- **CRUD Operations**: Fully supports CRUD functionalities, allowing users to:
  - **Create** new employee entries via POST requests.
  - **Read** employee data through GET requests, returning structured JSON responses.
  - **Update** existing records to keep information current.
  - **Delete** employee entries to maintain a clean database.

- **Scalable Architecture**: Designed to handle varying loads by easily deploying additional instances, ensuring performance during peak times.

- **Data Security and Compliance**: Hosting on the GreenLake Cloud Platform enables enhanced security features and compliance with data protection regulations, safeguarding sensitive employee information.

- **User-Friendly API**: The service offers a clean, RESTful API that allows developers to integrate easily with existing systems or build new applications leveraging employee data, following industry best practices for reliability.

### Technical Implementation
The Employee Management Service consists of several Java classes that collaboratively manage requests and employee data:
- **Employee Class**: Represents individual employee records, encapsulating relevant data fields with getter and setter methods.
- **Employees Class**: Manages a collection of Employee objects, providing functionality to retrieve and manipulate employee lists.
- **EmployeeController Class**: Serves as the entry point for HTTP requests, defining endpoints corresponding to CRUD operations.
- **EmployeeManager Class**: Initializes employee data and handles business logic for record management.
- **RestServiceApplication Class**: Acts as the main entry point for the Spring Boot application, configuring the application context and starting the embedded server.

### Benefits of the Service
Implementing the Employee Management Service offers several advantages:
- **Improved Efficiency**: Automation reduces the administrative burden on HR teams, enhancing operational efficiency.
- **Enhanced Data Accuracy**: A centralized system minimizes data duplication and inconsistencies.
- **Informed Decision-Making**: Easy access to employee data empowers managers and decision-makers with real-time information.
- **Flexibility and Integration**: The RESTful API facilitates seamless integration with other systems and applications, enhancing information flow across the organization.

### Simulation Experience
During the simulation, I successfully completed the following tasks:
1. **Proposal Development**: Crafted a detailed proposal for a RESTful web service managing employee records, outlining technical requirements and design considerations.
2. **Web Server Application**: Built a web server application using Java Spring Boot that accepts and responds to HTTP requests, supporting JSON data uploads for new employee records.
3. **Unit Testing**: Developed and executed a comprehensive set of unit tests to assess performance and ensure reliability.

This simulation significantly enhanced my understanding of software engineering practices, RESTful service development, application architecture, and testing methodologies.

Check out the simulation here: [Hewlett Packard Enterprise Software Engineering on Forage](https://www.theforage.com/simulations/hewlett-packard-enterprise/software-engineering-pcij).

---

## Table of Contents
1. [Features](#features)
2. [Technologies Used](#technologies-used)
3. [Project Structure](#project-structure)
4. [Installation](#installation)
5. [Usage](#usage)
6. [API Endpoints](#api-endpoints)
7. [Task Details](#task-details)
   - [Task 1: Create a Proposal for a RESTful Web Service](#task-1-create-a-proposal-for-a-restful-web-service)
   - [Task 2: Build a Basic RESTful Web Service](#task-2-build-a-basic-restful-web-service)
   - [Task 3: Implement the Ability to Upload Data](#task-3-implement-the-ability-to-upload-data)
   - [Task 4: Create Unit Tests](#task-4-create-unit-tests)
8. [Contributing](#contributing)
9. [License](#license)
10. [Contact](#contact)

## Features
- **Employee Management**: Supports CRUD operations (Create, Read, Update, Delete) for employee records.
- **Data Storage**: Securely stores employee data on the GreenLake Cloud Platform.
- **RESTful API**: Provides a clean and intuitive interface for accessing and manipulating employee data.

## Technologies Used
- **Java Spring Boot**: Framework for building the RESTful web service.
- **GreenLake Cloud Platform**: Cloud-based data storage solution.
- **Maven**: Dependency management and project structure.
- **JUnit / Mockito**: For unit testing functionalities.

## Project Structure
```
Employee-Management-Service/
├── Task 1/
│   └── Task 1.pdf
├── Task 2/
│   ├── Employee.java
│   ├── EmployeeController.java
│   ├── EmployeeManager.java
│   ├── Employees.java
│   └── RestServiceApplication.java
├── Task 3/
│   ├── Employee.java
│   ├── EmployeeController.java
│   ├── EmployeeManager.java
│   ├── Employees.java
│   └── RestServiceApplication.java
├── Task 4/
│   └── UnitTests.java
```

## Installation
1. **Clone the repository:**
   ```bash
   git clone https://github.com/Anushdubey01/Employee-Management-Service.git
   cd Employee-Management-Service
   ```
2. **Install dependencies:**
   Ensure you have Maven installed, and run:
   ```bash
   mvn install
   ```
3. **Run the application:**
   You can run the application using:
   ```bash
   mvn spring-boot:run
   ```

## Usage
Once the application is running, you can access it locally at `http://localhost:8080/employees`. 

## API Endpoints
### Get All Employees
- **Request:** `GET /employees`
- **Response:** Returns a JSON list of all employees.
```json
{
    "employees": [
        {
            "employee_id": "string",
            "first_name": "string",
            "last_name": "string",
            "email": "string",
            "title": "string"
        }
    ]
}
```

### Add New Employee
- **Request:** `POST /employees`
- **Body:**
```json
{
    "employee_id": "string",
    "first_name": "string",
    "last_name": "string",
    "email": "string",
    "title": "string"
}
```

## Task Details

### Task 1: Create a Proposal for a RESTful Web Service
The objective was to learn about Java Spring Boot and the GreenLake Cloud Platform to propose a RESTful web service for managing employee records.

#### Proposal Overview
The proposed web service will:
- Support HTTP methods: GET, POST, DELETE, and UPDATE.
- Manage employee data fields: `first_name`, `last_name`, `employee_id`, `email`, and `title`.
- Store data on a private cloud server (GreenLake).
  
### Task 2: Build a Basic RESTful Web Service
In this task, the goal was to develop a basic service that retrieves a list of employees.

#### Implementation Steps
1. **Create `Employee` Class**:
   - Define properties: `first_name`, `last_name`, `employee_id`, `email`, and `title`.
   - Implement getter methods for each property.

2. **Create `Employees` Class**:
   - Manage a list of `Employee` objects.
   - Include methods to get and set the employee list.

3. **Create `EmployeeManager` Class**:
   - Initialize `Employees` and hard-code 3-4 example employee records.

4. **Create `EmployeeController` Class**:
   - Implement an HTTP GET endpoint at `http://localhost:8080/employees` to return employee data in JSON format.

5. **Test the Application**:
   - Run the application and send a GET request to verify functionality.

### Task 3: Implement the Ability to Upload Data
This task expanded the service to support adding new employees via HTTP POST requests.

#### Implementation Steps
1. **Enhance `Employee` Class**:
   - Ensure all properties have appropriate getter and setter methods.

2. **Update `EmployeeController`**:
   - Add an HTTP POST endpoint to handle incoming employee data.

3. **Test the Application**:
   - Send a POST request to `http://localhost:8080/employees` with example employee data to confirm successful addition to the list.

### Task 4: Create Unit Tests
The final task was to implement unit tests to ensure all functionalities work as intended.

#### Implementation Steps
1. **Select Testing Framework**

: Choose between Mockito or JUnit for testing.

2. **Write Unit Tests**:
   - Test functionalities such as adding employees and retrieving employee lists.

3. **Run Tests**:
   - Rebuild the project and execute tests to confirm they all pass.
   - Address any failures by adjusting the application code or test cases as needed.

## Contributing
Contributions to improve the project are welcome! Feel free to submit a pull request or open an issue for any bugs or feature requests.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact
For any inquiries, please reach out to [anushdubey881@gmail.com](mailto:anushdubey881@gmail.com).
