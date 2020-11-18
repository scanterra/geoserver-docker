# Geoserver Docker

[![Actions Status](https://github.com/scanterra/geoserver-docker/workflows/build/badge.svg)](https://github.com/scanterra/geoserver-docker/actions)

## Contenido

* [Informacion general](#informacion-general)
* [Tecnologias](#tecnologias)
* [Setup](#setup)
* [CI/CD](#ci/cd)
* [Referencias](#referencias)

## Informacion General

Este repositorio es un fork del repositorio [geoserver-docker](https://github.com/GeoNode/geoserver-docker).  
Actualmente estamos usando la versión desde el commit: `8e86c22a4e1de421160485ef2129b5cc93917050`.

Scanterra no realizó cambios en este repositorio.

## Tecnologias

Las mismas utilizadas en [geoserver-docker](https://github.com/GeoNode/geoserver-docker).

* Utiliza:
* Imagenes:
    - [tomcat:9-jre8](https://hub.docker.com/_/tomcat)

## Setup

La generación de imágenes solo utiliza el Dockerfile local del repositorio.

- Requerimientos:
    - [`Docker`](https://docs.docker.com/)
- Generar imágen `scanterra/geoserver-docker:latest`
    - `docker build -t scanterra/data-docker:latest .`

Recordar que al momento de instanciar esta imágen debe estar generada la carpeta `/geoserver_data/data` con la información del repositorio [data-docker](https://github.com/scanterra/data-docker).

### CI/CD

Se deben configurar los siguientes secrets en este repositorio:
- **Docker Hub**, credenciales con los permisos necesarios para acceder, pullear y pushear a la organización [**Scanterra**](https://hub.docker.com/orgs/scanterra).
  - **DOCKERHUB_USERNAME:** nombre del usuario
  - **DOCKERHUB_PASSWORD:** contraseña del usuario

Ver este [documento](https://github.com/scanterra/scanterra_quickstart) con la información del flujo de CI/CD.

## Referencias

- [Readme Anterior](/README_OLD.md)
