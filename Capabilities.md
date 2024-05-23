#Linux 

Las capabilities permiten otorgar [[permisos]] específicos a los binarios

Por ejemplo, podemos otorgar una capability a python para que nos permita cambiar de [[usuarios|usuario]]

```bash
setcap cap_setuid+ep /usr/bin/python
python -c "import os;os.setuid(0)"
```

Para eliminar las capabilities de un binario:

```bash
setcap -r /usr/bin/python
```

Para buscar archivos con capabilities en el sistema:

```bash
getcap -r / 2>/dev/null
```