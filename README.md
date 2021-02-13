# App-Tdarr

## First Time Prerequisites

1. Run [Traefik](https://github.com/HackingServerHomelab/App-Traefik)

## Running the Containers

1. Update the following lines in [docker-compose.yml](./Docker/docker-compose.yml)
    * `../Data/media:/home/Tdarr/Media`
    * `../Data/temp:/temp`
    * `../Data/tdarr:/home/Tdarr/Documents/Tdarr`
    * `../Data/mongodb:/var/lib/mongodb`
2. Update the Traefik host label in [docker-compose.yml](./Docker/docker-compose.yml)
    * ``"traefik.http.routers.tdarr.rule=Host(`localhost`)"``
3. Run `docker-compose -f ./Docker/docker-compose.yml up -d`

## First Time Setup

1. Visit <https://your-ip>
