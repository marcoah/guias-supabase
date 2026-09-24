# 🔌 Guía: Obtención de Datos de Conexión PostgreSQL

[« Volver al Índice](./README.md) | [Paso Anterior](./03-obtencion-credenciales.md) | [Siguiente Paso: Conexión desde pgAdmin »](./05-conexion-pgadmin.md)

---

Para conectar aplicaciones de escritorio como **QGIS, pgAdmin o PowerBI**, necesitas los parámetros técnicos de acceso al servidor.

## 1. Localizar el Menú de Conexión

1. En el panel superior derecho de tu proyecto en Supabase, haz clic en el botón **Connect**.
2. Verás una lista de métodos de conexión.

## 2. Seleccionar el Método de Conexión

Existen dos tipos principales. Para QGIS y pgAdmin, elige la opción de **Transaction Pooler**.

> [!NOTE]
> El **Transaction Pooler** es mucho más estable para múltiples conexiones simultáneas.

## 3. Parámetros de Conexión Clave

Haz clic en **View Parameters** y copia los siguientes datos:

- **Host:** La dirección del servidor (ej. `aws-0-sa-east-1.pooler.supabase.com`).
- **Port:** `6543` (para el pooler) o `5432` (conexión directa).
- **Database name:** Generalmente `postgres`.
- **User:** El nombre de usuario (ej. `postgres.xxxxxxx`).

## 4. Gestión de la Contraseña

- **Seguridad:** Supabase **nunca** mostrará tu contraseña en este panel.
- Debes usar la contraseña que definiste al crear el proyecto en el [Paso 01](./01-configuracion-supabase.md).
- **¿La olvidaste?** Cámbiala en: `Project Settings` > `Database` > `Reset password`.

---

### 🚀 Aplicaciones Compatibles

Con estos datos podrás conectar aplicaciones SIG y herramientas de BI como:

- **QGIS:** Para gestión de capas vectoriales.
- **pgAdmin:** Para administración avanzada de SQL.
- **PowerBI / Tableau:** Para análisis de datos geográficos.
