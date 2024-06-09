---
id: 1716491727-migracin-cuando-hay-threads
aliases:
 - Migración cuando hay threads
---

#sistemas-distribuidos 

- Si el proceso está subdividido en hilos, se complica más la [[1716491727-migracin-de-procesos|migración]]
	- Se pueden migrar los hilos manteniendo sistemas de llamadas a procedimientos remotos como formas de comunicación
	- No se puede migrar toda la memoria si no se han migrado todos los threads del proceso (en estos casos sería mejor la [[1716491727-migracin-copiar-al-referenciar|enviar las páginas bajo demanda]])