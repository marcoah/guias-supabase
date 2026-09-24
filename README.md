# Guía Completa: Gestión de Datos Espaciales con Supabase y PostGIS

Esta documentación técnica detalla el flujo de trabajo profesional para crear, configurar y gestionar bases de datos espaciales en la nube utilizando **PostgreSQL**, **PostGIS** y **Supabase**.

Ideal para quienes buscan conectar sus datos geográficos con **QGIS**, **pgAdmin** y desplegar geoportales web modernos.

---

## Índice de Contenidos

Haz clic en cada paso para ver la guía detallada:

| Paso      | Guía de Implementación                                               | Descripción                                                  |
| :-------- | :------------------------------------------------------------------- | :----------------------------------------------------------- |
| ☁️ **01** | [**Configuración de Supabase**](./01-configuracion-supabase.md)      | Creación de cuenta, proyecto y base de datos inicial.        |
| 🗺️ **02** | [**Activación de PostGIS**](./02-activacion-postgis.md)              | Habilitar extensiones espaciales y herramientas adicionales. |
| 🔑 **03** | [**Obtención de Credenciales**](./03-obtencion-credenciales.md)      | Localización de API Keys y URLs del proyecto.                |
| 🔌 **04** | [**Parámetros de Conexión**](./04-parametros-conexion.md)            | Datos técnicos para conexión remota vía Transaction Pool.    |
| 🐘 **05** | [**Conexión desde pgAdmin 4**](./05-conexion-pgadmin.md)             | Administración avanzada de SQL local y remota.               |
| 🧭 **06** | [**Conexión desde QGIS**](./06-conexion-qgis.md)                     | Visualización y edición de capas directamente en tu SIG.     |
| 🚀 **07** | [**Importación con PostGIS GUI**](./07-importacion-capas-postgis.md) | Carga masiva y estable de Shapefiles a la nube.              |
| 🔄 **08** | [**Comparativa de Importación**](./08-comparativa-importacion.md)    | QGIS vs PostGIS GUI: ¿Cuál elegir y por qué?                 |
| 🛡️ **09** | [**Seguridad de Datos (RLS)**](./09-seguridad-datos-rls.md)          | Configuración de políticas para acceso público o privado.    |

---

## Objetivo Final: Geoportal HTML

Siguiendo esta guía, podrás visualizar capas vectoriales (agua potable, barrios, alcantarillado, servicios de salud, etc.) en un **Geoportal Web Interactivo**:

- **Sincronización:** Cambios en QGIS se reflejan al instante en la web.
- **API-First:** Consumo de datos espaciales mediante la API de Supabase.
- **Seguridad:** Configuración de políticas RLS para proteger tus datos.
