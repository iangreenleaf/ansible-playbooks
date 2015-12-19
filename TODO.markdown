* [ ] Figure out user situation. deploy, www-data, etc.
* [ ] Fix weird rbenv recipe
* [ ] All the TODOs in the code
* [ ] Fix ansible complain when force-link a dir

### Sandstorm vars so far: ###

sudo CHOSEN_INSTALL_MODE=2 PREFER_ROOT=yes USE_DEFAULTS=no ACCEPTED_FULL_SERVER_INSTALL=yes USE_SANDCATS=no USE_EXTERNAL_INTERFACE=yes START_AT_BOOT=yes PORT=6080 MONGO_PORT=6081 make install


$ host 198.199.111.47
# https://www.digitalocean.com/community/questions/how-do-i-set-up-reverse-dns-for-my-ip

### Email ###

```
sendmail -vt < /tmp/testemail.txt

# To: ian@iangreenleaf.com
# Subject: Put a subject here
# From: robot@iangreenleaf.com
#
# Of cause, here's the place to put the body
```


Or maybe edit /etc/mail/sendmail.mc
and run sendmailconfig
