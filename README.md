Elastic Beanstalk Config for ALL IN ONE PHP54 Environment
==============
##What it is##
- This config sets up an environment consist of **php54 + APC + FPM + Mongo + Redis + MySQL + Memcached** and other common PHP dependencies, it is a pretty much all in one piece vanilla setup which is much more completed than AWS offers. 
- This config doesn't require customization on the AMI.


##How to use##
- Copy the .ebextension folder to the root of your zip archive before you upload.
- You need to change *webapp.conf* section and also tunning /etc/php-fpm.d/www.conf to suit your needs.
- In the service section, you can turn on and off services also you can do that in private config zzzzz_loadnewservice.sh
- Please Make sure to use http://yaml-online-parser.appspot.com to check the syntax before uploading, this can save your time and soul!

##Note##
- Tested on ami-1624987f and as of Apri 28 2013. 
- If it doesn't work on your environment, please file an issue contain the AMI as well as send the eb-init logs within the machine.
- Even though it is good for general usage, but it is still wise to understand the config throughly (you can ssh into the box to dig through the logs in /var/log)

##Phpinfo##
- Better to show you what ini files it depends on:
>> apc.ini, aws.ini, bcmath.ini, curl.ini, dom.ini, environment.ini, fileinfo.ini, gd.ini, igbinary.ini, imagick.ini, intl.ini, json.ini, mbstring.ini, mcrypt.ini, memcache.ini, memcached.ini, mysqlnd.ini, mysqlnd_mysql.ini, mysqlnd_mysqli.ini, oauth.ini, odbc.ini, pdo.ini, pdo_mysqlnd.ini, pdo_odbc.ini, pdo_pgsql.ini, pdo_sqlite.ini, pgsql.ini, phar.ini, posix.ini, redis.ini, soap.ini, sqlite3.ini, ssh2.ini, sysvmsg.ini, sysvsem.ini, sysvshm.ini, uuid.ini, wddx.ini, xmlreader.ini, xmlrpc.ini, xmlwriter.ini, xsl.ini, zip.ini
- I have included a phpinfo dump in *phpinfo.webarchive* for your reference (open in safari)

##Reference##
- http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/customize-containers.html


***
Many thanks to https://github.com/carboncoders/elasticbeanstalk-nginx-php and https://github.com/arielscarpinelli/elastic-beanstalk-php-5.4-fpm-nginx-non-legacy
***