# Account Service

### Path: /Services/AccountService.cs

Le account service contient la logique commerciale de base pour l'inscription et la vérification du compte, l'authentification avec des jetons JWT et d'actualisation, la fonctionnalité de mot de passe oublié et de réinitialisation de mot de passe, ainsi que les méthodes CRUD pour la gestion des données de compte. Le service encapsule toutes les interactions avec le **data context** EF Core et expose un ensemble simple de méthodes utilisées par le **accounts controller**.

Le haut du fichier contient l'interface **IAccountService** qui définit les méthodes publiques pour le account service, et en dessous de l'interface se trouve la classe **AccountService** concrète qui implémente l'interface.