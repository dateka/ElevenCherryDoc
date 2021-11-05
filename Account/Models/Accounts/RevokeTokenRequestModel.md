# Revoke Token Request Model

### Path: /Models/Accounts/RevokeTokenRequest.cs

Le modèle de demande de jeton de révocation définit les paramètres des demandes POST entrantes vers la route **/accounts/revoke-token** de l'API standard, il est attaché à la route en le définissant comme paramètre de la méthode d'action **RevokeToken** du **account controller**. Lorsqu'une requête HTTP POST est reçue par la route, les données du corps sont liées à une instance de la classe **RevokeToken**, validées et transmises à la méthode.

Le champ **Token** est facultatif dans le corps de la demande car il peut également être transmis dans le cookie **refreshToken**, consultez le contrôleur de comptes pour plus de détails.