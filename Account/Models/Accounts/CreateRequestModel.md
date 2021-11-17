# Create Request Model

### Path: /Models/Accounts/CreateRequest.cs

Le mod�le de requ�te de cr�ation d�finit les param�tres des requ�tes POST entrantes vers la route **/accounts**, il est attach� � la route en le d�finissant comme param�tre de la m�thode d'action **Create** du **[accounts controller](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Controller/AccountsController.md)**. Lorsqu'une requ�te HTTP POST est re�ue par la route, les donn�es du corps sont li�es � une instance de la classe **CreateRequest**, valid�es et transmises � la m�thode.

Les annotations de donn�es .NET sont utilis�es pour g�rer automatiquement la validation du mod�le, **[Required]** rend toutes les propri�t�s requises, **[EmailAddress]** valide que la propri�t� de messagerie contient une adresse e-mail valide, **[EnumDataType(typeof(Role))]** valide que la propri�t� de r�le correspond � une des r�les de l'API (Admin ou User), **[MinLength(6)]** valide que le mot de passe contient au moins six caract�res et **[Comparer("Password")]** valide que la propri�t� de confirmation du mot de passe correspond � la propri�t� de mot de passe.