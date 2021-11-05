# Forgot Password Request Model

### Path: /Models/Accounts/ForgotPasswordRequest.cs

Le mod�le de demande de mot de passe oubli� d�finit les param�tres des requ�tes POST entrantes vers la route **/accounts/forgot-password** de l'API standard, il est attach� � la route en le d�finissant comme param�tre de la m�thode d'action **ForgotPassword** du accounts controller. Lorsqu'une requ�te HTTP POST est re�ue par la route, les donn�es du corps sont li�es � une instance de la classe **ForgotPasswordRequest**, valid�es et transmises � la m�thode.

Les annotations de donn�es .NET sont utilis�es pour g�rer automatiquement la validation du mod�le, **[Required]** rend l'e-mail obligatoire et **[EmailAddress]** valide qu'il contient une adresse e-mail valide.