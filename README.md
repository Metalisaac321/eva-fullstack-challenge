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
