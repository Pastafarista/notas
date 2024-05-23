#sistemas-distribuidos 

- Es una herramienta de código abierto diseñada para facilitar el despliegue de contenidos y servicios
- Se basa en el uso de [[Container|contenedores]] que aíslan las aplicaciones

## Características

- **Descubrimiento de servicios:** las aplicaciones se anuncian usando su IP o un DNS
- **Balanceo de carga**
- **Manipulación y configuración de almacenamiento:** permite montar un sistema de almacenamiento bajo demanda (discos duros o remotos)
- **Vuelta atrás a estados anteriores**
- **Empaquetado automático de contenedores:** automáticamente se le asignan cuanta CPU y RAM usan los contenedores (se puede especificar)
- **Autoreparado:** detecta contenedores que estén fallando, se paran y se reinician automáticamente
- **Accesos seguros:** gestión de contraseñas y accesos seguros para las aplicaciones que se vayan a distribuir

## Estructura

- [[Container]]
- [[Docker runtime]]
- [[Pod|Pods]]
- [[Deployment|Deployments]]
- [[Nodos Kubernetes|Nodos]]

## Capa de red: Proveedores CNI

- Para conectar las instancias de [[Docker runtime|docker]] entre los distintos [[Pod|pods]]/[[Nodos Kubernetes|nodos]] es necesario un programa externo:
	- Weave: flexibilidad en el uso de red
	- Flannel: facilidad de uso, muy popular 
	- Calico: Centrado en la eficiencia de comunicaciones
	- Canal