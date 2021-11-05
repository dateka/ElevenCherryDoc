# Account Entity

### Path: /Entities/Account.cs

La propriété **IsVerified** renvoie true si la date de **vérification** ou la date de **réinitialisation du mot de passe** a une valeur, cela permet d'activer la vérification du compte après l'enregistrement via les étapes mot de passe oublié + réinitialisation du mot de passe.

La méthode **OwnsToken** est une méthode pratique qui renvoie true si le jeton d'actualisation spécifié appartient au compte.