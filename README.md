Script_backup

Como criar um Backup do PostGres utilizando a lingaguem SHELL

Incluir as variáveis de ambiente "pg_dump" e "pg_restore" do postgres

Realizar as mudanças de dados do arquivo tais como:

#!/bin/bash

export PGPASSWORD = "forcajovem"

pg_dump -U USUÁRIO_POSTGRES -h LOCAL_BANCO_DE_DADOS -O -o -b -F c NOME_BANCO_DADOS > NOME_DO_BACKUP.backup

pg_restore -U USUÁRIO_POSTGRES -h LOCAL_BANCO_DE_DADOS -d NOME_BANCO_DADOS NOME_DO_BACKUP.backup

Realizar a execução do arquivo Shell.
