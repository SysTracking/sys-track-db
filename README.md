# SysTracking database

## Run environment

```bash
cp .env.example .env
```

Now complete attributes in .env file, for example you can complete like this :

```bash
MYSQL_DATABASE=sys_track
MYSQL_PORT=8001
MYSQL_USER=jdoe
MYSQL_PASSWORD=rootroot
MYSQL_ROOT_PASSWORD=rootroot
```

Then you can start docker environment :

```bash
docker compose up
```

If you have an error with network, you must configure network in docker-compose.yml like this :

```bash
...

networks:
  default:
    driver: bridge
    ipam:
      driver: default
      config:
        - subnet: 10.202.20.0/24 # specify your own subnet ip
```
