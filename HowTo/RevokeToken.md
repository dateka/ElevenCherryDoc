# Revoke token

Il s'agit d'une demande s�curis�e qui n�cessite un jeton d'authentification JWT � partir de l'�tape d'authentification (ou d'actualisation du jeton). Les utilisateurs administrateurs peuvent r�voquer les jetons de n'importe quel compte, tandis que les utilisateurs r�guliers ne peuvent r�voquer que leurs propres jetons.

1. Ouvrez un nouvel onglet de demande en cliquant sur le bouton plus (+) � la fin des onglets.
2. Remplacez la m�thode de requ�te http par ��POST�� avec le s�lecteur d�roulant � gauche du champ de saisie de l'URL.
3. Dans le champ URL, entrez l'adresse de la route pour rafraichir le token - http://localhost:4000/accounts/revoke-token
4. S�lectionnez l'onglet "Authorization" sous le champ URL, remplacez le type par "Bearer Token" dans le s�lecteur de type d�roulant et collez le jeton JWT de l'�tape d'authentification (ou d'actualisation) pr�c�dente dans le champ "Token".
5. S�lectionnez l'onglet "Body" sous le champ URL, changez le bouton radio du type de corps en "raw" et changez le s�lecteur de format en "JSON".
6. Saisissez un objet JSON contenant le jeton d'actualisation actif de l'�tape pr�c�dente dans la zone de texte ��Body��, par exemple�:
````
{
    "token": "METTRE LE NOUVEAU TOKEN RAFRAICHI"
}
````
7. Cliquez sur le bouton "Envoyer", vous devriez recevoir une r�ponse "200 OK" avec le message "Token revoked".

Remarque : vous pouvez �galement r�voquer le jeton dans le cookie refreshToken avec la route **/accounts/revoke-token**, pour r�voquer le cookie de jeton d'actualisation, envoyez simplement la m�me demande avec un corps vide.