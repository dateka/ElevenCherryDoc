# Verify Email Request Model

### Path: /Models/Accounts/VerifyEmailRequest.cs

Le mod�le de demande de v�rification par e-mail d�finit les param�tres des demandes POST entrantes vers la route **/accounts/verify-email** de l'API standard, il est attach� � la route en le d�finissant comme param�tre de la m�thode d'action **VerifyEmail** du **account controller**. Lorsqu'une requ�te HTTP POST est re�ue par la route, les donn�es du corps sont li�es � une instance de la classe **VerifyEmail**, valid�es et transmises � la m�thode.

Les annotations de donn�es .NET sont utilis�es pour g�rer automatiquement la validation du mod�le, **[Required]** rend le jeton requis.