# Reset Password Request Model

### Path: /Models/Accounts/ResetPasswordRequest.cs

Le mod�le de demande de r�initialisation de mot de passe d�finit les param�tres des demandes POST entrantes vers la route **/accounts/reset-password**, il est attach� � la route en le d�finissant comme param�tre de la m�thode d'action **ResetPassword** du **[account controller](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Controller/AccountsController.md)**. Lorsqu'une requ�te HTTP POST est re�ue par la route, les donn�es du corps sont li�es � une instance de la classe **ResetPassword**, valid�es et transmises � la m�thode.

Les annotations de donn�es .NET sont utilis�es pour g�rer automatiquement la validation du mod�le, **[Required]** rend toutes les propri�t�s requises, **[MinLength(6)]** valide que le mot de passe contient au moins six caract�res et **[Compare("Password")]** valide que le mot de passe de confirmation la propri�t� correspond � la propri�t� du mot de passe.