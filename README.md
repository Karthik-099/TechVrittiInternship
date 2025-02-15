<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

</head>
<body>
    <h1>TechVritti Internship - Installation and Setup</h1>
    
    Step 1: Clone the Repository
    Clone the repository to your local machine
    
        git clone https://github.com/Karthik-099/TechVrittiInternship.git
        cd TechVrittiInternship
    
    
    Step 2: Pull the Docker Image (Optional)
    If you don’t want to build the image locally, you can pull it from Docker Hub:
    
        docker pull karthik75/techvritti-app
    
    
    Step 3: Start the Application
    Run the application using Docker Compose:
    
        docker-compose up --build
    
    This will start:
    
        The PHP + Apache service (app).
        The MySQL database service (db).
        The Nginx web server (web).
    
    
    Step 4: Access the Application
    Once the containers are running, open your browser and navigate to:
    <ul>
        <li><a href="http://localhost:8080/index.html">Form Page</a></li>
        <li><a href="http://localhost:8080/quiz.html">Quiz Page</a></li>
        <li><a href="http://localhost:8080/php/admin.php">Admin Dashboard</a></li>
    </ul>
    
    Viewing the Database and Stored Data
    
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
