# Data Context

### Path: /Helpers/DataContext.cs

La classe de contexte de données est utilisée pour accéder aux données d'application via Entity Framework Core et est configurée pour se connecter à une base de données SQLite.   
Il dérive de la classe EF Core DbContext et possède une propriété **Accounts** publique pour accéder aux données de compte et les gérer. Le contexte de données est utilisé par les services pour gérer toutes les opérations de données de bas niveau.

Pour utiliser une base de données différente (par exemple, SQL Server, MySql, PostgreSQL), mettez à jour le fournisseur de base de données dans la méthode **OnConfiguration**, puis supprimez et régénérez les migrations de base de données avec la commande **dotnet ef migrations, ajoutez InitialCreate**.   
Les migrations de base de données sont exécutées au **startup** de sorte que la base de données est créée automatiquement la première fois que vous démarrez l'API.