# Accounts Controller

### Path: /Controllers/AccountsController.cs

AccountsController d�finit et g�re toutes les routes / endpoints pour l'API qui se rapportent aux comptes, y compris l'inscription, la v�rification, l'authentification, le mot de passe oubli�, l'actualisation et la r�vocation des jetons et les op�rations de gestion de compte (CRUD).   
Dans chaque m�thode de routage, le contr�leur appelle le service de compte pour effectuer l'action requise, ce qui permet au contr�leur de rester � all�g� � et compl�tement s�par� de la logique m�tier et du code d'acc�s aux donn�es.

Les routes qui n�cessitent une autorisation incluent l'attribut <span style="color:red"> **[Authorize]** </span> et sp�cifient �ventuellement un r�le (par exemple <span style="color:red"> **[Authorize(Role.Admin)]** </span>, si un r�le est sp�cifi�, la route est limit�e aux utilisateurs de ce r�le, sinon la route est limit�e � tous les utilisateurs authentifi�s utilisateurs quel que soit leur r�le.   
La logique d'authentification se trouve dans <span style="color:green"> **custom authorize attribute** </span>.

Les m�thodes de routage <span style="color:red"> **RevokeToken** </span>, <span style="color:red"> **GetById** </span>, <span style="color:red"> **Update** </span> et <span style="color:red"> **Delete** </span> incluent une v�rification d'autorisation personnalis�e suppl�mentaire pour emp�cher les utilisateurs non administrateurs d'acc�der � des comptes autres que le leur.   
Ainsi, les comptes d'utilisateurs r�guliers **(Role.User)** ont un acc�s CRUD � leur propre compte mais pas aux autres, et les comptes administrateur **(Role.Admin)** ont un acc�s CRUD complet � tous les comptes.

La m�thode <span style="color:red"> **setTokenCookie()** </span> ajoute un cookie HTTP contenant uniquement le jeton d'actualisation � la r�ponse pour une s�curit� accrue.   
Les cookies uniquement HTTP ne sont pas accessibles au javascript c�t� client, ce qui emp�che XSS (cross site scripting), et le jeton d'actualisation ne peut �tre utilis� que pour r�cup�rer un nouveau jeton � partir de la route <span style="color:red"> **/accounts/refresh-token** </span> qui emp�che CSRF (cross site request forgery).