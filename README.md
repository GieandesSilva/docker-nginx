# DOCKER + NGINX + LARAVEL 5.7 + MYSQL

O que você encontra aqui:
    
    * web-base   - Um serviço com ALPINE + NGINX
    * app-base   - Um serviço com ALPINE + PHP7.2-fpm + Laravel 5.7
    * db-base    - Um serviço com MYSQL5.7
    * redis-base - Um serviço com REDIS

## Instalação

* Faça o clone do projeto:

```bash
    git clone git@github.com:GieandesSilva/docker-nginx.git [nome-do-projeto]
```

* Entre na pasta [nome-do-projeto] e rode:

```bash
    docker-compose up -d
```

* Verifique se os containers estão de pé [opcional]:

```bash
    docker ps
```

* Acesse o container do aplicativo para instalar as dependências:

```bash
    docker exec -ti app-base sh
```
    
* Dentro do container execute os comandos:
    
```bash
    * Instale as dependências com composer:
    
        composer install

    * Faça uma cópia do .env.example:

        cp .env.example .env

    * Gere a chave para o aplicativo:
    
        php artisan key:generate
```

* Verifique o seu projeto rodando no link:

```bash
    http://localhost:8000/
```
            
## :D
Meu primeiro projeto com docker.

## Nós
[Gieandes Silva](http://gieandessilva.com)
