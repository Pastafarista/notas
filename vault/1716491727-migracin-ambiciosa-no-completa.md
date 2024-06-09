---
id: 1716491727-migracin-ambiciosa-no-completa
aliases:
 - Migración ambiciosa (no completa)
---

#sistemas-distribuidos 

- En este caso, solo se envían las páginas de memoria que se encuentren en la memoria principal, y han sido referenciadas o modificadas recientemente
- El resto de páginas de memoria del proceso se transfieren bajo demanda
- Minimiza los datos que se transfieren
- Deja rastro del proceso en la máquina origen, la cual mantiene las páginas de memoria hasta que el proceso muera o sean copiadas.