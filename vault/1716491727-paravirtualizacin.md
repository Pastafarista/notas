---
id: 1716491727-paravirtualizacin
aliases:
 - Paravirtualización
---

#sistemas-distribuidos 

- El S.O. es consciente de estar ejecutándose en un entorno virtualizado
- Se comunica con un [[1716491727-hipervisor-vmm|hipervisor]] de tipo nativo para llevar a cabo las tareas no [[1716491728-virtualizacin-de-sistemas|virtualizables]]
- El hipervisor dialoga con el hardware para realizar los procesos
- **Ventaja:** rendimiento
- **Inconveniente:** Suele limitar el soporte a sistemas operativos libres como Linux

## Ejemplos

- VirtualBox