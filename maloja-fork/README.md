Built from the fork at https://github.com/dbeley/maloja (no published image).

Usage:
    cp env.example .env   # fill in values
    docker compose up -d --build

Update to latest master:
    docker compose build && docker compose up -d

`docker compose pull` does NOT apply (no remote image). Use `build` to refresh.

Volumes (3-mount layout, matches the fork's example-compose.yml):
    ./config  -> /etc/maloja
    ./data    -> /var/lib/maloja
    ./logs    -> /var/log/maloja