# OpenGamesListWebApp_Chapter10-updated
This project is an attempt to update the sample app from Valerio De Sanctis' book [ASP.NET Core and Angular 2](http://a.co/8xZfy9L) so that it uses latest beta versions of OpenIddict. The sample code in the book relies on OpenIddict 1.0.0-alpha2-0419, which is [no longer available](https://github.com/openiddict/openiddict-core/issues/390). The latest version of OpenIddict at the moment (April 2017) is 
1.0.0-beta2-0559, which includes substantial changes since the Alpha version, including the removal of the OpenIddictDbContext class.

In the process of updating, I also went ahead and moved to Angular 2.4, Typescript 2.2, and the latest .csproj-based dotnet tooling.

# Installation Instructions
1. Clone the repository: 
`git clone https://github.com/astegmaier/OpenGamesListWebApp_Chapter10-updated.git`
2. Move to the root directory, and restore nuget packages: 
`dotnet restore`
3. Install npm packages: 
`npm install`
4. Install gulp if it isn't installed already: 
`npm install -g gulp`
5. Use gulp to build the client app (using the included gulpfile.js) in the client.
`gulp`
6. Switch to "Development Mode" in the command line: 
`set ASPNETCORE_ENVIRONMENT=Development`
7. Make sure you have a local development SQL Server available (This is typically installed with Visual Studio) that can be accessed with the connection string stored in appsettings.json.
8. Use migrations to create the development database and populate it correctly:
`dotnet ef migrations add FirstMigration`
`dotnet ef database update`
9. Start the application. This should seed the database automatically.
`dotnet run`
