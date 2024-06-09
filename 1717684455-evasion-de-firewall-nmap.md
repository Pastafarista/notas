---
id: 1717684455-evasion-de-firewall-con-nmap
aliases:
  - Evasión de firewall con nmap
tags:
  - linux
---

# Evasión de firewall con nmap

Podemos aplicar distintas técnica con la herramienta [[1717682023-RIJF|nmap]] para evadir un firewall:

- El parámetro `-f` fragmenta los paquetes, lo que puede ayudar a evadir los firewalls. Se le puede pasar un tamaño de fragmento con `--mtu` (poniendole numeros múltiplos de 8). Si se le pone un tamaño de fragmento más pequeño que el que soporta el firewall, este no podrá reensamblar los paquetes y no podrá filtrarlos, y por consecuente podremos evadirlo.

- El parámetro `-D` crea paquetes decoys con ips inventadas para confundir al firewall. Puede ser util para evadir firewalls que solo dejan pasar una ip específica. También puede funcionar para anonimizar el origen del ataque.

- También se puede especificar el source port con `--source-port` para evadir firewalls que filtran por puerto origen.

- Algunos firewalls tienen una lista negra de tamaños de paquetes reliacionados con herramientas de ataque, por lo que se puede evadir con `--data-length` para especificar un tamaño falso de paquete.

- También se puede falsificar la dirección MAC con `--spoof-mac` para evadir firewalls que filtran por MAC.

- Podemos hacer también un escaneo sigiloso con `-sS` para hacer un escaneo más sigiloso y rápido. Esto puede ser útil para evadir firewalls que detectan escaneos de nmap. En vez de hacer el three-way handshake, nmap manda un paquete SYN y espera a que el servidor responda con un SYN/ACK. Después en vez de responder con un ACK, manda un RST para cerrar la conexión. Algunos servidores no registran este tipo de escaneo.

- Con `--min-rate` se puede especificar el mínimo de paquetes por segundo que se enviarán. Esto puede hacer que el escaneo sea más rápido y menos detectable. Un buen número de min-rate es 5000.
