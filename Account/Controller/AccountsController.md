# Accounts Controller

### Path: /Controllers/AccountsController.cs

AccountsController définit et gère toutes les routes / endpoints pour l'API qui se rapportent aux comptes, y compris l'inscription, la vérification, l'authentification, le mot de passe oublié, l'actualisation et la révocation des jetons et les opérations de gestion de compte (CRUD).   
Dans chaque méthode de routage, le contrôleur appelle le service de compte pour effectuer l'action requise, ce qui permet au contrôleur de rester « allégé » et complètement séparé de la logique métier et du code d'accès aux données.

Les routes qui nécessitent une autorisation incluent l'attribut **[Authorize]** et spécifient éventuellement un rôle (par exemple **[Authorize(Role.Admin)]**, si un rôle est spécifié, la route est limitée aux utilisateurs de ce rôle, sinon la route est limitée à tous les utilisateurs authentifiés utilisateurs quel que soit leur rôle.   
La logique d'authentification se trouve dans **[custom authorize attribute](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Helpers/CustomAuthorizeAttribute.md)**.

Les méthodes de routage **RevokeToken**, **GetById**, **Update** et **Delete** incluent une vérification d'autorisation personnalisée supplémentaire pour empêcher les utilisateurs non administrateurs d'accéder à des comptes autres que le leur.   
Ainsi, les comptes d'utilisateurs réguliers **(Role.User)** ont un accès CRUD à leur propre compte mais pas aux autres, et les comptes administrateur **(Role.Admin)** ont un accès CRUD complet à tous les comptes.

La méthode **setTokenCookie()** ajoute un cookie HTTP contenant uniquement le jeton d'actualisation à la réponse pour une sécurité accrue.   
Les cookies uniquement HTTP ne sont pas accessibles au javascript côté client, ce qui empêche XSS (cross site scripting), et le jeton d'actualisation ne peut être utilisé que pour récupérer un nouveau jeton à partir de la route **/accounts/refresh-token** qui empêche CSRF (cross site request forgery).