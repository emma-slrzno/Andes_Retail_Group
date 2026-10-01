<a id="top"></a>

# 📊 Andes Retail Group Dashboard

[![Vista previa del Dashboard · Dashboard preview](Images/Dashboard.png)](https://public.tableau.com/app/profile/emma.solorzano7415/viz/Project_17885024557020/Dashboard2)

👉 [Ver el dashboard interactivo en Tableau Public · View the interactive dashboard on Tableau Public](https://public.tableau.com/app/profile/emma.solorzano7415/viz/Project_17885024557020/Dashboard2)

**🌎 Idioma / Language:** [🇪🇸 Español](#es) · [🇬🇧 English](#en)

---

<a id="es"></a>

## 🇪🇸 Español

Dashboard de Business Intelligence en **Tableau Public** que comunica los resultados del análisis del servicio **RappiPlus** (Andes Retail Group): rentabilidad, comportamiento de ventas e inversión en marketing, a partir de datos previamente validados y limpiados en Python.

### 1. Problema o contexto de negocio

La dirección de Andes Retail Group opera RappiPlus en **México, Colombia y Argentina** y necesita un panel único y visual para monitorear la salud del negocio sin depender de revisar tablas o notebooks. Las preguntas que debe poder responder de un vistazo son:

- ¿Cuánto vendemos y cuánto ganamos realmente después de costos y marketing?
- ¿Qué productos y categorías sostienen los ingresos?
- ¿Cómo se distribuye la inversión en marketing por canal y país?

### 2. Objetivo del dashboard

Traducir el análisis en una herramienta **visual, interactiva y accesible** para perfiles no técnicos, que permita explorar los indicadores clave del negocio y apoyar decisiones de inversión, catálogo y marketing.

### 3. Dataset utilizado

Los datos provienen de tres archivos que se validaron y limpiaron en el notebook del proyecto (duplicados, nulos y consistencia de montos) y se exportaron para alimentar el dashboard:

| Archivo | Contenido |
|---------|-----------|
| `orders_clean.csv` | Pedidos limpios: fecha, país, dispositivo, fuente de referencia, producto, cantidad, precio, descuento y monto total (24,950 pedidos, enero–junio 2025) |
| `catalog_clean.csv` | Costo unitario, categoría y proveedor por producto |
| `marketing_clean.csv` | Gasto diario en marketing por país y canal |

### 4. Herramientas y tecnologías

- **Tableau Public** para la visualización y publicación del dashboard
- **Python** (`pandas`) para la limpieza y preparación de los datos
- **SQL (PostgreSQL)** para el análisis de funnel y retención que complementa el proyecto

### 5. Proceso realizado

1. **Preparación de datos:** limpieza y validación en Python, y exportación de los tres datasets limpios.
2. **Modelado:** cruce de pedidos con el catálogo (por `nombre_producto`) para calcular COGS y ganancia, y con marketing para calcular profit.
3. **Diseño del dashboard:** visualización de los KPIs de rentabilidad, ventas y marketing en Tableau.
4. **Publicación:** dashboard disponible en Tableau Public para su consulta interactiva.

### 6. Principales hallazgos

| Indicador | Valor |
|-----------|------:|
| Revenue total | $51,965,834 |
| COGS total | $43,124,018 |
| Ganancia bruta | $8,841,816 (17.0%) |
| Gasto en marketing | $2,871,844 (5.5% del revenue) |
| **Profit** | **$5,969,972** |
| **Margen neto** | **11.49%** |
| Ticket promedio | $2,082.80 |

- El negocio es **rentable, pero con márgenes ajustados**: el costo de producto absorbe ~83% de los ingresos.
- **Laptop-Gaming-16GB** concentra ~84% del revenue (~$43.4M).
- El gasto en marketing está repartido casi parejo entre **social (34.1%)**, **orgánico (33.9%)** y **búsqueda pagada (32.0%)**.

### 7. Recomendaciones e impacto para el negocio

- **Diversificar el catálogo** para reducir la dependencia de un solo producto.
- **Proteger el margen** renegociando costos con proveedores y revisando descuentos: cada punto de margen bruto equivale a ~$520K.
- **Medir el retorno por canal** cruzando el gasto de marketing con conversiones e ingresos antes de reasignar presupuesto.

### 8. Consideraciones sobre los datos

- Existen **pedidos con volúmenes muy altos** (media de 7.12 unidades por orden vs. mediana de 2) que conviene auditar, ya que inflan el revenue y el ticket promedio.
- **101 registros de marketing no tienen canal**, por lo que el desglose por canal (~$2.69M) no cubre el total invertido (~$2.87M).
- ~4.8% de los pedidos presenta diferencias entre `precio × cantidad − descuento` y el monto registrado; el impacto agregado es pequeño.

### 9. Estructura del repositorio

```
├── Images/
│   └── Dashboard.png    # Vista previa del dashboard
└── README.md            # Bilingüe (ES/EN)
```
# Contacto

- LinkedIn: https://www.linkedin.com/in/emma-solorzano-hernandez-jauregui-200301345/
- Perfil de Tableau Public: https://public.tableau.com/app/profile/emma.solorzano7415/vizzes

[⬆️ Volver arriba](#top) · [🇬🇧 Read in English](#en)

---

<a id="en"></a>

## 🇬🇧 English

Business Intelligence dashboard built in **Tableau Public** that communicates the results of the **RappiPlus** service analysis (Andes Retail Group): profitability, sales behavior, and marketing investment, based on data previously validated and cleaned in Python.

### 1. Business problem and context

Andes Retail Group's leadership runs RappiPlus in **Mexico, Colombia, and Argentina** and needs a single, visual panel to monitor business health without having to go through tables or notebooks. The questions it must answer at a glance are:

- How much do we sell, and how much do we actually earn after costs and marketing?
- Which products and categories sustain revenue?
- How is marketing investment distributed by channel and country?

### 2. Dashboard objective

Turn the analysis into a **visual, interactive, and accessible** tool for non-technical audiences, allowing them to explore the key business indicators and support investment, catalog, and marketing decisions.

### 3. Datasets

The data comes from three files that were validated and cleaned in the project notebook (duplicates, missing values, and amount consistency) and exported to feed the dashboard:

| File | Content |
|------|---------|
| `orders_clean.csv` | Clean orders: date, country, device, referral source, product, quantity, price, discount, and total amount (24,950 orders, January–June 2025) |
| `catalog_clean.csv` | Unit cost, category, and supplier per product |
| `marketing_clean.csv` | Daily marketing spend by country and channel |

### 4. Tools and technologies

- **Tableau Public** for dashboard visualization and publishing
- **Python** (`pandas`) for data cleaning and preparation
- **SQL (PostgreSQL)** for the funnel and retention analysis that complements the project

### 5. Process

1. **Data preparation:** cleaning and validation in Python, and export of the three clean datasets.
2. **Modeling:** orders joined with the catalog (by `nombre_producto`) to compute COGS and gross profit, and with marketing to compute profit.
3. **Dashboard design:** visualization of profitability, sales, and marketing KPIs in Tableau.
4. **Publishing:** dashboard available on Tableau Public for interactive exploration.

### 6. Key findings

| Metric | Value |
|--------|------:|
| Total revenue | $51,965,834 |
| Total COGS | $43,124,018 |
| Gross profit | $8,841,816 (17.0%) |
| Marketing spend | $2,871,844 (5.5% of revenue) |
| **Profit** | **$5,969,972** |
| **Net margin** | **11.49%** |
| Average ticket | $2,082.80 |

- The business is **profitable, but with tight margins**: product cost absorbs ~83% of revenue.
- **Laptop-Gaming-16GB** accounts for ~84% of revenue (~$43.4M).
- Marketing spend is split almost evenly across **social (34.1%)**, **organic (33.9%)**, and **paid search (32.0%)**.

### 7. Recommendations and business impact

- **Diversify the catalog** to reduce dependence on a single product.
- **Protect margin** by renegotiating supplier costs and reviewing discounts: each point of gross margin is worth ~$520K.
- **Measure return by channel** by crossing marketing spend with conversions and revenue before reallocating budget.

### 8. Data considerations

- There are **very high-volume orders** (average of 7.12 units per order vs. a median of 2) that should be audited, since they inflate revenue and average ticket.
- **101 marketing records have no channel**, so the channel breakdown (~$2.69M) does not cover the total invested (~$2.87M).
- ~4.8% of orders show differences between `price × quantity − discount` and the recorded amount; the aggregate impact is small.

### 9. Repository structure

```
├── Images/
│   └── Dashboard.png    # Dashboard preview
└── README.md            # Bilingual (ES/EN)
```
# Contact

- LinkedIn: https://www.linkedin.com/in/emma-solorzano-hernandez-jauregui-200301345/
- Tableau Public profile: https://public.tableau.com/app/profile/emma.solorzano7415/vizzes
  
[⬆️ Back to top](#top) · [🇪🇸 Leer en español](#es)
