# Base Controller

### Path: /Controllers/BaseController.cs

Le contrôleur de base est hérité par tous les autres contrôleurs de l'API standard et comprend des propriétés et des méthodes communes accessibles à tous les contrôleurs.

La propriété **Account** renvoie le compte authentifié actuel pour la demande de la collection **HttpContext.Items** ou renvoie **null** si la demande n'est pas authentifiée.   
Le compte actuel est ajouté à la collection **HttpContext.Items** par le **[custom jwt middleware](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Middleware/CustomJWTMiddleware.md)** lorsque la demande contient un jeton JWT valide dans l'en-tête d'autorisation.