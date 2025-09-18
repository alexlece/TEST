# 2. Configurar tu espacio (Unity Catalog)

> Si tu entorno no usa Unity Catalog, puedes crear tablas gestionadas del workspace y saltarte los pasos SQL.

## 2.1. Crea catálogo y esquema (una sola vez por proyecto)
Abre una notebook SQL o celda `%%sql` y ejecuta:

```sql
CREATE CATALOG IF NOT EXISTS demo_uc;
CREATE SCHEMA IF NOT EXISTS demo_uc.validacion;

USE CATALOG demo_uc;
USE SCHEMA validacion;
```

- Este catálogo/esquema será *tu espacio de proyecto*.
- Asegúrate de tener permisos para crear y escribir.

## 2.2. Variables en la notebook
En la notebook de la práctica fijarás:
```python
catalog = "demo_uc"
schema = "validacion"
```
Así puedes **reubicar** fácilmente dónde se crean las tablas.
