# laravel-microservices
Simple Laravel Microservices with Docker & RabbitMQ

## Setup env

Copy .env.example to .env & insert your rabbitmq credentials

## Run

### Inside main repo
```
docker-compose up --build
docker-compose exec main sh
> php artisan migrate
```

### Inside admin repo
```
docker-compose up --build
docker-compose exec admin sh
> php artisan migrate --seed
```

## API Routes

### Main
```
( fetch products )
GET: /api/products

( like each product from random user )
POST: /api/products/{id}/like 
```
### Admin
```
( fetch products )
GET: /api/products

( fetch each product )
GET: /api/products/{id}

( insert product )
POST: /api/products

( update product )
PUT: /api/products/{id}

( delete product )
DELETE: /api/products/{id}
```

### External resources
Thanks to [Scalable Scripts](https://www.youtube.com/playlist?list=PLlameCF3cMEvU6Z_I2miuH7s5IJA_Kagp)
