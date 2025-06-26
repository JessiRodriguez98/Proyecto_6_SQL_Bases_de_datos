# Proyecto_6_SQL_Bases_de_datos
# Proyecto QA – Análisis de logs y base de datos en Urban.Taxi

Este proyecto se enfoca en dos tareas clave como QA Engineer:

1. Análisis de logs del servidor usando comandos de consola (trabajado en **Cygwin**).
2. Consultas en **SQL** para validar integridad de datos en una base de datos PostgreSQL sobre los viajes de la aplicación **Urban.Taxi**.

Ambas actividades permiten detectar errores operativos y verificar que los datos coincidan con las reglas de negocio.

---

## 🎯 Objetivo del Proyecto

- Analizar registros de log (logs) de errores del sistema desde la terminal.
- Realizar búsquedas, filtrado y clasificación de información mediante comandos Bash.
- Realizar consultas SQL a una base de datos para validar información crítica.
- Documentar todos los hallazgos y comandos en un solo documento en Word.

---

## 📁 Archivos incluidos en el repositorio
  
  Documento que contiene:
  - Todos los comandos Bash usados para análisis de logs.
  - Resultados obtenidos desde la consola.
  - Consultas SQL ejecutadas sobre la base de datos.
  - Tablas resultantes exportadas.
  - Resumen de hallazgos y posibles errores.

---

## 🧪 Parte 1: Análisis de logs (consola Bash - Cygwin)

### 🔍 Ejercicio 1: Filtrar solicitudes desde una IP específica

- Se buscó en los logs todas las solicitudes provenientes de IPs que comienzan con `233.201`.
- Se usaron comandos Bash para navegar, filtrar y extraer la información relevante.
- Se incluyeron ejemplos reales de líneas de log.

### 📁 Ejercicio 2: Clasificación de logs por tipo de error

- Se creó una estructura de carpetas (`bug1/events`) para guardar registros con errores 400 y 500 ocurridos el `30/12/2019`.
- Se extrajeron las líneas de log usando comandos `grep` y redirección `>>`.
- Se clasificaron los logs en dos archivos separados: `400.txt` y `500.txt`.

---

## 🗃️ Parte 2: Consultas SQL sobre base de datos

Base de datos utilizada: `chicago_taxi`  
Acceso remoto con:
- Usuario: `morty`  
- Contraseña: `smith`

### 🚖 Ejercicio 1: Contar total de automóviles registrados

- Se utilizó una consulta SQL con `COUNT(*)` sobre la tabla `cabs`.
- Objetivo: verificar si el número de taxis cubre la demanda planificada (10,550 vehículos).

### 🚕 Ejercicio 2: Compañías con menos de 100 automóviles

- Se realizó un agrupamiento por compañía (`GROUP BY`) y filtrado usando `HAVING`.
- Se retornaron solo las compañías con menos de 100 taxis registrados.

### 🌦️ Ejercicio 3: Clasificar el clima según condiciones

- Se consultó la tabla `weather_records` usando `CASE` para clasificar cada hora como:
  - `Good` si el clima era favorable.
  - `Bad` si había "rain" o "storm".
- Se limitó el periodo al 5 y 6 de noviembre de 2017.

### 📊 Ejercicio 4: Cantidad de viajes por compañía

- Se unieron las tablas `cabs` y `trips` para obtener la cantidad de viajes por compañía.
- Se filtraron los viajes por fechas específicas (15 y 16 de noviembre de 2017).
- Se ordenaron los resultados en orden descendente por cantidad de viajes (`trips_amount`).

---

## 🧰 Herramientas utilizadas

- **Cygwin**: Emulador de consola tipo UNIX para Windows.
- **PostgreSQL**: Base de datos consultada mediante consola SQL.
- **Microsoft Word**: Documento final entregado con toda la información integrada.
- **grep, mkdir, cat, echo, >, >>**: Comandos Bash usados para filtrar y manipular archivos de logs.

---

## 💼 Rol desempeñado

- Análisis de archivos de log en entorno de consola.
- Manipulación y clasificación de archivos mediante línea de comandos.
- Consulta de base de datos con SQL para identificar inconsistencias o posibles errores.
- Documentación clara y profesional del proceso y resultados.

---

## ✅ Estado del proyecto

✔️ Proyecto finalizado:  
Todas las tareas fueron ejecutadas con éxito y documentadas en el archivo `.docx`, incluyendo evidencias, comandos, resultados de consola y consultas SQL completas.

---

