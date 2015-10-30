# HHVM with settings for Magento2

docker run -d -p 9000:9000 -v /var/www:/var/www rtzio/hhvm-magento2

And in httpd.conf set proxy:

<LocationMatch "^/(.*\.php(/.*)?)$">ProxyPass fcgi://127.0.0.1:9000/var/www</LocationMatch>
