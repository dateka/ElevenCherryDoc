# Update Request Model

### Path: /Models/Accounts/UpdateRequest.cs

Le modèle de demande de mise à jour définit les paramètres des demandes PUT entrantes vers la route **/accounts/{id:int}**, il est attaché à la route en le définissant comme paramètre de la méthode d'action **Update** du **[account controller](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Controller/AccountsController.md)**. Lorsqu'une requête HTTP PUT est reçue par la route, les données du corps sont liées à une instance de la classe **UpdateRequest**, validées et transmises à la méthode.

Les annotations de données .NET sont utilisées pour gérer automatiquement la validation du modèle, **[EnumDataType(typeof(Role))]** valide que la propriété du rôle correspond à l'un des rôles de l'API (Admin ou User), **[EmailAddress]** valide que la propriété de l'e-mail contient un e-mail valide adresse, **[MinLength(6)]** valide que le mot de passe contient au moins six caractères et **[Compare("Password")]** valide que la propriété de confirmation de mot de passe correspond à la propriété de mot de passe.

Aucune des propriétés n'a l'attribut **[Required]**, ce qui les rend toutes facultatives, et les champs omis ne sont pas mis à jour dans la base de données.

Certains attributs de validation ne gèrent pas bien les chaînes vides, de sorte que les propriétés avec des attributs de validation remplacent les chaînes vides par **null** sur **l'ensemble** pour garantir que les valeurs de chaîne vides sont ignorées.