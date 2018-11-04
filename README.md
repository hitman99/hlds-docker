[![License Apache 2.0](https://goo.gl/joRzTI)](https://github.com/artem-panchenko/counter-strike-docker/blob/master/LICENSE)

![Half-Life Logo](http://files.gamebanana.com/img/ico/sprays/51f5acee815f0.png)

# Docker image for Half-Life Dedicated Server

### Build an image:

```
 $ make build
```

### Create and start new Half-Life server:

```
 $ docker run -d -p 27020:27015/udp -e START_MAP=bounce -e ADMIN_STEAM=0:1:1234566 -e SERVER_NAME="My Server" -e GAME="valve" --name cs hitman99/hlds
```

### Stop the server:

```
 docker stop cs
```

### Start existing (stopped) server:

```
 docker start cs
```

### Remove the server:

```
 docker rm cs
```

### Use image from [Docker Hub](https://hub.docker.com/r/hlds/server/):

```
 $ docker run -d -p 27020:27015/udp -e START_MAP=bounce -e ADMIN_STEAM=0:1:1234566 -e SERVER_NAME="My Server" -e GAME="valve" --name cs hitman99/hlds +log
```