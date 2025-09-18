0. Prerrequisitos

Esta práctica se realizará utilizando Azure DevOps Repos como sistema de control de versiones y Databricks Community Edition como entorno de ejecución.
El objetivo es mostrar de manera guiada un flujo de trabajo completo, de forma clara y práctica.

Lo que necesitas antes de empezar

Cuenta en Databricks Community Edition

Actualmente esta versión gratuita ya incluye Unity Catalog habilitado por defecto, lo cual simplifica la práctica.

Usaremos un cluster gratuito para la ejecución del código.

⚠️ En un entorno real corporativo es necesario configurar permisos, roles y acceso seguro a Unity Catalog, pero en esta práctica no se cubre esa parte.

Acceso a Azure DevOps Repos

Ahí se gestionará el repositorio de ejemplo.

Cada persona hará un fork de este repositorio hacia su propio espacio en Azure DevOps, porque no tienen permisos de edición sobre el repo de referencia.

Esto permite que cada equipo trabaje con autonomía, pero partiendo de la misma base.

Configurar la conexión entre Databricks y Azure DevOps Repos

En Databricks, accede a la sección Repos y selecciona Configurar Git Integration.

Elige Azure DevOps Services como proveedor.

Necesitarás un Personal Access Token (PAT) creado en Azure DevOps.

Una vez configurada la integración, podrás clonar tu fork directamente desde Databricks.

Qué no tratamos en esta práctica

Gestión avanzada de permisos en Unity Catalog (en un entorno corporativo, es crítico definir quién puede leer/escribir en cada catálogo y esquema).

Configuración de clusters dedicados o autoscaling (aquí se usa el cluster gratuito de Community Edition).

Integración con orígenes de datos corporativos (nos limitaremos a un dataset público para el ejemplo).
