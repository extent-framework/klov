## Klov - report server for ExtentReports 5  [![Join the chat at https://gitter.im/anshooarora/klov](https://badges.gitter.im/anshooarora/klov.svg)](https://gitter.im/anshooarora/klov?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

### Demo

* **Community:**  [klov.herokuapp.com](https://klov.herokuapp.com/projects)
* **Pro:**  [klov-pro.herokuapp.com](https://klov-pro.herokuapp.com/projects)

### Docker Hub

Klov is hosted at Docker Hub under [anshooarora/klov](https://hub.docker.com/r/anshooarora/klov).

### Installation

1. Install Docker ([Docker Desktop](https://docs.docker.com/desktop/) or [Engine](https://docs.docker.com/engine/), [Compose](https://docs.docker.com/compose/))
2. Download the [docker-compose.yml from this repository](https://github.com/extent-framework/klov-server/blob/master/docker-compose.yml) or:

```
$ curl https://raw.githubusercontent.com/extent-framework/klov-server/master/docker-compose.yml -o docker-compose.yml
```

3. Update the MongoDB connection details and the port where Klov is to be hosted at
4. Start Klov

```
docker-compose up
```

5. Open Klov at the $PORT you specified in `docker-compose.yml` or `default:80`

### Docker-compose.yml

```
version: '2'
services:
    klov:
        image: anshooarora/klov:1.0
        container_name: klov
        environment:
            - SPRING_DATA_MONGODB_URI=mongodb://{host}:{port}
        ports:
            - 80:80
```
