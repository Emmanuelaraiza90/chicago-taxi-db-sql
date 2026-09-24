# 🚖 Chicago Taxi Database Analysis & Server Log Management

Este repositorio contiene la evidencia técnica del Sprint 7 (TripleTen QA Engineering), enfocado en la manipulación de bases de datos relacionales y la gestión de registros de servidor (logs) a través de la línea de comandos. 

El proyecto simula un entorno real de resolución de problemas para una aplicación de viajes en taxi en Chicago, cruzando datos de viajes con condiciones meteorológicas e investigando fallos en el servidor.

## 🛠️ Tech Stack & Herramientas
* **Bases de Datos:** PostgreSQL, SQL (DML / DDL).
* **Consola (CLI):** Bash, manipulación de directorios y filtrado avanzado de texto.
* **Técnicas de Consulta:** `INNER JOIN`, Funciones de Agregación, `GROUP BY`, `HAVING`, `CASE/WHEN`.

## 🎯 Desafíos Técnicos Resueltos

### 1. Gestión y Análisis de Logs del Servidor (CLI)
* Navegación y creación de estructuras de directorios en servidor remoto para el aislamiento de errores (`mkdir bug1/events`).
* Uso de expresiones regulares y `grep` para aislar peticiones HTTP específicas por prefijo de IP (`233.201`).
* Filtrado y segmentación de logs masivos para separar transacciones exitosas de errores críticos (HTTP `400` y `500`) en archivos independientes para su posterior depuración.

### 2. Análisis Relacional de Datos (SQL)
* **Agrupación y Filtrado Avanzado:** Uso de `COUNT`, `GROUP BY` y el operador `HAVING` para identificar compañías de taxi con baja disponibilidad de flota (menos de 100 vehículos).
* **Lógica Condicional:** Implementación de sentencias `CASE` para clasificar las condiciones meteorológicas (Good/Bad) buscando dinámicamente palabras clave como "rain" o "storm" en los registros meteorológicos.
* **Uniones Complejas:** Ejecución de `INNER JOIN` entre las tablas `cabs` (vehículos) y `trips` (viajes) para calcular el volumen total de viajes procesados por compañía durante ventanas de tiempo específicas (Noviembre 2017).
