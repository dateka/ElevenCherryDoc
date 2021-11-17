# forgot password

Pour réactiver l'accès à un compte avec un mot de passe oublié, vous devez soumettre l'adresse e-mail du compte à la route **/accounts/forgot-password**, la route enverra alors un jeton à l'e-mail qui vous permettra de réinitialiser le mot de passe du compte.

1. Ouvrez un nouvel onglet de demande en cliquant sur le bouton plus (+) à la fin des onglets.
2. Remplacez la méthode de requête http par « POST » avec le sélecteur déroulant à gauche du champ de saisie de l'URL.
3. Dans le champ URL, entrez l'adresse de la route d'enregistrement de votre API - **http://localhost:4000/accounts/forgot-password**
4. Sélectionnez l'onglet "Body" sous le champ URL, changez le bouton radio du type de corps en "raw" et changez le sélecteur de format en "JSON".
5. Saisissez un objet JSON contenant les propriétés utilisateur requises dans la zone de texte « Body », par exemple :

```
{
    "email": "damien@example.com"
}
```
6. Cliquez sur le bouton "Send", vous devriez recevoir une réponse "200 OK" avec un message "Please check your email for password reset instructions" dans le Body de la réponse.