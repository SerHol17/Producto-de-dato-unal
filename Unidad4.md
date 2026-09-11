# Unidad 4 - Infraestructura de Datos

```{image} _static/images/banner_unidad4.png
:alt: Banner Unidad 4 — Almacenamiento, pipelines y Big Data
:class: bg-light
:width: 100%
```

## Presentacion de la unidad

Hasta ahora trabajamos con archivos CSV que caben en memoria. Limpiamos, validamos, visualizamos y comunicamos. Pero un producto de datos real recibe miles de registros cada hora, de fuentes distintas, en formatos distintos. Necesitamos entender donde guardarlos, como moverlos y como procesarlos cuando pandas ya no alcanza.

Esta unidad recorre la evolucion del almacenamiento de datos desde los Data Warehouses de los 90s hasta los Lakehouses modernos, construye pipelines de datos completos en Python, e introduce PySpark para procesar datos que no caben en la memoria de una sola maquina.

---

## Que vamos a cubrir

::::{grid} 1 1 2 3
:class-container: text-center
:gutter: 3

:::{grid-item-card}
:link: notebooks/U4_S1_almacenamiento
:link-type: doc
:class-header: bg-light

**4.1 Evolucion del almacenamiento**
^^^

De Data Warehouse a Data Mesh: que problema resuelve cada generacion, cuando usar cada uno y como llegamos a donde estamos hoy. Warehouse, Lake, Lakehouse, Delta Lake, Mesh.
:::

:::{grid-item-card}
:link: notebooks/U4_S2_pipelines
:link-type: doc
:class-header: bg-light

**4.2 Data Pipelines ETL/ELT**
^^^

Mover datos de A a B no es copiar archivos. Diferencia entre ETL y ELT, orquestacion, pipeline completo en Python, scheduling con cron y scripts.
:::

:::{grid-item-card}
:link: notebooks/U4_S3_pyspark
:link-type: doc
:class-header: bg-light

**4.3 Big Data con PySpark**
^^^

Cuando pandas no escala, Spark procesa datos distribuidos en un cluster. PySpark DataFrames, transformaciones, acciones, SQL sobre datos masivos, lectura y escritura en Parquet y Delta.
:::

::::

---

## Por que importa esta unidad

```{admonition} El problema real
:class: warning
Un CSV de 500 filas cabe en memoria. Un CSV de 50 millones no. Y cuando tienes 200 fuentes que generan datos cada minuto, no puedes sentarte a correr un notebook manualmente. Necesitas infraestructura: donde almacenar, como mover y como procesar a escala.
```

El recorrido de la unidad sigue esta logica:

1. **Almacenamiento** — donde guardar los datos y en que formato, segun el caso de uso.
2. **Pipelines** — como mover datos de la fuente al destino, de forma automatica y confiable.
3. **Big Data** — como procesar datos que no caben en una sola maquina.

---

## Linea del tiempo

| Epoca | Tecnologia | Problema que resuelve |
|---|---|---|
| 1990s | Data Warehouse | Reportes de negocio sobre datos estructurados |
| 2010s | Data Lake (Hadoop) | Almacenar todo (estructurado y no) a bajo costo |
| 2015+ | Lakehouse | Combinar la flexibilidad del Lake con la estructura del Warehouse |
| 2019+ | Delta Lake | Transacciones ACID y time travel sobre archivos en un Lake |
| 2020+ | Data Mesh | Descentralizar: cada equipo es dueno de sus datos como producto |

---

## Herramientas de la unidad

| Herramienta | Subseccion | Proposito |
|---|---|---|
| Apache Spark / PySpark | 4.3 | Procesar datos a escala |
| Parquet / Delta Lake | 4.1, 4.3 | Formatos de almacenamiento eficientes |
| Python (scripts, funciones) | 4.2 | Construir pipelines ETL/ELT |
| cron / scheduling | 4.2 | Automatizar ejecucion de pipelines |

---

## Recursos de la unidad

::::{grid} 1 1 2 3
:gutter: 3

:::{grid-item-card} Notebook 4.1
:link: notebooks/U4_S1_almacenamiento
:link-type: doc
:class-header: bg-light

Evolucion del almacenamiento de datos
:::

:::{grid-item-card} Notebook 4.2
:link: notebooks/U4_S2_pipelines
:link-type: doc
:class-header: bg-light

Data Pipelines ETL/ELT
:::

:::{grid-item-card} Notebook 4.3
:link: notebooks/U4_S3_pyspark
:link-type: doc
:class-header: bg-light

Big Data con PySpark
:::

::::
