#sistemas-distribuidos 

- Las estrategias de datos distribuidos (DDP) se utilizan para hacer uso de los [[Multicomputador|multicomputadores]]
- El objetivo de estas estrategias es procesar la información de la forma más eficiente posible, aprovechando el procesamiento en paralelo y la replicación de unidades
- No todos los nodos son iguales, se elegirán en función de sus características
- El DDP debe tener funciones de recuperación ante errores, perdidas de información, caídas de nodos, pérdidas de datos...

## Características:

- **Disponibilidad:** Como hay muchos sistemas interconectados, en caso de la caída de un nodo, una unidad replicada podría asumir su carga rápidamente
- **Compartición de recursos:** Se permite compartir software/hardware entre usuarios. Las bases de datos se pueden mantener distribuidas entre las instalaciones
- **Crecimiento incremental:** No hace falta tirar equipos viejos para comprar equipos nuevos. Se pueden mantener los viejos para aplicaciones con menos carga de trabajo
- **Mayor productividad:** Los sistemas distribuidos suelen tener mayor rapidez ante programas con gran carga de trabajo ("divide y vencerás")