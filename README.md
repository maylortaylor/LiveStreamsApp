# .NET CORE 2.1 & Angular 6.1.6 Web Application

# Getting Started

## In your first terminal / bash/ command prompt

1.   Navigate to the `LiveStreams.Web/ClientApp` folder. (this is where the Angular app is located)
     Then run:

             npm install

     (this will install all of the NPM packages for the Angular app)

2.   Stay in the `LiveStreams.Web/ClientApp` folder and run:

             ng build

     (this will build the Angular app)

3.   Navigate back to `LiveStrams.Web/` folder. (main folder for Web project)
     Then run:

             dotnet restore

     (this should install any dependecies that .NET needs)

4.   Stay in the `LiveStrams.Web/` folder.
     Then run:

             dotnet run

     (this should run the Web application at [https://localhost:5001](https://localhost:5001))

## In your second terminal / bash/ command prompt

1.   Navigate to the `/LiveStreams.Api/` folder. (main folder for the API project)
     Then run:

          dotnet restore

2.   Stay in the `/LiveStreams.Api/` folder and run:

     dotnet run

(this should run the API on [https://localhost:5050/api](https://localhost:5050/api))

# Being Safe And Secure

1.   Add an appsettings.development.json file to your project. Use this file for storing all your configuration values
2.   Use appsettings.json only as an example template and never to store any settings. This file will be checked into source control and will be used by developers to setup their own appsettings.{env.EnvironmentName}.json file
3.   Add a .gitignore rule to ignore appsettings.{env.EnvironmentName}.json

         # ignore appsettings configuration files
         **/appsettings.development.json
         **/appsettings.staging.json
         **/appsettings.production.json

# ASP.NET Core + Angular 6.1 + API server + IdentityServer 4

This solution has 3 projects.

1. **LiveStreams.Api** --> Intended to be the API to send data from the database to the Web Client. Runs locally on [http://localhost:5050](http://localhost:5050)

Restore dependencies:

        dotnet restore

Run before using project

        dotnet run

2. **LiveStreams.IdentityServer4** --> Templated from the [dotnet templates](https://github.com/IdentityServer/IdentityServer4.Templates)

Install with:

        dotnet new -i identityserver4.templates

Then using:

        dotnet new is4aspid

3. **LiveStreams.Web** --> Intended to be the Web Client project. This serves the Angular 6 application. It runs locally on [http://localhost:5001](http://localhost:5001)

Restore dependencies:

        dotnet restore

Run before using project

        dotnet run
