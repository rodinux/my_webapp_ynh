<!--
Ohart ongi: README hau automatikoki sortu da <https://github.com/YunoHost/apps/tree/master/tools/readme_generator>ri esker
EZ editatu eskuz.
-->

# My Webapp YunoHost-erako

[![Integrazio maila](https://dash.yunohost.org/integration/my_webapp.svg)](https://dash.yunohost.org/appci/app/my_webapp) ![Funtzionamendu egoera](https://ci-apps.yunohost.org/ci/badges/my_webapp.status.svg) ![Mantentze egoera](https://ci-apps.yunohost.org/ci/badges/my_webapp.maintain.svg)

[![Instalatu My Webapp YunoHost-ekin](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=my_webapp)

*[Irakurri README hau beste hizkuntzatan.](./ALL_README.md)*

> *Pakete honek My Webapp YunoHost zerbitzari batean azkar eta zailtasunik gabe instalatzea ahalbidetzen dizu.*  
> *YunoHost ez baduzu, kontsultatu [gida](https://yunohost.org/install) nola instalatu ikasteko.*

## Aurreikuspena

This application allows you to easily install a custom Web application, providing files access with [SFTP](https://yunohost.org/en/filezilla).

It can also create a MySQL database - which will be backed up and restored with your application. The connection details will be stored in the file `db_access.txt` located in the root directory.

PHP-FPM version can also be selected among `none`, `7.4`, `8.0`, `8.1` and `8.2`.

**Once installed, go to the chosen URL to know the user, domain and port you will have to use for the SFTP access.** The password is one you chosen during the installation. Under the Web directory, you will see a `www` folder which contains the public files served by this app. You can put all the files of your custom Web application inside.


**Paketatutako bertsioa:** 1.0~ynh15
## Dokumentazioa eta baliabideak

- Jatorrizko aplikazioaren kode-gordailua: <https://github.com/YunoHost-Apps/my_webapp_ynh>
- YunoHost Denda: <https://apps.yunohost.org/app/my_webapp>
- Eman errore baten berri: <https://github.com/YunoHost-Apps/my_webapp_ynh/issues>

## Garatzaileentzako informazioa

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

**Informazio gehiago aplikazioaren paketatzeari buruz:** <https://yunohost.org/packaging_apps>
