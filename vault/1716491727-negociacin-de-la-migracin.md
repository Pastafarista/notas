---
id: 1716491727-negociacin-de-la-migracin
aliases:
 - Negociación de la migración
---

#sistemas-distribuidos 

- ¿Quién se queda el proceso?

Mecanismo de negociación del [[1716491727-ddp|S.O. distribuido]] Charlotte:

- Se deja la responsabilidad de migración y planificación a largo plazo a la utilidad "Starter"
- Cada proceso Starter se encarga de vigilar el estado de un grupo de máquinas dentro del sistema. 
- La decisión de migrar se toma al poner de acuerdo dos procesos Starter

Cuando están de acuerdo se realizan una serie de pasos:

1. El Starter de la máquina origen "$S$" decide que un proceso "$P$" debe migrar a una máquina destino "$D$". Primero envía un mensaje al Starter de $D$ para solicitar una transferencia
2. Si el Starter de $D$ está listo para recibir procesos, envía un mensaje positivo
3. El starter de $S$ comunica al kernel su decisión de migrar $P$ a $D$. El kernel le envía un mensaje de "oferta" a $D$ con las estadísticas de $P$, para que decida si el estado actual de $D$ puede hacerse cargo
4. Si $D$ está falto de recursos, puede rechazar la oferta. En caso contrario, le pasa un mensaje a su Starter, para que decida si acepta o rechaza el proceso
5. Si el Starter acepta a $P$, se manda un mensaje de "inmigrar" el proceso. El kernel de $D$ reenvía la petición a $S$, y reserva los recursos necesarios para recibir a $P$