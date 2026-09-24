# 🌍 03 · Datos Espaciales con PostGIS

[« Volver al índice general](../README.md)

---

Flujo de trabajo para crear, configurar y gestionar una base de datos espacial en la nube con **PostgreSQL**, **PostGIS** y **Supabase**, conectada con **QGIS** y lista para alimentar un geoportal web.

> **Requisitos previos:**
> - Proyecto creado ([01 · Registro básico](../01-registro/README.md)).
> - Parámetros de conexión a mano ([02 · Parámetros de conexión](../02-configuracion-basica/02-parametros-conexion.md)).

| Paso | Guía | Descripción |
| :-- | :-- | :-- |
| 🗺️ 01 | [**Activación de PostGIS**](./01-activacion-postgis.md) | Habilitar las extensiones espaciales y otras herramientas opcionales. |
| 🧭 02 | [**Conexión desde QGIS**](./02-conexion-qgis.md) | Ver, editar y gestionar capas desde el SIG. |
| 🚀 03 | [**Importación con PostGIS GUI**](./03-importacion-postgis-gui.md) | Carga masiva y estable de Shapefiles a la nube. |
| 🔄 04 | [**Comparativa de importación**](./04-comparativa-importacion.md) | Cuándo usar QGIS y cuándo PostGIS GUI. |
| 🛡️ 05 | [**Seguridad con RLS**](../02-configuracion-basica/04-seguridad-rls.md) | Publicar las capas para el geoportal sin exponer la edición. |

---

### Resultado esperado

Una base de datos espacial en Supabase, conectada con las herramientas de escritorio y lista para alimentar un **geoportal web interactivo**:

- **Sincronización:** los cambios realizados en QGIS se reflejan en la base de datos central.
- **API-First:** las capas se pueden consumir mediante la API de Supabase ([04 · Consultas a la API](../04-consultas-api/README.md)).
- **Seguridad:** las políticas RLS protegen el acceso a la información.
