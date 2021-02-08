# Cara Switch Versi PHP di Linux Ubuntu

## Contoh Kasus PHP 5.6 ke 7.2

### Disable Module PHP yang mau diganti
<pre>
sudo a2dismod php5.6
</pre>

### Enable Module PHP yang ingin dipakai
<pre>	
sudo a2enmod php7.2
</pre>

### Restart Apache
<pre>
sudo service apache2 restart
</pre>

### Jalankan Perintah Berikut di Command Line 
<pre>
- sudo update-alternatives --set php /usr/bin/php7.2
- sudo update-alternatives --set phar /usr/bin/phar7.2
- sudo update-alternatives --set phar.phar /usr/bin/phar.phar7.2
- sudo update-alternatives --set phpize /usr/bin/phpize7.2
- sudo update-alternatives --set php-config /usr/bin/php-config7.2

Note: sesuaikan dengan versi yang ingin diganti
</pre>