# UD5.2.XPath---Catalogo-Cloud
- Nombre: Daniel Jiménez Ramírez
- Profesor: Willman Acosta
- Actividad: Auditoría de Infraestructura Cloud - AEE
# Explicacion Actividad
### Misión 1: Mapeo de Seguridad (Navegación Absoluta/Relativa)
**Objetivo:** Hacer una consulta que liste los puertos de servicios que corren solo en el servidores de París.
**Consulta:** /catalogo_cloud/centro_datos[@ubicacion="Paris"]/servidor/software/servicios/servicio/@puerto /string()
---
### Misión 2: Auditoría de Mantenimiento (Filtrado por Valores)
**Objetivo:** Hacer una consulta que devuelva la version del sistema operativo cuyo ID sea srv-db-01.
**Consulta:** /catalogo_cloud/centro_datos/servidor[@id="srv-db-01"]/software/so/@version /string()
---
### Misión 3: Inventario de Alta Capacidad (Predicados Matemáticos)
**Objetivo:** Hacer una consulta que devuelva los nodos completos con una capacidad de disco mayor o igual a 8.
**Consulta:** /catalogo_cloud/centro_datos/servidor/hardware/discos/disco[@capacidad_tb >= 8]
---
### Misión 4: Eficiencia Energética (Uso de Funciones o Índices)
**Objetivo:** Hacer una consulta que encuentre el primer servidor de la lista que esté actualmente apagado.
**Consulta:** /catalogo_cloud/centro_datos/servidor[@estado="apagado"][1]
---
### Misión 5: Desafío del Auditor Senior (Navegación Inversa / Existencia)
**Objetivo:** Hacer una consulta para saber la arquitectura de CPU de los servidores con una GPU instalada.
**Consulta:** /catalogo_cloud/centro_datos/servidor[hardware/gpu]/hardware/cpu/@arquitectura /string()
