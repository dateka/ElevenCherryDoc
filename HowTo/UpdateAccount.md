# Update an Account

Il s'agit d'une demande s�curis�e qui n�cessite un jeton d'authentification JWT � l'�tape d'authentification. Les utilisateurs administrateurs peuvent mettre � jour n'importe quel compte, y compris son r�le, tandis que les utilisateurs r�guliers sont limit�s � leur propre compte et ne peuvent pas mettre � jour leur r�le. Les propri�t�s oubli�s ou vides ne sont pas mises � jour.

1. Ouvrez un nouvel onglet de demande en cliquant sur le bouton plus (+) � la fin des onglets.
2. Remplacez la m�thode de requ�te http par ��PUT�� avec le s�lecteur d�roulant � gauche du champ de saisie de l'URL.
3. Dans le champ URL, entrez l'adresse de la route **/accounts/{id}** avec l'ID du compte que vous souhaitez mettre � jour, par exemple - http://localhost:4000/accounts/1
4. S�lectionnez l'onglet "Authorization" sous le champ URL, changez le bouton radio du type de corps en "Bearer Token" et coller le JWT token dans le champs "Token".
5. S�lectionnez l'onglet "Body" sous le champ URL, changez le bouton radio du type de corps en "raw" et changez le s�lecteur de format en "JSON".
6. Saisissez un objet JSON dans la zone de texte ��Body�� contenant les propri�t�s que vous souhaitez mettre � jour, par exemple pour mettre � jour le pr�nom et le nom�:
````
{
    "firstName": "Luffy",
    "lastName": "Monkey .D"
}
````

5. Cliquez sur le bouton "Send", vous devriez recevoir une r�ponse "200 OK" avec le d�tail des updates r�alis�s.