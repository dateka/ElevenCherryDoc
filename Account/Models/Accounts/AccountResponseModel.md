# Account Response Model

### Path: /Models/Accounts/AccountResponse.cs

Le mod�le de r�ponse de compte d�finit les donn�es de compte renvoy�es par les m�thodes **GetAll**, **GetById**, **Create** et **Update** du **account controller** et du **account service**.   
Il comprend les d�tails de base du compte et exclut les donn�es sensibles telles que les mots de passe hach�s et les jetons.