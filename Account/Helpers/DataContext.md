# Data Context

### Path: /Helpers/DataContext.cs

La classe de contexte de donn�es est utilis�e pour acc�der aux donn�es d'application via Entity Framework Core et est configur�e pour se connecter � une base de donn�es SQLite.   
Il d�rive de la classe EF Core DbContext et poss�de une propri�t� **Accounts** publique pour acc�der aux donn�es de compte et les g�rer. Le contexte de donn�es est utilis� par les services pour g�rer toutes les op�rations de donn�es de bas niveau.

Pour utiliser une base de donn�es diff�rente (par exemple, SQL Server, MySql, PostgreSQL), mettez � jour le fournisseur de base de donn�es dans la m�thode **OnConfiguration**, puis supprimez et r�g�n�rez les migrations de base de donn�es avec la commande **dotnet ef migrations, ajoutez InitialCreate**.   
Les migrations de base de donn�es sont ex�cut�es au **startup** de sorte que la base de donn�es est cr��e automatiquement la premi�re fois que vous d�marrez l'API.