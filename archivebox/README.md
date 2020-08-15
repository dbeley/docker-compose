# archivebox

```
mkdir data
docker-compose run archivebox init
docker-compose run archivebox manage createsuperuser
docker-compose up -d
```

```
docker-compose run archivebox add 'https://example.com'
docker-compose run archivebox add < links.txt
```
