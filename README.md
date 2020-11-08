# Send basic mail in ruby with pony

## How to install

```
git clone https://github.com/vgauther/send-basic-mail-in-ruby-with-pony
gem install pony
```
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
