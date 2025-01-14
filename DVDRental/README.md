## DVDRental from PostgreSQL

**Restaurar pelo PGAdmin**
1. Com o arquivo  dvdrental.tar. 
OBS: Você pode usar uma ferramenta de compactação como 7-Zip ou WinRAR para extrair o conteúdo do arquivo dvdrental.zip. Depois de extraído, você pode criar um novo arquivo e salvá-lo como dvdrental.tar.

2. Abra o pgAdmin e conecte-se ao seu servidor de banco de dados PostgreSQL.

3. Na coluna esquerda do pgAdmin, localize o grupo "Servers" e expanda-o. Em seguida, expanda o servidor para o qual deseja restaurar o arquivo dvdrental.tar.

4. Clique com o botão direito do mouse na opção "Bancos de dados" no servidor e selecione "Restaurar..." no menu de contexto.

5. Na caixa de diálogo "Restaurar", navegue até o local onde você salvou o arquivo dvdrental.tar. Selecione o arquivo e clique no botão "OK" ou "Abrir" para iniciar o processo de restauração.

6. Configure as opções de restauração conforme necessário. Você pode especificar o banco de dados de destino, escolher se deseja remover objetos existentes, definir o formato como "Personalizado ou Tar" e ajustar outras opções de acordo com suas necessidades.

7. Clique no botão "Restaurar" para iniciar o processo de restauração. O pgAdmin lerá o arquivo dvdrental.tar e restaurará o esquema e os dados do banco de dados adequadamente.

8. Assim que o processo de restauração for concluído, você verá uma mensagem de sucesso indicando que a restauração foi bem-sucedida.



**Restaurar via terminal**
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
