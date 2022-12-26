---
title: "Useful Commands"
description: "Some useful commands and guides"
created: 01-02-2022
tags:
- linux
- bash
- programming
- shortcuts
---

## PARA MONTAR GDRIVE EN LOCAL
- Primero entrar en `/etc/fuse.conf` y descomentar: `user_allow_other`
```
rclone mount --allow-other --allow-non-empty --daemon gdrive: /home/antjrobles/gdrive
```
- Para montar en Ubuntu
```
rclone mount gdrive: /home/antjrobles/gdrive --allow-other --vfs-cache-mode writes --daemon
```
- Para añadir carpeta nueva de Google Drive
    * Crear la carpeta con el nombre que se quiera y darles permisos `777`
    *  `rclone config` y añadir la carpeta de google drive que queramoos añadir (buscar el id de la carpeta en la dirección de la URL, el parte final)
    *  `rclone mount --allow-other --allow-non-empty --daemon nuevo_remote: /carpeta/local/`

## SABER TAMAÑO CARPETA

```
du -bsh /ruta...
du -hs *
df -h
ls -lh
```
## SAMBA CONTAINER
```
-s home;/share;yes;no;yes;antjrobles -g map to guest = never -g restrict anonymous = 2
puertos 139:139 y 445:445
```
## ENTRAR EN CONTENEDOR
```
docker ps (ver numero del contenedor)
```
```
pdocker exec -it "nº de contenedor" /bin/bash
```


##  COPIAR ARCHIVOS ENTRE TERMINALES SSH

`sudo scp -P 1984 (archivo a copiar) usuario@ip:/ruta de destino`
`sudo scp -r -P 1984 (archivo a copiar) usuario@ip:/ruta de destino` (Para copiar carpetas de manera recursiva). `-v`para verbose

## RESTIC (SAMPLE)
`sudo restic -r /mnt/BLUEDRIVE/restic/  --verbose --verbose  backup / --exclude=/mnt --exclude=/home/antjrobles/gdrive/`


## COPY FILES FROM INSIDE CONTAINER TO HOST
`sudo docker cp (número de container):/route/to/file /route/to/HOST   (NO HAY QUE ENTRAR EN EL CONTENEDOR, HACERLO CON EL USUARIO NORMAL, DESDE antjrobles)`

## COPY FILES FROM HOST TO CONTAINER
`sudo docker cp /route/to/file (coinainer id):/route/to/dest`

## IMGCLONE

-EN RASPY4B: `sudo imgclone -s /dev/sdb -p -d nombredelaimagen.img`
-EN RASPY4: `sudo imgclone -s /dev/sda -p -d nombredelaimaagen.img`

## ACTUALIZAR CONTENEDORES (DOCKER-COMPOSE)
-Entrar en la carpeta donde está el archivo `docker-compose.yml`
```
docker-compose pull 'nombre de la imagen
```
```
docker-compose up -d 'nombre de la imagen
```


## REINDEXAR "FACES" en PHOTOPRISM
```
docker-compose exec photoprism photoprism faces index
```
- Correr este comando en la carpeta de Photoprism


## INICIAR SCRUTINY
-Dentro del contenedor, correr este comando
```
scrutiny-collector-metrics run
```

## NCDU
Comando para saber tamaño de carpetas
```sudo ncdu / ```(analiza todo el sistema)
```sudo ncdu -x ```(excluye mount points)

## COMMAND INSIDE DOCKER
- Si ```apt-get install nano```no funciona. hacedlo con ```apk add nano```

## SHOW QCODE FROM WIREGUAD
`docker exec -it (container number) /app/show-peer (Number of peer)`.
Ejemplo: `docker exec -it 7ua32xdsw1 /app/show-peer 3`

## RSYNC [(Learn Linux TV)](https://www.youtube.com/watch?v=GqSxR93xK6E)
- To copy (backup) files from one place to another:
```rsync -avvz "archivo a copiar" /ruta/de/destino```
- To copy files from one server to another and specifying the `port`<br>
 ```rsync -avvz -e 'ssh -p 1984' "file to copy" antjrobles@192.168.0.52:/ruta/de/destino```
 - SAMPLES:
 ```
 rsync archive.txt /mnt/BLUEDRIVE/backups
 ```
 
```
 rsync -avvz -e 'ssh -p 1984' backup-nextcloud.sh antjrobles@192.168.0.52:/home/antjrobles/mis_scripts/Rsync
```

## ENABLE REMOTE DOCKER API
- Navigate to `/lib/systemd/system/`
- Edit `docker.service`
- Add this `ExecStart=/usr/bin/dockerd -H fd:// -H tcp://0.0.0.0:4243 --containerd=/run/containerd/containerd.sock`. And comment the old `ExecStart=...`
- `sudo systemctl daemon-reload`
- `sudo systemctl restart docker.service`
## CREATE A SHARED FOLDER
1. crear carpeta origen en el host origen:
`sudo mkdir /mnt/MIHDD/my_shared`
2. Dar permisos a la carpeta 'sudo chmod 777 /mnt/MIHDD/my_shared
3. instalar 'sshfs' en el host y en el host destino `sudo apt-get install sshfs`
4. en el host (no origen) ejecutar el siguiente comando `sshfs -p 1984 antjrobles@192.168.0.37:/mnt/MIHDD/my_shared /home/antjrobles/my_shared`  (antes crear la carpteta /home/antjrobles/my_shared en el host (no origen)
5. Comprobar que puedes crear archivos y copiar/mover en la carpteta. Sin el comando sudo `cp "archivo_a_copiar" /home/antjrobles/my_shared/`. 

## COMPROBAR TAMAÑO OCUPADO POR ARCHIVOS 
`sudo du / -d 1 -h -c` 
- (`/`) es la ruta. Añadir `-x` después de `du` para excluir`mount points`

## ACTUALIZAR PORTAINER
```bash
docker stop portainer
docker rm portainer
docker pull portainer/portainer-ce
docker run -d --name=portainer --hostname=portainer --network=host --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data -e TZ='Europe/Madrid' portainer/portainer-ce
```

