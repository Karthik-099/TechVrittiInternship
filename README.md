<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

</head>
<body>
    <h1>TechVritti Internship - Installation and Setup</h1>
    
    <h2>Step 1: Clone the Repository</h2>
    <p>Clone the repository to your local machine:</p>
    <pre>
        git clone https://github.com/Karthik-099/TechVrittiInternship.git
        cd TechVrittiInternship
    </pre>
    
    <h2>Step 2: Pull the Docker Image (Optional)</h2>
    <p>If you don’t want to build the image locally, you can pull it from Docker Hub:</p>
    <pre>
        docker pull karthik75/techvritti-app
    </pre>
    
    <h2>Step 3: Start the Application</h2>
    <p>Run the application using Docker Compose:</p>
    <pre>
        docker-compose up --build
    </pre>
    <p>This will start:</p>
    <ul>
        <li>The PHP + Apache service (app).</li>
        <li>The MySQL database service (db).</li>
        <li>The Nginx web server (web).</li>
    </ul>
    
    <h2>Step 4: Access the Application</h2>
    <p>Once the containers are running, open your browser and navigate to:</p>
    <ul>
        <li><a href="http://localhost:8080/index.html">Form Page</a></li>
        <li><a href="http://localhost:8080/quiz.html">Quiz Page</a></li>
        <li><a href="http://localhost:8080/php/admin.php">Admin Dashboard</a></li>
    </ul>
    
    <h2>Viewing the Database and Stored Data</h2>
    
    <h3>Step 1: Access the MySQL Container</h3>
    <p>To view the data stored in the MySQL database:</p>
    <pre>
        docker exec -it techvritti-db-1 mysql -u user -p
    </pre>
    <p>Enter the password when prompted:</p>
    <pre>
        password: password
    </pre>
    
    <h3>Step 2: Run Queries</h3>
    <p>Once inside the MySQL shell, run the following commands:</p>
    <pre>
        USE internship_portal;

        -- View all students
        SELECT * FROM students;

        -- View all quiz questions
        SELECT * FROM questions;
    </pre>
    
   
</body>
</html>
