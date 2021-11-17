# Base Controller

### Path: /Controllers/BaseController.cs

Le contr�leur de base est h�rit� par tous les autres contr�leurs de l'API standard et comprend des propri�t�s et des m�thodes communes accessibles � tous les contr�leurs.

La propri�t� **Account** renvoie le compte authentifi� actuel pour la demande de la collection **HttpContext.Items** ou renvoie **null** si la demande n'est pas authentifi�e.   
Le compte actuel est ajout� � la collection **HttpContext.Items** par le **[custom jwt middleware](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Middleware/CustomJWTMiddleware.md)** lorsque la demande contient un jeton JWT valide dans l'en-t�te d'autorisation.