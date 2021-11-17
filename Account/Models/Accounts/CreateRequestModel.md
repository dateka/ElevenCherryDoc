# Create Request Model

### Path: /Models/Accounts/CreateRequest.cs

Le modèle de requête de création définit les paramètres des requêtes POST entrantes vers la route **/accounts**, il est attaché à la route en le définissant comme paramètre de la méthode d'action **Create** du **[accounts controller](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Controller/AccountsController.md)**. Lorsqu'une requête HTTP POST est reçue par la route, les données du corps sont liées à une instance de la classe **CreateRequest**, validées et transmises à la méthode.

Les annotations de données .NET sont utilisées pour gérer automatiquement la validation du modèle, **[Required]** rend toutes les propriétés requises, **[EmailAddress]** valide que la propriété de messagerie contient une adresse e-mail valide, **[EnumDataType(typeof(Role))]** valide que la propriété de rôle correspond à une des rôles de l'API (Admin ou User), **[MinLength(6)]** valide que le mot de passe contient au moins six caractères et **[Comparer("Password")]** valide que la propriété de confirmation du mot de passe correspond à la propriété de mot de passe.