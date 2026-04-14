# DataProject-Dashboard-Analisis-de-Datos
# Análisis de Ventas (EDA) — Chocolate Sales 2023–2024
Este documento resume el análisis exploratorio de ventas (EDA) de una empresa internacional de chocolates. Incluye cómo se prepararon los datos, qué KPIs se crearon y las conclusiones principales.

## 1. Descripción del proyecto
Este proyecto analiza las ventas de una empresa internacional de chocolates usando datos de 2023 y 2024. La idea es entender qué se vende, cuándo se vende y dónde se vende, para apoyar decisiones de negocio.
Se revisa la evolución de ventas por productos, categorías y marcas, y también por tiempo (año, mes, semana y día). Además, se comparan resultados por tipo de tienda y por país para tener una visión global.
También se analiza a quién se le vende: edad, género y si el cliente está fidelizado. Esto ayuda a entender mejor los hábitos de compra y a segmentar.
Por último, se revisan ventas y beneficios a lo largo del tiempo para ver si los meses con más ventas también son los más rentables.

## 2. Estructura del proyecto
Datos
Los datos se obtienen de un dataset publicado en Kaggle  https://www.kaggle.com/ (Chocolate Sales: Complete EDA + ML Pipeline) y se guardan en el archivo Datos_originales.

### 2.1 Transformación y limpieza de datos
•	Se cargan los CSV en Excel (archivo Transformación de Datos), separando los campos por comas.
•	En la hoja Ventas, Id Pedido se usa como clave para relacionar la información del resto de hojas.
•	También se usan como identificadores: Id Producto (Productos), Id Cliente (Clientes) y Id Tienda (Tienda).
•	Se añaden columnas para traer datos de Tienda/Clientes/Productos (por ejemplo: Nombre Tienda, Ciudad, País, Tipo Tienda, Edad, Género, Miembro Fidelizado, Fecha Registro, Nombre Producto, Marca y Categoría) usando BuscarX.
•	Se da formato de fecha (dd/mm/aaaa) a Fecha Pedido y Fecha Registro y se añade la columna Día de la semana.
•	Se aplica formato numérico (contabilidad) a Descuento, Ingresos, Coste y Beneficio.
•	Si faltan valores en Nombre Producto, Marca o Categoría, se rellenan como "Desconocido" para completar la tabla.
•	En el Excel final (Análisis de Ventas) se eliminan los registros “Desconocido” porque no aportan a los KPIs.
•	Se cambia Miembro Fidelizado de 1/0 a Sí/No.

### 2.2 Análisis descriptivo (KPIs y tablas)
Los datos limpios se guardan en la hoja Datos_Ventas del Excel Análisis de Ventas. Estos son los campos principales:
•	Id Pedido: identificador único del pedido.
•	Fecha Pedido: fecha en la que se registra el pedido.
•	Día de la semana: día de la semana del pedido.
•	Id Producto: identificador del producto.
•	Id Tienda: identificador de la tienda.
•	Nombre Tienda: nombre (ficticio) de la tienda.
•	Ciudad: ciudad donde se vende.
•	País: país donde se vende.
•	Tipo Tienda: tipo de tienda (ej. aeropuerto, online, etc.).
•	Id Cliente: identificador del cliente.
•	Edad: edad del cliente.
•	Género: género del cliente.
•	Miembro Fidelizado: indica si pertenece al programa de fidelización.
•	Fecha Registro: fecha de alta del cliente.
•	Cantidad: unidades vendidas en el pedido.
•	Precio Unitario: precio por unidad.
•	Descuento: descuento aplicado.
•	Ingresos: importe bruto de la venta.
•	Coste: costes asociados.
•	Beneficio: ingresos menos costes.
•	Nombre Producto: nombre y % del ingrediente principal.
•	Marca: marca del producto.
•	Categoría: categoría del producto.
KPIs (qué se mide)
•	Campos usados: Id Pedido, Fecha Pedido, Día de la semana, Producto, Tienda, Cliente, Cantidad, Ingresos, Beneficio, Marca, Categoría, País, Tipo de tienda, Edad, Género y Fidelización.
Tablas dinámicas / visualizaciones
-	Totales: productos vendidos, pedidos, ingresos, beneficios y clientes.
•	Top 5 productos con más y menos pedidos.
•	Distribución de productos por marca y por categoría (%).
•	Ventas por país.
•	Ventas por año/mes y por semana/día.
•	Ventas por tipo de tienda.
•	Ventas por género, edad y fidelización.
•	Relación ventas vs. ingresos/beneficios/margen.
•	Evolución de ventas y beneficios.

## 3. Dashboard
En la hoja Dashboard se muestran los datos así:
•	Panel superior: tarjetas con productos vendidos, pedidos, clientes, ingresos, beneficio y margen promedio.
•	Parte central: ventas por año/mes y por semana/día + top 5 productos con más y menos pedidos.
•	Parte final: ventas por tipo de tienda, evolución de importes y beneficio, ventas por país y por género.
•	Lateral izquierdo: título y filtros (Año, Edad, Fidelización).
•	Lateral derecho: filtro de Tipo de tienda + % por categoría y % por marca.

## 4. Informe (hallazgos del análisis)
Aquí se resumen los principales hallazgos del análisis (qué se vende, cuándo se vende, dónde se vende y a qué tipo de clientes).

### 4.1 Evolución de ventas por fecha
Las ventas cambian según la época del año. En 2023, el mes con más productos vendidos fue diciembre. En 2024, el mejor mes fue junio.
Por día de la semana, la mayor parte de ventas cae en fines de semana: en 2023 destacó el domingo y en 2024 el sábado.

### 4.2 Productos, categorías y marcas
El producto con más pedidos es el Chocolate Negro 50%.
La categoría que más se vende es Praliné y la marca líder es Cadbury.

### 4.3 Ventas por canal (tipo de tienda)
El canal Aeropuerto es el que más vende en 2023 y 2024. Además, el producto líder cambia según el canal:
•	En aeropuertos, el que más se vende es el Chocolate Negro 50%.
•	En centros comerciales, destaca el Chocolate Blanco 80%.
•	En tienda online y en minoristas, vuelve a liderar el Chocolate Negro 50%.
Esto sugiere que conviene ajustar el surtido y las promociones según el canal donde se vende.

### 4.4 Perfil de cliente
Canadá es el país con más ventas. El rango de edad con más compras es 28–37 años. En general, las ventas por género están bastante equilibradas.
Detalle: en aeropuertos de Alemania, el Chocolate Negro 50% se vende más al público femenino.
Los clientes fidelizados compran un poco más, así que el programa sí ayuda (aunque el impacto es moderado).

### 4.5 Ventas vs. beneficios
En 2023 y 2024 hay picos claros de ventas en diciembre. Pero vender más no siempre significa ganar más: en esos meses también suben los costes, así que el beneficio no crece en la misma proporción.

## 5. Resultados y conclusiones
•	Hay estacionalidad: picos en diciembre 2023 y junio 2024.
•	Se vende más en fines de semana.
•	El Chocolate Negro 50% es el producto más vendido.
•	Praliné es la categoría líder y Cadbury la marca con más peso.
•	El canal Aeropuerto es el que más impulsa las ventas.
•	El segmento con más compras es 28–37 años.
•	Por género, las ventas están bastante equilibradas (con el detalle de Alemania en aeropuertos).
•	Los clientes fidelizados rinden un poco mejor.
Con estos resultados se puede planificar mejor por temporada, ajustar surtido/promos por canal y afinar la segmentación de clientes.
