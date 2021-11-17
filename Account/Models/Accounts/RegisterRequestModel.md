# Register Request Model

### Path: /Models/Accounts/RegisterRequest.cs

Le mod�le de demande de registre d�finit les param�tres des demandes POST entrantes vers la route **/accounts/register**, il est attach� � la route en le d�finissant comme param�tre de la m�thode d'action **Register** du **[account controller](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Controller/AccountsController.md)**. Lorsqu'une requ�te HTTP POST est re�ue par la route, les donn�es du corps sont li�es � une instance de la classe **RegisterRequest**, valid�es et transmises � la m�thode.

Les annotations de donn�es .NET sont utilis�es pour g�rer automatiquement la validation du mod�le, **[Required]** rend toutes les propri�t�s requises, **[EmailAddress]** valide que la propri�t� email contient une adresse email valide, **[MinLength(6)]** valide que le mot de passe contient au moins six caract�res, **[Compare("Mot de passe")]** valide que la propri�t� de confirmation de mot de passe correspond � la propri�t� de mot de passe, et **[Range(typeof(bool), "true", "true")]** valide que la propri�t� d'acceptation des termes contient **true**.