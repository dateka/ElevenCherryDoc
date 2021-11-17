# Authenticate Response Model

### Path: /Models/Accounts/AuthenticateResponse.cs

Le modèle de réponse d'authentification définit les données renvoyées par les méthodes **Authenticate** et **RefreshToken** du **[accounts controller](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Controller/AccountsController.md)** et du **[account service](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Services/AccountService.md)**. Il comprend les détails de base du compte, un jeton jwt et un jeton d'actualisation.

La propriété du jeton d'actualisation est décorée avec l'attribut **[JsonIgnore]** qui empêche la propriété d'être renvoyée dans le corps de la réponse de l'API. Cela est dû au fait que le jeton d'actualisation est renvoyé en tant que cookie HTTP uniquement au lieu d'être dans le corps.