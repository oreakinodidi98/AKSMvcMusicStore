# Demo

## Section 1: Application Overview

- **Goal**: Modernize a legacy .NET Framework application and deploy it seamlessly on AKS
- **What is this app?**
  - MVC Music Store — a classic Microsoft sample app for learning ASP.NET MVC
  - It's a lightweight online music store that lets users browse albums by genre, add them to a shopping cart, and check out
  - Originally built as a tutorial over a decade ago, it has evolved through MVC 3 → MVC 4 → MVC 5
- **Tech stack (current state — legacy)**
  - ASP.NET MVC 5 on .NET Framework 4.8 -> has to run on windows container
  - Entity Framework 6 for data access (SQL Server / LocalDB)
  - OWIN-based authentication with ASP.NET Identity
  - Classic NuGet packages: jQuery 1.10, Bootstrap 3, Modernizr
  - Old-style `.csproj` (MSBuild XML format, not SDK-style)
- **Architecture — follows the MVC pattern**
  - **Models** — data entities (Album, Genre, Artist, Cart) + Entity Framework DbContext
  - **Controllers** — handle HTTP requests (Store, ShoppingCart, Account, Home, etc.)
  - **Views** — Razor `.cshtml` templates that render HTML
- **Why is this a good modernization candidate?**
  - It's a real, runnable app — not a toy "Hello World"
  - Uses patterns and dependencies common in enterprise .NET Framework apps
  - Has authentication, database access, and multiple controllers — representative of real workloads
  - Small enough to demo end-to-end in a single session

## Aim

- how to move this to a newer version of dotnet framework
- How to enable modern password authentication with Managed identity

## Steps

- Select Github Copilot App Mod
- Run Assesment
- Owner has been trying to move this app to move into passswordless authentication roughly a year ago
- The assesment tool has updated and now able to transform application effectively
- report shows the different issues that need to be addressed/updated
- Can move from AD into Entra -> can migrate from SQL server to Managed identity