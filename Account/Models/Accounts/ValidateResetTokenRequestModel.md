# Validate Reset Token Request Model

### Path: /Models/Accounts/ValidateResetTokenRequest.cs

Le mod�le de demande de jeton de r�initialisation de validation d�finit les param�tres des demandes POST entrantes vers la route **/accounts/validate-reset-token**, il est attach� � la route en le d�finissant comme param�tre de la m�thode d'action **ValidateResetToken** du **account controller**. Lorsqu'une requ�te HTTP POST est re�ue par la route, les donn�es du corps sont li�es � une instance de la classe **ValidateResetToken**, valid�es et transmises � la m�thode.

Les annotations de donn�es .NET sont utilis�es pour g�rer automatiquement la validation du mod�le, **[Required]** rend le jeton requis.