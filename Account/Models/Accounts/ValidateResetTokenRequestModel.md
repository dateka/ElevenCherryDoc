# Validate Reset Token Request Model

### Path: /Models/Accounts/ValidateResetTokenRequest.cs

Le modèle de demande de jeton de réinitialisation de validation définit les paramètres des demandes POST entrantes vers la route **/accounts/validate-reset-token**, il est attaché à la route en le définissant comme paramètre de la méthode d'action **ValidateResetToken** du **account controller**. Lorsqu'une requête HTTP POST est reçue par la route, les données du corps sont liées à une instance de la classe **ValidateResetToken**, validées et transmises à la méthode.

Les annotations de données .NET sont utilisées pour gérer automatiquement la validation du modèle, **[Required]** rend le jeton requis.