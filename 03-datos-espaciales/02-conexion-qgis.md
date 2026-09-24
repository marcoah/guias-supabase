# Guía: Conexión de la Base de Datos en QGIS

[« Índice de la sección](./README.md) | [Anterior: Activación de PostGIS](./01-activacion-postgis.md) | [Siguiente: Importación con PostGIS GUI »](./03-importacion-postgis-gui.md)

---

En esta sección aprenderás a conectar **QGIS** con tu base de datos de **Supabase** para visualizar, editar y gestionar capas geográficas directamente desde tu SIG.

## 1. Configuración de la Nueva Conexión

1. Abre **QGIS** y localiza el panel de **Navegador**.
2. Haz clic derecho sobre el icono de **PostgreSQL** y selecciona **Conexión nueva...**.

## 2. Parámetros de Conexión

Completa los campos en la pestaña **General** con los datos de tu proyecto ([Parámetros de conexión](../02-configuracion-basica/02-parametros-conexion.md)):

- **Nombre:** Elige un nombre descriptivo (ej. `Geoportal_Supabase`).
- **Anfitrión (Host):** Pega la dirección del host de Supabase.
- **Puerto:** `6543`.
- **Base de datos:** `postgres`.

![Configuración de Conexión en QGIS](./img/02-conexion-qgis.png)
_Figura 1: Ejemplo de cómo llenar los campos de conexión en QGIS._

## 3. Autenticación y Credenciales

Para evitar errores de acceso, configura la seguridad de la siguiente manera:

1. Haz clic en el botón de **Autenticación**.
2. Ve a la pestaña **Básica**.
3. Ingresa tu **Nombre de usuario** y **Contraseña** de Supabase.
4. **Recomendación:** Marca las casillas **Guardar nombre de usuario** y **Guardar contraseña** para no tener que escribirlas cada vez que abras QGIS.

## 4. Verificación Final

1. Haz clic en el botón **Probar conexión**.
2. Si aparece el mensaje: _"La conexión con Geoportal_Supabase tuvo éxito"_, haz clic en **Aceptar**.

> [!TIP]
> **Refrescar:** Si realizas cambios en las tablas desde pgAdmin o mediante SQL, simplemente haz clic derecho sobre la conexión en QGIS y selecciona **Actualizar** para ver los cambios reflejados.

---

### Resultado Esperado

Ahora, en tu panel de navegador de QGIS, podrás desplegar tu conexión, entrar en el esquema `public` y visualizar tus tablas espaciales como capas vectoriales.
