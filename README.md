# Dotnet API with Postgres, DTO and Docker
A Web API CRUD (Create, Read, Update, Delete) application using .NET Core, DTO and Postgres.

## DTO
DTO, or Data Transfer Object, is a design pattern used in object-oriented programming to transfer data between different layers of a program. The main goal of a DTO is to provide a simple interface for transferring data without any business logic from one layer to another.

### Run codes
```
dotnet new sln -o DotnetApiPostgres
cd DotnetApiPostgres
dotnet new webapi --use-controllers -n "DotnetApiPostgres.Api"
dotnet sln add DotnetApiPostgres.Api/DotnetApiPostgres.Api.csproj
cd DotnetApiPostgres.Api
```

### Open VSCode `code .` and install nuget packages
```
dotnet add package Npgsql.EntityFrameworkCore.PostgreSQL
dotnet add package Microsoft.EntityFrameworkCore.Design
```

### Migrations
```
dotnet tool install --global dotnet-ef
dotnet tool update --global dotnet-ef
dotnet ef migrations add "init"
dotnet ef database update
```

### Run on local
```
dotnet run
http://localhost:5133/api/people
http://localhost:5133/swagger
```

## Reference
- [ASP.NET Core API CRUD With Postgres](https://medium.com/codex/asp-net-core-api-crud-with-postgres-71544c94b8c7) by Ravindra Devrani \
- Learn [dotnet sln](https://learn.microsoft.com/en-us/dotnet/core/tools/dotnet-sln)