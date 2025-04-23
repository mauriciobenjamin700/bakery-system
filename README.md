# Projeto BakerySystem

## Como Executar

- Clone este repositório: `github.com/mauriciobenjamin700/bakery-system`
- Abra o projeto
- Clone os seguintes repositórios dentro do projeto
- `github.com/mauriciobenjamin700/bakery-system-api`
- `github.com/mauriciobenjamin700/bakery-system-db`
- `github.com/mauriciobenjamin700/bakery-system-web`

Crie um arquivo `.env` na raiz do projeto e coloque o seguinte conteúdo nele:

```bash
DB_URL="postgresql+asyncpg://user:password@bakery-system-db:5432/db"
DB_USER="user"
DB_PASSWORD="password"
DB_HOST="bakery-system-db"
DB_PORT="5432"
DB_NAME="db"
TEST_DB_URL="sqlite+aiosqlite:///:memory:"
TOKEN_ALGORITHM="HS256"
TOKEN_EXPIRES_IN_MINUTES=60
TOKEN_SECRET_KEY="your_secret_key"
```

Tenha o `docker` instalado em sua maquina

Use o comando `docker compose up -d --build` para ligar a aplicação e acesse o [localhost](http://localhost) para visualizar o projeto.

A API se encontra [neste link](http://localhost/api/docs) caso queira dar uma olhada.
