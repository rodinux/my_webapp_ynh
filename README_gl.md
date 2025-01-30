<!--
NOTA: Este README foi creado automáticamente por <https://github.com/YunoHost/apps/tree/master/tools/readme_generator>
NON debe editarse manualmente.
-->

# My Webapp para YunoHost

[![Nivel de integración](https://dash.yunohost.org/integration/my_webapp.svg)](https://dash.yunohost.org/appci/app/my_webapp) ![Estado de funcionamento](https://ci-apps.yunohost.org/ci/badges/my_webapp.status.svg) ![Estado de mantemento](https://ci-apps.yunohost.org/ci/badges/my_webapp.maintain.svg)

[![Instalar My Webapp con YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=my_webapp)

*[Le este README en outros idiomas.](./ALL_README.md)*

> *Este paquete permíteche instalar My Webapp de xeito rápido e doado nun servidor YunoHost.*  
> *Se non usas YunoHost, le a [documentación](https://yunohost.org/install) para saber como instalalo.*

## Vista xeral

This application allows you to easily install a custom Web application, providing files access with [SFTP](https://yunohost.org/en/filezilla).

It can also create a MySQL database - which will be backed up and restored with your application. The connection details will be stored in the file `db_access.txt` located in the root directory.

PHP-FPM version can also be selected among `none`, `7.4`, `8.0`, `8.1` and `8.2`.

**Once installed, go to the chosen URL to know the user, domain and port you will have to use for the SFTP access.** The password is one you chosen during the installation. Under the Web directory, you will see a `www` folder which contains the public files served by this app. You can put all the files of your custom Web application inside.


**Versión proporcionada:** 1.0~ynh15
## Documentación e recursos

- Repositorio de orixe do código: <https://github.com/YunoHost-Apps/my_webapp_ynh>
- Tenda YunoHost: <https://apps.yunohost.org/app/my_webapp>
- Informar dun problema: <https://github.com/YunoHost-Apps/my_webapp_ynh/issues>

## Info de desenvolvemento

**WARNING: This fork is experimental and only used for wordpress installed with my_webapp.** 

To work with wordpess add a file with a nginx conf with the paramters commented in the file "etc/nginx/conf.d/$domain.d/$app.d/sample.conf"

Please send your pull request to the [wordpress_spec branch](https://github.com/rodinux/my_webapp_ynh/tree/worpress_spec).

You may consider for example the line added in the `php-fpm.conf` file to take into account a Wordfence extension and few values for php-fpm.

Please do pull request on the [wordpress_spec branch](https://github.com/rodinux/my_webapp_ynh/tree/wordpress_spec).

To try the wordpress_spec branch, please proceed like that.


``` bash
sudo yunohost app install https://github.com/rodinux/my_webapp_ynh/tree/wordpress_spec --debug
or
sudo yunohost app upgrade my_webapp -u https://github.com/rodinux/my_webapp_ynh/tree/wordpress_spec --debug
```

**Máis info sobre o empaquetado da app:** <https://yunohost.org/packaging_apps>
