# Account Entity

### Path: /Entities/Account.cs

La propri�t� **IsVerified** renvoie true si la date de **v�rification** ou la date de **r�initialisation du mot de passe** a une valeur, cela permet d'activer la v�rification du compte apr�s l'enregistrement via les �tapes mot de passe oubli� + r�initialisation du mot de passe.

La m�thode **OwnsToken** est une m�thode pratique qui renvoie true si le jeton d'actualisation sp�cifi� appartient au compte.