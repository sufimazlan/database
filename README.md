# database

## install and create database

### 1. Install postgress.

`sudo apt install postgres `

### 2. Configure conf file. This allows PostgreSQL to listen on all available IP addresses.
https://blog.devart.com/configure-postgresql-to-allow-remote-connection.html

`sudo nano /etc/postgresql/12/main/postgresql.conf` :

```
change from #listen_addresses = 'localhost' to listen_addresses = '*'
```


`sudo nano /etc/postgresql/12/main/pg_hba.conf` :

change from 

```
# IPv4 local connections: 

host    all             all             127.0.0.1/32            md5
```

to

```
# IPv4 local connections:

host    all             all             0.0.0.0/0            md5
```

### 3. Restart postgres service

`sudo service postgresql restart`
