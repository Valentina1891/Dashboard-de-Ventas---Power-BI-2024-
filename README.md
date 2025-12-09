📊 Dashboard de Ventas – Power BI (2024)

Este proyecto es un dashboard profesional de análisis de ventas usando Power BI, diseñado como parte de un portafolio.
Incluye métricas clave, gráficos interactivos, cálculo de variaciones mensuales (MoM), márgenes y visualización geográfica.

📁 Dataset
Se usó un dataset de 1000 filas con ventas del año 2024 completo, generado especialmente para análisis avanzados:

17 productos
5 categorías
4 sucursales
Cantidades reales
Precios y costos basados en productos
Estacionalidad mensual

Archivo:
/dataset/ventas.xlsx

🧠 KPIs incluidos

Ventas Totales
Margen Bruto (%)
Margen de Ganancia
Variación Mensual (MoM %)
Unidades Vendidas

📈 Gráficos principales
Ventas por Categoría
Margen por Categoría
Tendencia de Ventas por Mes
Distribución Geográfica de Sucursales
Ranking de Productos por Ventas y Margen

🛠 DAX Usado
Venta Total
Venta Total =
SUMX(ventas, ventas[Cantidad] * ventas[PrecioUnitario])

Venta Mes Anterior
Venta Mes Anterior =
CALCULATE([Venta Total], DATEADD(ventas[Fecha], -1, MONTH))

Variación MoM %
Variación MoM % =
VAR mesActual = [Venta Total]
VAR mesAnterior = [Venta Mes Anterior]
RETURN DIVIDE(mesActual - mesAnterior, mesAnterior)

🧰 Tecnologías usadas

Power BI Desktop
DAX
Modelamiento de datos
Python (para generar dataset)

📸 Capturas del dashboard
Vista completa
/imagenes/Vista completa.png
KPIs

Categorías

Tendencia

Mapa

👨‍💻 Autor

Valentina Valdivia
Power BI · SQL · Data Analytics
Chile 🇨🇱