🍫 DataProject — Dashboard & Análisis de Datos
📊 Análisis de Ventas (EDA) — Chocolate Sales 2023–2024
Este documento resume el análisis exploratorio de ventas (EDA) de una empresa internacional de chocolates. Incluye la preparación de datos, los KPIs creados y las conclusiones principales.

📁 1. Descripción del proyecto
Este proyecto analiza las ventas de una empresa internacional de chocolates usando datos de 2023 y 2024. La idea es entender qué se vende, cuándo se vende y dónde se vende, para apoyar decisiones de negocio.
Se revisa la evolución de ventas por productos, categorías y marcas, y también por tiempo (año, mes, semana y día). Además, se comparan resultados por tipo de tienda y por país para tener una visión global.
También se analiza a quién se le vende: edad, género y si el cliente está fidelizado. Esto ayuda a entender mejor los hábitos de compra y a segmentar.
Por último, se revisan ventas y beneficios a lo largo del tiempo para ver si los meses con más ventas también son los más rentables.

🗂️ 2. Estructura del proyecto

📦 Datos
Los datos provienen del dataset de Kaggle: Chocolate Sales: Complete EDA + ML Pipeline  y se almacenan en el archivo Datos_originales.

🧹 2.1 Transformación y limpieza de datos
•	Se cargan los CSV en Excel (archivo Transformación de Datos), separando los campos por comas.
•	En la hoja Ventas, Id Pedido se usa como clave para relacionar la información del resto de hojas.
•	También se usan como identificadores: Id Producto (Productos), Id Cliente (Clientes) y Id Tienda (Tienda).
•	Se añaden columnas para traer datos de Tienda/Clientes/Productos (por ejemplo: Nombre Tienda, Ciudad, País, Tipo Tienda, Edad, Género, Miembro Fidelizado, Fecha Registro, Nombre Producto, Marca y Categoría) usando BuscarX.
•	Se da formato de fecha (dd/mm/aaaa) a Fecha Pedido y Fecha Registro y se añade la columna Día de la semana.
•	Se aplica formato numérico (contabilidad) a Descuento, Ingresos, Coste y Beneficio.
•	Si faltan valores en Nombre Producto, Marca o Categoría, se rellenan como "Desconocido" para completar la tabla.
•	En el Excel final (Análisis de Ventas) se eliminan los registros “Desconocido” porque no aportan a los KPIs.
•	Se cambia Miembro Fidelizado de 1/0 a Sí/No.

📊 2.2 Análisis descriptivo (KPIs y tablas)
Los datos limpios se guardan en Datos_Ventas dentro del Excel Análisis de Ventas.

Campos principales:

Id Pedido

Fecha Pedido

Día de la semana

Id Producto

Id Tienda

Nombre Tienda
Ciudad

País

Tipo Tienda

Id Cliente

Edad

Género

Miembro Fidelizado

Fecha Registro

Cantidad

Precio Unitario

Descuento

Ingresos

Coste

Beneficio

Nombre Producto

Marca

Categoría

KPIs analizados:

Productos vendidos

Pedidos totales

Ingresos

Beneficio

Clientes únicos

Top 5 productos más y menos vendidos

Distribución por marca y categoría

Ventas por país

Ventas por año/mes/semana/día

Ventas por tipo de tienda

Ventas por género, edad y fidelización

Relación ventas vs. ingresos/beneficios

Evolución temporal de ventas y beneficios

📈 3. Dashboard

El dashboard incluye:
Panel superior: tarjetas de KPIs (ventas, pedidos, clientes, ingresos, beneficio, margen).

Zona central:

Ventas por año/mes

Ventas por semana/día

Top 5 productos más y menos vendidos

Zona inferior:

Ventas por tipo de tienda

Evolución de ingresos y beneficios

Ventas por país

Ventas por género

Lateral izquierdo: título + filtros (Año, Edad, Fidelización).

Lateral derecho: filtro de Tipo de tienda + % por categoría y marca.

🔍 4. Informe

Aquí se resumen los principales hallazgos del análisis (qué se vende, cuándo se vende, dónde se vende y a qué tipo de clientes).

📅 4.1 Evolución de ventas por fecha

En 2023, el mejor mes fue diciembre.

En 2024, el mejor mes fue junio.

Las ventas aumentan en fines de semana:

2023 → domingo

2024 → sábado

🍬 4.2 Productos, categorías y marcas

Producto más vendido: Chocolate Negro 50%.

Categoría líder: Praliné.

Marca más fuerte: Cadbury.

🏬 4.3 Ventas por canal (tipo de tienda)

El canal Aeropuerto es el más fuerte en ambos años.

Producto líder por canal:

Aeropuerto → Chocolate Negro 50%

Centro comercial → Chocolate Blanco 80%

Online / Minoristas → Chocolate Negro 50%

Esto sugiere adaptar surtido y promociones según el canal.

👥 4.4 Perfil de cliente

País con más ventas: Canadá.

Rango de edad dominante: 28–37 años.

Ventas por género: bastante equilibradas.

Caso particular:

En aeropuertos de Alemania, el Chocolate Negro 50% se vende más a mujeres.

Los clientes fidelizados compran ligeramente más.

💰 4.5 Ventas vs. beneficios

Picos de ventas en diciembre (2023 y 2024).

Pero el beneficio no crece igual: los costes también suben en esos meses

🧾 5. Resultados y conclusiones

Estacionalidad clara: diciembre 2023 y junio 2024.

Más ventas en fines de semana.

Producto estrella: Chocolate Negro 50%.

Categoría líder: Praliné.

Marca dominante: Cadbury.

Canal más rentable: Aeropuerto.

Segmento principal: 28–37 años.

Género equilibrado (con matices por país).

Fidelización con impacto moderado pero positivo.

Conclusión:  
Con estos resultados se puede planificar mejor por temporada, ajustar surtido/promos por canal y afinar la segmentación de clientes.
