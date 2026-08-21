# 🔐 Secure File Manager

A secure file storage and sharing application built using **Java, Spring Boot, Spring Security, JPA, MySQL, and AES-GCM Encryption**. The system ensures that uploaded files are encrypted before storage and can only be downloaded using a valid download key.

---

## 📌 Project Overview

The Secure File Storage System provides a secure way to upload, store, and retrieve files. Files are encrypted using AES-GCM before being stored, ensuring confidentiality and integrity. Each uploaded file is associated with a unique download key, preventing unauthorized access.

---

## 🚀 Features

* Secure File Upload
* AES-GCM File Encryption
* Secure File Download
* Download Key Validation
* File Metadata Management
* Spring Security Integration
* MySQL Database Storage
* RESTful API Architecture

---

## 🛠️ Tech Stack

### Backend

* Java 21
* Spring Boot 3.x
* Spring Security
* Spring Data JPA

### Database

* MySQL

### Build Tool

* Maven

### Encryption

* AES-GCM (Advanced Encryption Standard)

### Additional Libraries

* Lombok
* Hibernate

---

## 📂 Project Structure

```text
Secure-File-Storage-System/
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── controller/
│   │   │   ├── service/
│   │   │   ├── repository/
│   │   │   ├── model/
│   │   │   └── config/
│   │   │
│   │   └── resources/
│   │       └── application.properties
│   │
│   └── test/
│
├── .gitignore
├── README.md
├── pom.xml
├── mvnw
└── mvnw.cmd
```

---

## 🔒 Security Workflow

### Upload Process

1. User uploads a file.
2. System generates a unique download key.
3. File is encrypted using AES-GCM.
4. Encrypted file is stored in the database.
5. Download key is returned to the user.

### Download Process

1. User provides File ID and Download Key.
2. System validates the key.
3. Encrypted file is retrieved.
4. File is decrypted securely.
5. Original file is returned.

---

## 📡 API Endpoints

### Upload File

```http
POST /api/files/upload
```

### Download File

```http
GET /api/files/download/{fileId}?key={downloadKey}
```

### View Encrypted Data

```http
GET /api/files/raw/{fileId}?key={downloadKey}
```

---

## ⚙️ Installation & Setup

### Prerequisites

* Java 21
* Maven
* MySQL Server

### Clone Repository

```bash
git clone https://github.com/antaryamidas/Secure-File-Storage-System.git
```

### Configure Database

Update `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/securedb
spring.datasource.username=root
spring.datasource.password=your_password
```

### Run Application

```bash
mvn clean install
mvn spring-boot:run
```

Application will start on:

```text
http://localhost:8080
```

---

## 🧪 Testing

Run all tests:

```bash
mvn test
```

---

## 🎯 Learning Outcomes

* Spring Boot Development
* REST API Design
* Spring Security Implementation
* File Handling in Java
* Database Integration using JPA
* AES-GCM Encryption Techniques
* Secure Application Development

---

## 🔮 Future Enhancements

* JWT Authentication
* Role-Based Access Control (RBAC)
* Cloud Storage Integration (AWS S3)
* Secure File Sharing Links
* File Expiration Support
* Audit Logging
* Multi-Factor Authentication

---

 

## 📄 License

This project is developed for academic and educational purposes.

---

⭐ If you found this project useful, consider giving it a star on GitHub.
