# Data container

A very generic data container to persist data and provide volumes.

There are three volumes exposed:

1. `/app` for the application
2. `/var/lib/mysql` for the database
3. `/data` for the cache store



## Docker Compose example

```
data:
  image: c4tech/generic-data
  volumes:
    - ./:/app

dbdata:
  image: c4tech/generic-data
  volumes:
    - ./database:/var/lib/mysql

cachedata:
  image: c4tech/generic-data
  volumes:
    - ./cache:/data
```
