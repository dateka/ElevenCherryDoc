# Update Request Model

### Path: /Models/Accounts/UpdateRequest.cs

Le mod�le de demande de mise � jour d�finit les param�tres des demandes PUT entrantes vers la route **/accounts/{id:int}**, il est attach� � la route en le d�finissant comme param�tre de la m�thode d'action **Update** du **[account controller](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Controller/AccountsController.md)**. Lorsqu'une requ�te HTTP PUT est re�ue par la route, les donn�es du corps sont li�es � une instance de la classe **UpdateRequest**, valid�es et transmises � la m�thode.

Les annotations de donn�es .NET sont utilis�es pour g�rer automatiquement la validation du mod�le, **[EnumDataType(typeof(Role))]** valide que la propri�t� du r�le correspond � l'un des r�les de l'API (Admin ou User), **[EmailAddress]** valide que la propri�t� de l'e-mail contient un e-mail valide adresse, **[MinLength(6)]** valide que le mot de passe contient au moins six caract�res et **[Compare("Password")]** valide que la propri�t� de confirmation de mot de passe correspond � la propri�t� de mot de passe.

Aucune des propri�t�s n'a l'attribut **[Required]**, ce qui les rend toutes facultatives, et les champs omis ne sont pas mis � jour dans la base de donn�es.

Certains attributs de validation ne g�rent pas bien les cha�nes vides, de sorte que les propri�t�s avec des attributs de validation remplacent les cha�nes vides par **null** sur **l'ensemble** pour garantir que les valeurs de cha�ne vides sont ignor�es.