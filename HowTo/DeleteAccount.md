# Delete account

Il s'agit d'une demande s�curis�e qui n�cessite un jeton d'authentification JWT � partir de l'�tape d'authentification. Les utilisateurs administrateurs peuvent supprimer n'importe quel compte, tandis que les utilisateurs normaux sont limit�s � leur propre compte.

1. Ouvrez un nouvel onglet de demande en cliquant sur le bouton plus (+) � la fin des onglets.
2. Remplacez la m�thode de requ�te http par ��DELETE�� avec le s�lecteur d�roulant � gauche du champ de saisie de l'URL.
3.Dans le champ URL, entrez l'adresse de la route /accounts/{id} avec l'ID du compte que vous souhaitez supprimer, par exemple - http://localhost:4000/accounts/1
4. S�lectionnez l'onglet "Authorization" sous le champ URL, remplacez le type par "Bearer Token" dans le s�lecteur de type d�roulant et collez le jeton JWT de l'�tape d'authentification (ou d'actualisation) pr�c�dente dans le champ "Token".
5. Cliquez sur le bouton "Send", vous devriez recevoir une r�ponse "200 OK" avec le message "Account deleted successfully".