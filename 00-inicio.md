# 🌍 Guía Completa: Gestión de Datos Espaciales con Supabase y PostGIS

[Comenzar la guía: Configuración de Supabase »](./01-configuracion-supabase.md)

---

Esta guía presenta el flujo de trabajo para crear, configurar y gestionar una base de datos espacial en la nube con **PostgreSQL**, **PostGIS** y **Supabase**.

Está dirigida a quienes necesitan conectar sus datos geográficos con **QGIS**, **pgAdmin 4** y un geoportal web moderno.

## Objetivo de la Guía

Al finalizar, podrás publicar y administrar capas vectoriales —como redes de agua potable, barrios, alcantarillado o servicios de salud— desde una base de datos espacial centralizada y accesible en línea.

## Índice de Contenidos

Sigue los temas en orden para completar la configuración:

| Paso | Tema | Descripción |
| :--- | :--- | :--- |
| ☁️ **01** | [**Configuración de Supabase**](./01-configuracion-supabase.md) | Creación de cuenta, organización, proyecto y base de datos inicial. |
| 🗺️ **02** | [**Activación de PostGIS**](./02-activacion-postgis.md) | Habilitación de extensiones espaciales y herramientas adicionales. |
| 🔑 **03** | [**Obtención de Credenciales**](./03-obtencion-credenciales.md) | Localización de la URL del proyecto y las API Keys. |
| 🔌 **04** | [**Parámetros de Conexión**](./04-parametros-conexion.md) | Datos técnicos para la conexión remota a PostgreSQL. |
| 🐘 **05** | [**Conexión desde pgAdmin 4**](./05-conexion-pgadmin.md) | Administración de la base de datos mediante SQL. |
| 🧭 **06** | [**Conexión desde QGIS**](./06-conexion-qgis.md) | Visualización, edición y gestión de capas desde el SIG. |
| 🚀 **07** | [**Importación con PostGIS GUI**](./07-importacion-capas-postgis.md) | Carga masiva y estable de Shapefiles a la nube. |
| 🔄 **08** | [**Comparativa de Importación**](./08-comparativa-importacion.md) | Criterios para elegir entre QGIS y PostGIS GUI. |
| 🛡️ **09** | [**Seguridad de Datos con RLS**](./09-seguridad-datos-rls.md) | Políticas de acceso público, privado y edición de datos. |

---

### Resultado Esperado

Una base de datos espacial en Supabase conectada con tus herramientas de escritorio y lista para alimentar un **geoportal web interactivo**.

- **Sincronización:** los cambios realizados en QGIS se reflejan en la base de datos central.
- **API-First:** las capas se pueden consumir mediante la API de Supabase.
- **Seguridad:** las políticas RLS protegen el acceso a la información.
