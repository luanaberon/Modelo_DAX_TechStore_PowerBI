# Modelo DAX — TechStore / RetailPro

Modelo de datos en Power BI construido para RetailPro, una distribuidora ficticia de
tecnología, como parte de una certificación de Análisis de Datos (Coderhouse). Contiene
un esquema en estrella (tabla de hechos Fact_Ventas + dimensiones de clientes,
productos, categorías y fechas), con relaciones 1:* de dirección única y una tabla de
medidas DAX dedicada.

## Herramientas usadas
- Power BI Desktop (modelado, Power Query, DAX)
- SQL Server (SSMS) — origen de los datos consultados
- GitHub — control de versiones y entrega pública de cada checkpoint

## Contenido del repositorio
- Beron_Luana_Checkpoint2.pbix — modelo de datos completo

## Modelo de datos
- Fact_Ventas (tabla de hechos) relacionada con Dim_Clientes, Dim_Productos y
  Dim_Fechas (todas 1:* con dirección de filtro Única).
- Dim_Productos relacionada con Dim_Categorias.
- _Medidas: tabla sin columnas que agrupa 5 medidas DAX — % Crecimiento Anual,
  Total Ventas, Ventas LY, Ventas Online y Ventas YTD.

## Cómo ejecutar el proyecto completo
Los datos de origen y las consultas SQL de este proyecto viven en repositorios
separados del mismo proyecto RetailPro:
1. Ventas_Tech_DB — script de creación de la base de datos y carga de datos
   (ventas_tech_db.sql), para SQL Server.
2. Repositorio con las consultas de negocio (m4_consultas_negocio.sql) y las
   consultas con JOIN (m5_consultas_joins.sql).
3. Una vez cargada la base, abrí Beron_Luana_Checkpoint2.pbix en Power BI Desktop y
   actualizá el origen de datos (Inicio > Transformar datos > Configuración del
   origen de datos) para apuntar a tu propia instancia de SQL Server.

## Autora
Luana Beron
