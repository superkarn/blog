---
layout: post
title:  "Creating ASP.NET Core project with React and Authentication"
date:   2020-12-27 00:00:00 +0000
categories: 
---

When creating a new ASP.NET Core project with React and built-in authentication (IdentityServer), you can use the following command (see [here](https://docs.microsoft.com/en-us/aspnet/core/security/authentication/identity-api-authorization?view=aspnetcore-5.0) for more information):
```
dotnet new react -o my-new-app -au Individual
```

This will create a new project with ASP.NET as an API backend, standard create-react-app (CRA) as the front end, and IdentityServer for authentication and authorization.  However, the default database is SQLite.  If you try to switch to SQL Server, you'll run into the following error:

> Entity Framework Core: Column 'Id' in table 'Users' is of a type that is invalid for use as a key column in an index


This is because the initial EF migration files were generated with SQLite data types.  You will need to delete and regenerate the migration files for SQL Server.

1. Uninstall `Microsoft.EntityFrameworkCore.Sqlite`
1. Install `Microsoft.EntityFrameworkCore.SqlServer`
1. Update the connection string
1. In `Startup.cs`, update `ConfigureServices()` to use SQL Server
```
services.AddDbContext<ApplicationDbContext>(options =>
    options.UseSqlServer(
        Configuration.GetConnectionString("DefaultConnection")));
```
1. Remove existing migration files (because they're meant for SQLite) 
```
/Data/Migrations/00000000000000_CreateIdentitySchema.cs
/Data/Migrations/00000000000000_CreateIdentitySchema.Designer.cs
/Data/Migrations/ApplicationDbContextModelSnapshot.cs
```
1. Regenerate the migration files for SQL Server
```
dotnet ef migrations add CreateIdentitySchema --output-dir "Data/Migrations"
```
1. Run EF Migration to generate the initial tables