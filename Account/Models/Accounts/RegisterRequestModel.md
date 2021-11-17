# Register Request Model

### Path: /Models/Accounts/RegisterRequest.cs

Le modèle de demande de registre définit les paramètres des demandes POST entrantes vers la route **/accounts/register**, il est attaché à la route en le définissant comme paramètre de la méthode d'action **Register** du **[account controller](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Controller/AccountsController.md)**. Lorsqu'une requête HTTP POST est reçue par la route, les données du corps sont liées à une instance de la classe **RegisterRequest**, validées et transmises à la méthode.

Les annotations de données .NET sont utilisées pour gérer automatiquement la validation du modèle, **[Required]** rend toutes les propriétés requises, **[EmailAddress]** valide que la propriété email contient une adresse email valide, **[MinLength(6)]** valide que le mot de passe contient au moins six caractères, **[Compare("Mot de passe")]** valide que la propriété de confirmation de mot de passe correspond à la propriété de mot de passe, et **[Range(typeof(bool), "true", "true")]** valide que la propriété d'acceptation des termes contient **true**.