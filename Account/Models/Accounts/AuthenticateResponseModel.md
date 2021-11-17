# Authenticate Response Model

### Path: /Models/Accounts/AuthenticateResponse.cs

Le mod�le de r�ponse d'authentification d�finit les donn�es renvoy�es par les m�thodes **Authenticate** et **RefreshToken** du **[accounts controller](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Controller/AccountsController.md)** et du **[account service](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Services/AccountService.md)**. Il comprend les d�tails de base du compte, un jeton jwt et un jeton d'actualisation.

La propri�t� du jeton d'actualisation est d�cor�e avec l'attribut **[JsonIgnore]** qui emp�che la propri�t� d'�tre renvoy�e dans le corps de la r�ponse de l'API. Cela est d� au fait que le jeton d'actualisation est renvoy� en tant que cookie HTTP uniquement au lieu d'�tre dans le corps.