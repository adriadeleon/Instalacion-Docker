# Instalacion-Docker  |  By Adrià 

___
- Comienzo de instalación
___

Se necesita Docker para trabajar con contenedores de Windows. Docker está formado por el motor de Docker (dockerd.exe) y el cliente de Docker (docker.exe). La forma más fácil de instalar todo se encuentra en la guía de inicio rápido, que te ayudará a preparar todo el equipo y ejecutar el primer contenedor.


Antes de poder usar Docker, deberás instalar las imágenes de contenedor. Para ello te dejo un enlace a las imagenes, donde vas a poder instalarlas despues de la descarga: https://docs.microsoft.com/es-es/virtualization/windowscontainers/manage-containers/container-base-images

___

- Después de buscar en google he visto que podemos configurarlo mediante un archivo de configuración y he creído que este metodo es más efectivo que hacerlo con interfaz gráfica.

El método preferido para configurar el motor de Docker en Windows es usar un archivo de configuración. El archivo de configuración se encuentra en 'C:\ProgramData\Docker\config\daemon.json'. Puedes crear este archivo si aún no existe.

- Primer paso:

Solo necesitas agregar los cambios de configuración deseados al archivo de configuración. Por ejemplo, en este ejemplo se configura el motor de Docker para que acepte las conexiones entrantes a través del puerto 2375. Las demás opciones de configuración usarán los valores predeterminados.

`{
    "authorization-plugins": [],
    "dns": [],
    "dns-opts": [],
    "dns-search": [],
    "exec-opts": [],
    "storage-driver": "",
    "storage-opts": [],
    "labels": [],
    "log-driver": "",
    "mtu": 0,
    "pidfile": "",
    "data-root": "",
    "cluster-store": "",
    "cluster-advertise": "",
    "debug": true,
    "hosts": [],
    "log-level": "",
    "tlsverify": true,
    "tlscacert": "",
    "tlscert": "",
    "tlskey": "",
    "group": "",
    "default-ulimits": {},
    "bridge": "",
    "fixed-cidr": "",
    "raw-logs": false,
    "registry-mirrors": [],
    "insecure-registries": [],
    "disable-legacy-registry": false
}`

Del mismo modo, en este ejemplo se configura el demonio de Docker para mantener las imágenes y los contenedores en una ruta alternativa. Si no se especifica, el valor predeterminado es **c:\programdata\docker.**

`Debemos modificar el archivo con estos valores: 
{   
    "data-root": "d:\\docker"
}`

___
- Configuracion con Docker Service
___

El motor de Docker también se puede configurar modificando el servicio de Docker con sc config. Con este método, se establecen marcas de motor de Docker directamente en el servicio de Docker. Ejecute el siguiente comando en un símbolo del sistema:

![image](https://user-images.githubusercontent.com/98842240/168109371-84eb6c35-87af-462a-95c3-04f120b4366d.png)

___

Una vez instalado Docker podemos acceder a CMD y ejecutar el comando para ver a la ballena saludarnos con un Hello World.

![image](https://user-images.githubusercontent.com/98842240/167869185-849f1bf4-c9bd-4dee-9463-210de9f49e7c.png)


![image](https://user-images.githubusercontent.com/98842240/167874761-368c8ea9-6aaa-4ff5-8866-07412d3d1017.png)

