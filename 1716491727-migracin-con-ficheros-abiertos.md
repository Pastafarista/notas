---
id: 1716491727-migracin-con-ficheros-abiertos
aliases:
 - Migración con ficheros abiertos
---

#sistemas-distribuidos 

Tenemos dos casos cuando [[1716491727-migracin-de-procesos|migramos procesos]] con ficheros abiertos:

- El proceso se migra de forma temporal a un nodo, y durante ese tiempo no hace lecturas
- El proceso se migra y hace lecturas/escrituras 

Se comparten bloques de disco para evitar una carga de la red con datos que no son necesarios