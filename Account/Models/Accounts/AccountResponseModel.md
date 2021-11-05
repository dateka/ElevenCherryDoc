# Account Response Model

### Path: /Models/Accounts/AccountResponse.cs

Le modèle de réponse de compte définit les données de compte renvoyées par les méthodes **GetAll**, **GetById**, **Create** et **Update** du **account controller** et du **account service**.   
Il comprend les détails de base du compte et exclut les données sensibles telles que les mots de passe hachés et les jetons.