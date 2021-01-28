# Cara Membuat Virtual Host Apache di Linux Localhost

### Install Apache
<code>
1. sudo apt-get update
2. sudo apt-get install apache2
</code>

### Buat Folder website
<code>
Contoh 2 website : 
1. sudo mkdir -p /var/www/example.com/public_html
2. sudo mkdir -p /var/www/test.com/public_html
</code>

### Beri Permission
<code>
1. sudo chown -R $USER:$USER /var/www/example.com/public_html
2. sudo chown -R $USER:$USER /var/www/test.com/public_html

Note: Variabel $USER akan mengambil nilai dari user saat ini yang sedang aktif saat tombol Enter ditekan.

- sudo chmod -R 755 /var/www
</code>

### Buat File masing-masing website Contoh index.html
<code>
- sudo gedit /var/www/example.com/public_html/index.html

buat struktur html di index.html
&lt;html&gt;
    &lt;div&gt;
    	Success! this example.com
    &lt;/div&gt;
&lt;/html&gt;
</code>