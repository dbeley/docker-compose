FileBrowser Quantum — built from https://github.com/gtsteffaniak/filebrowser (image: gtstef/filebrowser:stable)

Setup:
    cp env.example .env           # fill in SOURCE_FOLDER, DOMAIN, DEFAULT_NETWORK
    mkdir -p data
    cp config.yaml.example data/config.yaml
    docker compose up -d

config.yaml lives in ./data/ (bind-mounted into the container at
/home/filebrowser/data/config.yaml). Edit it there and restart to apply.
The database and cache also live in ./data/.