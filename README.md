# database

## install and create database

1. Install postgress.
`sudo apt install postgres `

2. Configure conf file. This allows PostgreSQL to listen on all available IP addresses.
https://blog.devart.com/configure-postgresql-to-allow-remote-connection.html
- postgresql.conf 
`sudo nano /etc/postgresql/12/main/postgresql.conf`

- pg_hba.con
`sudo nano /etc/postgresql/12/main/pg_hba.conf`

3. Restart postgres service
`sudo service postgresql restart`
