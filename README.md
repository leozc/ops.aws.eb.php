Elastic Beanstalk Config for PHP54
==============
This stack set up an environment consist of
php54 + APC + FPM + Mongo + Redis and all in one piece plus this doesn't requires custom AMI.
You need to change webapp.conf for your need also tunning /etc/php-fpm.d/www.conf to suit your situation 



Many thanks to https://github.com/carboncoders/elasticbeanstalk-nginx-php and https://github.com/arielscarpinelli/elastic-beanstalk-php-5.4-fpm-nginx-non-legacy
