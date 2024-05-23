#sistemas-distribuidos 

- En [[Multicomputador|entornos distribuidos]] es importante que las cargas de trabajo estén repartidas de forma equitativa.
- Necesitamos migrar procesos de nodos más cargados a otros menos cargados

## ¿Qué se migra?

- Normalmente, se destruye el proceso en el sistema de origen y se recrea en el de destino. Como mínimo se mueve el bloque de control del proceso
- Si tienen enlaces abiertos con otro procesos habrá que redireccionar los mensajes al nuevo nodo

## Tipos de migración

- [[Migración ambiciosa (completa)|Ambicioso (completo)]]
- [[Migración precopia|Precopia]]
- [[Migración ambiciosa (no completa)|Ambicioso (no completo)]]
- [[Migración copiar al referenciar|Copiar al referenciar]]
- [[Volcado]]
- [[Migración con ficheros abiertos|Ficheros abiertos]]


![[Negociación de la migración]]