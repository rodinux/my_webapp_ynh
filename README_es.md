<!--
Este archivo README esta generado automaticamente<https://github.com/YunoHost/apps/tree/master/tools/readme_generator>
No se debe editar a mano.
-->

# My Webapp para Yunohost

[![Nivel de integración](https://apps.yunohost.org/badge/integration/my_webapp)](https://ci-apps.yunohost.org/ci/apps/my_webapp/)
![Estado funcional](https://apps.yunohost.org/badge/state/my_webapp)
![Estado En Mantención](https://apps.yunohost.org/badge/maintained/my_webapp)

[![Instalar My Webapp con Yunhost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=my_webapp)

*[Leer este README en otros idiomas.](./ALL_README.md)*

> *Este paquete le permite instalarMy Webapp rapidamente y simplement en un servidor YunoHost.*  
> *Si no tiene YunoHost, visita [the guide](https://yunohost.org/install) para aprender como instalarla.*

## Descripción general

This application allows you to easily install an "empty" web application, in which you deploy your own custom website in the form of "static" HTML/CSS/JS assets or PHP.

Files can be uploaded [via SFTP](https://yunohost.org/en/filezilla) or any other method of your chosing.

During installation, you can also chose to initialize a MySQL or PostgreSQL database, which will be backed up and restored just like the other files in your application. The connection details will be stored in the file `db_access.txt` located in the root directory of the app.

PHP-FPM version can also be selected among (none), `7.4`, `8.0`, `8.1`, `8.2`, `8.3` and `8.4`.

**Once installed, go to the chosen URL to know the user, domain and port you will have to use for the SFTP access.** The password is the one specified during the installation. Under the app directory, you will see a `www` folder which contains the public files served by this app. You can put all the files of your custom web application inside.

You can also customize 404 errors - if you enable the option in the config panel. Simply create an `error` folder in the `www` root directory, containing your custom `html` files. 


**Versión actual:** 1.0~ynh20
## Documentaciones y recursos

- Catálogo YunoHost: <https://apps.yunohost.org/app/my_webapp>
- Reportar un error: <https://github.com/YunoHost-Apps/my_webapp_ynh/issues>

## Información para desarrolladores

**WARNING: This fork is experimental and only used for wordpress installed with my_webapp with a plugin wordfence.**

This fork is to work with wordpess, add a my_wordpress.conf uncommenting the parameters commented in the file "etc/nginx/conf.d/$domain.d/$app.d/sample.conf".

```
cp -a "etc/nginx/conf.d/$domain.d/$app.d/sample.conf" "etc/nginx/conf.d/$domain.d/$app.d/my_wordpress.conf"
```

Please send your pull request to the [wordpress_spec_wordfence branch](https://github.com/rodinux/my_webapp_ynh/tree/worpress_spec_wordfence).

You may consider for example the line added in the `php-fpm.conf` file to take into account a Wordfence extension and few values for php-fpm.

Please do pull request on the [wordpress_spec_worfence branch](https://github.com/rodinux/my_webapp_ynh/tree/wordpress_spec).

To try the wordpress_spec_wordfence branch, please proceed like that.

``` bash
sudo yunohost app install https://github.com/rodinux/my_webapp_ynh/tree/worpress_spec_wordfence --debug
or
sudo yunohost app upgrade my_webapp -u https://github.com/rodinux/my_webapp_ynh/tree/wordpress_spec_wordfence --debug
```

**Mas informaciones sobre el empaquetado de aplicaciones:** <https://yunohost.org/packaging_apps>
