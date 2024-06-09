---
id: 1716491727-migracin-de-procesos
aliases:
 - Migración de procesos
---

#sistemas-distribuidos 

- En [[1716491727-multicomputador|entornos distribuidos]] es importante que las cargas de trabajo estén repartidas de forma equitativa.
- Necesitamos migrar procesos de nodos más cargados a otros menos cargados

## ¿Qué se migra?

- Normalmente, se destruye el proceso en el sistema de origen y se recrea en el de destino. Como mínimo se mueve el bloque de control del proceso
- Si tienen enlaces abiertos con otro procesos habrá que redireccionar los mensajes al nuevo nodo

## Tipos de migración

- [[1716491727-migracin-ambiciosa-completa|Ambicioso (completo)]]
- [[1716491727-migracin-precopia|Precopia]]
- [[1716491727-migracin-ambiciosa-no-completa|Ambicioso (no completo)]]
- [[1716491727-migracin-copiar-al-referenciar|Copiar al referenciar]]
- [[1716491728-volcado|Volcado]]
- [[1716491727-migracin-con-ficheros-abiertos|Ficheros abiertos]]


![[1716491727-negociacin-de-la-migracin|Negociación de la migración]]