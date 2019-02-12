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

10. Changed a bunch of stuff applicable to the whole App  
Changes to the Pages/Shared/_Layout.cshtml like the value on the Title tag will be seen though out the whole app.  
I changed the App's Title, text on the nav-brand class, and the value on the asp-page attribute which I think is where the link will go when clicked.

11. Examining the Create page model  
The `OnGet` method initializes any state needed for the page. The Create page doesn't have any state to initialize, so Page is returned.  
The `Movie` property  uses the `[BindProperty]` attribute to opt-in to model binding. When the Create form posts the form values, the ASP.NET Core runtime binds the posted values to the `Movie` model.  
The `OnPostAsync` method is run when the page posts form data