# Account Response Model

### Path: /Models/Accounts/AccountResponse.cs

Le modèle de réponse de compte définit les données de compte renvoyées par les méthodes **GetAll**, **GetById**, **Create** et **Update** du **[account controller](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Controller/AccountsController.md)** et du **[account service](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Services/AccountService.md)**.   
Il comprend les détails de base du compte et exclut les données sensibles telles que les mots de passe hachés et les jetons.