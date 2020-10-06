## Descripción

Eva Fullstack Challenge project

## Instalación

Para correr el proyecto se necesita instalar docker y docker-compose

```bash
# Bajar el repo de git
$ git clone https://github.com/Metalisaac321/eva-fullstack-challenge

# Navegar a la carpeta del proyecto
$ cd eva-fulstack-challenge

# Inicializar los submodulos de git
$ git submodule update --init --recursive
```

## Correr la aplicación

```bash
$ docker-compose up --build -d

```

## Puertos

```
front => localhost:4200
api => localhost:3000
postgres => localhost:5432 (usuario: root, password: SuperSecretPassword)
```

## Pruebas unitarias
### Backend
```bash
# Correr el contenedor de docker para las pruebas con la base de datos
$ docker run --name postgresTest -p 5433:5432  -e POSTGRES_PASSWORD=SuperSecretPassword -e POSTGRES_DB=db -d postgres

# Navegar a la carpeta del proyecto
$ cd eva-fulstack-challenge-backend

# Instalar paquetes necesarios 
$ npm i

# Correr las pruebas
$ npm run test
```

### Frontend
```bash

# Navegar a la carpeta del proyecto
$ cd eva-fulstack-challenge-frontend

# Instalar paquetes necesarios
$ npm i

# correr las pruebas
npm run test
```

## Notas adicionales
Los archivos CSV (seed) estan guardados en eva-fullstack-challenge-backend y se inicalizan la primera vez que se corre el contenedor de docker si necesita ver cuando se terminaron de cargar los datos use el siguiente comando:
```bash
# Este comando sirve para ver los logs del contenedor de docker donde se esta ejecutando el back.
$ docker logs --follow eva-fullstack-challenge-backend-container
```