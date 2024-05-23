#Linux 

Para crear usuarios en Linux usamos el comando *useradd*

```bash
# Crear usuario pepe con shell bash y home /home/pepe
useradd pepe -s /bin/bash -d /home/pepe
```

Con *passwd* le podemos asignar una contraseña

```bash
passwd pepe
```

El problema que tenemos es que pepe no es el dueño de su home, es el usuario root, por lo tanto vamos a cambiar los [[permisos]]:

```bash
# Cambiar el grupo y el propietario de /home/pepe
chgrp pepe /home/pepe
chown pepe /home/pepe
```

Con *usermod* podemos añadir al usuario a un [[grupos|grupo]]

```bash
usermod -a -G Alumnos pepe
```