# Delete account

Il s'agit d'une demande sécurisée qui nécessite un jeton d'authentification JWT à partir de l'étape d'authentification. Les utilisateurs administrateurs peuvent supprimer n'importe quel compte, tandis que les utilisateurs normaux sont limités à leur propre compte.

1. Ouvrez un nouvel onglet de demande en cliquant sur le bouton plus (+) à la fin des onglets.
2. Remplacez la méthode de requête http par « DELETE » avec le sélecteur déroulant à gauche du champ de saisie de l'URL.
3.Dans le champ URL, entrez l'adresse de la route /accounts/{id} avec l'ID du compte que vous souhaitez supprimer, par exemple - http://localhost:4000/accounts/1
4. Sélectionnez l'onglet "Authorization" sous le champ URL, remplacez le type par "Bearer Token" dans le sélecteur de type déroulant et collez le jeton JWT de l'étape d'authentification (ou d'actualisation) précédente dans le champ "Token".
5. Cliquez sur le bouton "Send", vous devriez recevoir une réponse "200 OK" avec le message "Account deleted successfully".