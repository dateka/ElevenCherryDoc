# Revoke Token Request Model

### Path: /Models/Accounts/RevokeTokenRequest.cs

Le mod�le de demande de jeton de r�vocation d�finit les param�tres des demandes POST entrantes vers la route **/accounts/revoke-token** de l'API standard, il est attach� � la route en le d�finissant comme param�tre de la m�thode d'action **RevokeToken** du **account controller**. Lorsqu'une requ�te HTTP POST est re�ue par la route, les donn�es du corps sont li�es � une instance de la classe **RevokeToken**, valid�es et transmises � la m�thode.

Le champ **Token** est facultatif dans le corps de la demande car il peut �galement �tre transmis dans le cookie **refreshToken**, consultez le contr�leur de comptes pour plus de d�tails.