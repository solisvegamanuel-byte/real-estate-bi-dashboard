# Dashboard de Análisis Comercial Inmobiliario - Andes Capital Real Estate

Este proyecto consiste en el desarrollo de un **dashboard interactivo de Business Intelligence (Power BI / Tableau)** diseñado para la empresa inmobiliaria *Andes Capital Real Estate*. 

El objetivo es transformar la información transaccional dispersa en un **modelo de datos multidimensional en esquema estrella**, permitiendo evaluar el desempeño comercial, la rentabilidad por tipo de propiedad y canal de venta, la evolución temporal de los ingresos y el comportamiento de recurrencia de los clientes a través de un análisis de cohortes.

---

## 💡 Preguntas de Negocio

El panel ejecutivo y analítico responde a las siguientes cuestiones clave:
1. **¿Cuál es el ingreso total generado por las ventas de propiedades y el volumen de comisiones cobradas?**
2. **¿Qué tipos de propiedad (Residencial, Comercial, etc.) representan la mayor fuente de ingresos?**
3. **¿Qué segmentos de clientes (Primera vez, Inversionista, etc.) generan el mayor volumen de compras?**
4. **¿Cómo evolucionan las ventas en el tiempo y cuál es el crecimiento año contra año (*Year-over-Year - YoY*)?**
5. **¿Existe recurrencia de compra en los clientes tras su primera transacción?** (Análisis de Cohortes).

---

## 📐 Modelo de Datos (Esquema Estrella)

El proyecto estructura la información en un modelo analítico optimizado relacionando tablas de hechos y dimensiones:

* **`hecho_ventas_propiedades` (Tabla de Hechos):** Registra cada transacción (`id_venta`, `fecha_venta`, `precio_venta`, `porcentaje_comision`, `monto_comision`, `canal_venta`).
* **`dim_clientes` (Dimensión):** Información demográfica y perfil del comprador (`id_cliente`, `segmento_comprador`, `pais`, `ciudad`).
* **`dim_propiedades` (Dimensión):** Características de los inmuebles (`id_propiedad`, `tipo_propiedad`, `barrio`, `habitaciones`, `tamano_m2`, `precio_publicado`, `categoria_propiedad`).
* **`dim_fecha` (Dimensión Calendario):** Creada para habilitar Inteligencia de Tiempo (`Date`, `Año`, `Mes`, `Mes Numero`, `Año-Mes`).

---

## 📊 Medidas e Inteligencia de Tiempo (DAX / Cálculos BI)

Se implementaron métricas analíticas avanzadas para el seguimiento del negocio:
* **Métricas Principales:** Ingresos Totales, Monto Total de Comisiones, Promedio de Precio por $m^2$, Ticket Promedio de Venta.
* **Inteligencia de Tiempo:** Ventas Acumuladas (*YTD* / *MTD*), Ventas del Año Anterior (*PY*), Crecimiento Absoluto y Porcentual YoY ($YoY\%$).
* **Análisis de Cohortes:** Retención y tasa de recompra de clientes agrupados por mes de primera adquisición.

---

## 🛠️ Herramientas y Tecnologías

* **Herramienta de BI:** Power BI / Tableau Desktop
* **Modelado de Datos:** Esquema Estrella / DAX
* **Procesamiento previo:** Python (Pandas) / Jupyter Notebook
* **Visualizaciones:** Indicadores KPI, Gráficos de Líneas (Tendencias), Gráficos de Barras (Segmentaciones) y Tablas Matriciales (Cohortes).

---

## 🚀 Estructura del Repositorio

```text
.
├── datasets/
│   ├── hecho_ventas_propiedades.csv   # Registros transaccionales de ventas
│   ├── dim_clientes.csv               # Dimensión de clientes
│   └── dim_propiedades.csv            # Dimensión de propiedades
├── notebook_preparacion_datos.ipynb   # Guía y validaciones previas en Python
├── dashboard_inmobiliario.pbix        # Archivo de Power BI (o enlace a Tableau Public)
└── README.md                          # Documentación del proyecto
