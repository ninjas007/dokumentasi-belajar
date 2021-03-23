# Buat Migration File dan Migrate Schema Table Laravel Custom Folder Path

### Make Migration Custom Folder Path

<pre>
* perintahnya: buat tabel dengan namatable terus path foldernya (harus udah dibuat karena tidak langsung dibuatin laravelnya)
* kalau alter tinggal ganti create_namatable_table nya
<br>
php artisan make:migration create_namatable_table --path=database/migrations/features/2021-03/dll/
</pre>

### Migrate Schema Table
<pre>	
* harus akses ke foler pathnya
<br>
php artisan migrate --path=database/migrations/features/2021-03/dll
</pre>