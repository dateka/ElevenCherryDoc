# verify an account

1. Ouvrez un nouvel onglet de demande en cliquant sur le bouton plus (+) � la fin des onglets.
2. Remplacez la m�thode de requ�te http par ��POST�� avec le s�lecteur d�roulant � gauche du champ de saisie de l'URL.
3. Dans le champ URL, entrez l'adresse de la route d'enregistrement de votre API - **http://localhost:4000/accounts/verify-email**
4. S�lectionnez l'onglet "Body" sous le champ URL, changez le bouton radio du type de corps en "raw" et changez le s�lecteur de format en "JSON".
5. Saisissez un objet JSON contenant les propri�t�s utilisateur requises dans la zone de texte ��Body��, par exemple�:

```
{
    "token": "REMPLACER AVEC VOTRE TOKEN"
}
```
6. Cliquez sur le bouton "Send", vous devriez recevoir une r�ponse "200 OK" avec un message "verification  successful" dans le Body de la r�ponse.