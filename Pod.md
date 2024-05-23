#sistemas-distribuidos 

- Unidades de despliegue de aplicaciones en [[Kubernetes]]
- Consiste en un grupo de uno o más [[Container|contenedores]], que permiten compartir recursos en red
- Lo ideal es un contenedor por pod, pero en algunos casos se pueden unir varios contenedores para tener una aplicación más grande
- Los pods son volátiles, se crean bajo demanda. Esto significa que realizan su función y se destruyen