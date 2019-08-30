To get started, create your docker image:
```
docker build -t lisk-sdk --build-arg user_name=$USER --build-arg user_id=$UID .
```

Now bring everything up:
```
docker-compose up -d
```

You'll now have Postgres running and a development environment container running
To see: `docker ps`

You can enter the environment with `docker exec -it ( name or id of container here ) /bin/bash`

And you should be able to access Postgres from within the environment:
```
psql -d lisk_dev -h db -U lisk
```
