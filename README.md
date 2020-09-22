# .NET Core MVC 3.1 YouTube Tutorial

 This project is created by following the course of the YouTuber "Les Jackson" step by step (but surely with a little touch of my own programming style).

## Tutorial

You can find a full-course introduction to .NET Core's MVC REST API on the following [URL](https://www.youtube.com/watch?v=fmvcAzHpsk8). The tutorial is given by the YouTuber "Les Jackson" and is (in my opinion) made for people with none- to a little understanding to REST since everything is being thoroughly explained.

## Project description

The idea behind this application is to hold a table in our SQL Server Database which contains all the available .NET commands together with their explanation. As mentioned, this project uses a Microsoft SQL Server Database to store everything in, which brings me to the following requirements.

## Requirements

You need the following assets:

* Sql Server
  * > It is also possible to manually swap the database to one you prefer, e.g. H2/Memory Database. These changes should happen in the `Startup.cs`- and `Commander.csproj`-files. (Adding them through the NuGet Package Manager)
  <br/>Note: when swapping out the databases, do not forget to take out SqlServer's package reference out of `Commander.csproj`.

* Dotnet (including its command tools)
  * E.g. `dotnet ef migrations add [Name]`
  * You can install it with the following command: `dotnet tool install --global dotnet-ef`.

* A Sql Server user with `sysadmin` permissions with the following credentials
  * Username: `CommanderAPI`
  * Password: `password`
  * > When creating a user with different credentials, do not forget to swap out the connection string inside `appsettings.json`.

* An IDE of your choice
  * Recommended: Visual Studio 2019 (latest version)
  * Optional: Visual Studio Code with the [following extensions](https://marketplace.visualstudio.com/items?itemName=doggy8088.netcore-extension-pack)

* The `CommanderDB` which can be created by entering the following command inside the terminal of this project:
  * `dotnet ef database update`
  * This command will automatically create the database for you due to an already existing migration. If you change or add models/properties, these changes should be applied with the following command: `dotnet ef migrations add [ShortDescriptionOfTheChanges]`, followed with the command above.

## Run project

This project will run on the localhost on ports 5000 (HTTP) and 5001 (HTTPS). These can of course be changed inside the `launchSettings.sjon`-file.

You can start this project by pressing the green play-button on Visual Studio, using F5 (Debugging) or CTRL+F5 (/w Debugging).

In an IDE like VSCode you can run this project by entering the following command inside the terminal: `dotnet run`.

## Credits

All credits go to the maker of this tutorial as I am just a student replicating his code / following his course to expand my skills.

[Les Jacksons's GitHub](https://github.com/binarythistle) and [YouTube channel](https://www.youtube.com/c/binarythistle)
