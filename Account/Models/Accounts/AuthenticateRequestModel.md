# Authenticate Request Model

### Path: /Models/Accounts/AuthenticateRequest.cs

Le mod�le de demande d'authentification d�finit les param�tres des demandes POST entrantes vers la route **/accounts/authenticate**, il est attach� � la route en le d�finissant comme param�tre de la m�thode d'action **Authenticate** du **account controller**. Lorsqu'une requ�te HTTP POST est re�ue par la route, les donn�es du corps sont li�es � une instance de la classe **AuthenticateRequest**, valid�es et transmises � la m�thode.

Les annotations de donn�es .NET sont utilis�es pour g�rer automatiquement la validation du mod�le, l'attribut **[Required]** d�finit � la fois l'e-mail et le mot de passe comme champs obligatoires. Ainsi, si l'un ou l'autre manque, un message d'erreur de validation est renvoy� par l'API. De m�me, l'attribut **[EmailAddress]** valide que la propri�t� email contient une adresse email valide.