# PandoraFMS-Trabalho

## Getting Started.

Pull the images

```
docker pull brunoeleodoro/pandorafms:7
docker pull brunoeleodoro/mycentos
docker pull brunoeleodoro/myubuntu:latest
```


Create the network 
```
docker network create trabalho
```


Let's start our PandoraFMS server using the following command line: 
```
docker run --name pandorafms -v trabalho_rogerio:/var/lib/mysql -p 80:80 -d --network=trabalho --cap-add=NET_ADMIN --cap-add=NET_RAW brunoeleodoro/pandorafms:7
```
- **--name**: Container name
- **-v** : We need to specify the volume
- **-p** : The first port is the port that you want to access using your host machine, and the second one is the port exposed inside the container
- **--network**: To be sure that all the hosts will be in the same network, we need to specify one.
- **--cap-add** : Adding capabilities to change the network configuraton
