# 🔄 Guía: Comparativa de Importación (QGIS vs PostGIS GUI)

[« Volver al Índice](./README.md) | [Paso Anterior](./07-importacion-capas-postgis.md) | [Siguiente Paso: Conclusión »](./README.md)

---

Existen dos formas principales de subir datos a Supabase: desde la interfaz de QGIS o mediante la herramienta externa de PostGIS. Aquí analizamos cuál elegir según el caso.

## 1. Importación Directa desde QGIS

Ideal para capas pequeñas o si no deseas salir del entorno SIG.

1. Ve al menú **Base de datos** > **Administrador de BD**.
2. Conéctate a tu servidor de Supabase y selecciona el esquema `public`.
3. Haz clic en el icono **Importar capa/archivo**.
4. Configura los parámetros:
   - **Capa de entrada:** Selecciona tu archivo (ej. Barrios).
   - **Esquema:** `public`.
   - **Tabla de destino:** Nombre de la tabla en la nube.
   - **Opciones:** Activa "Clave primaria" y "Columna de geometría" (`geom`).
   - **SRID:** Asegúrate de que tanto el origen como el destino sean `4326` (WGS84).
5. Haz clic en **Aceptar**.

> [!WARNING]
> **Rendimiento:** QGIS suele ser más lento para subir datos a la nube. Si la capa es grande (ej. redes de alcantarillado), la conexión puede quedar "colgada" o generar tablas vacías.

## 2. Recomendación: PostGIS GUI

Para archivos medianos o grandes (más de 1 MB), el **PostGIS Shapefile Import/Export Manager** es mucho más estable y rápido.

- **Ventaja:** Maneja mejor la latencia de internet y evita bloqueos en la base de datos remota.
- **Tip:** Si una tabla queda bloqueada por un proceso fallido de QGIS, simplemente renombra la nueva importación (ej. `alcantarillado_v2`).

## 3. Seguridad y Mantenimiento

Independientemente del método que uses, recuerda habilitar la seguridad en el panel de **Supabase**:

1. Entra al **Table Editor**.
2. Para cada tabla nueva, haz clic en **Enable RLS** (Row Level Security).
3. Esto asegura que la tabla cumpla con las políticas de seguridad de la plataforma.

---

### 📊 Resumen Técnico

| Situación                       | Herramienta Recomendada     |
| :------------------------------ | :-------------------------- |
| Capas pequeñas (< 500 KB)       | Administrador de BD de QGIS |
| Redes densas o archivos pesados | PostGIS Shapefile Manager   |
| Análisis SQL avanzado           | pgAdmin 4                   |
