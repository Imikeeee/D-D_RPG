# D-D_RPG
GitHub Copilot: Certainly! Here's a brief documentation of the `dotnet-rpg` project:

### Summary
The `dotnet-rpg` project is a C# web application that provides a RESTful API for managing characters and weapons in a role-playing game. It uses ASP.NET Core, Entity Framework Core, and AutoMapper.

### Project Structure
The project is structured as follows:
- `Controllers`: Contains the API controllers.
- `Data`: Contains the database context and repository classes.
- `Dtos`: Contains the data transfer objects used by the API.
- `Models`: Contains the entity models used by the database context.
- `Profiles`: Contains the AutoMapper profiles used for object mapping.
- `Properties`: Contains project properties such as assembly information.
- `Services`: Contains the service classes used by the API.
- `appsettings.json`: Contains the application configuration settings.
- `Program.cs`: Contains the entry point of the application.
- `Startup.cs`: Contains the application configuration and middleware pipeline.

### Dependencies
The project has the following dependencies:
- `Microsoft.AspNetCore.Authentication.JwtBearer`: Provides authentication middleware that uses JWT tokens.
- `Microsoft.AspNetCore.Mvc.NewtonsoftJson`: Provides JSON serialization and deserialization functionality.
- `Microsoft.EntityFrameworkCore`: Provides Entity Framework Core functionality.
- `Microsoft.EntityFrameworkCore.Design`: Provides design-time support for Entity Framework Core.
- `Microsoft.EntityFrameworkCore.Sqlite`: Provides SQLite database support for Entity Framework Core.
- `Microsoft.EntityFrameworkCore.Tools`: Provides Entity Framework Core tools for the command line.
- `Microsoft.Extensions.Configuration`: Provides configuration functionality.
- `Microsoft.Extensions.Configuration.Json`: Provides JSON configuration file support.
- `Microsoft.Extensions.DependencyInjection`: Provides dependency injection functionality.
- `Microsoft.Extensions.Hosting`: Provides hosting functionality.
- `Microsoft.IdentityModel.Tokens`: Provides classes for working with JWT tokens.
- `AutoMapper.Extensions.Microsoft.DependencyInjection`: Provides AutoMapper integration with dependency injection.

### API Endpoints
The API provides the following endpoints:
- `POST /api/auth/register`: Registers a new user.
- `POST /api/auth/login`: Logs in a user and returns a JWT token.
- `GET /api/characters`: Gets a list of all characters.
- `GET /api/characters/{id}`: Gets a character by ID.
- `POST /api/characters`: Creates a new character.
- `PUT /api/characters/{id}`: Updates a character by ID.
- `DELETE /api/characters/{id}`: Deletes a character by ID.
- `GET /api/weapons`: Gets a list of all weapons.
- `GET /api/weapons/{id}`: Gets a weapon by ID.
- `POST /api/weapons`: Creates a new weapon.
- `PUT /api/weapons/{id}`: Updates a weapon by ID.
- `DELETE /api/weapons/{id}`: Deletes a weapon by ID.

### Authentication
The API uses JWT authentication. To access protected endpoints, clients must include a JWT token in the `Authorization` header of their requests. The token can be obtained by logging in with a valid username and password using the `/api/auth/login` endpoint.

### Database
The project uses SQLite as its database. The database is created and seeded with test data when the application starts up.

### Running the Project
To run the project, navigate to the root directory of the project in the terminal and run the following commands:
```
dotnet restore
dotnet run
```
This will restore the project dependencies and start the web server. You can then access the API endpoints using a tool such as Postman or a web browser.
