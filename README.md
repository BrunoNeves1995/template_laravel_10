
# Setup Docker Para Projetos Laravel (10)
### Passo a passo
Clone Repositório
```sh
git clone https://github.com/BrunoNeves1995/template_laravel_10.git
```

Clone os Arquivos do Laravel
```sh
git clone https://github.com/BrunoNeves1995/template_laravel_10 laravel-
```


Copie os arquivos docker-compose.yml, Dockerfile e o diretório docker/ para o seu projeto
```sh
cp -rf template_laravel_10/* laravel-
```
```sh
cd laravel-
```


Crie o Arquivo .env
```sh
cp .env.example .env
```


Atualize as variáveis de ambiente do arquivo .env
```dosini
APP_NAME="Especializa Ti"
APP_URL=http://localhost:8989

DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=root

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```


Suba os containers do projeto
```sh
docker-compose up -d
```


Acessar o container
```sh
docker-compose exec app bash
```


Instalar as dependências do projeto
```sh
composer install
```


Gerar a key do projeto Laravel
```sh
php artisan key:generate
```

Remover o git
```sh
rm -rf .git/
```


Acessar o projeto
[http://localhost:81](http://localhost:81)
