# 🔑 Guía: Obtención de Credenciales (URL y API Key)

[« Volver al Índice](./README.md) | [Paso Anterior](./02-activacion-postgis.md) | [Siguiente Paso: Parámetros de Conexión »](./04-parametros-conexion.md)

---

Para conectar tu base de datos con un geoportal web, necesitas obtener la URL de acceso y la llave de autorización (API Key).

## 1. Acceso a la Configuración del Proyecto

1. En el panel lateral izquierdo, haz clic en el icono de **Project Settings** (engrane ⚙️).
2. Selecciona la opción **API**.

## 2. Obtener la URL del Proyecto (Project URL)

Localiza el campo **Project URL** dentro de la sección **API Settings**.
Copia la dirección que empieza por `https://...` y guárdala.

## 3. Obtener la API Key (Anon Public)

Localiza la clave etiquetada como **anon public**. Haz clic en el icono para copiar la cadena de caracteres.

> [!IMPORTANT]
> **Seguridad Crítica:** Nunca expongas tu `Service Role Key` (llave de servicio). Esta llave tiene permisos de administrador y puede borrar toda tu base de datos si cae en manos equivocadas. Solo usa la clave **`anon public`** para el Geoportal.

---

### NOTA

Guarda estos dos datos en un archivo de texto seguro. Esta combinación será la que permitirá que tu sitio web interactúe con la base de datos para visualizar mapas y capas.
