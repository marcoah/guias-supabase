# 🔎 04 · Consultas a la API

[« Volver al índice general](../README.md)

---

> [!NOTE]
> 🚧 Sección en preparación.

Cómo consultar los datos de Supabase desde fuera del panel: la API REST generada automáticamente (PostgREST) y la librería `supabase-js`.

> **Requisitos previos:**
> - [Credenciales de API](../02-configuracion-basica/01-credenciales-api.md) (URL del proyecto y API Key pública).
> - [Políticas RLS](../02-configuracion-basica/04-seguridad-rls.md) configuradas: sin ellas la API devuelve `[]`.

## Temas previstos

| Paso | Guía | Descripción |
| :-- | :-- | :-- |
| 01 | Primera consulta REST | `curl` / navegador / Postman con la API Key. |
| 02 | Consultas con `supabase-js` | `select`, `insert`, `update`, `delete` desde JavaScript. |
| 03 | Filtros y operadores | `eq`, `ilike`, `in`, rangos, orden y selección de columnas. |
| 04 | Paginación y conteo | `range`, `limit` y `count`. |
| 05 | Relaciones entre tablas | Consultas anidadas con claves foráneas. |
| 06 | Funciones RPC | Exponer funciones SQL (incluidas las espaciales) como endpoints. |
