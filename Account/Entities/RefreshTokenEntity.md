# Refresh Token Entity

### Path: /Entities/RefreshToken.cs

La classe d'entité de jeton d'actualisation représente les données d'un jeton d'actualisation dans l'application.

L'attribut **[Owned]** marque la classe de jeton d'actualisation en tant que type d'entité détenue, ce qui signifie qu'elle ne peut exister qu'en tant qu'enfant/dépendant d'une autre classe d'entité.   
Dans cet exemple, un jeton d'actualisation appartient toujours à **account entity**.

L'attribut **[Key]** définit explicitement le champ id comme clé primaire dans la table de base de données. Les propriétés portant le nom **Id** sont automatiquement transformées en clés primaires par EF Core.   
Cependant, dans le cas des entités **Owned**, EF Core crée une clé primaire composite composée de l'identifiant et de l'identifiant du propriétaire, ce qui peut provoquer des erreurs avec les champs d'identifiant générés automatiquement.   
Le marquage explicite de l'identifiant avec l'attribut **[Key]** indique à EF Core de faire uniquement du champ id la clé primaire dans la table db.