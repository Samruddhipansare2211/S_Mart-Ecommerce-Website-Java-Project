# 🛒 Smart E-Commerce Platform with CI/CD Automation

## 📌 Project Overview
This project is a **Smart E-Commerce Web Application** developed during my internship.  
It allows users to browse products, manage a shopping cart, and complete a basic checkout process.  
An admin panel is provided for managing product listings.

The application is built using **Java Spring Boot** with a **Thymeleaf-based frontend** and is **deployed on AWS using a CI/CD pipeline** for automated build and deployment.

---

## 🚀 Key Highlights
- Full-stack Java Spring Boot application
- MVC architecture with RESTful routing
- CI/CD pipeline for automated deployment
- Cloud-hosted on AWS EC2 (Ubuntu Server)

---

## 🧩 Features

### 👤 User Features
- User Authentication & Authorization
- Product Browsing and Listing
- Add to Cart & Remove from Cart
- Basic Checkout Functionality
- Dynamic UI using Thymeleaf

### 🧑‍💼 Admin Features
- Admin Login
- Add / Update / Delete Products
- Manage Product Listings

---

## 🔧 Technologies Used

### Backend
- Java 17  
- Spring Boot 3.2.4  
- Spring MVC  
- Spring Data JPA  
- Hibernate  

### Frontend
- Thymeleaf  
- HTML5  
- CSS3  

### Database
- MySQL  

### DevOps & Cloud
- Jenkins (CI/CD Pipeline)
- Git & GitHub
- Maven
- AWS EC2 (Ubuntu Server)
- Linux

---

## ⚙️ CI/CD Pipeline Flow
1. Code pushed to GitHub repository  
2. GitHub Webhook triggers Jenkins pipeline  
3. Maven builds the Spring Boot application  
4. Automated testing and packaging  
5. Application deployed to AWS EC2 server  
6. Service restarted automatically  

---

## 🏗️ Project Architecture
- MVC Architecture (Controller → Service → Repository)  
- RESTful Routing  
- JPA for database interaction  
- Thymeleaf for dynamic content rendering  

### System Diagram (Simplified)
```text
User → Thymeleaf UI → Spring MVC → Services → MySQL Database
````

### Technology Stack (Mini Table)

| Layer    | Technology             |
| -------- | ---------------------- |
| Backend  | Java, Spring Boot      |
| Frontend | Thymeleaf              |
| Database | MySQL                  |
| DevOps   | Jenkins CI/CD, AWS EC2 |

---

## 🛠️ Setup & Installation

### Prerequisites

* Java 17
* Maven
* MySQL
* Git

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/smart-ecommerce-project.git
cd smart-ecommerce-project
mvn clean install
```

### Step 2: Configure Database

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/ecommerce_db
spring.datasource.username=root
spring.datasource.password=your_password
```

### Step 3: Run the Application

```bash
mvn spring-boot:run
```

### Step 4: Access the Application

```
http://localhost:8080
```

---

## 🌐 Deployment

* Application deployed on **AWS EC2 (Ubuntu Server)**
* CI/CD implemented using **Jenkins**
* Automated build, test, and deployment

---

## 📈 Future Enhancements

* Payment Gateway Integration
* Order History & Tracking
* Role-Based Access Control
* Docker & Kubernetes Deployment
* Cloud Monitoring and Logging

---

## 👨‍💻 Author

**Samruddhi Pansare**
Intern – Java | Spring Boot | AWS | DevOps

---

