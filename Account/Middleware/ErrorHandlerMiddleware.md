# Global Error Handler Middleware

### Path: /Middleware/ErrorHandlerMiddleware.cs

Le gestionnaire d'erreurs global est utilisé pour capturer toutes les erreurs et supprimer le besoin d'un code de gestion des erreurs dupliqué dans l'application standard. Il est configuré en tant que middleware dans la méthode **Configure** de la classe **Startup.cs**.

Les erreurs de type **AppException** sont traitées comme des erreurs personnalisées (spécifiques à l'application) qui renvoient une réponse **400 Bad Request**, la classe **KeyNotFoundException** intégrée .NET est utilisée pour renvoyer des réponses **404 Not Found**, toutes les autres exceptions ne sont pas gérées et renvoient une **500 Internal Server Error** réponse ainsi que d'être connecté à la console.

Consultez le **account service** pour des exemples d'erreurs personnalisées et d'erreurs introuvables générées par l'API.