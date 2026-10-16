RaceDay API – README
1. Project Overview
RaceDay API is an ASP.NET Core Web API project designed for a road-running, walking, and cycling event platform. The system is intended to help event organisers manage events and allow participants to enrol in event categories and access relevant race information.
The project uses a database to store users, organisers, participants, events, categories, enrolments, and results.
2. Technologies Used
The following technologies are used in the project:
•	C#
•	ASP.NET Core Web API
•	.NET 10
•	Entity Framework Core
•	Microsoft SQL Server LocalDB
•	Swagger / OpenAPI
•	Visual Studio
3. Database Design
The RaceDay database is named RaceDayDB. It contains the following tables:
•	Users: Stores user details, email addresses, password hashes, and roles.
•	Organisers: Stores information about event organisers.
•	Participants: Stores participant information.
•	Events: Stores event names, dates, locations, descriptions, and statuses.
•	Categories: Stores event categories, distances, and entry fees.
•	Enrolments: Stores participant enrolments, race numbers, and payment statuses.
•	Results: Stores race results, finish times, positions, and result statuses.
The database was created using Entity Framework Core Code First migrations.
4. Installation Requirements
To run the project, the following software is required:
•	Visual Studio with the ASP.NET and web development workload.
•	.NET 10 SDK.
•	SQL Server LocalDB.
•	The required NuGet packages for the project.
5. Database Configuration
The project uses SQL Server LocalDB to connect to the RaceDayDB database.
The connection string is configured in the appsettings.json file.
To create or update the database, open the Package Manager Console in Visual Studio, select RaceDay.API as the default project, and run:
Update-Database
6. How to Run the Application
Follow these steps to run the RaceDay API:
1.	Open the RaceDay solution in Visual Studio.
2.	Set RaceDay.API as the startup project.
3.	Build the solution to check for errors.
4.	Open the Swagger URL displayed by Visual Studio.
Swagger allows developers to view and test the API endpoints that have been implemented.
7. User Roles and Authentication
The project database includes a role field for identifying different types of users.
Organiser: Intended to manage events and event categories.
Participant: Intended to enrol in event categories and access relevant event information.
Authentication, password hashing, and role-based access control must be implemented and tested before these features can be considered complete.
8. API Functionality
The planned functionality of the RaceDay API includes:
•	User registration and login.
•	Organiser profile management.
•	Participant profile management.
•	Event management.
•	Event category management.
•	Participant enrolments.
•	Race results management.
The available endpoints can be viewed in Swagger when the application is running. Only endpoints that have been implemented and tested should be considered complete.
9. Testing and Continuous Integration
The project should include automated unit tests to check that the API functions correctly. GitHub Actions should also be configured to build the project and run the tests automatically when changes are pushed to GitHub.
The test project and workflow must be created and verified before they are described as completed. A screenshot of a successful workflow run should be included if required by the assessment instructions.
10. GitHub Repository
GitHub repository link: https://github.com/Daven061028/RaceDay1
The repository should contain the source code, database models, migrations, configuration files, tests, workflow files, and project documentation required for the assessment.
11. AI Use Disclosure
AI assistance was used to support the development and documentation of the RaceDay API project. The code and functionality should be reviewed, understood, and tested by the student. This disclosure should be updated to comply with the assessment requirements and accurately reflect the assistance used.
12. Current Project Status
The project currently has the Entity Framework Core models and database context, an initial migration, the RaceDayDB database, and a working Swagger startup.
Before final submission, the required API endpoints, authentication, role-based access control, automated tests, and GitHub Actions workflow must be completed and tested. The demonstration video and repository link must also be added.

