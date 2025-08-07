# docker-compose

## Features

A curated collection of `docker-compose` files to help you spin up your own self-hosted services. Each service lives in its own folder with a `docker-compose.yml` and sample environment file.

- 80+ ready-to-use service definitions
- Out-of-the-box [Traefik](https://traefik.io/) reverse proxy labels
- Uses `.env` files for clean configuration
- Minimal defaults that you can easily customize

## Getting Started

### Requirements

- [Docker](https://docs.docker.com/get-docker/) and [Docker Compose](https://docs.docker.com/compose/install/)
- Optional: a running [Traefik](https://traefik.io/) instance

### Running a Service

1. Choose a service folder (e.g. `jellyfin`).
2. Create a `.env` file next to the `docker-compose.yml`. Example:
   ```env
   DATA_FOLDER=/path/to/data
   DEFAULT_NETWORK=traefik-network
   DOMAIN=yourdomain.home
   ... # depending on the service you might need more variables, see the included README.md if it exists
   ```
   `DEFAULT_NETWORK` and `DOMAIN` are only required if you use Traefik.
3. Start the container:
   ```bash
   docker compose up -d
   ```

### Not using Traefik?

- Comment out the `labels` and `networks` sections.
- Uncomment the `ports` section to expose services directly.

### Managing Containers

```bash
docker compose down  # stop
docker compose pull  # update image
docker compose up -d # run
```

## Highlights

- **AdGuard Home** – network-wide ad-blocker
- **Dokuwiki** – flexible wiki software
- **Filebrowser** – simple web file manager
- **Jellyfin** – media server
- **Navidrome** – Subsonic-compatible music server
- **Paperless-NGX** – document management
- **Shaarli** – minimalist bookmarking service
- **slskd** – Soulseek file sharing client
- **Wallabag** – read-it-later service
- **Watchtower** – automatic container updater

## Contributing

Issues and pull requests are welcome! I don't use all the services at once so some services might not be up-to-date, feel free to submit new services or improvements.

## License

MIT
