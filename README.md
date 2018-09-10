# Docker compose with old wordpress website

Assumed old environments...

- WordPress 3.1.x
- PHP 5.3.x
- MySQL 5.1.x (Add 5.1.x dump into 5.5 database)

```bash
$ docker-compose up (-d)
```

- Access phpMyAdmin (Port 8080) and import your wordpress db dump.
- Move your wp files into `www` directory. Do not forget dot files like `.htaccess`
- Access port 3000 and fun...
- !!! Do not use for production !!!
