# Refresh token

Cette étape ne peut être effectuée qu'après l'étape d'authentification, car un cookie de jeton d'actualisation valide est requis.

1. Ouvrez un nouvel onglet de demande en cliquant sur le bouton plus (+) à la fin des onglets.
2. Remplacez la méthode de requête http par « POST » avec le sélecteur déroulant à gauche du champ de saisie de l'URL.
3. Dans le champ URL, entrez l'adresse de la route pour rafraichir le token - http://localhost:4000/accounts/refresh-token
4. Cliquez sur le bouton "Send", vous devriez recevoir une réponse "200 OK" avec les détails du compte, y compris un nouveau jeton JWT dans le corps de la réponse et un nouveau jeton d'actualisation dans les cookies de réponse.