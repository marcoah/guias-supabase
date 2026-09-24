# 🔑 Guía: Obtención de Credenciales (URL y API Key)

[« Índice de la sección](./README.md) | [Anterior: Crear cuenta y proyecto](../01-registro/01-crear-cuenta-y-proyecto.md) | [Siguiente: Parámetros de conexión »](./02-parametros-conexion.md)

---

Para que una aplicación web (por ejemplo, un geoportal o un formulario) se comunique con tu base de datos a través de la API de Supabase, necesitas la URL del proyecto y una llave de autorización (API Key).

## 1. Acceso a la Configuración del Proyecto

1. En el panel lateral izquierdo, haz clic en el icono de **Project Settings** (engrane ⚙️).
2. Busca las secciones **Data API** (URL del proyecto) y **API Keys** (llaves).

> [!TIP]
> El botón **Connect** de la parte superior del panel también muestra la URL y la llave pública, listas para copiar.

## 2. Obtener la URL del Proyecto (Project URL)

Localiza el campo **Project URL**. Tiene la forma `https://<id-del-proyecto>.supabase.co`. Cópiala y guárdala.

## 3. Obtener la API Key Pública

Supabase ofrece dos juegos de llaves. Según la antigüedad del proyecto verás uno u otro (o ambos):

| Tipo | Llave pública (usar en el navegador) | Llave secreta (solo en servidores) |
| :-- | :-- | :-- |
| **Nuevas** | `publishable` (empieza con `sb_publishable_...`) | `secret` (empieza con `sb_secret_...`) |
| **Heredadas (Legacy)** | `anon public` | `service_role` |

Copia la llave **pública** (`publishable` o `anon`). Es la que usarás en tu sitio web.

> [!IMPORTANT]
> **Seguridad crítica:** Nunca expongas la llave **secreta** (`secret` o `service_role`). Esa llave ignora las políticas RLS y tiene permisos de administrador: puede leer y borrar toda tu base de datos si cae en manos equivocadas. En el navegador usa **solo** la llave pública, y protege los datos con [políticas RLS](./04-seguridad-rls.md).

---

### Resultado Esperado

Guarda la **URL del proyecto** y la **llave pública** en un lugar seguro. Esta combinación es la que permite que tu sitio web consulte la base de datos (ver [Consultas a la API](../04-consultas-api/README.md)).
