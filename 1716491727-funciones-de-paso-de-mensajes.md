---
id: 1716491727-funciones-de-paso-de-mensajes
aliases:
 - Funciones de paso de mensajes
---

#sistemas-distribuidos 

- **Send:** Mandar mensajes con la petición y un identificador de nodo (opcionalmente se pueden enviar a todos los nodos)
- **Receive:** Recibir el mensaje emitido normalmente con un buffer de recepción. Se indica un identificador del nodo que se está escuchando (también se puede hacer con todos los nodos)

## Pueden ser:

- [[1716491727-sistema-fiable|Fiables]]
- [[1716491727-sistemas-no-fiables|No fiables]]
- [[1716491727-llamada-bloqueante|Bloqueantes]]
- [[1716491727-llamada-no-bloqueante|No bloqueante]]