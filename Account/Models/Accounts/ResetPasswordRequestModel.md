# Reset Password Request Model

### Path: /Models/Accounts/ResetPasswordRequest.cs

Le modèle de demande de réinitialisation de mot de passe définit les paramètres des demandes POST entrantes vers la route **/accounts/reset-password**, il est attaché à la route en le définissant comme paramètre de la méthode d'action **ResetPassword** du **[account controller](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Controller/AccountsController.md)**. Lorsqu'une requête HTTP POST est reçue par la route, les données du corps sont liées à une instance de la classe **ResetPassword**, validées et transmises à la méthode.

Les annotations de données .NET sont utilisées pour gérer automatiquement la validation du modèle, **[Required]** rend toutes les propriétés requises, **[MinLength(6)]** valide que le mot de passe contient au moins six caractères et **[Compare("Password")]** valide que le mot de passe de confirmation la propriété correspond à la propriété du mot de passe.