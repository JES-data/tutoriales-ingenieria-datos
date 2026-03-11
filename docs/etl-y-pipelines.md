---
layout: default
title: Pipelines ETL y ELT
nav_order: 2
---

# ⚙️ Pipelines ETL: El Corazón de la Ingeniería de Datos

Un pipeline de datos es el conjunto de procesos automatizados que mueven la información desde los sistemas fuente hasta donde el negocio puede tomar decisiones.

---

## 1. ¿Qué es ETL vs. ELT?
Aunque ambos términos se usan mucho, hoy en día la tendencia en la nube es **ELT**.

* **ETL (Extract, Transform, Load):** Transformamos los datos en un servidor intermedio antes de guardarlos. Ideal para cuando necesitamos anonimizar o limpiar datos pesados antes de que entren al almacén.
* **ELT (Extract, Load, Transform):** Cargamos los datos crudos (*raw*) al Data Lake y luego usamos la potencia de cómputo del Data Warehouse (ej. Synapse, Snowflake, Databricks) para transformarlos. **Es el estándar moderno**.

---

## 2. Los 3 Pilares del Pipeline

### 📥 1. Extracción (Extract)
Es el arte de conectarse a sistemas heterogéneos:
* APIs REST / Webhooks.
* Bases de datos SQL (Transaccionales).
* Logs de servidores.
* Archivos planos (CSV, JSON, Parquet).

### 🧹 2. Transformación (Transform)
Aquí ocurre la "magia" del valor de negocio:
* **Limpieza:** Eliminar duplicados y manejar valores nulos.
* **Validación:** Asegurar que los tipos de datos sean correctos.
* **Enriquecimiento:** Unir datos de diferentes fuentes para crear una visión 360°.

### 📦 3. Carga (Load)
Es el destino final donde la información se vuelve accesible para BI (Power BI, Tableau) o modelos de ML.

---

## 🛠️ Herramientas que utilizo
Para automatizar esto de forma escalable, prefiero herramientas que permitan el **código como infraestructura**:

* **Azure Data Factory (ADF):** Orquestación visual y robusta.
* **Python/PySpark:** Para transformaciones complejas a gran escala.
* **dbt (Data Build Tool):** La herramienta que está revolucionando la capa de transformación SQL.

---

## 💡 ¿Cómo optimizo un Pipeline?
Como ingeniero, no solo hago que funcione, hago que sea **eficiente**:
1.  **Monitoreo:** Implemento alertas ante fallos de carga.
2.  **Idempotencia:** Aseguro que si un proceso falla y lo reintento, los datos no se dupliquen.
3.  **Particionamiento:** Optimizo el almacenamiento para que las consultas sean rápidas y baratas.

---

## 🚀 ¿Necesitas automatizar tus datos?
Los pipelines ineficientes son una fuga de dinero. Si buscas optimizar tu arquitectura de datos, **[hablemos en LinkedIn](tu-enlace-a-linkedin)**.
