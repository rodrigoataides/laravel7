
# Setup Docker Para Projetos Laravel 7 com PHP 7
[Assine a Unlocke, e Seja VIP!](https://unlocke.com.br)

### Passo a passo
Clone Repositório
```sh
git clone https://github.com/rodrigoataides/laravel7.git laravel7
```

```sh
cd laravel7/
```


Alterne para a branch laravel 7.x
```sh
git checkout laravel7
```


Remova o versionamento
```sh
rm -rf .git/
```

Atualize as variáveis de ambiente do arquivo .env
```dosini
APP_NAME=laravel7
APP_URL=http://localhost:8989

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=nome_que_desejar_db
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


Acesse o projeto
[http://localhost:8180](http://localhost:8180)
