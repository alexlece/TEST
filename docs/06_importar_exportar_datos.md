# 6. Importar y exportar datos

## 6.1. Importar un CSV local (sencillo)
1. En Databricks, **Upload data** → sube un CSV.
2. Cárgalo con Spark:
```python
df = spark.read.format("csv").option("header", True).load("/FileStore/tables/miarchivo.csv")
df.write.mode("overwrite").saveAsTable(f"{catalog}.{schema}.mi_tabla_entrada")
```

## 6.2. Exportar a archivos (para compartir)
```python
spark.table(f"{catalog}.{schema}.iris_predictions") \
    .write.mode("overwrite").format("csv").option("header", True) \
    .save("/FileStore/export/iris_predictions_csv")
```

## 6.3. JDBC (cuando aplique)
- Se puede **leer/escribir** a bases de datos vía JDBC.
- Necesitarás credenciales seguras (Secrets) y el driver adecuado.
- Pide a tu admin las pautas corporativas antes de usarlo.
