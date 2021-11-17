# Account Service

### Path: /Services/AccountService.cs

Le account service contient la logique commerciale de base pour l'inscription et la v�rification du compte, l'authentification avec des jetons JWT et d'actualisation, la fonctionnalit� de mot de passe oubli� et de r�initialisation de mot de passe, ainsi que les m�thodes CRUD pour la gestion des donn�es de compte. Le service encapsule toutes les interactions avec le **data context** EF Core et expose un ensemble simple de m�thodes utilis�es par le **accounts controller**.

Le haut du fichier contient l'interface **IAccountService** qui d�finit les m�thodes publiques pour le account service, et en dessous de l'interface se trouve la classe **AccountService** concr�te qui impl�mente l'interface.