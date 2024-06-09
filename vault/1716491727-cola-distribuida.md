---
id: 1716491727-cola-distribuida
aliases:
 - Cola distribuida
---

#sistemas-distribuidos 

- Los mensajes se reciben en el mismo orden en el que se enviaron. Funciona como un FIFO
- Cada nodo contiene un proceso que realizará los recursos en [[1716491727-exclusin-mutua|Exclusión mutua]] (árbitro)
- La red está completamente conectada, cualquier nodo puede [[1716491727-paso-de-mensajes|enviar mensajes]] a otros nodos de la red
- Todos los nodos mantienen un vector del estado del recurso compartido:
	1. El proceso $P$ necesita acceder al recurso compartido, así que el nodo local actualiza su vector local.
	2. El nodo local envía un mensaje al resto de nodos para que también actualicen sus vectores
	3. Cuando el proceso $P$ se va a desencolar, accede a la zona de exclusión mutua 
	4. También envía un mensaje al resto de nodos para que saquen al proceso del vector
	5. El resto de procesos reciben el mensaje y comprueban si es el turno para acceder a la sección crítica