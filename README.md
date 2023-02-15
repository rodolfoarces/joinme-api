# Join Me

Create de env file

```
cp /joinme/.env.example /joinme/.env && ln -s ./joinme/.env ./.env
```

Application container image

```
docker-compose -f docker-compose.yml build app
```

Start the application

```
docker-compose -f docker-compose.yml up -d
```

Delete the lock file

```
docker-compose -f docker-compose.yml exec app rm -rf vendor composer.lock
```

Download componentes

```
docker-compose -f docker-compose.yml exec app composer install
```

Generate keys

```
docker-compose -f docker-compose.yml exec app php artisan key:generate
```


