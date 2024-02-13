<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="200" alt="Nest Logo" /></a>
</p>

# Teslo API

1. Clonar proyecto
2. `yarn install`
3. Clonar el archivo `.env.template` y renombrarlo a `.env`
4. Cambiar las variables de entorno
5. Levantar la base de datos

```
docker compose up -d
```

6. Levantar: `yarn start:dev`

7. Ejecutar SEED

```
http://localhost:3000/api/seed
```

# Development notes:
Ejecutar este comando
```
docker compose build
```
El comando docker-compose build construye las imágenes de los servicios definidos en el archivo Docker Compose. Al ejecutarlo, Docker Compose lee el archivo de configuración y busca las definiciones de servicios. Luego, para cada servicio, busca las instrucciones de construcción ("build"), como el contexto y el Dockerfile. Finalmente, genera las imágenes según estas instrucciones.

# Production notes:
Ejecutar este comando
```
docker compose -f docker-compose.prod.yml build
```

## Docker Repo Name

[klerith/teslo-shop-cors:latest](https://hub.docker.com/repository/docker/klerith/teslo-shop-cors/general)

docker buildx build --platform linux/amd64,linux/arm64 -t klerith/teslo-shop-cors:1.0.0 --push .
