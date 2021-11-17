# Update an Account

Il s'agit d'une demande sécurisée qui nécessite un jeton d'authentification JWT à l'étape d'authentification. Les utilisateurs administrateurs peuvent mettre à jour n'importe quel compte, y compris son rôle, tandis que les utilisateurs réguliers sont limités à leur propre compte et ne peuvent pas mettre à jour leur rôle. Les propriétés oubliés ou vides ne sont pas mises à jour.

1. Ouvrez un nouvel onglet de demande en cliquant sur le bouton plus (+) à la fin des onglets.
2. Remplacez la méthode de requête http par « PUT » avec le sélecteur déroulant à gauche du champ de saisie de l'URL.
3. Dans le champ URL, entrez l'adresse de la route **/accounts/{id}** avec l'ID du compte que vous souhaitez mettre à jour, par exemple - http://localhost:4000/accounts/1
4. Sélectionnez l'onglet "Authorization" sous le champ URL, changez le bouton radio du type de corps en "Bearer Token" et coller le JWT token dans le champs "Token".
5. Sélectionnez l'onglet "Body" sous le champ URL, changez le bouton radio du type de corps en "raw" et changez le sélecteur de format en "JSON".
6. Saisissez un objet JSON dans la zone de texte « Body » contenant les propriétés que vous souhaitez mettre à jour, par exemple pour mettre à jour le prénom et le nom :
````
{
    "firstName": "Luffy",
    "lastName": "Monkey .D"
}
````

5. Cliquez sur le bouton "Send", vous devriez recevoir une réponse "200 OK" avec le détail des updates réalisés.