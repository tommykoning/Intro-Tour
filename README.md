## Dev omgeving opzetten

### v-host opzetten
1. Open kladblok als administrator
2. Ga naar open bestand
3. Open bestand C:/Windows/System32/drivers/etc/hosts
4. Voeg deze lijn toe: 127.0.0.1 intro-tour.local

### Apache v-hosts opzetten

1. Open file httpd-v-hosts.conf
    * wamp: {wamp64:install-dir}\bin\apache\apache2.4.27\conf\extra\httpd-v-hosts.conf
    * xamp: {xamp:install-dir}\apache\conf\extra\httpd-v-hosts.conf
2. Voeg deze lijn toe:
 ```
 <VirtualHost *:80>
    DocumentRoot "(project root)/public"
    ServerName "intro-tour.local"
</VirtualHost>
```
3. Start apache opnieuw op
4. Maak .env bestand aan
5. kopieer inhoud van .env.example
6. verander lijn 5 in ``APP_URL=http://intro-tour.local``
7. run command ``php artisan key:generate``