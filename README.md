# Send basic mail in ruby with pony

## How to install

```SHELL
git clone https://github.com/vgauther/send-basic-mail-in-ruby-with-pony
gem install pony
```

You must install the gem yaml but it's always installed before with the installation of Ruby or Ruby On Rails.

## How to use

First you need to change the settings in config.yml

```YML
via: smtp
fromname: name <-- the name display as the sender
authenticate: true
account:
    hostname: smtp.example.com <-- smtp server link
    port: 587 <-- port used for tls connection
    username: example@example.com <-- id for your connection to the smtp server
    password: password <-- password for your connection to the smtp server
    tls: true

```

Then change the content in message.txt. This will be the message in your mail.

The next step is to prepare the list of peoples's email witch you want to send your mail.

You'll find this code at line 85 in mail_sender.rb.

```Ruby
# Contacts
  contacts = ['john@example.com', 'doe@example.com'] # <-- Array with target
# Send emails
  MailSender.new('config.yml',
                 contacts, # <-- Array with target
                 'Change for your object', # <-- Array with target
                 'message.txt', # <-- File for your message
                 'attachment.pdf').handle # <-- File for your attachement you can delete it if you dont want to use
```

Then launch the script.

```SHELL
ruby mail_sender.rb
```
