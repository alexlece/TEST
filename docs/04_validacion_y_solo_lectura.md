# 4. Validación colaborativa y solo lectura

## 4.1. Acceso en solo lectura
- Solicita que tu unidad tenga **READ** sobre catálogos/esquemas de las primeras líneas.
- Con eso podrás **consultar** sus tablas y notebooks, pero no modificarlas.

## 4.2. Joins entre espacios
Ejemplo (ajusta catálogo/esquema reales):
```sql
SELECT a.*, b.campo_comparacion
FROM demo_uc.validacion.iris_predictions a
LEFT JOIN prod_uc.modelo_fabrica.iris_predictions b
  ON a.real = b.real;
```

> Así contrastas resultados de tu espacio con los de otros equipos sin duplicar datos.
