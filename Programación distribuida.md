#sistemas-distribuidos 

Cuando programamos en [[Multicomputador|sistemas distribuidos]] se nos presentan nuevos problemas:

- No hay direcciones de memoria (comunicación de procesos mediante  paso de mensajes)
- Gestión de recursos:
	- Cada nodo debe tener capacidad de auto-gestión
	- Deben estar sincronizados (maestro/esclavo)
- Interfaz de usuarios con esquema [[Aplicaciones cliente-servidor|cliente/servidor]]

Para que todo funcione bien el [[DDP|sistema operativo distribuido]] debe proporcionar las siguientes **funciones de soporte**:

- Software de intercambio de datos
- Tener alta disponibilidad
- Capacidad de gestión de procesos en entornos distribuidos

Además en seguridad debe cumplir:

- Protección de datos y recursos privados
- Garantía de autenticidad de usuarios
- Sistemas de criptografía y seguridad para el intercambio de información