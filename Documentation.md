# Introduction #

_MailMeToo_ was developed in 2011, when the _MailMe_ notification style in _Growl_ sent notifications as emails in a rather unsatisfactory way. Since then, _The Growl Project_'s developers decided to replace the original _MailMe_ style with our version, so by using _Growl 2.0_ or newer you're already using this plugin.

Consequently, I decided to only distribute the plugin's version for _Growl 1.2.2_, which is the latest to support Mac OS X 10.6. All other system versions are covered by _Growl 2.0_ and later versions.


---


Like the _MailMe_ plugin, _MailMeToo_ delivers notifications by sending an email for every notification it is set to process.

The _MailMeToo_ plugin was created to give the user more control on how the emails are sent: in _MailMe_ the user can only configure the destination email address, then _Mail.app_ is used to route the email to its destination. In _MailMeToo_ users are allowed to provide an SMTP account's information like in any email client. Emails are sent through the specified server using the specified account information.

![http://growl-mail-smtp.googlecode.com/svn/wiki/prefs.png](http://growl-mail-smtp.googlecode.com/svn/wiki/prefs.png)

If you are not familiar with SMTP configuration, and if you don't have any particular reason not to use the _MailMe_ plugin, then better use _MailMe_ as a simpler solution. I built this plugin because I couldn't get _MailMe_ to work with _Mail.app_ at work, and because I needed a clean Cocoa class to send emails through SMTP for another project.

# Features #

_MailMeToo_ supports the following:
  * Basic and TLS (SSL) connections, including the STARTTLS command, which allows basic connections to switch to TLS.
  * Anonymous and authenticated connections, with AUTH modes PLAIN, LOGIN and CRAM-MD5.
  * Import SMTP accounts already configured in Mail.app
  * Passwords are safely stored in the OSX Keychain

# Compatibility #

_MailMeToo_ has been successfully tested with Growl version 1.2.2. It is only supposed to be used with Mac OS X 10.6 _Snow Leopard_ as Growl 2.0 includes _MailMeToo_ (as _MailMe_) and doesn't need the plugin, covering Mac OS X 10.7 and later.

# Testing #

After filling the required fields, hit the _Preview_ button on bottom of the preferences pane. An email should be sent to the specified recipient. If something goes wrong, something should be logged. You can access the logs through _Console.app_, in your _Utilities_ folder.