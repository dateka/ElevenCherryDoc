# Refresh token

Cette �tape ne peut �tre effectu�e qu'apr�s l'�tape d'authentification, car un cookie de jeton d'actualisation valide est requis.

1. Ouvrez un nouvel onglet de demande en cliquant sur le bouton plus (+) � la fin des onglets.
2. Remplacez la m�thode de requ�te http par ��POST�� avec le s�lecteur d�roulant � gauche du champ de saisie de l'URL.
3. Dans le champ URL, entrez l'adresse de la route pour rafraichir le token - http://localhost:4000/accounts/refresh-token
4. Cliquez sur le bouton "Send", vous devriez recevoir une r�ponse "200 OK" avec les d�tails du compte, y compris un nouveau jeton JWT dans le corps de la r�ponse et un nouveau jeton d'actualisation dans les cookies de r�ponse.