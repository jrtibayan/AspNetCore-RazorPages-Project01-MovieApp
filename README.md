# Movie App made with Razor Pages in ASP.NET Core
Learning to build a Razor Pages App in ASP.NET Core. An app that display and manage a database of movies.

## What I learned from this Project.
1. Create a Razor Pages Web App  
This created a bunch of files necessary for a basic Razor Page App

2. Add Models folder
3. Create Movie Class inside Models folder  
This created Movie.cs file which contain the basic code of the created Movie Class

4. Added properties to Movie Class  
A Movie may contain different properties.  
In this case we added a Title, Genre, Release Date, and Price.  
We also added **ID** property because it is **required by database** as primary key

5. Added Movies folder inside Pages folder

6. Added Scaffold Item \(Razor Pages using Entity Framework \(CRUD\)\) inside Pages>Movies folder  
This created files inside Pages>Movies folder that are to be used for CRUD operations.  
This also updated appsettings.json with the connection string used to connect to a local database.

7. Ran `Add-Migration Initial` and `Update-Database` on Tools > NuGet Package Manager > Package Manager Console

8. Test the App.  
Go to localhost:port/Movies and try out the app.  
You should now be able to do CRUD operations

9. Troubleshoot if not working  
If you get error `SqlException: Cannot open database "RazorPagesMovieContext-GUID" requested by the login. The login failed.
Login failed for user 'User-name'.` - you missed migration step.