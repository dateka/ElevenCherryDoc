# Account Response Model

### Path: /Models/Accounts/AccountResponse.cs

Le mod�le de r�ponse de compte d�finit les donn�es de compte renvoy�es par les m�thodes **GetAll**, **GetById**, **Create** et **Update** du **[account controller](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Controller/AccountsController.md)** et du **[account service](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Services/AccountService.md)**.   
Il comprend les d�tails de base du compte et exclut les donn�es sensibles telles que les mots de passe hach�s et les jetons.