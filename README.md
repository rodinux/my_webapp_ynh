<!--
N.B.: This README was automatically generated by https://github.com/YunoHost/apps/tree/master/tools/README-generator
It shall NOT be edited by hand.
-->

# My Webapp for YunoHost

[![Integration level](https://dash.yunohost.org/integration/my_webapp.svg)](https://dash.yunohost.org/appci/app/my_webapp) ![Working status](https://ci-apps.yunohost.org/ci/badges/my_webapp.status.svg) ![Maintenance status](https://ci-apps.yunohost.org/ci/badges/my_webapp.maintain.svg)

[![Install My Webapp with YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=my_webapp)

*[Lire ce readme en français.](./README_fr.md)*

> *This package allows you to install My Webapp quickly and simply on a YunoHost server.
If you don't have YunoHost, please consult [the guide](https://yunohost.org/#/install) to learn how to install it.*

## Overview

This application allows you to easily install a custom Web application, providing files access with [SFTP](https://yunohost.org/en/filezilla).

It can also create a MySQL database - which will be backed up and restored with your application. The connection details will be stored in the file `db_access.txt` located in the root directory.

PHP-FPM version can also be selected among `none`, `7.4`, `8.0`, `8.1` and `8.2`.

**Once installed, go to the chosen URL to know the user, domain and port you will have to use for the SFTP access.** The password is one you chosen during the installation. Under the Web directory, you will see a `www` folder which contains the public files served by this app. You can put all the files of your custom Web application inside.


## Disclaimers / important information

#### SFTP port

You may have change the SSH port as described in this section: [Modify the SSH port](https://yunohost.org/en/security#modify-the-ssh-port); then you should use this port to update your website with SFTP.



## Documentation and resources

* Upstream app code repository: <https://github.com/YunoHost-Apps/my_webapp_ynh>
* YunoHost documentation for this app: <https://yunohost.org/app_my_webapp>
* Report a bug: <https://github.com/YunoHost-Apps/my_webapp_ynh/issues>

## Developer info

**WARNING: This fork is experimental and only used for wordpress installed with my_webapp.** 

To work with wordpess add a nginx.conf with the paramters commented in the file example.conf

Please send your pull request to the [wordpress_spec branch](https://github.com/rodinux/my_webapp_ynh/tree/worpress_spec).

You may consider for example the line added in the `php-fpm.conf` file to take into account a Wordfence extension and few values for php-fpm.

Please do pull request on the [wordpress_spec branch](https://github.com/rodinux/my_webapp_ynh/tree/wordpress_spec).

To try the wordpress_spec branch, please proceed like that.


``` bash
sudo yunohost app install https://github.com/rodinux/my_webapp_ynh/tree/worpress_spec --debug
or
sudo yunohost app upgrade my_webapp -u https://github.com/rodinux/my_webapp_ynh/tree/wordpress_spec --debug
```

**More info regarding app packaging:** <https://yunohost.org/packaging_apps>
