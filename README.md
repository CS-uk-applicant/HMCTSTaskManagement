# HMCTSTaskManagement
Task management system built with ASP.NET Core razor pages
This is a simple task management system built using ASP.NET Core Razor Pages. It allows users to perform basic CRUD operations on tasks, which includes:
Creating, Viewing tasks, Updating, Deleting tasks

The backend of the system is built using Entity Framework Core to handle data operations, and the frontend is a Razor Pages app to present the data and interact with the user.

Features-
Create New Task: You can add a new task by specifying a title, description, and due date.
View Tasks: All tasks are displayed on the main page, showing the title, description, status, and due date.
Update Task Status: You can change the status of any task (e.g., Pending, Completed).
Delete Task: If you no longer need a task, you can delete it from the system.
Error Handling: Basic error handling is implemented to ensure the app runs smoothly.

Tech Stack-
Frontend: Razor Pages (ASP.NET Core)
Backend: C#, Entity Framework Core, ASP.NET Core
Database: In-memory db(for simplicity, but can be switched to SQL Server or other databases)

Setup-
To run this project locally, follow these steps:
1. Clone the repository:
git clone https://github.com/CS-uk-applicant/HMCTSTaskManagement
2. Open the project in Visual Studio:
3. Restore NuGet packages:
dotnet restore
4. Run the project:
dotnet run
This should run the project.

API Endpoints:
1. Home page - List of Tasks
URL: /
Method: GET
Purpose: Shows all the tasks that have been added so far.
Params: None

2. Create Task Page (form)
URL: /CreateTask
Method: GET
Purpose: Displays a form where user can fill title, description, status and due date.

3. Submit New Task
URL: /CreateTask
Method: POST
Purpose: Saves the new task into the database (in-memory db in my case).
Fields:
Required- Title, Status, DueDateTime
Optional- Description

4. View a Task
URL: /ViewTask/{id}
Method: GET
Purpose: Open a detailed view for a single task by id.
Params:
id (int)

5. Update Task
URL: /UpdateTask/{id}
Method(s):
GET: Loads the form with existing data in db
POST: Saves the updated task to db
Params:
id(int)

6. Delete a Task
URL: id={id}&handler=Delete
Method: POST
Purpose: Deletes the task based on its id.
Params:
id(int)


Running Tests:
To run tests for the project, you'll need to use the test project (CodeProject.Tests).

Contributing:
If you'd like to contribute to this project, feel free to fork the repository and create a pull request with your changes. 
If you find any bugs or have suggestions, feel free to open an issue. Contributions are always welcome!
