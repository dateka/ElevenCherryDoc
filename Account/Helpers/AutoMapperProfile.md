# Auto Mapper Profile

### Path: /Helpers/AutoMapperProfile.cs

Le profil de mappeur automatique contient la configuration de mappage utilisée par l'application, AutoMapper est un package disponible sur Nuget qui permet le mappage automatique des valeurs de propriété entre différents types de classe en fonction des noms de propriété.   
Dans l'exemple, nous l'utilisons pour mapper entre les entités de compte et quelques types de modèles de demande et de réponse différents.

Le mappage de **UpdateRequest** vers le **Account** inclut une configuration personnalisée pour ignorer les propriétés vides sur le modèle de demande lors du mappage vers une entité de compte, il s'agit de rendre les champs facultatifs lors de la mise à jour d'un compte.