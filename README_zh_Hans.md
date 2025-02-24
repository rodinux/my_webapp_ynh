<!--
注意：此 README 由 <https://github.com/YunoHost/apps/tree/master/tools/readme_generator> 自动生成
请勿手动编辑。
-->

## 概况

This application allows you to easily install an "empty" web application, in which you deploy your own custom website in the form of "static" HTML/CSS/JS assets or PHP.

Files can be uploaded [via SFTP](https://yunohost.org/en/filezilla) or any other method of your chosing.

During installation, you can also chose to initialize a MySQL or PostgreSQL database, which will be backed up and restored just like the other files in your application. The connection details will be stored in the file `db_access.txt` located in the root directory of the app.

PHP-FPM version can also be selected among (none), `7.4`, `8.0`, `8.1`, `8.2`, `8.3` and `8.4`.

**Once installed, go to the chosen URL to know the user, domain and port you will have to use for the SFTP access.** The password is the one specified during the installation. Under the app directory, you will see a `www` folder which contains the public files served by this app. You can put all the files of your custom web application inside.

You can also customize 404 errors - if you enable the option in the config panel. Simply create an `error` folder in the `www` root directory, containing your custom `html` files. 


**分发版本：** 1.0~ynh20
## 文档与资源

- YunoHost 商店： <https://apps.yunohost.org/app/my_webapp>
- 报告 bug： <https://github.com/YunoHost-Apps/my_webapp_ynh/issues>

## 开发者信息

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

**有关应用打包的更多信息：** <https://yunohost.org/packaging_apps>
