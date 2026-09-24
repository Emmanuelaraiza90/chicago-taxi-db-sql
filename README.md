# 🚖 Chicago Taxi Database Analysis & Server Log Management

![QA](https://img.shields.io/badge/QA-DATABASE_TESTING-blue?style=for-the-badge) ![SQL](https://img.shields.io/badge/SQL-POSTGRESQL-blue?style=for-the-badge) ![CLI](https://img.shields.io/badge/CLI-BASH_&_LINUX-blue?style=for-the-badge) ![STATUS](https://img.shields.io/badge/STATUS-COMPLETED-green?style=for-the-badge)

Este repositorio contiene la evidencia técnica del Sprint 7 (TripleTen QA Engineering), enfocado en la manipulación de bases de datos relacionales y la gestión de registros de servidor (logs) a través de la línea de comandos. El proyecto simula un entorno real de resolución de problemas para una aplicación de viajes en taxi en Chicago, cruzando datos de viajes con condiciones meteorológicas e investigando fallos en el servidor.

---

## 🎯 Objetivo del Proyecto

Garantizar la integridad de los datos almacenados en el backend y diagnosticar incidentes de servidor. Esto se logró aislando errores críticos HTTP (400/500) en la terminal de Linux y ejecutando consultas SQL avanzadas para correlacionar la disponibilidad de la flota de taxis con las condiciones meteorológicas.

---

## 🛠️ Herramientas y Entorno

* **Bases de Datos:** PostgreSQL, SQL (DML / DDL).
* **Consola (CLI):** Bash, manipulación de directorios y filtrado avanzado de texto.
* **Técnicas de Consulta:** `INNER JOIN`, Funciones de Agregación, `GROUP BY`, `HAVING`, `CASE/WHEN`.
* **Entorno:** Servidor Remoto (TripleTen).

---

## 📊 Resumen de Ejecución y Pruebas

| Artefacto / Tarea | Detalle Técnico |
| :--- | :--- |
| **Análisis de Logs (CLI)** | Aislamiento de errores HTTP 400 y 500 mediante `grep` y filtrado por IP (`233.201`). |
| **Volumetría de Datos** | Detección de compañías con baja disponibilidad de flota (menos de 100 vehículos) usando `HAVING`. |
| **Correlación de Negocio** | Uso de `CASE/WHEN` para clasificar clima (Good/Bad) buscando métricas de "rain" o "storm". |
| **Cruces Complejos (SQL)** | Ejecución de `INNER JOIN` entre tablas `cabs` y `trips` para extraer métricas de Noviembre 2017. |

---

## 🚀 Desafíos Técnicos Resueltos

**1. Gestión y Análisis de Logs del Servidor (CLI)**
* Navegación y creación de estructuras de directorios en servidor remoto para el aislamiento de errores (`mkdir bug1/events`).
* Uso de expresiones regulares para aislar peticiones HTTP específicas y segmentación de logs masivos para separar transacciones exitosas de errores críticos en archivos independientes.

**2. Análisis Relacional de Datos (SQL)**
* **Agrupación y Filtrado Avanzado:** Uso de `COUNT`, `GROUP BY` y el operador `HAVING` para análisis de capacidad.
* **Uniones Complejas:** Ejecución de `INNER JOIN` para calcular el volumen total de viajes procesados por compañía durante ventanas de tiempo específicas.

---

## 📸 Evidencia Visual de Ejecución

**Gestión de Servidor y Aislamiento de Logs (Consola Bash):**
![Logs Bash](chicago-taxi-db-sqlCaptura%20de%20pantalla%202026-09-23%20a%20la(s)%2018.10.58.jpg)

**Estructuración de Consultas SQL Avanzadas (JOINs & Funciones de Agregación):**
![SQL Query](chicago-taxi-db-sqlCaptura%20de%20pantalla%202026-09-23%20a%20la(s)%2018.25.52.jpg)

**Resultados de Persistencia y Volumetría en Base de Datos:**
![SQL Results](chicago-taxi-db-sqlCaptura%20de%20pantalla%202026-09-23%20a%20la(s)%2018.24.38.jpg)

---

## ✍️ Autor

**Jehova Emmanuel González Araiza**
*QA Automation Engineer | Industrial Engineer*

* [LinkedIn](https://linkedin.com/in/emmanuel-araiza-engineer)
* [GitHub](https://github.com/Emmanuelaraiza90)
