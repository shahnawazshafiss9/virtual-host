# Simple step to create virrtual host
 
  
 cd etc/apache2/
 
 sudo cp 000-default.conf site.conf
 
 ```
 sudo nano site.conf
  
  	ServerName	site.com
 	Serveralias	www.site.com
 	Docuementroote	/var/www/html/site
 ```
 ## site enble	
 sudo a2ensite site.conf
 
 ```
 sudo systemctl restart apache2
 sudo service apache2 restart
 ```
 ## set host name
 
 sudo nano /etc/hosts
 ```
 127.0.0.1   site.com
 ``
 ## set permission to storage directory	
```
sudo chmod -R 777 storage/ 	

# -----------------------------------------------------------------------------------------------------------------------------------------------------
# --------------------------------------------------Window Vitual Host---------------------------------------------------------------------------------

## First Changes
``` 
C:\Windows\System32\drivers\etc\hosts
127.0.0.1       site.com
```


## Second changes

```
c:\xampp\apache\conf\extra\httpd-vhosts.conf
<VirtualHost *:80>
    DocumentRoot "D:\xampp\htdocs\site"
    ServerName site.com
</VirtualHost>
```
