## DVDRental from PostgreSQL


**Comandos:**

```shell
# Make Database
psql -c "CREATE DATABASE \"dvdrental\";"

# Load insert data
pg_restore -U postgres -d dvdrental dvdrental.tar

# Access Database
psql

\c "dvdrental"

# # Access schema
\dt public.*

```