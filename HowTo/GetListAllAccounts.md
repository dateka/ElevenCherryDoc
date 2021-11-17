# Get List of All Accounts

Il s'agit d'une demande s�curis�e qui n�cessite un jeton d'authentification JWT � partir de l'�tape d'authentification. La route api est limit�e aux utilisateurs administrateurs.

1. Ouvrez un nouvel onglet de demande en cliquant sur le bouton plus (+) � la fin des onglets.
2. Remplacez la m�thode de requ�te http par ��GET�� avec le s�lecteur d�roulant � gauche du champ de saisie de l'URL.
3. Dans le champ URL, entrez l'adresse de la route d'enregistrement de votre API - **http://localhost:4000/accounts**
4. S�lectionnez l'onglet "Authorization" sous le champ URL, changez le bouton radio du type de corps en "Bearer Token" et coller le JWT token dans le champs "Token".
5. Cliquez sur le bouton "Send", vous devriez recevoir une r�ponse "200 OK" avec un tableau contenant la liste de tous les comptes enregistr�s.