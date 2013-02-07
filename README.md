a2ensite & a2dissite for Linux Arch
===================================

### Installation
```$ sudo mkdir -p /etc/httpd/conf/sites-available /etc/httpd/conf/sites-enabled```

```$ sudo cp path/to/scripts/a2* /usr/sbin```

```$ sudo chmod +x /usr/sbin/a2*```

Afterwards edit your /etc/httpd/conf/httpd.conf and put this line somewhere on the end of the file:

```Include conf/sites-enabled/```


### Usage

For the scripts to work, you first need to create your virtual host in the /etc/httpd/conf/sites-available folder. 
The a2ensite script is run with only 1 argument: the name of the virtual-host file. It then links the file to the sites-enabled folder, checks for any syntax errors and restarts your apache.

The a2dissite script disables the virtualhost by removing the link in the sites-enabled folder and restarts apache.
