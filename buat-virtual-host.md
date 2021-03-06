# Cara Membuat Virtual Host Apache di Linux Localhost

### Install Apache
<pre><code>
1. sudo apt-get update
2. sudo apt-get install apache2
</code></pre>

### Buat Folder website
<pre>
<code>
Contoh 2 website : 
1. sudo mkdir -p /var/www/example.com/public_html
2. sudo mkdir -p /var/www/test.com/public_html
</code>
</pre>

### Beri Permission
<pre>
<code>
1. sudo chown -R $USER:$USER /var/www/example.com/public_html
2. sudo chown -R $USER:$USER /var/www/test.com/public_html

Note: Variabel $USER akan mengambil nilai dari user saat ini yang sedang aktif saat tombol Enter ditekan.

- sudo chmod -R 755 /var/www
</code>
</pre>

### Buat File masing-masing website Contoh index.html
<pre>
<code>
- sudo gedit /var/www/example.com/public_html/index.html

buat struktur html di masing-masing website. contoh index.html  
<br> 
&lt;html&gt;
    &lt;div&gt;
    	Success! this example.com
    &lt;/div&gt;
&lt;/html&gt;
</code>
</pre>

### Buat File Virtual Host
<pre>
<code>
- sudo cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/example.com.conf
<br>
Buka file yang sudah dibuat
- sudo gedit /etc/apache2/sites-available/example.com.conf
- ganti isinya seperti ini (sesuaikan dengan websitenya)
<br>
&lt;VirtualHost *:80&gt;
    ServerAdmin admin@example.com
    ServerName example.com
    ServerAlias www.example.com
    DocumentRoot /var/www/example.com/public_html
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
&lt;/VirtualHost&gt;

<br>
- lakukan juga untuk website kedua
</code>
</pre>

### Mengaktifkan File Virtual Host
<pre>
<code>
- sudo a2ensite example.com.conf
- sudo a2ensite test.com.conf

nonaktifkan konfigurasi default
- sudo a2dissite 000-default.conf
</code>
</pre>

### Restart Apache
<pre>
<code>
- sudo systemctl restart apache2 atau sudo service apache2 restart
</code>
</pre>

### Mengatur File Host Lokal IP
<pre>
<code>
- sudo gedit /etc/hosts
<br>
- masukkan ip local jika berada dilocal. jika menggunakan vps silahkan gunakan ipnya
127.0.0.1   localhost
127.0.0.1 example.com
127.0.0.1 test.com
</code>
</pre>

### Uji Coba website
<pre>
<code>
- Silahkan masukkan url di browser test.com atau example.com
</code>
</pre>