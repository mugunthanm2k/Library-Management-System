# Library-Management-System


## **System Architecture**

```
library-management-system/
├── backend/                        # Spring Boot application
│   ├── pom.xml
│   └── src/main/
│       ├── java/com/library/
│       │   ├── LibraryManagementApplication.java
│       │   ├── config/CorsConfig.java
│       │   ├── controller/
│       │   │   ├── BookController.java
│       │   │   ├── MemberController.java
│       │   │   ├── BorrowController.java
│       │   │   ├── AuthorController.java
│       │   │   └── DashboardController.java
│       │   ├── service/
│       │   │   ├── BookService.java
│       │   │   ├── MemberService.java
│       │   │   └── BorrowService.java
│       │   ├── repository/
│       │   │   ├── BookRepository.java
│       │   │   ├── MemberRepository.java
│       │   │   ├── AuthorRepository.java
│       │   │   └── BorrowRecordRepository.java
│       │   ├── model/
│       │   │   ├── Book.java
│       │   │   ├── Author.java
│       │   │   ├── Member.java
│       │   │   └── BorrowRecord.java
│       │   ├── dto/
│       │   │   ├── BookDTO.java
│       │   │   ├── MemberDTO.java
│       │   │   ├── BorrowRecordDTO.java
│       │   │   └── DashboardStatsDTO.java
│       │   └── exception/
│       │       ├── GlobalExceptionHandler.java
│       │       ├── ResourceNotFoundException.java
│       │       └── BadRequestException.java
│       └── resources/
│           ├── application.properties
│           └── schema.sql
│
└── library_frontend/                       # React + Vite application
    ├── package.json
    ├── vite.config.js
    ├── tailwind.config.js
    └── src/
        ├── main.jsx
        ├── App.jsx
        ├── index.css
        ├── services/api.js
        ├── components/
        │   ├── Layout.jsx
        │   ├── Modal.jsx
        │   ├── Toast.jsx
        │   └── PageHeader.jsx
        └── pages/
            ├── Dashboard.jsx
            ├── Books.jsx
            ├── Members.jsx
            └── Borrows.jsx
```

---
## Prerequisites section
### Install first:

Java 17+
Node.js 18+
MySQL 8+
Maven 3.8+

### IDE's :
Eclipse 
Intellij
VS Code

## **Step-by-step setup**

### 1. Clone the repo
```bash
git clone https://github.com/your-username/library-management-system.git
```
### 2. UnZip
```
upzip the file 
```
### 3. Database setup ()
```bash
Open MySQL DB workbench 
create DB **"library_db"** 
```
### 4. Configure database credentials
open backend/src/main/resources/application.properties and update:
```
propertiesspring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD
```
### 5. Run the backend
```bash
cd backend
mvn spring-boot:run
```
Runs on http://localhost:8080

### 6. Run the frontend
```bash
cd library_frontend
npm install
npm run dev
```
 Runs on http://localhost:5173
 
### 6. Open the app

Visit http://localhost:5173 in the browser — sample data is already loaded from the SQL schema.
