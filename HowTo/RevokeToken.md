# Revoke token

Il s'agit d'une demande sécurisée qui nécessite un jeton d'authentification JWT à partir de l'étape d'authentification (ou d'actualisation du jeton). Les utilisateurs administrateurs peuvent révoquer les jetons de n'importe quel compte, tandis que les utilisateurs réguliers ne peuvent révoquer que leurs propres jetons.

1. Ouvrez un nouvel onglet de demande en cliquant sur le bouton plus (+) à la fin des onglets.
2. Remplacez la méthode de requête http par « POST » avec le sélecteur déroulant à gauche du champ de saisie de l'URL.
3. Dans le champ URL, entrez l'adresse de la route pour rafraichir le token - http://localhost:4000/accounts/revoke-token
4. Sélectionnez l'onglet "Authorization" sous le champ URL, remplacez le type par "Bearer Token" dans le sélecteur de type déroulant et collez le jeton JWT de l'étape d'authentification (ou d'actualisation) précédente dans le champ "Token".
5. Sélectionnez l'onglet "Body" sous le champ URL, changez le bouton radio du type de corps en "raw" et changez le sélecteur de format en "JSON".
6. Saisissez un objet JSON contenant le jeton d'actualisation actif de l'étape précédente dans la zone de texte « Body », par exemple :
````
{
    "token": "METTRE LE NOUVEAU TOKEN RAFRAICHI"
}
````
7. Cliquez sur le bouton "Envoyer", vous devriez recevoir une réponse "200 OK" avec le message "Token revoked".

Remarque : vous pouvez également révoquer le jeton dans le cookie refreshToken avec la route **/accounts/revoke-token**, pour révoquer le cookie de jeton d'actualisation, envoyez simplement la même demande avec un corps vide.