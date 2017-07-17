## Mongo Stateful With Docker (Linux container running in docker for windows)

Some times, we need up a docker container linux based, but our develop environment is windows. As we know, volumes between windows/linux with docker does not works in the best way. 

To provide an example, I made this repository to exemplify this case, creating a volume in docker for windows and running mongodb (keeping your data stateful) in a linux container.

### Creating a volume

```
docker volume create mongodata
```

### Running MongoDb Service

```
docker-compose up
```

### Considerations

After stopping your container and run again, your mongo data is the same.
