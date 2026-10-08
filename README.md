# 🏠 Real Estate Analytics | De datos inmobiliarios a decisiones comerciales

**Business Intelligence | Power BI · Power Query · DAX · Análisis de Ventas · Cohortes**

## 1. 📊 Contexto y problema de negocio

El sector inmobiliario requiere analizar constantemente el desempeño de sus operaciones comerciales para identificar oportunidades de crecimiento y mejorar la toma de decisiones.

Una empresa inmobiliaria puede disponer de información sobre ventas, propiedades, clientes y comisiones, pero cuando los datos se encuentran distribuidos en diferentes tablas resulta difícil obtener una visión integral del negocio.

El desafío de este proyecto consistió en transformar información transaccional de operaciones inmobiliarias en una solución de Business Intelligence que permitiera evaluar el rendimiento comercial desde diferentes perspectivas.

### Preguntas de negocio

- ¿Cuántos ingresos generan las operaciones inmobiliarias?
- ¿Cuántas propiedades se venden durante el período analizado?
- ¿Cuánto dinero se genera en comisiones?
- ¿Qué tipos de propiedades presentan mayor participación en las ventas?
- ¿Qué canales comerciales concentran las operaciones?
- ¿Cómo evolucionan las ventas respecto a períodos anteriores?
- ¿Qué diferencias existen entre segmentos de compradores?
- ¿Cómo se comportan las cohortes de clientes?

**Problema central:** convertir registros de operaciones inmobiliarias en indicadores comerciales claros y herramientas interactivas que permitan comprender el desempeño del negocio.

---

## 2. 🎯 Objetivo y estrategia de análisis

El objetivo fue desarrollar un reporte interactivo en Power BI que permitiera analizar las ventas inmobiliarias, los ingresos, las comisiones y los patrones comerciales mediante indicadores y visualizaciones.

Organicé la solución en cinco etapas:

1. **Preparación:** revisar y organizar las fuentes de información.
2. **Modelado:** relacionar los registros de ventas con las dimensiones de propiedades, clientes y fechas.
3. **Indicadores:** construir medidas DAX para evaluar el desempeño comercial.
4. **Visualización:** desarrollar páginas orientadas a la supervisión ejecutiva y el análisis detallado.
5. **Análisis de cohortes:** incorporar una perspectiva temporal del comportamiento de los clientes.

La estrategia consistió en diseñar una herramienta capaz de responder preguntas generales de negocio y permitir investigaciones más específicas mediante filtros y visualizaciones.

---

## 3. 🧰 Tecnologías utilizadas

| Herramienta | Aplicación |
|---|---|
| Power BI Desktop | Construcción del reporte interactivo |
| Power Query | Preparación y transformación de información |
| DAX | Medidas e indicadores comerciales |
| Modelado de datos | Relaciones entre hechos y dimensiones |
| Inteligencia de tiempo | Comparaciones temporales y acumulados |
| Visualizaciones interactivas | Exploración de ingresos, ventas y clientes |

### Tablas principales del modelo

| Tabla | Función |
|---|---|
| `hecho_ventas_propiedades` | Registro de operaciones inmobiliarias |
| `dim_propiedades` | Características de los inmuebles |
| `dim_clientes` | Información y segmentos de compradores |
| `Dim_Fecha` | Análisis temporal de operaciones |

La organización de los datos permite estudiar las transacciones desde diferentes dimensiones comerciales.

---

## 4. 🔎 Desarrollo del proyecto

### Etapa 1. Preparación y organización de datos

**Problema:** la información inmobiliaria debía organizarse para poder calcular indicadores comerciales y realizar comparaciones entre propiedades, clientes y períodos.

Trabajé con una estructura de datos compuesta por registros de ventas y tablas descriptivas.

Entre los campos utilizados se encuentran:

- Identificadores de ventas, clientes y propiedades.
- Fechas de operación.
- Precios de venta.
- Montos de comisión.
- Tipos de propiedad.
- Canales comerciales.
- Segmentos de compradores.

**Trabajo realizado:**

- Revisión de los campos disponibles.
- Organización de variables numéricas, temporales y categóricas.
- Preparación de las tablas para el modelo.
- Incorporación de una dimensión de fechas.
- Selección de campos para indicadores y segmentaciones.

**Resultado:** una estructura de información preparada para construir medidas y analizar operaciones inmobiliarias desde distintas perspectivas.

### Etapa 2. Modelado de datos

**Problema:** para estudiar las ventas de manera integral era necesario relacionar la información transaccional con las características de las propiedades y de los clientes.

Se estructuró el modelo alrededor de `hecho_ventas_propiedades`, utilizando dimensiones para contextualizar las operaciones.

Esta organización permite analizar las ventas según:

- Período.
- Tipo de propiedad.
- Canal comercial.
- Segmento de comprador.

**Resultado:** un modelo que facilita la aplicación de filtros y la construcción de visualizaciones comerciales.

### Etapa 3. Desarrollo de indicadores con DAX

**Problema:** los registros individuales no ofrecían una visión inmediata del rendimiento general de la actividad inmobiliaria.

Desarrollé indicadores para resumir los resultados de las operaciones.

| Indicador | Propósito |
|---|---|
| Total de ingresos | Cuantificar el valor de las ventas |
| Cantidad total de ventas | Medir el volumen de operaciones |
| Comisión total | Evaluar las comisiones registradas |
| Ticket promedio | Calcular el valor promedio de las operaciones |
| Ventas YTD | Analizar los resultados acumulados del año |
| Ventas año anterior | Comparar contra el período anterior |
| Crecimiento YoY | Evaluar la variación interanual |
| Retención de cohorte % | Explorar la continuidad de las cohortes |

**Resultado:** un conjunto de métricas dinámicas para evaluar el comportamiento comercial, considerando distintos períodos y segmentaciones.

### Etapa 4. Dashboard Overview Ejecutivo

**Problema:** los responsables comerciales necesitan conocer rápidamente el rendimiento del negocio sin revisar todos los registros.

Diseñé una primera página con una visión general de las operaciones inmobiliarias.

**Elementos implementados:**

- Tarjeta de ingresos totales.
- Tarjeta de cantidad total de ventas.
- Tarjeta de comisiones.
- Tarjeta de ticket promedio.
- Gráfico de participación por tipo de propiedad.
- Gráfico de participación por canal de venta.
- Comparación temporal de indicadores.
- Segmentadores para explorar los resultados.

**Resultado:** una vista ejecutiva que permite identificar el volumen de ventas, el valor generado y la distribución comercial de las operaciones.

### Etapa 5. Dashboard de detalle

**Problema:** los indicadores generales permiten observar el rendimiento, pero no siempre explican los factores detrás de sus variaciones.

Desarrollé una segunda página orientada al análisis más específico de las operaciones.

Esta sección incorpora:

- Evolución temporal de las ventas.
- Comparaciones con períodos anteriores.
- Desglose por canal comercial.
- Tabla de operaciones.
- Información sobre importes y comisiones.
- Filtros temporales.

**Resultado:** una herramienta que permite investigar variaciones comerciales y consultar información con mayor nivel de detalle.

### Etapa 6. Análisis de cohortes

**Problema:** analizar únicamente el volumen de ventas no permite estudiar cómo se distribuye la actividad de los clientes a lo largo del tiempo.

Incorporé una tercera página dedicada al análisis de cohortes y segmentos.

El reporte contiene campos y medidas relacionados con:

- Mes de cohorte.
- Mes de venta.
- Segmento de comprador.
- Volumen de operaciones.
- Indicadores de clientes.
- Retención de cohorte.

La finalidad es observar el comportamiento de grupos de clientes a través del tiempo y complementar el análisis comercial.

**Resultado:** una perspectiva adicional del negocio que permite explorar patrones temporales y diferencias entre segmentos.

La interpretación de la retención requiere considerar cómo se definieron las cohortes, los clientes activos y los períodos de seguimiento.

---

## 5. 📈 Resultados y hallazgos

### Resultado 1. Consolidación del rendimiento comercial

El proyecto permite consultar ingresos, comisiones, volumen de operaciones y ticket promedio dentro de un mismo entorno.

**Valor:** facilita el seguimiento de diferentes indicadores sin necesidad de consultar tablas transaccionales de forma independiente.

### Resultado 2. Comparación entre propiedades y canales

Las visualizaciones permiten identificar qué tipos de propiedad y canales comerciales concentran una mayor participación en las operaciones.

**Valor:** ofrece una base para investigar la composición comercial y las diferencias entre segmentos del negocio.

### Resultado 3. Seguimiento temporal de las ventas

Las medidas de inteligencia de tiempo permiten comparar resultados de diferentes períodos.

**Valor:** facilita identificar variaciones comerciales y períodos que requieren mayor atención.

### Resultado 4. Análisis detallado de operaciones

La segunda página permite complementar los indicadores generales con información más específica.

**Valor:** ayuda a investigar los factores asociados a los resultados observados en el dashboard ejecutivo.

### Resultado 5. Incorporación de cohortes

El reporte incluye una perspectiva de análisis temporal por grupos de clientes.

**Valor:** permite explorar la evolución de las cohortes y plantear preguntas relacionadas con la continuidad de su actividad.

### Alcance de los resultados

El reporte demuestra la construcción de una solución interactiva para analizar información comercial inmobiliaria.

No se atribuyen incrementos de ventas, reducciones de costos o mejoras en retención a la implementación del dashboard, ya que tales impactos requerirían una evaluación adicional.

---

## 6. ✅ Validación y confiabilidad del análisis

La confiabilidad de un reporte comercial depende tanto de los datos utilizados como de las medidas y relaciones del modelo.

Por ello, los principales aspectos que deben verificarse son:

| Control | Objetivo |
|---|---|
| Relaciones del modelo | Evitar duplicaciones o filtros inconsistentes |
| Total de ingresos | Conciliar los indicadores con la tabla de operaciones |
| Cantidad de ventas | Comprobar el conteo de transacciones |
| Comisiones | Verificar la agregación de los importes |
| Ticket promedio | Revisar el cálculo con el total y número de ventas |
| Inteligencia de tiempo | Comprobar la coherencia entre períodos |
| Segmentadores | Verificar las interacciones de los gráficos |
| Cohortes | Validar la definición de retención y sus denominadores |

### Evidencia técnica

El archivo `.pbix` contiene las tres páginas del reporte, los elementos visuales, sus referencias a medidas y las tablas utilizadas.

Para completar una auditoría cuantitativa es necesario verificar las expresiones DAX, sus resultados y la información de origen directamente en Power BI.

**Criterio de confiabilidad:** las conclusiones comerciales deben poder reproducirse a partir de las transacciones y sus reglas de cálculo.

---

## 7. 💡 Conclusiones y recomendaciones

El proyecto permitió desarrollar una solución de Business Intelligence para consultar información de ventas inmobiliarias desde una perspectiva ejecutiva y operativa.

La principal aportación consistió en organizar diferentes aspectos del negocio —ingresos, ventas, comisiones, propiedades, canales y clientes— en un reporte interactivo.

### Recomendaciones de negocio

**1. Monitorear los indicadores comerciales de forma periódica**

Utilizar los KPIs del Overview para identificar cambios en el rendimiento e investigar posibles desviaciones.

**2. Evaluar el desempeño de los canales de venta**

Comparar tanto el volumen de operaciones como los importes y comisiones asociados a cada canal.

**3. Investigar diferencias entre tipos de propiedad**

Identificar qué categorías presentan mayor participación comercial y analizar si esas diferencias se mantienen en distintos períodos.

**4. Profundizar en el comportamiento de los clientes**

Utilizar las cohortes y los segmentos de compradores como punto de partida para investigar continuidad de actividad y oportunidades comerciales.

**5. Fortalecer el análisis temporal**

Complementar las variaciones interanuales con comparaciones mensuales y análisis de estacionalidad cuando los datos sean suficientes.

### Valor aportado

El proyecto demuestra la capacidad de desarrollar una herramienta analítica que facilita transformar registros comerciales en información comprensible y explorable.

Desde el punto de vista técnico, se aplicaron habilidades de modelado, DAX, inteligencia de tiempo y diseño de dashboards.

Desde una perspectiva de negocio, la solución puede apoyar el seguimiento comercial y la investigación de oportunidades en el mercado inmobiliario.

---

## 8. 📁 Recursos del proyecto

**Archivo principal**

- `Proyecto sprint 11(1).pbix`

**Páginas del dashboard**

1. Overview.
2. Detalle.
3. Cohortes.

### Vista previa

*Insertar aquí una captura de cada página del dashboard.*

### Acceso al reporte

*Agregar enlace al archivo Power BI o a su publicación, si se encuentra disponible.*

---

## 👨‍💻 Autor

**Manuel Eduardo Solís Vega**

Data Analyst Jr. | Python · SQL · Power BI · Business Intelligence

Proyecto desarrollado como parte de mi portafolio profesional, enfocado en análisis inmobiliario, visualización de indicadores comerciales y toma de decisiones basada en datos.
