# Docker compose with old wordpress website

Assumed old environments...

- WordPress 3.1.x
- PHP 5.3.x
- MySQL 5.1.x (Add 5.1.x dump into 5.5 database)

```bash
$ docker-compose up (-d)
```

- Access phpMyAdmin (Port 8080) and import your wordpress db dump.
- Modify `siteurl` and `home` for docker machine. Below is example.

```sql
UPDATE `wp_options` SET `option_value` = 'http://<localhost or docker machine ip>:3000/<path to siteurl>' WHERE `wp_options`.`option_id` = 1;
UPDATE `wp_options` SET `option_value` = 'http://<localhost or docker machine ip>:3000/<path to home>' WHERE `wp_options`.`option_id` = 37;
```

- Move your wp files into `www` directory. Do not forget dot files like `.htaccess`
- Access port 3000 and fun...
- !!! Do not use for production !!!
