# 3. Ejecutar la notebook base

1. Abre `/notebooks/ml_practica_iterativa.ipynb`.
2. En la primera celda, ajusta `catalog` y `schema`.
3. Ejecuta las celdas en orden:
   - Instala dependencias con `%pip install ...`
   - Carga dataset público (Iris)
   - Crea **tabla de entrada**
   - (Opcional) Crea **tabla intermedia** con transformaciones simples
   - Entrena un **modelo sencillo**
   - Escribe **tabla final** de predicciones
4. Verifica con `display(spark.table(...))` que las tablas existen.

> La notebook está escrita en lenguaje claro y comenta cada paso.
