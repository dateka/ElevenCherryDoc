# Custom App Exception

### Path: /Helpers/AppException.cs

L'exception d'application est une classe d'exception personnalisée utilisée pour différencier les exceptions gérées et non gérées.   
Les exceptions gérées sont celles générées par l'application et utilisées pour afficher des messages d'erreur conviviaux au client, par exemple la logique métier ou les exceptions de validation causées par une entrée incorrecte de l'utilisateur.   
Les exceptions non gérées sont générées par le framework .NET et peuvent être causées par des bogues dans le code de l'application.

Consultez le **[account service](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Services/AccountService.md)** pour des exemples d'exceptions d'application qui sont levées. Découvrez où les différents types d'exceptions sont gérés dans le **[error handler middleware](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Middleware/ErrorHandlerMiddleware.md)**.