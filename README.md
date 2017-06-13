Simple nginx setup with full vhosts flexibility
===============================================

The role does install main nginx conf file, but the vhost configs shall be provided by the user in the form
of a template. The current vhost config is passed into the template as `item` var.

```
nginx_vhosts:
  - name: name_of_host
    config_template: "shared/nginx/vhost.conf"
```

## Special feature

The role makes sure that there are no other vhosts than configured. This means that when you remove or rename
a vhost you don't have to clean it up manually on the server.

## Other vars 

Look into `defaults/main.yml`.



