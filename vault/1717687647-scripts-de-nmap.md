---
id: 1717687647-scripts-de-nmap
aliases:
  - Scripts de nmap
tags:
  - linux
---

# Scripts de nmap

La herramienta [[1717682023-RIJF|nmap]] cuenta con muchos scripts programados en lua.

Con la flag `-sC` se lanzan una serie de scripts que detectan servicios y versiones. Se puede combinar con `-sV` para detectar versiones de servicios.

```bash
nmap -sCV <ip>
```

Para ver la lista de scripts que se pueden lanzar, se puede usar el comando:

```bash
ls /usr/share/nmap/scripts/
```

Para lanzar un script en concreto, se puede usar el comando:

```bash
nmap --script <script> <ip>
```

También se le puede indicar una categoría de scripts con el comando:

```bash
nmap --script <category> <ip>
```

Se pueden combinar categorías, por ejemplo podemos lanzar un script que pertenezca a las categorías `vuln` y `safe` con el comando:

```bash
nmap --script "vuln and safe" <ip>
```

El script `http-enum` enumera directorios y archivos de un servidor web. Se puede lanzar con el comando:

```bash
nmap --script http-enum <ip>
```
