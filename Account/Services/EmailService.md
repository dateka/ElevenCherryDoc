# Email Service

### Path: /Services/EmailService.cs

Le service de messagerie est un wrapper léger autour de la bibliothèque du client de messagerie .NET **MailKit** pour simplifier l'envoi d'e-mails depuis n'importe où dans l'API. Il est utilisé par le **[account service](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Services/AccountService.md)** pour envoyer des e-mails de vérification de compte et de réinitialisation de mot de passe.

Pour plus d'informations sur MailKit, consultez **https://github.com/jstedfast/MailKit**.