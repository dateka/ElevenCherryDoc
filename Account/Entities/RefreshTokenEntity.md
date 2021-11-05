# Refresh Token Entity

### Path: /Entities/RefreshToken.cs

La classe d'entit� de jeton d'actualisation repr�sente les donn�es d'un jeton d'actualisation dans l'application.

L'attribut **[Owned]** marque la classe de jeton d'actualisation en tant que type d'entit� d�tenue, ce qui signifie qu'elle ne peut exister qu'en tant qu'enfant/d�pendant d'une autre classe d'entit�.   
Dans cet exemple, un jeton d'actualisation appartient toujours � **account entity**.

L'attribut **[Key]** d�finit explicitement le champ id comme cl� primaire dans la table de base de donn�es. Les propri�t�s portant le nom **Id** sont automatiquement transform�es en cl�s primaires par EF Core.   
Cependant, dans le cas des entit�s **Owned**, EF Core cr�e une cl� primaire composite compos�e de l'identifiant et de l'identifiant du propri�taire, ce qui peut provoquer des erreurs avec les champs d'identifiant g�n�r�s automatiquement.   
Le marquage explicite de l'identifiant avec l'attribut **[Key]** indique � EF Core de faire uniquement du champ id la cl� primaire dans la table db.