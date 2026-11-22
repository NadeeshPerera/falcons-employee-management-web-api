# Falcons Employee Management System: Web API

The **ASP.NET Core Web API** for the Falcons Employee Management System. It exposes REST endpoints for employees, roles, projects, tasks, timesheets and leave.
The frontend is **[falcons-employee-management-react-app](https://github.com/NadeeshPerera/falcons-employee-management-react-app)** (React).

![C#](https://img.shields.io/badge/C%23-239120?logo=csharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET_Core_3.1-512BD4?logo=dotnet&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?logo=microsoftsqlserver&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?logo=microsoftazure&logoColor=white)
![AWS RDS](https://img.shields.io/badge/AWS_RDS-527FFF?logo=amazonrds&logoColor=white)

> The API was originally deployed to Azure App Service with a SQL Server database on AWS RDS. Both were decommissioned after the project ended.

## Endpoints (controllers)

| Controller | Purpose |
|---|---|
| `LoginController`, `UserLoginController`, `AuthRoleController` | Sign-in and role-based access (Admin / Employee) |
| `EmployeeDetailsController`, `EmployeeRoleController`, `EmployeeStatusController` | Employee records, roles and status |
| `ProjectController`, `StatusController` | Projects and project status |
| `TasksController`, `MyTasks` | Task assignment and an employee's own tasks |
| `Mytimesheet`, `TimeSheetlogs` | Timesheet entry and team logs |
| `LeaveEnquiryController`, `MyLeaveRequestController` | Leave requests and approvals |

## Tech stack

C# · ASP.NET Core 3.1 Web API · SQL Server (ADO.NET) · Azure App Service · AWS RDS · Visual Studio 2019 · SSMS

## Run locally

1. Create a SQL Server database named `falcons` and run `DB_table_Querries.sql` to create the tables.
2. Set the connection string. Keep credentials out of source control by using [user secrets](https://learn.microsoft.com/aspnet/core/security/app-secrets):
   ```bash
   dotnet user-secrets init
   dotnet user-secrets set "ConnectionStrings:TimesheetAppCon" "Server=localhost;Database=falcons;Trusted_Connection=True;"
   ```
3. Run the API:
   ```bash
   dotnet run
   ```

## Team Falcon

University group project (SLTC Research University, 2022). Team members:
K.S. Winodahewa · E.M.M.S. Ekanayaka · G.S.K. Abeywickrama · Nayani Nawarathne · R.M.J.N. Kumari Rajapaksha · Aqeel Ahamadh · S.A.S.A. Dissanayake · Tharushi Umayanga · M.M.R.Y.M.B. Amarathunga · **S.P.N.M. Perera (Nadeesh Perera)**
