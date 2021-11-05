# Auto Mapper Profile

### Path: /Helpers/AutoMapperProfile.cs

Le profil de mappeur automatique contient la configuration de mappage utilis�e par l'application, AutoMapper est un package disponible sur Nuget qui permet le mappage automatique des valeurs de propri�t� entre diff�rents types de classe en fonction des noms de propri�t�.   
Dans l'exemple, nous l'utilisons pour mapper entre les entit�s de compte et quelques types de mod�les de demande et de r�ponse diff�rents.

Le mappage de **UpdateRequest** vers le **Account** inclut une configuration personnalis�e pour ignorer les propri�t�s vides sur le mod�le de demande lors du mappage vers une entit� de compte, il s'agit de rendre les champs facultatifs lors de la mise � jour d'un compte.