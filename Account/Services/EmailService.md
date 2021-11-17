# Email Service

### Path: /Services/EmailService.cs

Le service de messagerie est un wrapper l�ger autour de la biblioth�que du client de messagerie .NET **MailKit** pour simplifier l'envoi d'e-mails depuis n'importe o� dans l'API. Il est utilis� par le **[account service](https://github.com/dateka/ElevenCherryDoc/blob/main/Account/Services/AccountService.md)** pour envoyer des e-mails de v�rification de compte et de r�initialisation de mot de passe.

Pour plus d'informations sur MailKit, consultez **https://github.com/jstedfast/MailKit**.