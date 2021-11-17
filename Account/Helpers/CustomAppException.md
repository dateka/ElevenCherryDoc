# Custom App Exception

### Path: /Helpers/AppException.cs

L'exception d'application est une classe d'exception personnalis�e utilis�e pour diff�rencier les exceptions g�r�es et non g�r�es.   
Les exceptions g�r�es sont celles g�n�r�es par l'application et utilis�es pour afficher des messages d'erreur conviviaux au client, par exemple la logique m�tier ou les exceptions de validation caus�es par une entr�e incorrecte de l'utilisateur.   
Les exceptions non g�r�es sont g�n�r�es par le framework .NET et peuvent �tre caus�es par des bogues dans le code de l'application.

Consultez le **[account service](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Services/AccountService.md)** pour des exemples d'exceptions d'application qui sont lev�es. D�couvrez o� les diff�rents types d'exceptions sont g�r�s dans le **[error handler middleware](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Middleware/ErrorHandlerMiddleware.md)**.