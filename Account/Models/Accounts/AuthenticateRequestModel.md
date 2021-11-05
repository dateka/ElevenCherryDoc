# Authenticate Request Model

### Path: /Models/Accounts/AuthenticateRequest.cs

Le modèle de demande d'authentification définit les paramètres des demandes POST entrantes vers la route **/accounts/authenticate**, il est attaché à la route en le définissant comme paramètre de la méthode d'action **Authenticate** du **account controller**. Lorsqu'une requête HTTP POST est reçue par la route, les données du corps sont liées à une instance de la classe **AuthenticateRequest**, validées et transmises à la méthode.

Les annotations de données .NET sont utilisées pour gérer automatiquement la validation du modèle, l'attribut **[Required]** définit à la fois l'e-mail et le mot de passe comme champs obligatoires. Ainsi, si l'un ou l'autre manque, un message d'erreur de validation est renvoyé par l'API. De même, l'attribut **[EmailAddress]** valide que la propriété email contient une adresse email valide.