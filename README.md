# 📚 Guías de Supabase

Recopilación de guías prácticas, configuraciones y trucos para trabajar con **Supabase** (PostgreSQL en la nube). Sirve como material de referencia para las clases: cada sección se puede seguir por separado y cada guía indica sus requisitos previos.

---

## 🗂️ Secciones

| # | Sección | Contenido | Estado |
| :-- | :-- | :-- | :-- |
| 01 | [**Registro básico**](./01-registro/README.md) | Crear la cuenta, la organización y el primer proyecto. | ✅ Disponible |
| 02 | [**Configuración básica**](./02-configuracion-basica/README.md) | Credenciales de API, parámetros de conexión, pgAdmin y seguridad RLS. | ✅ Disponible |
| 03 | [**Datos espaciales (PostGIS)**](./03-datos-espaciales/README.md) | PostGIS, QGIS, importación de Shapefiles y geoportales. | ✅ Disponible |
| 04 | [**Consultas a la API**](./04-consultas-api/README.md) | Consultas REST y con `supabase-js`: filtros, paginación, RPC. | 🚧 En preparación |
| 05 | [**Conexión con Power BI**](./05-power-bi/README.md) | Conectar Power BI a la base de datos de Supabase. | 🚧 En preparación |
| 06 | [**Trucos varios**](./06-trucos/README.md) | Recetas cortas, atajos y soluciones a problemas frecuentes. | 🚧 En preparación |

---

## 🧭 Ruta sugerida

```text
01 Registro ──► 02 Configuración básica ──┬──► 03 Datos espaciales
                                          ├──► 04 Consultas a la API
                                          ├──► 05 Power BI
                                          └──► 06 Trucos varios
```

Las secciones **01** y **02** son la base de todas las demás. A partir de ahí, cada sección es independiente.

---

## 📁 Estructura del repositorio

```text
guias-supabase/
├── README.md                    ← Este índice general
├── _plantilla-guia.md           ← Plantilla para escribir nuevas guías
├── 01-registro/
├── 02-configuracion-basica/
├── 03-datos-espaciales/
├── 04-consultas-api/
├── 05-power-bi/
└── 06-trucos/
```

Cada sección tiene:

- Un `README.md` con el índice de sus guías.
- Guías numeradas (`01-...md`, `02-...md`) en el orden en que se recomienda seguirlas.
- Una carpeta `img/` con las capturas de pantalla de esa sección.

---

## ✍️ Cómo añadir una guía nueva

1. Copia [`_plantilla-guia.md`](./_plantilla-guia.md) dentro de la carpeta de la sección.
2. Renómbrala con el siguiente número disponible y un nombre corto en minúsculas y con guiones (ej. `05-backups-automaticos.md`).
3. Guarda las capturas en la carpeta `img/` de la sección, con el mismo prefijo numérico que la guía (ej. `img/05-backups-1.png`).
4. Agrega la guía a la tabla del `README.md` de la sección y actualiza los enlaces «Anterior / Siguiente» de las guías vecinas.

---

## 🙌 Créditos

- Guía de importación con PostGIS GUI documentada por [JonatanLara](https://github.com/jonatanLara).
