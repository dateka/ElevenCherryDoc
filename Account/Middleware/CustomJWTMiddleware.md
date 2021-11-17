# Custom JWT Middleware

### Path: /Middleware/JwtMiddleware.cs

Le middleware JWT personnalis� v�rifie s'il y a un jeton dans l'en-t�te **Authorization** de la demande et, si c'est le cas, tente de�:

1. Valider le jeton
1. Extraire l'identifiant du compte du jeton
1. Attachez le compte authentifi� � la collection **HttpContext.Items** actuelle pour le rendre accessible dans le cadre de la demande actuelle

S'il n'y a pas de jeton dans l'en-t�te de la demande ou si l'une des �tapes ci-dessus �choue, aucun compte n'est attach� au contexte http et la demande ne pourra acc�der qu'aux routes publiques.   
L'autorisation est effectu�e par **[custom authorize attribute](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Helpers/CustomAuthorizeAttribute.md)** qui v�rifie qu'un compte est attach� au contexte http, si l'autorisation �choue, une r�ponse **401 Unauthorized** est renvoy�e.