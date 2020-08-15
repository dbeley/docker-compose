# docker-compose

A collection of docker-compose files.

I personally use those files with the traefik reverse proxy. If you don't use it, just comment the labels and networks sections related to traefik (you also might have to add/uncomment the ports section).

If you see variables like `$DATA_FOLDER` in a docker-compose.yml file, just put a file called `.env` in the same directory as the docker-compose.yml file with this content:
```
DATA_FOLDER=/path/to/data
```
