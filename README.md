
RaceDay API
1. Project Overview
RaceDay API is an ASP.NET Core Web API project for a road-running, walking, and cycling event platform. It is designed to support event organisers and participants by managing users, events, event categories, enrolments, and race results.
This project is being developed as part of the RaceDay programming assessment.
2. Technologies Used
- C#
- ASP.NET Core Web API
- .NET 10
- Entity Framework Core (Code First)
- Microsoft SQL Server LocalDB
- Swagger / OpenAPI
- Visual Studio
3. Main Data Entities
The database currently contains the following entities:
- Users — user details, email, password hash, and role.
- Organisers — organiser profile linked to a user.
- Participants — participant profile linked to a user.
- Events — event details, date, location, description, status, and organiser.
- Categories — categories for an event, including distance and entry fee.
- Enrolments — participant enrolments in categories, including payment status and race number.
- Results — result details linked to an enrolment.
4. Requirements
To run the project locally, install:
- Visual Studio with the ASP.NET and web development workload.
- The .NET 10 SDK.
- SQL Server LocalDB (usually available with Visual Studio).
- The NuGet packages listed in RaceDay.API.csproj.
5. Database Setup
The project uses SQL Server LocalDB. The connection string is configured in RaceDay.API/appsettings.json:
{
  "ConnectionStrings": {
    "RaceDayConnection": "Server=(localdb)\\MSSQLLocalDB;Database=RaceDayDB;Trusted_Connection=True;MultipleActiveResultSets=true;TrustServerCertificate=True"
  }
}
The database name is RaceDayDB.
To create or update the database using Entity Framework Core:
1. Open the solution in Visual Studio.
2. Open Tools → NuGet Package Manager → Package Manager Console.
3. Set Default project to RaceDay.API.
4. Run:
Update-Database
The initial migration is named InitialCreate. If the database already exists and is up to date, you may not need to run the command again.
6. Run the API
1. Open the RaceDay solution in Visual Studio.
2. Set RaceDay.API as the startup project.
3. Build the solution.
4. Run the project with Ctrl + F5 or F5.
5. When running in the Development environment, open the Swagger UI URL shown by Visual Studio.
Swagger provides an interface for viewing and testing the API endpoints that have been implemented.
7. Authentication and Roles
The database model includes a user role field intended to support these roles:
- Organiser — intended to manage events and their categories.
- Participant — intended to enrol in event categories and view relevant event or result information.
Session authentication, password hashing, and role-based endpoint protection must be implemented and tested before these features can be considered complete.
8. API Endpoints
The available endpoints depend on the controllers implemented in the project. Open Swagger while the API is running to see the current endpoint list.
Planned API functionality includes:
- User registration and login.
- Organiser and participant profile management.
- Event management.
- Event category management.
- Participant enrolments.
- Race results.
Do not assume a planned endpoint is available until it appears in Swagger and has been tested.
9. Testing and Continuous Integration
Unit tests and a GitHub Actions workflow should be added to build and test the solution automatically when code is pushed to GitHub.
Current status: Add the test project and CI workflow here once they have been created and verified. Include a screenshot of a successful GitHub Actions run in the final submission if required by the assessment instructions.
11. GitHub Repository
Add your repository URL here:
https://github.com/Daven061028/RaceDay1
12. AI Use Disclosure
AI assistance was used to support development and documentation. The project code and functionality should be reviewed, understood, tested, and adapted by the student. Update this statement to match the assessment's AI-use disclosure requirements and the assistance actually used.
13. Project Status
The current development setup includes the Entity Framework Core context and models, an initial migration, the RaceDayDB LocalDB database, and Swagger startup.
Before final submission, verify that all required endpoints, authentication and role checks, unit tests, GitHub Actions workflow, and demonstration video are completed and working. Follow the official assessment brief for the final submission requirements.
