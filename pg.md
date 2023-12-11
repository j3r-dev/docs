```
apt install -y postgresql-client
```

- Test connection
```
pg_isready -d <db_name> -h <host_name> -p <port_number> -U <db_user>
```

- Open connection
```
psql -h <hostname> -p <port> -U <username> -d <database>
```