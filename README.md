Some useful links and commands you may need:

[FIX] unable to connect packaglist: https://stackoverflow.com/questions/38818464/configuration-does-not-allow-connection-to-http-packagist-org-packages-json   

Composer.phar location: C:\ProgramData\ComposerSetup\bin

Installation/Redirecting with virtual hosts: https://www.codementor.io/@magarrent/how-to-install-laravel-5-xampp-windows-du107u9ji

Enable user auth in Laravel: composer require laravel/ui --dev
	                           php artisan ui vue --auth
	                           continue as requested.
				   
[FIX] Forbidden error on phpmyadmin: 
1) Open

httpd-xampp.conf

which is at /opt/lampp/etc/extra/

2) Find <Directory "/opt/lampp/phpmyadmin">

3) Now just add Require all granted before

4) So the code will look like this
<Directory "/opt/lampp/phpmyadmin">
    AllowOverride AuthConfig Limit
    Order allow,deny
    Allow from all
    Require all granted
</Directory>

5) Now finally Restart the xampp with this command /opt/lampp/lampp restart

That's it and you are Done!

It also work with xampp. :)
				   
