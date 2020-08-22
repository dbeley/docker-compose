# docker-compose

A collection of docker-compose files.

I personally use those files with the traefik reverse proxy. If you don't use it, just comment the labels and networks sections related to traefik (you also might have to add/uncomment the ports section).

If you see variables like `$DATA_FOLDER` in a docker-compose.yml file, just put a file called `.env` in the same directory as the docker-compose.yml file with this content:
```
DATA_FOLDER=/path/to/data
```

## Usage

If you want to use traefik, start the traefik container first and create a .env file in every subfolder you use containing the following

```
DEFAULT_NETWORK=traefik-network
DOMAIN=yourdomain.home
```

Depending on the container, you might have to create an .env file and fill in variables for the container to work (i.e. to set up export folder) even if you don't use traefik.

If you don't want to use traefik, comment the labels/networks and uncomments the ports to use plain docker.


Run a docker-compose file

```
docker-compose up -d
```

Stop

```
docker-compose down
```
