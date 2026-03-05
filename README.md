## Prerequisites section
### Install first:

Java 17+
Node.js 18+
MySQL 8+
Maven 3.8+

## Step-by-step setup
### 1. Clone the repo
`bash
git clone https://github.com/your-username/library-management-system.git
cd library-management-system
`
2. Database setup
bash# Login to MySQL and run the schema
mysql -u root -p < backend/src/main/resources/schema.sql
3. Configure database credentials
Tell them to open backend/src/main/resources/application.properties and update:
propertiesspring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD
4. Run the backend
bashcd backend
mvn spring-boot:run
# Runs on http://localhost:8080
5. Run the frontend
bashcd frontend
npm install
npm run dev
# Runs on http://localhost:5173
6. Open the app
Visit http://localhost:5173 in the browser — sample data is already loaded from the SQL schema.
