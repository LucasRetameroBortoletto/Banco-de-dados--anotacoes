# Aula 02
#### Para verificar o status e demais informações do banco de dados, utilizamos o camando: 
```bash
pg_lsclusters
```
#### Para acesso via root, sem senha (SOCKET LOCAL), utilizamos o comando: 
```bash
sudo -u postgres psql
```
#### Para retornar ao usuario anterior : 
```bash
\q
```
#### Para alterar a senha do Postgres, utilizar o comando: 
```sql
ALTER USER postgres PASSWORD 'SENHA'
```
Após as alterações da senha o acesso, via localhost (Socket Externo), é feito através do comando:
```bash
sudo psql

### Configurações inciais do POSTGRES:

- Para habilitar conecões externas, de outros IPs, for necessário as sguintes etapas:

1. Navegar até a pasta do POSTGRESQL (`/etc/postgresql/18/main/`).

2.Editar o arquivo `postgresql.conf` através do comando: 

```bash
sudo nano postgresql.conf
```
3.Editar a linha listen_adresses = '*'; 


4.Editar o arquivo `pg_hba.conf.`
```bash
sudo nano pg_hba.conf
```

5.Nas últimas, linhas adcionamos as seguintes configurações:
`host all all 0.0.0.0/0 scram-sha-256`

`host all all 10.87.47.0/24 scram-sha-256`

## Criação do primeiro Banco de Dados 
```mermaid
graph TD
A[(Banco de Dados)]
```

Para criar o Banco de Dados, utilizamos o comando:
```sql
CREATE DATABASE cidades;
```
Para verificar os bancos existentes: 
```sql
\l
``` 




