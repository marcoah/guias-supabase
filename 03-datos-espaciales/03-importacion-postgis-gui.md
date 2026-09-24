# 🚀 Guía: Importación de Capas Vectoriales (Shapefiles) a Supabase

[« Índice de la sección](./README.md) | [Anterior: Conexión desde QGIS](./02-conexion-qgis.md) | [Siguiente: Comparativa de importación »](./04-comparativa-importacion.md)

---

Para subir archivos geográficos (Shapefiles) de forma eficiente y estable, utilizaremos la herramienta **PostGIS Shapefile Import/Export Manager**.

## 1. Conexión al Servidor desde PostGIS GUI

1. Abre la aplicación **PostGIS Shapefile Import/Export Manager**.
2. Haz clic en **View Connection Details** e ingresa los datos de Supabase ([Parámetros de conexión](../02-configuracion-basica/02-parametros-conexion.md)):
   * **Username:** Tu usuario de Postgres.
   * **Password:** Tu contraseña del proyecto.
   * **Server Host:** El host de Supabase.
   * **Port:** `6543`.
   * **Database:** `postgres`.
3. Haz clic en **OK**. Si aparece *"Connection succeeded"*, estás listo para importar.

## 2. Proceso de Importación

1. Haz clic en **Add File** y selecciona los archivos `.shp` que deseas subir (ej. Bomberos, Policía, Salud).
2. **Configuración Crítica (SRID):** 
   * Es fundamental que tus archivos tengan un sistema de referencia compatible con la web.
   * En la columna **SRID**, escribe **`4326`** para cada capa (esto corresponde a **WGS84**).
3. Haz clic en **Import**. Verás en el log el mensaje: *"Shapefile import completed"*.

> [!TIP]
> **Nombres Limpios:** Antes de subir tus capas, asegúrate de que los nombres de los archivos no tengan espacios, tildes o caracteres especiales (ej. usa `red_alcantarillado` en lugar de `Red de Alcantarillado`).

## 3. Verificación de Datos en la Nube

Una vez importados, verifica tus datos de tres formas:

* **En QGIS:** Refresca tu conexión de PostgreSQL. Arrastra la nueva tabla al lienzo. Verás que los datos ya no son locales, sino que se sirven desde la nube.
* **En pgAdmin 4:** Selecciona la tabla, haz clic derecho y elige **View Data**. Podrás ver la columna `geom` y el visor geográfico integrado.
* **En Supabase:** Entra al **Table Editor**. Verás tus capas como tablas de datos. ¡Incluso puedes editar valores alfanuméricos directamente!

## 4. Sincronización en Tiempo Real

La mayor ventaja de este flujo es la **edición multiusuario**:
* Si editas un atributo en el portal de Supabase, el cambio se refleja instantáneamente en QGIS.
* Esto permite mantener geoportales actualizados globalmente sin necesidad de enviar archivos pesados por correo.

---
**Documentado por:** [JonatanLara](https://github.com/jonatanLara)
