# Unidad 1 - Introducción a Desarrollo de Productos de Datos 

```{image} _static/images/banner_unidad1.jpg
:alt: Banner Unidad 1 — Ilustración conceptual de datos transformándose en productos digitales (dashboards, reportes, APIs)
:class: bg-light
:width: 100%
```

## Presentación de la unidad

Antes de construir un producto de datos, necesitamos hablar el mismo idioma. Esta unidad sienta las bases: desde manipular datos con Python, pasando por limpiarlos y visualizarlos, hasta generar reportes que se producen solos.

La idea es simple — si un analista repite el mismo informe cada semana, ese proceso debería ser código, no trabajo manual.

---

## ¿Qué es un producto de datos?

```{image} _static/images/que_es_producto_datos.jpg
:alt: Diagrama que muestra la diferencia entre un análisis ad-hoc y un producto de datos (fiable, reutilizable, autoservicio)
:width: 80%
:align: center
```

Un producto de datos es cualquier solución basada en datos que entrega valor de forma **repetible** y **autoservicio** a un consumidor — ya sea una persona, otro sistema o un proceso de negocio. A diferencia de un análisis puntual que responde una pregunta y se archiva, un producto de datos está diseñado para vivir en producción: se actualiza, se mantiene y escala.

Algunos ejemplos concretos:

- Un **dashboard** que muestra en tiempo real las ventas por región.
- Un **reporte automatizado** que llega cada lunes al correo del gerente.
- Una **API** que devuelve predicciones de demanda a un sistema ERP.
- Una **aplicación web** donde el equipo de marketing segmenta clientes sin escribir código.

Durante esta unidad construiremos las habilidades fundamentales para llegar a esos productos.

---

## Subsección 1.1 — Python para datos

```{image} _static/images/python_logo.webp
:alt: Logo de Python
:width: 30%
:align: center
```

### ¿Por qué empezar aquí?

Todo producto de datos tiene código detrás. No necesitamos ser expertos en ingeniería de software, pero sí necesitamos manejar con soltura las estructuras fundamentales para poder automatizar, transformar y presentar datos.

### Temas que revisaremos

::::{grid} 1 1 2 2
:gutter: 3

:::{grid-item-card} Estructuras de datos
:class-header: bg-light

Listas, diccionarios, tuplas, sets. Cómo elegir la estructura correcta según el problema.
:::

:::{grid-item-card} Pandas y DataFrames
:class-header: bg-light

Creación, indexación, filtrado, agrupación, joins y transformaciones con `pandas`.
:::

:::{grid-item-card} Funciones y modularidad
:class-header: bg-light

Escribir código reutilizable: funciones, scripts organizados y buenas prácticas de nombrado.
:::

:::{grid-item-card} Lectura y escritura de archivos
:class-header: bg-light

CSV, Excel, JSON, bases de datos. Conectarse a las fuentes de datos más comunes.
:::

::::

### Herramientas que usaremos

| Herramienta | Uso principal |
|---|---|
| **Jupyter Notebook / Lab** | Exploración y prototipado rápido |
| **VS Code** | Desarrollo de scripts y proyectos |
| **Git / GitHub** | Control de versiones y colaboración |
| **pandas** | Manipulación y limpieza de datos |

```{admonition} Nota
:class: tip
Python será el lenguaje base de todo el curso. Lo usaremos de forma consistente desde la exploración hasta el despliegue en producción.
```

---

## Subsección 1.2 — Limpieza y normalización de datos

```{image} _static/images/limpieza_datos.jpg
:alt: Diagrama que muestra datos sucios a la izquierda (nulos, duplicados, atípicos) y datos limpios a la derecha en un DataFrame ordenado
:width: 80%
:align: center
```

### ¿Por qué importa?

Un producto de datos es tan bueno como los datos que consume. Si la fuente tiene valores faltantes, registros duplicados o valores atípicos sin tratar, cualquier dashboard, reporte o modelo que construyamos sobre esos datos será poco fiable.

### Temas que abordaremos

::::{grid} 1 1 2 2
:gutter: 3

:::{grid-item-card} Valores nulos
:class-header: bg-light

Detección, estrategias de imputación (media, mediana, moda, interpolación) y cuándo eliminar registros.
:::

:::{grid-item-card} Duplicados
:class-header: bg-light

Identificación de registros repetidos, criterios para deduplicación, `drop_duplicates` y sus parámetros.
:::

:::{grid-item-card} Valores atípicos
:class-header: bg-light

Detección con IQR, z-score y visualización. Decisión de corregir, transformar o conservar.
:::

:::{grid-item-card} Normalización y encoding
:class-header: bg-light

Min-max scaling, z-score, encoding de variables categóricas (one-hot, label encoding, ordinal).
:::

::::

```{admonition} En la práctica
:class: tip
La limpieza no es un paso que se hace una vez — en un producto de datos, se automatiza como parte del pipeline. Lo que aprendamos aquí lo reutilizaremos en la Unidad 4 cuando construyamos pipelines ETL.
```

---

## Subsección 1.3 — Visualización de datos

```{image} _static/images/visualizacion_datos.jpg
:alt: Collage con ejemplos de gráficos: barras, dispersión, heatmap, líneas de tiempo, creados con Matplotlib, Seaborn y Plotly
:width: 80%
:align: center
```

### El rol de la visualización

Visualizar no es decorar — es la herramienta más rápida para encontrar patrones, detectar problemas y comunicar hallazgos. En un producto de datos, las visualizaciones son la interfaz entre los datos y el usuario final.

### Librerías que usaremos

::::{grid} 1 1 3 3
:gutter: 3

:::{grid-item-card} Matplotlib
:class-header: bg-light

La base. Control total sobre ejes, colores, anotaciones. Ideal para gráficos personalizados y publicaciones.
:::

:::{grid-item-card} Seaborn
:class-header: bg-light

Gráficos estadísticos con una línea de código: distribuciones, correlaciones, heatmaps, boxplots.
:::

:::{grid-item-card} Plotly
:class-header: bg-light

Gráficos interactivos para dashboards y reportes web. Zoom, hover, filtros dinámicos.
:::

::::

### Tipos de gráficos por objetivo

| Objetivo | Gráfico recomendado |
|---|---|
| Comparar categorías | Barras, barras agrupadas |
| Ver distribución | Histograma, boxplot, violín |
| Relación entre variables | Dispersión, heatmap de correlación |
| Evolución temporal | Líneas, áreas |
| Composición | Torta (con mesura), barras apiladas |

```{admonition} Criterio clave
:class: warning
Elegir el gráfico correcto importa más que hacerlo bonito. Un gráfico mal elegido confunde; uno bien elegido explica sin necesidad de texto.
```

---

## Subsección 1.4 — Reportes automáticos

```{image} _static/images/reporte_automatico.jpg
:alt: Flujo que muestra datos entrando, un script procesándolos y un reporte PDF/HTML generándose automáticamente
:width: 80%
:align: center
```

### El problema que resolvemos

En muchas organizaciones, generar un reporte semanal implica:

1. Abrir Excel, copiar datos de varias fuentes.
2. Actualizar tablas y gráficos manualmente.
3. Formatear, exportar a PDF y enviar por correo.

Ese proceso es frágil, lento y propenso a errores. Un **reporte automatizado** reemplaza esos pasos con un script que se ejecuta solo y entrega el resultado listo para consumir.

### ¿Qué vamos a construir?

::::{grid} 1 1 2 2
:gutter: 3

:::{grid-item-card} Reportes con Jupyter + Papermill
:class-header: bg-light

Parametrizar notebooks para que se ejecuten con distintos datos de entrada y generen reportes HTML o PDF.
:::

:::{grid-item-card} Reportes con Jinja2 + HTML/PDF
:class-header: bg-light

Plantillas dinámicas que combinan datos y visualizaciones para generar reportes en HTML o PDF con `weasyprint`.
:::

:::{grid-item-card} Automatización del flujo
:class-header: bg-light

Ejecutar reportes de forma programada: scripts con `cron`, tareas programadas o pipelines simples.
:::

:::{grid-item-card} Distribución
:class-header: bg-light

Enviar el resultado por correo, subirlo a un servidor o publicarlo como página web estática.
:::

::::

### Flujo típico de un reporte automatizado

```{image} _static/images/flujo_reporte.jpg
:alt: Diagrama de flujo horizontal — (1) Fuente de datos → (2) Script de extracción → (3) Transformación y análisis → (4) Renderizado del reporte → (5) Distribución (correo, web, storage)
:width: 100%
:align: center
```

```{admonition} Resultado esperado
:class: note
Al finalizar esta unidad, cada estudiante habrá construido un reporte automatizado que toma datos de una fuente, genera visualizaciones y se exporta en formato HTML o PDF sin intervención manual.
```

---

## Recursos de la unidad

::::{grid} 1 1 2 2
:gutter: 3

:::{grid-item-card} 📓 Notebook 1.1
:link: notebooks/U1_S1_python_datos
:link-type: doc
:class-header: bg-light

Python para datos — Pandas y DataFrames
:::

:::{grid-item-card} 📓 Notebook 1.2
:link: notebooks/U1_S2_limpieza_normalizacion
:link-type: doc
:class-header: bg-light

Limpieza y normalización de datos
:::

:::{grid-item-card} 📓 Notebook 1.3
:link: notebooks/U1_S3_visualizacion
:link-type: doc
:class-header: bg-light

Visualización con Matplotlib, Seaborn y Plotly
:::

:::{grid-item-card} 📓 Notebook 1.4
:link: notebooks/U1_S4_reportes_automaticos
:link-type: doc
:class-header: bg-light

Primer reporte automatizado
:::

::::
