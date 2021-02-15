# Cara Membuat Virtual Host Xampp di Linux Localhost

### Edit file konfigurasi apache httpd.conf

<pre>
<ul>
<li>>sudo nano /opt/lampp/etc/httpd.conf</li>
<li>Cari baris kode di bawah ini, lalu hapus tanda #</li>
<li>Include etc/extra/httpd-vhosts.conf</li>
</ul>
</pre>

### Edit file konfigurasi virtual host
<pre>
sudo nano /opt/lampp/etc/extra/httpd-vhosts.conf
</pre>

### Tambahkan virtual host pada baris bagian bawah
<pre>
	&lt;VirtualHost *:80&gt;
	    ServerAdmin admin@localhost
	    DocumentRoot "/opt/lampp/htdocs"
	    ServerName localhost
	    ErrorLog "logs/localhost-error_log"
	    CustomLog "logs/localhost-access_log" common
	&lt;/VirtualHost&gt;

	&lt;VirtualHost *:80&gt;
	    ServerAdmin admin@test.dev
	    DocumentRoot "/opt/lampp/htdocs/test"
	    ServerName test.dev
	    ErrorLog "logs/test.dev-error_log"
	    CustomLog "logs/test.dev-access_log" common
	&lt;/VirtualHost&gt;

<ul>
	<li>Sesuaikan DocumentRoot dengan root folder project</li>
</ul>
</pre>

### Edit etc hosts
<pre>
sudo nano /etc/hosts
<ul>
	<li>Misal : test.dev</li>
	<li>Tambahkan : 127.0.0.1   test.dev</li>
</ul>
</pre>

### Restart Xampp
<pre>
sudo /opt/lampp/lampp restart
</pre>

### Jalankan di browser test.dev
<pre>
buka browser dan jalankan test.dev
</pre>

