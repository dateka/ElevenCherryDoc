# Forgot Password Request Model

### Path: /Models/Accounts/ForgotPasswordRequest.cs

Le modèle de demande de mot de passe oublié définit les paramètres des requêtes POST entrantes vers la route **/accounts/forgot-password** de l'API standard, il est attaché à la route en le définissant comme paramètre de la méthode d'action **ForgotPassword** du accounts controller. Lorsqu'une requête HTTP POST est reçue par la route, les données du corps sont liées à une instance de la classe **ForgotPasswordRequest**, validées et transmises à la méthode.

Les annotations de données .NET sont utilisées pour gérer automatiquement la validation du modèle, **[Required]** rend l'e-mail obligatoire et **[EmailAddress]** valide qu'il contient une adresse e-mail valide.