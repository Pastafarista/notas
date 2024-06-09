---
id: 1716491727-bsquedas-a-nivel-de-sistema
aliases:
 - Búsquedas a nivel de sistema
---

---
id: Búsquedas a nivel de sistema
aliases:
  - Búsquedas a nivel de sistema
tags:
  - Linux
---

# Búsquedas a nivel de sistema

Para realizar búsquedas utilizaremos el comando *find*

- Buscar los archivos con passwd en el nombre
```bash
find / -name 'passwd' 2>/dev/null
```

- También podemos usar expresiones regulares en los nombres de los archivos

```bash
find / -name pas\* 2>/dev/null
```

- Buscar archivos con [[1716491727-permisos-suid|permisos SUID]]

```bash
find / -perm 4000 -type -d 2>/dev/null
```

- Buscar archivos de root con capacidad de escritura

```bash
find / -user root -writable 2>/dev/null
```
