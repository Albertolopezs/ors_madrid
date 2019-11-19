# ors_madrid
Adaptación del servicio de OpenRouteService para la ciudad de Madrid, España
Créditos GIScience https://github.com/GIScience

**Clonar el repositorio**

https://github.com/GIScience/openrouteservice

Utilizada versión 5.0.2

**Modificar el mapa**

Dirección del mapa original - > ./docker/data/heidelberg.osm.gz 

Obtenemos el mapa de https://download.bbbike.org/osm/bbbike/Madrid/

Añadimos el mapa (Madrid.osm.gz) en -> ./docker/data/

Eliminamos el mapa antiguo

**Modificamos el DockerFile y docker-compose.yml**

Dockerfile

	Valor original -> ARG OSM_FILE=docker/data/heidelberg.osm.gz

	Nuevo valor -> ARG OSM_FILE=docker/data/Madrid.osm.gz


docker-compose

En ors-app -> build -> args
			
	Original -> OSM_FILE: ./docker/data/heidelberg.osm.gz

	Nuevo - > OSM_FILE: ./docker/data/Madrid.osm.gz
