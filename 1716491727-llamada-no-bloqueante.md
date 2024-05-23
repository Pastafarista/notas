---
id: 1716491727-llamada-no-bloqueante
aliases:
 - Llamada no bloqueante
---

#sistemas-distribuidos 

- Las llamadas no bloqueantes devuelven el control a la [[1716491727-funciones-de-paso-de-mensajes|función]] tan pronto como sea posible (el mensaje ha sido puesto en cola de envío)
- Normalmente se usa una variable que indica el estado de la llamada (terminada/no terminada)
- También se suele usar un buffer de datos de envío/recepción los cuales se pueden reutilizar siempre que no se indique que la llamada a terminado
- Las llamadas bloqueantes solapan los tiempos de comunicación:
	- En las bloqueantes el [[1716491727-cliente|Cliente]] envía el mensaje y se mantiene parado hasta que el [[1716491727-servidor|Servidor]] envíe el resultado
	- En las no bloqueantes el cliente obtiene un "recibo", que se consultará cuando se requiera el resultado de la llamada anterior. Mientras que ese recibo no indique que tenemos respuesta el cliente seguirá trabajando
