# Setup
1. clone this repository
2. `cd` into the repository
3. `mkdir` a `data` directory
4. run following command to build
```
docker build -t psql-wal2json . 
```
5. run following command to start PostgreSQL with wal2json plugin
```
docker run -e POSTGRES_PASSWORD=Pass2021 -v /$(pwd)/data:/var/lib/postgresql/data -p 5432:5432 psql-wal2json
```

Remarks:
```
host: localhost
username: postgres
database: postgres
```