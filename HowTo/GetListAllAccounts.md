# Get List of All Accounts

Il s'agit d'une demande sécurisée qui nécessite un jeton d'authentification JWT à partir de l'étape d'authentification. La route api est limitée aux utilisateurs administrateurs.

1. Ouvrez un nouvel onglet de demande en cliquant sur le bouton plus (+) à la fin des onglets.
2. Remplacez la méthode de requête http par « GET » avec le sélecteur déroulant à gauche du champ de saisie de l'URL.
3. Dans le champ URL, entrez l'adresse de la route d'enregistrement de votre API - **http://localhost:4000/accounts**
4. Sélectionnez l'onglet "Authorization" sous le champ URL, changez le bouton radio du type de corps en "Bearer Token" et coller le JWT token dans le champs "Token".
5. Cliquez sur le bouton "Send", vous devriez recevoir une réponse "200 OK" avec un tableau contenant la liste de tous les comptes enregistrés.