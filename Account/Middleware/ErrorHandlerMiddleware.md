# Global Error Handler Middleware

### Path: /Middleware/ErrorHandlerMiddleware.cs

Le gestionnaire d'erreurs global est utilis� pour capturer toutes les erreurs et supprimer le besoin d'un code de gestion des erreurs dupliqu� dans l'application standard. Il est configur� en tant que middleware dans la m�thode **Configure** de la classe **Startup.cs**.

Les erreurs de type **AppException** sont trait�es comme des erreurs personnalis�es (sp�cifiques � l'application) qui renvoient une r�ponse **400 Bad Request**, la classe **KeyNotFoundException** int�gr�e .NET est utilis�e pour renvoyer des r�ponses **404 Not Found**, toutes les autres exceptions ne sont pas g�r�es et renvoient une **500 Internal Server Error** r�ponse ainsi que d'�tre connect� � la console.

Consultez le **account service** pour des exemples d'erreurs personnalis�es et d'erreurs introuvables g�n�r�es par l'API.