# 🐘 Guía: Conexión de la Base de Datos con pgAdmin 4

[« Volver al Índice](./README.md) | [Paso Anterior](./04-parametros-conexion.md) | [Siguiente Paso: Conexión desde QGIS »](./06-conexion-qgis.md)

---

En esta sección aprenderás a gestionar tu base de datos remota mediante **pgAdmin 4**, configurando tanto una conexión local como la conexión a **Supabase**.

## 1. Conexión Local (PostgreSQL Local)

Útil para pruebas y desarrollo privado.

1. Abre **pgAdmin 4** y selecciona **Add New Server**.
2. **General:** Asigna el nombre `Localhost`.
3. **Connection:**
   - **Host:** `localhost`
   - **Port:** `5432`
   - **Username:** `postgres`
   - **Password:** La que hayas configurado en tu PC (ej. `admin`).
4. Haz clic en **Save**.

## 2. Conexión Remota (Supabase)

Permite administrar la base de datos real que alimentará tu geoportal.

1. En pgAdmin, haz clic derecho en **Servers** > **Register** > **Server**.
2. **Pestaña General:** Asigna un nombre identificativo (ej. `Geoportal Supabase`).
3. **Pestaña Connection:** Usa los parámetros de **Transaction Pooler** ([Paso 04](./04-parametros-conexion.md)):
   - **Host:** Pega la dirección del Host de Supabase.
   - **Port:** `6543`.
   - **Username:** Pega el usuario proporcionado por Supabase.
   - **Password:** La contraseña de tu proyecto en Supabase.
4. **Importante:** Marca la casilla **Save password**.
5. Haz clic en **Save**.

## 3. Verificación de la Conexión

Navega en el árbol de archivos lateral para verificar que puedes ver tus esquemas y tablas:
`Servers` > `Geoportal Supabase` > `Databases` > `postgres` > `Schemas` > `public` > `Tables`.

---

### Resultado Esperado

Ahora puedes ejecutar consultas SQL, crear tablas y administrar usuarios directamente en la nube desde tu computadora local.
