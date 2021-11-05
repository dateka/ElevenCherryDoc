# Custom Authorize Attribute

### Path: /Helpers/AuthorizeAttribute.cs

L'attribut d'autorisation personnalisé est ajouté aux méthodes d'action du contrôleur qui nécessitent que l'utilisateur soit authentifié et qu'il ait éventuellement un rôle spécifié.   
Si un rôle est spécifié (par exemple **[Authorize(Role.Admin)]**), la route est limitée aux utilisateurs de ce rôle, sinon la route est limitée à tous les utilisateurs authentifiés, quel que soit leur rôle.

L'autorisation est effectuée par la méthode **OnAuthorization** qui vérifie s'il existe un compte authentifié attaché à la demande en cours (**context.HttpContext.Items["Account"]**) et que le compte est autorisé en fonction de son rôle (si spécifié).

En cas d'autorisation réussie, aucune action n'est entreprise et la demande est transmise à la méthode d'action du contrôleur, si l'autorisation échoue, une réponse **401 Unauthorized** est renvoyée.