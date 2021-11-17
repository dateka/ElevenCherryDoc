# Custom JWT Middleware

### Path: /Middleware/JwtMiddleware.cs

Le middleware JWT personnalisé vérifie s'il y a un jeton dans l'en-tête **Authorization** de la demande et, si c'est le cas, tente de :

1. Valider le jeton
1. Extraire l'identifiant du compte du jeton
1. Attachez le compte authentifié à la collection **HttpContext.Items** actuelle pour le rendre accessible dans le cadre de la demande actuelle

S'il n'y a pas de jeton dans l'en-tête de la demande ou si l'une des étapes ci-dessus échoue, aucun compte n'est attaché au contexte http et la demande ne pourra accéder qu'aux routes publiques.   
L'autorisation est effectuée par **[custom authorize attribute](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Helpers/CustomAuthorizeAttribute.md)** qui vérifie qu'un compte est attaché au contexte http, si l'autorisation échoue, une réponse **401 Unauthorized** est renvoyée.