# Cara Undo / Reset Commit Apabila Terlanjur Push Ke Repo Github

### Reset ke commit yang kita inginkan
<pre>
	git reset --hard &lt;commit's number&gt;

	contoh : git reset --hard gdg2t62382e8 
</pre>

### Force push ke branch yang dikerjakan
<pre>
	misal branch master : git push -f origin HEAD^:master
</pre>


### Terakhir jalankan 
<pre>
	git reset -f --soft HEAD~

	atau 

	git reset --soft HEAD~
</pre>