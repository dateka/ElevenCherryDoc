# App Settings

### Path: /Helpers/AppSettings.cs

La classe de param�tres d'application contient des propri�t�s d�finies dans le fichier **appsettings.json** et est utilis�e pour acc�der aux param�tres d'application via des objets inject�s dans des classes � l'aide du syst�me d'injection de d�pendance (DI) int�gr� .NET.   
Par exemple, le **[account service](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Services/AccountService.md)** acc�de aux param�tres de l'application via un objet **IOptions<AppSettings> appSettings** qui est inject� dans le constructeur.

Le mappage des sections de configuration aux classes est effectu� dans la m�thode **ConfigureServices** du fichier **Startup.cs**.