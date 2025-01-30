<!--
注意：此 README 由 <https://github.com/YunoHost/apps/tree/master/tools/readme_generator> 自动生成
请勿手动编辑。
-->

# YunoHost 上的 My Webapp

[![集成程度](https://dash.yunohost.org/integration/my_webapp.svg)](https://dash.yunohost.org/appci/app/my_webapp) ![工作状态](https://ci-apps.yunohost.org/ci/badges/my_webapp.status.svg) ![维护状态](https://ci-apps.yunohost.org/ci/badges/my_webapp.maintain.svg)

[![使用 YunoHost 安装 My Webapp](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=my_webapp)

*[阅读此 README 的其它语言版本。](./ALL_README.md)*

> *通过此软件包，您可以在 YunoHost 服务器上快速、简单地安装 My Webapp。*  
> *如果您还没有 YunoHost，请参阅[指南](https://yunohost.org/install)了解如何安装它。*

## 概况

This application allows you to easily install a custom Web application, providing files access with [SFTP](https://yunohost.org/en/filezilla).

It can also create a MySQL database - which will be backed up and restored with your application. The connection details will be stored in the file `db_access.txt` located in the root directory.

PHP-FPM version can also be selected among `none`, `7.4`, `8.0`, `8.1` and `8.2`.

**Once installed, go to the chosen URL to know the user, domain and port you will have to use for the SFTP access.** The password is one you chosen during the installation. Under the Web directory, you will see a `www` folder which contains the public files served by this app. You can put all the files of your custom Web application inside.


**分发版本：** 1.0~ynh15
## 文档与资源

- 上游应用代码库： <https://github.com/YunoHost-Apps/my_webapp_ynh>
- YunoHost 商店： <https://apps.yunohost.org/app/my_webapp>
- 报告 bug： <https://github.com/YunoHost-Apps/my_webapp_ynh/issues>

## 开发者信息

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

**有关应用打包的更多信息：** <https://yunohost.org/packaging_apps>
