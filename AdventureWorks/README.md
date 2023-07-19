## Adventureworks from PostgreSQL


**Comandos:**

```shell
# Make Database
psql -c "CREATE DATABASE \"adventure_works\";"

# Load insert data
psql -d adventure_works < install.sql

# Access Database
\c "adventure_works"

# # Access schema
\dt (humanresources|person|production|purchasing|sales).*

```