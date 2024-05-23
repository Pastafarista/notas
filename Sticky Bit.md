#Linux 

Hay que tener en cuenta que prevalece los [[permisos]] del directorio antes que el de los archivos

Para evitar esto podemos usar el *Sticky Bit*, el cual previene que **otros** usuarios puedan eliminar o renombrar un archivo 

Para añadírselo a un directorio:

```bash
chmod +t prueba
chmod 1755 prueba
```

Ahora vemos que el directorio tiene una $t$ en el espacio de ejecución de otros, representando que tiene el *Sticky Bit*

- Como está en minúscula significa que el directorio tenía [[permisos]] de ejecución para otros, si fuese una $T$ mayúscula sería lo contrario

![[Pasted image 20240131105418.png]]

Cuando un directorio tenga el *Sticky Bit* aunque el directorio tenga permisos de escritura, los archivos dentro de este no podrán ser eliminados por otros usuarios

[Mas info](https://deephacking.tech/permisos-sgid-suid-y-sticky-bit-linux/#:~:text=Permiso%20SGID,-El%20permiso%20SGID&text=Si%20se%20establece%20en%20un,perteneciente%2C%20el%20grupo%20del%20directorio.)