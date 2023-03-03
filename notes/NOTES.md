# Notes

- Colima environment (Docker desktop )

        $ colima start --cpu 4 --memory 8 --mount-type 9p
        $ open -a docker (Para que aparezcan las imagenes en el contexto)
        $ colima list
        $ docker context list
        $ docker context use desktop-linux


PREMISA

SEGUN ESTO ME JODI

Las imágenes de Docker en el contexto de Desktop-Linux no se almacenan en el sistema operativo host (en este caso, macOS), sino dentro de la máquina virtual de Docker. En macOS, Docker utiliza una máquina virtual llamada "Docker Desktop VM" para ejecutar los contenedores. Por lo tanto, las imágenes de Docker se almacenan en esta máquina virtual en lugar de en el sistema operativo host.

La ubicación exacta de las imágenes de Docker en la máquina virtual de Docker puede variar según la configuración de Docker en macOS. Sin embargo, en general, las imágenes de Docker se almacenan en el directorio /var/lib/docker dentro de la máquina virtual de Docker.

Las imágenes de Docker no se almacenan directamente en el contexto de Colima en sí, sino en los nodos del clúster de Docker que están siendo administrados por Colima. En macOS, los nodos de Docker que están siendo administrados por Colima se ejecutan en una máquina virtual, y las imágenes de Docker se almacenan en esa máquina virtual. La ubicación exacta de las imágenes de Docker en la máquina virtual de Colima puede variar según la configuración de Colima en macOS.

Para acceder a la máquina virtual de Colima y ver la ubicación exacta de las imágenes de Docker, se puede utilizar el siguiente comando:

colima ssh


screen ~/Library/Containers/com.docker.docker/Data/vms/0/tty

Este comando inicia una sesión de terminal dentro de la máquina virtual de Docker.

docker-machine ssh default



la vaina esta por aca 
/Users/dposada/Library/Containers/com.docker.docker/Data/vms/0

Peor creo que al desinstalar docker desktop barrieron con las imagenes ... 

ademas no hay dokcer machine

No encontre la carpeta donde estan las imagenes, se almacenan por capas y es delicado. pero ... se pueden sacar backups

docker save, docker load (imagenes)

docker export (contenedores se vuelven imagen)

tener en cuenta docker commit







# Troubleshooting

    docker context inspect


salida a uno de los canales de slack (maria)
