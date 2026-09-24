# 🛡️ Guía: Seguridad de Datos con RLS (Row Level Security)

[« Volver al Índice](./README.md) | [Paso Anterior](./08-comparativa-importacion.md) | [Siguiente Paso: Conclusión »](./README.md)

---

Una vez que tus capas geográficas están en la nube (Supabase), el paso final es configurar quién puede ver o editar esa información. Para ello utilizamos las **Políticas RLS**.

## 1. ¿Qué es RLS (Row Level Security)?

**RLS** es una capa de seguridad de PostgreSQL que permite definir reglas específicas de acceso para cada fila de una tabla.

> [!IMPORTANT]
> **Seguridad por Defecto:** Aunque tengas la API Key y la URL del proyecto, Supabase bloqueará el acceso a los datos por defecto si no existe una política activa. Esto se hace para evitar que tu información sea vulnerable desde el primer segundo.

## 2. Habilitar RLS en tus Tablas

Para cada capa importada (Barrios, Bomberos, Salud, etc.), debes activar el interruptor de seguridad:

1. Ve al **Table Editor** en el panel lateral de Supabase.
2. Selecciona la tabla (ej. `barrios`).
3. Haz clic en el botón **No active RLS policies** para abrir el gestor de seguridad.

![Habilitar RLS](./img/09-habilitar-rls.png)
_Figura 1: Activación del interruptor RLS en el Table Editor._

## 3. Crear una Política de Acceso

Existen dos escenarios comunes según el objetivo de tu Geoportal:

### A. Acceso de Solo Lectura (Público) 🌍

Ideal para que cualquier persona en Internet pueda ver el mapa, pero **nadie** pueda borrar o editar los puntos.

- Haz clic en **Create Policy**.
- Selecciona la plantilla: _"Enable read access for all users"_.
- Esto permitirá que las herramientas externas (como un mapa web en HTML) consuman los datos.

### B. Acceso Total (Lectura y Escritura) ✍️

Si tu Geoportal permite que técnicos en campo editen información desde una App móvil:

- Selecciona la opción **ALL** (esto otorga permisos de `SELECT`, `INSERT`, `UPDATE` y `DELETE`).
- Haz clic en **Save Policy**.

## 4. Gestión Masiva (Authentication Panel)

Si tienes muchas capas (Agua, Alcantarillado, Policía, etc.), es más rápido gestionarlas desde aquí:

1. Ve a **Authentication** (icono de candado) > **Policies**.
2. Verás un resumen de todas tus tablas. Aquellas con advertencias rojas necesitan una política.
3. Haz clic en **New Policy** para cada una y aplica el permiso necesario.

## 5. Verificación de Acceso

Una vez configuradas las políticas:

1. Regresa al **Table Editor**.
2. Al seleccionar cualquier tabla, verás que las filas de datos ahora son visibles.

> [!TIP]
> **¿Resultado Vacío?** Si al consultar tu API desde JavaScript o QGIS recibes un resultado vacío `[]`, lo primero que debes revisar es si activaste la política RLS correctamente.
