---
id: 1716491727-permisos-suid
aliases:
 - Permisos SUID
---

#Linux 

Permite ejecutar binarios de forma temporal como el [[1716491728-usuarios|usuario]] propietario del archivo

```bash
# Agregar permiso suid
chmod 4755
chmod u+s
```


Cuando hagamos ls -l se mostrará en el espacio de ejecución (x) una s, si es minúscula significa que el archivo tiene [[1716491727-permisos|Permisos]] de ejecución y si es mayúscula que no tenía permisos de ejecución

![[Pasted image 20240131130113.png]]

Para buscar archivos con el permisos SUID del sistema:

```bash
find / -type f -perm -4000 2>/dev/null
```

[Mas info](https://deephacking.tech/permisos-sgid-suid-y-sticky-bit-linux/#:~:text=Permiso%20SGID,-El%20permiso%20SGID&text=Si%20se%20establece%20en%20un,perteneciente%2C%20el%20grupo%20del%20directorio.)
