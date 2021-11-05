# Verify Email Request Model

### Path: /Models/Accounts/VerifyEmailRequest.cs

Le modèle de demande de vérification par e-mail définit les paramètres des demandes POST entrantes vers la route **/accounts/verify-email** de l'API standard, il est attaché à la route en le définissant comme paramètre de la méthode d'action **VerifyEmail** du **account controller**. Lorsqu'une requête HTTP POST est reçue par la route, les données du corps sont liées à une instance de la classe **VerifyEmail**, validées et transmises à la méthode.

Les annotations de données .NET sont utilisées pour gérer automatiquement la validation du modèle, **[Required]** rend le jeton requis.