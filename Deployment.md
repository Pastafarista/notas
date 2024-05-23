#sistemas-distribuidos 

- Representan los despliegues de aplicaciones
- Están formados por uno o más [[Pod|pods]], ejecutándose en una o más máquinas ([[Nodos Kubernetes|nodos]])
- Ofrece un punto de entrada o de interacción con la aplicación, que puede redirigirse a alguno de los pods del sistema
- En caso de haber pods replicados, el deployment intentará balancear las peticiones entre varios [[Nodos Kubernetes|nodos]]