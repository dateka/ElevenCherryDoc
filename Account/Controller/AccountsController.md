# Accounts Controller

### Path: /Controllers/AccountsController.cs

AccountsController définit et gère toutes les routes / endpoints pour l'API qui se rapportent aux comptes, y compris l'inscription, la vérification, l'authentification, le mot de passe oublié, l'actualisation et la révocation des jetons et les opérations de gestion de compte (CRUD).   
Dans chaque méthode de routage, le contrôleur appelle le service de compte pour effectuer l'action requise, ce qui permet au contrôleur de rester « allégé » et complètement séparé de la logique métier et du code d'accès aux données.

Les routes qui nécessitent une autorisation incluent l'attribut <span style="color:red"> **[Authorize]** </span> et spécifient éventuellement un rôle (par exemple <span style="color:red"> **[Authorize(Role.Admin)]** </span>, si un rôle est spécifié, la route est limitée aux utilisateurs de ce rôle, sinon la route est limitée à tous les utilisateurs authentifiés utilisateurs quel que soit leur rôle.   
La logique d'authentification se trouve dans <span style="color:green"> **custom authorize attribute** </span>.

Les méthodes de routage <span style="color:red"> **RevokeToken** </span>, <span style="color:red"> **GetById** </span>, <span style="color:red"> **Update** </span> et <span style="color:red"> **Delete** </span> incluent une vérification d'autorisation personnalisée supplémentaire pour empêcher les utilisateurs non administrateurs d'accéder à des comptes autres que le leur.   
Ainsi, les comptes d'utilisateurs réguliers **(Role.User)** ont un accès CRUD à leur propre compte mais pas aux autres, et les comptes administrateur **(Role.Admin)** ont un accès CRUD complet à tous les comptes.

La méthode <span style="color:red"> **setTokenCookie()** </span> ajoute un cookie HTTP contenant uniquement le jeton d'actualisation à la réponse pour une sécurité accrue.   
Les cookies uniquement HTTP ne sont pas accessibles au javascript côté client, ce qui empêche XSS (cross site scripting), et le jeton d'actualisation ne peut être utilisé que pour récupérer un nouveau jeton à partir de la route <span style="color:red"> **/accounts/refresh-token** </span> qui empêche CSRF (cross site request forgery).