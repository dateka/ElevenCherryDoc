# App Settings

### Path: /Helpers/AppSettings.cs

La classe de paramètres d'application contient des propriétés définies dans le fichier **appsettings.json** et est utilisée pour accéder aux paramètres d'application via des objets injectés dans des classes à l'aide du système d'injection de dépendance (DI) intégré .NET.   
Par exemple, le **[account service](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Services/AccountService.md)** accède aux paramètres de l'application via un objet **IOptions<AppSettings> appSettings** qui est injecté dans le constructeur.

Le mappage des sections de configuration aux classes est effectué dans la méthode **ConfigureServices** du fichier **Startup.cs**.