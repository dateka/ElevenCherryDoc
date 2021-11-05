# Custom Authorize Attribute

### Path: /Helpers/AuthorizeAttribute.cs

L'attribut d'autorisation personnalis� est ajout� aux m�thodes d'action du contr�leur qui n�cessitent que l'utilisateur soit authentifi� et qu'il ait �ventuellement un r�le sp�cifi�.   
Si un r�le est sp�cifi� (par exemple **[Authorize(Role.Admin)]**), la route est limit�e aux utilisateurs de ce r�le, sinon la route est limit�e � tous les utilisateurs authentifi�s, quel que soit leur r�le.

L'autorisation est effectu�e par la m�thode **OnAuthorization** qui v�rifie s'il existe un compte authentifi� attach� � la demande en cours (**context.HttpContext.Items["Account"]**) et que le compte est autoris� en fonction de son r�le (si sp�cifi�).

En cas d'autorisation r�ussie, aucune action n'est entreprise et la demande est transmise � la m�thode d'action du contr�leur, si l'autorisation �choue, une r�ponse **401 Unauthorized** est renvoy�e.